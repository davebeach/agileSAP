# Function Module READ_WORKLOAD
## Use
This function module is a component of the CS-SDL interface with which an external scheduling system can be connected to the order processing function in the application areas Plant Maintenance and Customer Service .

## Integration
The function module READ_WORKLOAD defines the interface with which the actual dates for the technician are read from the external scheduling system when the graphical monitor is started or refreshed.

## Prerequisites
You have assigned the function module READ_WORKLOAD to the fixed value R in Customizing under  Plant Maintenance and Customer Service    Maintenance and Service Processing    Maintenance and Service Orders    Scheduling    External Scheduling    Configure Communication  .

## Features
Import Parameters

<div class="table-wrapper tablenoborder">
   <table summary="" class="table" frame="border" border="1" rules="all" style="width: auto;">
   <tbody class="tbody">
        <tr class="row">
        <td class="entry" valign="top">
            <p class="p"><span class="ph emphasis emphasis">Parameter Name</span></p>
        </td>
        <td class="entry" valign="top">
            <p class="p"><span class="ph emphasis emphasis">Component</span></p>
         </td>
        <td class="entry" valign="top">
            <p class="p"><span class="ph emphasis emphasis">Data Type</span></p>
        </td>
        <td 
            <p class="p"><span class="ph emphasis emphasis">Length</span></p>
        </td>
        <td class="entry" valign="top">
          <p class="p"><span class="ph emphasis emphasis">Short Text</span></p>
        </td>
        </tr>
       <tr class="row">
          <td class="entry" valign="top">
             <p class="p"> START_DATE </p>
             
             
          </td>
          
          
          <td class="entry" valign="top">&nbsp;</td>
          
          
          <td class="entry" valign="top">
             <p class="p"> DATS </p>
             
             
          </td>
          
          
          <td class="entry" valign="top">
             <p class="p"> 8 </p>
             
             
          </td>
          
          
          <td class="entry" valign="top">
             <p class="p"> Date and time, local date of user </p>
             
             
          </td>
          
          
       </tr>
       
       
       <tr class="row">
          <td class="entry" valign="top">
             <p class="p"> END_DATE </p>
             
             
          </td>
          
          
          <td class="entry" valign="top">&nbsp;</td>
          
          
          <td class="entry" valign="top">
             <p class="p"> DATS </p>
             
             
          </td>
          
          
          <td class="entry" valign="top">
             <p class="p"> 8 </p>
             
             
          </td>
          
          
          <td class="entry" valign="top">
             <p class="p"> Date and time, local date of user </p>
             
             
          </td>
          
          
       </tr>
       
       
       <tr class="row">
          <td class="entry" valign="top">
             <p class="p"> WORKCENTER_ </p>
             
             
             <p class="p">ID</p>
             
             
          </td>
          
          
          <td class="entry" valign="top">&nbsp;</td>
          
          
          <td class="entry" valign="top">
             <p class="p"> NUMC </p>
             
             
          </td>
          
          
          <td class="entry" valign="top">
             <p class="p"> 8 </p>
             
             
          </td>
          
          
          <td class="entry" valign="top">
             <p class="p"> Operating resources object ID </p>
             
             
          </td>
          
          
       </tr>
       
       
    </tbody>
     </table>
</div>

<p>When this function module is called, the system transfers the work center ID that inquires about the current technician assignments to you using the parameter WORKCENTER_ID . At the same time, you receive a list of the current technicians for this work center in the table MSM_PERSON . The components OTYPE has the fixed value P .</p>

<p>After the function module has been called, the list of technician assignments should be available in the table RIGHT_HAND . The component REFID must refer to a valid PERNR component. You transfer the order number using the component ID . The component TYPE must have the fixed value X .</p>