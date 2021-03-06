Lab 6.1 - Segmentation - Profile Attribute Segmentation
==========
<table style="border-collapse: collapse; border: none;" class="tab" cellspacing="0" cellpadding="0">

<tr style="border: none;">

<div align="left">
<td width="600" style="border: none;">
<table>
<tbody valign="top">
      <tr width="500">
            <td valign="top"><h3>Objective:</h3></td>
            <td valign="top"><br>In this exercise, we’ll create a basic segment using a single field in Call Center ExperienceEvent.
</br>
<br>A marketer wants to create a basic segment for customers who report Account security issues with a Call Center representative.</br>
            </td>
     </tr>
     <tr width="500">
           <td valign="top"><h3>Prerequisites:</h3></td>
           <td valign="top"><br>none</td>
     </tr>
</tbody>
</table>
</td>
</div>

<div align="right">
<td style="border: none;" valign="top">

<table>
<tbody valign="top">
      <tr>
            <td valign="middle" height="70"><b>section</b></td>
            <td valign="middle" height="70"><img src="https://github.com/adobe/AEP-Hands-on-Labs/blob/master/assets/images/left_hand_nav_menu_segments.png?raw=true" alt="Segments"></td>
      </tr>
      <tr>
            <td valign="middle" height="70"><b>version</b></td>
            <td valign="middle" height="70">1.0.1</td>
      </tr>
      <tr>
            <td valign="middle" height="70"><b>date</b></td>
            <td valign="middle" height="70">2020-01-06</td>
      </tr>
</tbody>
</table>
</td>
</div>

</tr>
</table>

Instructions:
-----------------
1.	Navigate to Segment Builder in the left navigation

      <kbd><img src="./images/segmenthome.png"  /></kbd>

2.    Click "Create segment" on the top right.

      <kbd><img src="./images/createsegment.png"  /></kbd>

3.	Click the gear icon to the right of Fields in the left pane

      <kbd><img src="./images/segmentfieldsgear.png"  /></kbd>

4.	Verify ‘Show full XDM schema’ is selected, and if not, select it
           
      <kbd><img src="./images/segment_gear.png"  /></kbd>
      
5.	Click on the gear icon again to hide the setting

      <kbd><img src="./images/segmentfieldsgearclose.png"  /></kbd>

6.	Select ‘Events’ under Fields

      <kbd><img src="./images/segmentevents.png"  /></kbd>

7.	Click on ‘XDM ExperienceEvent’ under Browse Classes

      <kbd><img src="./images/segment_xdm_ee.png"  /></kbd>
      
8.	Click on ‘Adobeamericaspot 1’ to expand the objects below that namespace
      
      <kbd><img src="./images/segment_xdm_pot1.png"  /></kbd>

9.	Click on ‘callcenterDetails’
   
      <kbd><img src="./images/segment_xdm_calldetails.png"  /></kbd>      

10.	Drag the ‘callSelectedReason’ field over to the Segment canvas
            
      <kbd><img src="./images/segment_fsi_callselectedreason.png"  /></kbd>    
      
11.	In the text box to the right of equals, type “Account Security Issue” and press ‘Enter’
           
      <kbd><img src="./images/segment_fsi_account_security_issue.png"  /></kbd>  

12.	Enter the segment name “Call Center Account Security” followed by your Student ID (e.g. “Call Center Account Security 025”)
	<br>Enter the same value as the description
      
      <kbd><img src="./images/segment_fsi_segmentname.png"  /></kbd>       
           
13.	Save the Segment
           
      <kbd><img src="./images/segment_fsi_save.png"  /></kbd>  
      
NOTE: Estimate link may not show results if qualified profiles are statistically small and not recognized across datset scans 
<br>
<br>
<br>


Lab 6.2 - Segmentation - Profile Attribute with Experience Event Segmentation (Multi-Entity Segmentation)
==========
<table style="border-collapse: collapse; border: none;" class="tab" cellspacing="0" cellpadding="0">

<tr style="border: none;">

<div align="left">
<td width="600" style="border: none;">
<table>
<tbody valign="top">
      <tr width="500">
            <td valign="top"><h3>Objective:</h3></td>
            <td valign="top"><br>Similar to the prior lab, in this lab you will build a customer segment based on the unified experience event data (from EE Schemas/Datasets) that are streaming into platform</td>
     </tr>
     <tr width="500">
           <td valign="top"><h3>Prerequisites:</h3></td>
           <td valign="top"><br>none</td>
     </tr>
</tbody>
</table>
</td>
</div>

<div align="right">
<td style="border: none;" valign="top">

<table>
<tbody valign="top">
      <tr>
            <td valign="middle" height="70"><b>section</b></td>
            <td valign="middle" height="70"><img src="https://github.com/adobe/AEP-Hands-on-Labs/blob/master/assets/images/left_hand_nav_menu_segments.png?raw=true" alt="Segments"></td>
      </tr>
      <tr>
            <td valign="middle" height="70"><b>version</b></td>
            <td valign="middle" height="70">1.0.1</td>
      </tr>
      <tr>
            <td valign="middle" height="70"><b>date</b></td>
            <td valign="middle" height="70">2020-01-06</td>
      </tr>
</tbody>
</table>
</td>
</div>

</tr>
</table>

Instructions:
-----------------
<ol>
 <li>In the left navigation, select 'Segments' if you are not already there.</li>
<li>In the upper right corner, select 'Create Segment'.</li>
<li>In the right pane within the 'Create Segment' interface, enter the segment name 'High Credit Card Propensity' following by your Student Number (e.g. 'High Credit Card Propensity 001'). Enter the same value in the Description field.</li>
<li>If the 'Streaming' toggle is not active, activate it.</li>
<li>In the left pane, drill down the 'XDM ExperienceEvent' under Attributes by clicking on it.</li>
<li>Under 'Browse Attributes', click on 'Adobeamericaspot 1'.</li>
<li>Expand 'propensityProfileDetails' and drag 'propensityCreditCard' to the segment canvas</li>	
<li>Select "is greater than" from the condition list box and enter "5" in the text box</li>	

<kbd><img src="./images/seg_propensity.png"  /></kbd>  	

<li>In the left pane, select 'Events' under 'Fields.</li>
<li>Click on 'XDM ExperienceEvent' under 'Browse Classes'.</li>
<li>Click on 'Adobeamericaspot1' to expand the object. </li>
<li>Click on 'transactionDetails' to expand the object</li>
<li>Locate 'transactionType' and drag this to the segment canvas.</li>
<li>Once 'transactionType' appears in the segment canvas, select 'Equals' as the condition and enter 'Savings' in the text box and press 'Enter'.</li>

<kbd><img src="./images/seg_transType.png"  /></kbd>  	

<li>In the left pane, locate 'transactionSKU' and drag this field to the segment canvas underneath 'transactionType' (the first event). The new event should be "stacked" below the first event as shown below</li>

<kbd><img src="./images/seg_transSku.png"  /></kbd>  	

<li>Enter 'prd1076' in the text box to the right of 'transactionSKU =' and press 'Enter'.</li>     
<li>At the top of the ‘Events’ canvas, update the time value to ‘In last 24 Hour(s)’</li>
<li>Save your segment</li>
</ol>    
 
<br>
<br>
<br>

Return to [Lab Agenda Directory](https://github.com/adobe/AEP-Hands-on-Labs/blob/master/labs/fsi/README.md#lab-agenda)
 
 
