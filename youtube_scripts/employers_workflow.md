INTRO 

Hi

I’m Jimmy Carter, author of Machete, the cloud application for managing day labor centers. In this video, we will discuss the basics of the Machete UI and the workflow for recording new orders in Machete.

The Machete UI was designed in 2011 using the jQueryUI framework. The UI is mostly server-side, generated with ASP.NET MVC, but the data tables and a few of the modal dialogs are rendered in javascript. Most Interactions occur through HTML loads, triggered by javascript. The complexity of this client/server hybrid is the primary reason for the current redesign in Angular2.

The UI has a set of tabs visible across the whole application. <POINT AT TABS> Each tab represents feature of Machete. In this video, we will be discussing the Employers tab, which is the primary method of entering in order data for Machete v1.

EMPLOYERS
The Employers tab opens up a data table of existing Employer records, sorted by Date Updated, in descending order.  Notice the two tabs, “List Employers” and “Create New Employer.” <POINT AT TABS> These jQueryUI tabs are a central to the design of Machete version one.

The search box will search most visible fields for the data table. <SEARCH JIMMY> The search is server-side, implemented dynamically using the EntityFramework ORM. Searching for my name brings up my Employer record.

Double-clicking on a row opens a new tab, <D-CLICK JIMMY> an ‘Edit Employer’ tab that has the employer’s name as the tab text. This List-Create-Edit tab sequence is repeated throughout the application. 

Opening my Employer record, you see the data captured about me. Below the employer record, another set of List-Create-Edit tabs opens up. These are the Work Orders for the open Employer record. 

WORK ORDERS
Opening a Work Order loads more HTML from the server. A Work Order represents a single contact (i.e. a phone call or web request) from an Employer, who is requesting some number of workers for one or more days. An Employer can have multiple Work Order records. <POINT AT LIST> While most Employers only have a few Work Order records, some have hundreds.

The Work Order record duplicates the contact and address information of the Employer, since the location of the work can be different from the Employer’s address, or the Employer address might change in the future. <POINT OUT> There are also fields for storing additional data necessary to fill the order.

The quickest way to create a new Work Order is to click the Copy Employer Info button <POINT>, then click the Save button. <POINT> This has been the most likely use case for Casa Latina. It’s possible, but uncommon, that the employer’s address is different from where the work will take place. Is such cases, the user taking the order would change the address here.

WORK ASSIGNMENTS
A final set of List-Create-Edit tabs also opens up below the Work Order record. This set is for Work Assignments. An assignment defines a space that one Worker will fill. For example, I may call Casa Latina and ask for two painters to help paint my house. This order would result in 1 Work Order record and 2 Work Assignment records created in the database.

While the Employer and Work Order tabs open to a list of existing records, the Work Assignment tabs at the bottom of this workflow open to the Create Work Assignment tab. We chose to do this to save time, since the most likely action at this point is that the user is creating a new assignment.

The defaults are settings most likely to be used. Sometimes the amount of labor needed is uncertain, or the employers will give a range of hours needed. If a range is given, then totals on the forms and the printed orders will display the range. You can click Save to create a default Work Assignment.

Saving the assignment opens up the new assignment in the Edit tab. The assignment's Work Order ID number is visible, along with an assignment suffix. Clicking on the List Work Assignments tab will cause the data table to refresh, and the new assignment will be visible.

Additionally, an 'Activate order' button appears. Activating a Work Order indicates that it is complete. This action changes its status from Pending to Active elsewhere in the application. Active orders are ready to be assigned workers through other workflows.
