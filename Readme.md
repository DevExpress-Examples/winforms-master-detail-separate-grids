<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128627753/13.1.4%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/E883)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->

# Data Grid for Windows Forms - How to display master-detail tables in separate grid controls

A data source in this example is a DataSet object that contains master and detail tables linked by the `CustomersPersons` relationship. 
The example shows how to display these tables in separate [Grid Controls](https://docs.devexpress.com/WindowsForms/3455/controls-and-libraries/data-grid).
The first grid is bound to a master table. The second grid displays details for the master row selected in the first grid.

To link two grid controls, the second grid is bound to a BindingSource component that is initialized as follows:
- The `BindingSource.DataSource` property is set to the first grid's data source.
- The `BindingSource.DataMember` property is set to `CustomersPersons` (the name of the relationship between the master and detail tables).

<!-- default file list -->
## Files to Look At

* [Form1.cs](./CS/Q205299/Form1.cs) (VB: [Form1.vb](./VB/Q205299/Form1.vb))

<!-- default file list end -->

## Documentation
- [Master-Detail Relationships](https://docs.devexpress.com/WindowsForms/3473/controls-and-libraries/data-grid/master-detail-relationships)
- [Data Binding Common Concepts](https://docs.devexpress.com/WindowsForms/2395/common-features/data-binding-common-concepts)

## See Also
- [How to use two XtraGrid controls to display collections of persistent objects with a one-to-many association](https://supportcenter.devexpress.com/ticket/details/a2750/how-to-use-two-xtragrid-controls-to-display-collections-of-persistent-objects-with-a-one)
- [DevExpress WinForms Troubleshooting - Grid Control](https://go.devexpress.com/CheatSheets_WinForms_Examples_T934742.aspx)

