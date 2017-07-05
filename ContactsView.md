| [ <--- Back to main ReadMe](README.md) | _____________________________ | [ <--- Previous Step (Accounts List) ](AccountsList.md) |
|:---------------------------------------|:------------------------------|:--------------------------------------------------------|
# Contacts View -- the Detail view of Master-Detail

### Create a DataGrid inside a DataView to display Contacts of Account
##### Now we need another DataGrid to display _SFDC Contacts_ that responds to the clicked row from _SFDC Accounts_. In order to do this we first need to create a DataView that is associated with the _Account_   entity.

   * Right-click on the Container and "Add Column Right" (Optional --
     repeat this to add a third column)

     <a href="./images/Accounts/Page_Grid_Container_Add.jpg"><img
     src="./images/Accounts/Page_Grid_Container_Add.jpg" ></a>

   * Configure columns for a 4-4-4 grid space (this is just an example
     layout for screen real estate - 3 even columns)  
     <a
     href="./images/Accounts/Page_Grid_Container_Assign_Width.jpg"><img
     src="./images/Accounts/Page_Grid_Container_Assign_Width.jpg"></a>  
        -The Container view should look something like the following:  
           <a
     href="./images/Accounts/Page_Grid_Container_Layout_2.png"><img hspace=60
     src="./images/Accounts/Page_Grid_Container_Layout_2.png"></a>

* Select DataView and place it on the page in the second column. Give it
  a Common Name of "ContactsDataView"
    -  Set the _Data source_ of the _**ContactsDataView**_ to List widget:
       Data grid '**AccountsGrid**'  
  <a href="./images/Accounts/Contacts_DataView_Wrapper.jpg"><img
  src="./images/Accounts/Contacts_DataView_Wrapper.jpg" ></a>
        Association to Account (do not auto-populate the fields)

* Add a DataGrid inside the _**ContactsDataView**_ and give it a name
  "ContactsGrid"

  <a
  href="./images/Accounts/Contacts_DataGrid_Assign_Grid_Name.jpg"><img
  src="./images/Accounts/Contacts_DataGrid_Assign_Grid_Name.jpg"
  align="left" ></a>

* Assign the Data Source to reference List Widget --> Data grid 'AccountsGrid'
  * reference List Widget --> Data grid 'AccountsGrid'  
    <a href="./images/Accounts/Contacts_DataGrid_DataSource.jpg"><img
    src="./images/Accounts/Contacts_DataGrid_DataSource.jpg" ></a>
  * If you did not hit OK on the previous step your DataGrid will look like the following showing a name of ***grid1***  
      <a href="./images/Accounts/Contacts_DataGrid_DataSource_grid1.jpg"><img
          src="./images/Accounts/Contacts_DataGrid_DataSource_grid1.jpg" ></a>

* Select ***Yes*** to the Auto-Populate option to fill in the default fields of the Contact  
    <a href="./images/Accounts/Automatically_Fill_Contents_DataGrid.jpg"><img
              src="./images/Accounts/Automatically_Fill_Contents_DataGrid.jpg" ></a><br/>

* The Mendix Designer view should look something like the following:  
    <a href="./images/Accounts/Page_Mendix_Accounts_Contacts.jpg"><img
                  src="./images/Accounts/Page_Mendix_Accounts_Contacts.jpg" ></a>
* Run Locally (or wherever you choose to run it)

    >Results will vary depending on the ***Salesforce*** data you have available.  
    >The data I am referencing was imported as a sample dataset into ***Salesforce***.
    >
    >**NOT ALL ACCOUNT HAVE CONTACTS in my data** -- that is the reason for the
    >initial error.
    >
    > If your data is more complete and have Contacts for all Accounts, then you will not see this error
    >

    - Running with my data I see the following  
        <a href="./images/Accounts/Running_Accounts_Contacts_Initial.jpg"><img
      src="./images/Accounts/Running_Accounts_Contacts_Initial.jpg" ></a>

    - Clicking OK on the error  
        <a href="./images/Accounts/Running_Accounts_Contacts_AfterOkError.jpg"><img
          src="./images/Accounts/Running_Accounts_Contacts_AfterOkError.jpg" ></a>

    - Clicking on another ***Account*** row  
        <a href="./images/Accounts/Running_Accounts_Contacts_OnClickRefresh.jpg"><img
          src="./images/Accounts/Running_Accounts_Contacts_OnClickRefresh.jpg" ></a>
  - A quick screenshot of it running  
    <a href="./images/Accounts/Anim_MD_Accounts_Contacts_C2A.gif"><img
    src="./images/Accounts/Anim_MD_Accounts_Contacts_C2A.gif"
    hspace="40"></a>

> **So far all the inputs and configurations have been primarily using the
> default settings with the obvious exception of giving a name to a Widget.**
>
 >There are a couple obvious and reasonably simple steps to further configure our services and UI
>1. Gracefully handle empty or null input values for microservices
>    - configure visibility of the DataGrid based on an ***expression value***  
>       **OR**
>    - Extend the microservice to be more flexible on running with a null input parameter
>
>2. Modify the data / columns being display to make better use of screen real estate
>
___


| [ <--- Back to main ReadMe](README.md) | __________________________ | [Next Step (Avoiding Errors for empty parameters) --->](AvoidErrorForEmptyValue.md) |
|:---------------------------------------|:---------------------------|:-----------------------------------------------------------------------------------|
