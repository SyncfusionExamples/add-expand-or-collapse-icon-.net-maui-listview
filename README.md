# How to expand or collapse group header of .NET MAUI ListView(SfListView)?

The [.NET
MAUI ListView (SfListView)](https://www.syncfusion.com/maui-controls/maui-listview) supports expanding or collapsing groups when a group header is tapped by setting the [AllowGroupExpandCollapse](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.ListView.SfListView.html#Syncfusion_Maui_ListView_SfListView_AllowGroupExpandCollapse) property to **True**. Additionally, it allows displaying the expanded and collapsed state of the group with an icon by customizing the [GroupHeaderTemplate](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.ListView.SfListView.html#Syncfusion_Maui_ListView_SfListView_GroupHeaderTemplate) based on the ***IsExpand*** property, which determines whether the group is expanded or collapsed.

Steps
1. Define the GroupHeaderTemplate with an Image to display the icon. Bind the IsExpand property to the Image.Source with converter.
2. Define the converter to return the appropriate group icon based on the IsExpand property.


**Output**

![Expand/Collapse icon in the group header of .NET MAUI ListView (SfListView)](https://www.syncfusion.com/uploads/user/kb/maui/maui-1837/maui-1837_img1.png)

Download the complete sample from [GitHub](https://github.com/SyncfusionExamples/add-expand-or-collapse-icon-.net-maui-listview)

https://github.com/SyncfusionExamples/add-expand-or-collapse-icon-.net-maui-listview

**Conclusion**

I hope you
enjoyed learning how to expand or collapse group headers in the .NET MAUI ListView.

You can
refer to our [.NET MAUI
ListView feature tour](https://www.syncfusion.com/maui-controls/maui-listview) page to know about its
other groundbreaking feature representations and [documentation](https://help.syncfusion.com/maui/listview/getting-started), and
how to quickly get started with configuration specifications. You can also
explore our [.NET MAUI ListView example](https://github.com/syncfusion/maui-demos/tree/master/MAUI/ListView) to
understand how to create and manipulate data.

For current
customers, check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If
you are new to Syncfusion®, try our 30-day [free trial](https://www.syncfusion.com/downloads/maui) to check out our other controls.

Please let us know in the comments section below if you have any queries or require clarification. Contact us through our [support forums](https://www.syncfusion.com/forums), [Direct-Trac](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/maui?control=sflistview). We
are always happy to assist you!
