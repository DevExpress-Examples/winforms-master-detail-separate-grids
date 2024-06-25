<!-- default badges list -->
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/E883)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
[![](https://img.shields.io/badge/💬_Leave_Feedback-feecdd?style=flat-square)](#does-this-example-address-your-development-requirementsobjectives)
<!-- default badges end -->
<!-- default file list -->
*Files to look at*:

* [Form1.cs](./CS/Q205299/Form1.cs) (VB: [Form1.Designer.vb](./VB/Q205299/Form1.Designer.vb))
* [Form1.Designer.cs](./CS/Q205299/Form1.Designer.cs) (VB: [Form1.Designer.vb](./VB/Q205299/Form1.Designer.vb))
<!-- default file list end -->
# How to Display Master-Detail Tables in Separate Grid Controls


<p><strong>Description</strong>:<br />
How to display master-detail tables in two different grids?  A master table should be displayed in one GridControl.  Another GridControl should contain details for the selected master row in the first grid.</p><p><strong>Solution</strong>:<br />
The most popular way to visualize Master-Detail tables in an XtraGrid is by displaying the detail data embedded into master rows that then expand to show the detail view.  However, sometimes it may be desirable to display the detail data in a Grid control of it's own, and as you navigate through the master data in a master grid the detail data in the detail grid displays all the related detail controls for the selected master record.</p><p>It is easy to implement this, if you are using an ADO.NET dataset (<strong>System.Data.DataSet</strong>).  The <strong>GridControl</strong> object intended for displaying the detail data should be bound to an ADO.NET data relation.  Please look at the attached sample.  The <strong>DataMember</strong> property of GridControl2 is the name of a data relation for the Customers table, which is assigned to the <strong>DataSource</strong> property.</p>

```vb
<newline/>
' Bind to a relation<newline/>
GridControl2.DataSource = DataSet11.Customers<newline/>
GridControl2.DataMember = "CustomersOrders"<newline/>

```

<p>If you are using a third-party data object or you have built your own, and it can contain master-detail data like <strong>System.Data.DataSet</strong> then you will probably be able to bind it's detail data to an XtraGrid as shown above.</p><p><strong>See Also:</strong><br />
<a href="https://www.devexpress.com/Support/Center/p/A2750">How to use two XtraGrid controls to display collections of persistent objects with a one-to-many association</a></p>

<br/>


<!-- feedback -->
## Does this example address your development requirements/objectives?

[<img src="https://www.devexpress.com/support/examples/i/yes-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=winforms-master-detail-separate-grids&~~~was_helpful=yes) [<img src="https://www.devexpress.com/support/examples/i/no-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=winforms-master-detail-separate-grids&~~~was_helpful=no)

(you will be redirected to DevExpress.com to submit your response)
<!-- feedback end -->
