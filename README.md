**[View document in Syncfusion .NET MAUI Knowledge Base](https://www.syncfusion.com/kb/13130/how-to-add-expand-or-collapse-icon-in-the-group-header-of-net-maui-listview-sflistview)**

## Sample

```xaml
<ContentPage.Resources>
    <ResourceDictionary>
        <local:BoolToImageConverter x:Key="BoolToImageConverter"/>
    </ResourceDictionary>
</ContentPage.Resources>

<ListView:SfListView x:Name="listView"
                    ItemSize="70" 
                    GroupHeaderSize="50"
                    SelectionMode="Single"
                    IsStickyGroupHeader="True"
                    ItemsSource="{Binding ContactsInfo}"
                    AllowGroupExpandCollapse="True">

    <ListView:SfListView.GroupHeaderTemplate>
        <DataTemplate>
        <StackLayout Orientation="Horizontal" BackgroundColor="#E4E4E4">
            <Image Source="{Binding IsExpand, Converter={StaticResource BoolToImageConverter}}" HeightRequest="30" WidthRequest="30" VerticalOptions="Center" Margin="10,0"/>
        </StackLayout>
        </DataTemplate>
    </ListView:SfListView.GroupHeaderTemplate>

    <ListView:SfListView.ItemTemplate>
        <DataTemplate>
            <code>
            . . .
            . . .
            <code>
        </DataTemplate>
    </ListView:SfListView.ItemTemplate>
</ListView:SfListView>

C#:

ListView.DataSource.GroupDescriptors.Add(new GroupDescriptor()
{
    PropertyName = "ContactName",
    KeySelector = (object obj1) =>
    {
        var item = (obj1 as ListViewContactInfo);
        return item.ContactName[0].ToString();
    },
});

public class BoolToImageConverter : IValueConverter
{
    public object Convert(object value, Type targetType, object parameter, CultureInfo culture)
    {
        return (bool)value ? "group_expand.png" : "group_collapse.png";
    }

    public object ConvertBack(object value, Type targetType, object parameter, CultureInfo culture)
    {
        throw new NotImplementedException();
    }
}
```