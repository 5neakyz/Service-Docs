<script setup>
import WelcomeItem from "./WelcomeItem.vue";
// import DocumentationIcon from "./icons/IconDocumentation.vue";
// import ToolingIcon from "./icons/IconTooling.vue";
// import EcosystemIcon from "./icons/IconEcosystem.vue";
// import CommunityIcon from "./icons/IconCommunity.vue";
// import SupportIcon from "./icons/IconSupport.vue";
</script>

<template>
  <welcomeItem>
    <h1>TRIAGE DOCUMENT</h1>
    <p>By Ben Knox</p>
    <blockquote>
      <p>
        This is a quickly put together website and so (as is noticeable) not
        great
      </p>
    </blockquote>
  </welcomeItem>
  <welcomeItem>
    <template #heading1>CRO Lines - Booking In</template>
    <h3 id="CRO-sbs">Step by Step</h3>
    <br />
    <ol>
      <li>
        <p>
          On the <abbr title="Component Repair Order">CRO</abbr> Repair Line
          Screen click the search button (F3) and enter the serial number of the
          device, and search.
        </p>
      </li>
      <blockquote>
        <p>
          This should
          <a href="#rma-team">(If it Doesn’t)</a> return a line with all the
          relevant info about the device.<br />
          The Status should be <strong>planned</strong>.<br />
          You can ignore any lines with Status <strong>Completed </strong>or
          <strong>Cancelled</strong>, these have already been processed.<br />
          Always Check the Error Description; DVR’s often need Footage
          Retrieval.
        </p>
      </blockquote>
      <li>
        <p>
          On the Line <abbr title="Right Mouse Button">RMB</abbr> and select
          Receipt. The Status should change from <strong>Planned</strong> to
          <strong>Released</strong>.
          <a href="#booking-in-errors"> (Cannot Receipt In)</a>
        </p>
        <blockquote>
          <p>
            This will now book the unit in and create a Shop Order for it.<br />How
            to <a href="#rma-team">(Un-Receipt)</a> a unit (if you booked it in
            by accident or need to change something.
          </p>
        </blockquote>
      </li>
      <li>
        <p>
          <abbr title="Right Mouse Button">RMB</abbr> the line and select
          <strong>
            Print <abbr title="Component Repair Order">CRO</abbr> Label</strong
          >.
        </p>
      </li>
      <blockquote>
        <p>A Quick Report query box will pop up, press ok (Enter key)</p>
      </blockquote>
      <li>
        <p>
          Press the printer button in the top right and print.
          <a href="#printer-settings">Printer Settings</a>
        </p>
      </li>
      <blockquote>
        <p>
          Double check the information on the ticket preview matches<br />
          If there is no shop order number then you have printed before
          receipting in the unit.<br />If the Printer settings are correct, then
          you can double click the printer and it will print.
        </p>
      </blockquote>
      <li>
        <p>Finally stick the label to the correct unit.</p>
      </li>
    </ol>
    <br />
  </welcomeItem>
  <welcomeItem>
    <template #heading4>Error Type Codes</template>
    <table id="CRO-type-codes">
      <thead>
        <tr>
          <th>Code</th>
          <th>Description</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>A</td>
          <td>Standard Repair</td>
        </tr>
        <tr>
          <td>B</td>
          <td>Dekit</td>
        </tr>
        <tr>
          <td>C</td>
          <td>Standard Repair but for JCB</td>
        </tr>
        <tr>
          <td>H</td>
          <td>Return to Stores (Dekit)</td>
        </tr>
        <tr>
          <td>F</td>
          <td>Decommission</td>
        </tr>
      </tbody>
    </table>
    <div id="printer-settings"></div>
  </welcomeItem>
  <welcomeItem>
    <template #heading4>Printer Settings</template>
    <p>
      In printer preferences the default stock will always be
      <strong>USER</strong>.<br />
      You will need to set the dimensions to <strong>101.6mm x 127.0mm</strong>.
    </p>
    <blockquote>
      <p>
        You cannot be permanently change which profile the printer defaults to,
        so just change the dimensions of the default profile (USER).<br />
        The Dimensions of the Default Profile (USER) might change if someone
        else logs onto your computer.
      </p>
    </blockquote>
    <div id="booking-in-errors"></div>
  </welcomeItem>
  <welcomeItem id="booking-in-errors">
    <template #heading3>Booking in Errors</template>
    <h4 id="rma-team">
      <abbr title="Return Materials Authorization">RMA</abbr> Team
    </h4>
    <p>
      If a unit is not on a <abbr title="Component Repair Order">CRO</abbr> then
      you need to Email the
      <abbr title="Return Materials Authorization">RMA</abbr> Team with all the
      info you have on the unit.
    </p>
    <blockquote>
      <p>
        The Serial number of the unit.<br />
        Any paperwork the device has come with.<br />
        are any units in the same box on a
        <abbr title="Component Repair Order">CRO</abbr>?<br />
        The info on the delivery note on the box.
      </p>
    </blockquote>
    <br />
    <hr />
    <br />
    <h4 id="serial-number-is-already-in-use">
      Serial Number is already in use
    </h4>
    <p>
      <strong>Reason</strong><br />
      The unit is showing on stock.<br />
      <strong>Resolution</strong><br />
      Search in <abbr title="Inventory Part in Stock">IPIS</abbr> using the
      serial number that was presented in the error box and
      <a href="#count">Count</a> the device off.<br />
      Then you can book the device in.
    </p>
    <br />
    <hr />
    <br />
    <h4 id="product-structure-header-does-not-exist-for-shop-order-part">
      Product Structure Header does not exist for shop order part
    </h4>
    <p>
      <strong>Reason</strong><br />
      The unit does not have a repair structure type in Product Structure.<br />
      <strong>Resolution</strong><br />
      Speak with line manager<br />
      It might be “easier” to create a new serial object with a similar but
      fully setup Part No.<br />
      The actual way is to raise a
      <abbr title="Product Engineering">PE</abbr> request, truthfully this
      should not take very long providing the part already has all the necessary
      approvals.
    </p>
    <br />
    <hr />
    <br />
    <h4
      id="field-serial_no-is-mandatory-for-inventory-part-in-stock-and-requires-a-value"
    >
      Field [Serial_NO} is mandatory for inventory part in stock and requires a
      value
    </h4>
    <p>
      <strong>Reason</strong><br />
      This Error is because the unit does not have a part no, or its
      <strong>unknown</strong>.<br />
      <strong>Resolution</strong><br />
      Check the device has a serial object / part serial.
      <a href="#search-via-psn"
        >(Search via <abbr title="Persistent Serial Number">PSN</abbr>)</a
      ><br />
      If it does have a part serial then just re-add it to the
      <abbr title="Component Repair Order">CRO</abbr>.
      <a href="#adding-to-a-cro"
        >(Adding to a <abbr title="Component Repair Order">CRO</abbr>)</a
      ><br />
      If it does not then you will need to generate an object
      <a href="#generating-objects">(Generating Objects)</a> and then add the
      unit to the <abbr title="Component Repair Order">CRO</abbr>.
      <a href="#adding-to-a-cro"
        >(Adding to a <abbr title="Component Repair Order">CRO</abbr>)</a
      >
    </p>
    <br />
    <hr />
    <br />
    <h4 id="serial--already-exists-and-is-contained-in-parent....">
      Serial [] already exists and is contained in parent…
    </h4>
    <p>
      <strong>Reason</strong><br />
      The unit has multiple serial objects and the
      <abbr title="Component Repair Order">CRO</abbr> has picked the wrong part
      serial.<br /><strong>Resolution</strong><br />
      Using
      <a href="#search-via-psn"
        >(Search via <abbr title="Persistent Serial Number">PSN</abbr>)</a
      >
      get all the serial numbers for the device and open all of the part
      serials. one (typically the one using the Serial number of the device) of
      the part serials will have its Current Position as:
      <strong>Contained</strong>. Open the attachments tab, then select
      characteristics, in the technical class remove the
      <abbr title="Persistent Serial Number">PSN</abbr>. Then re-add the device
      to the <abbr title="Component Repair Order">CRO</abbr>.
      <a href="#creating-&amp;-adding-to-a-cro"
        >(Adding to a <abbr title="Component Repair Order">CRO</abbr>)</a
      >
    </p>
    <br />
    <hr />
    <br />
    <h4
      id="the-ownership-should-be-customer-owned-to-receive-parts-directly-to-the-cro-repair-line"
    >
      The ownership should be Customer-Owned to receive parts directly to the
      <abbr title="Component Repair Order">CRO</abbr> repair line
    </h4>
    <p>
      <strong>Reason</strong><br />
      on the line the ownership of the unit is set to Company owned. the
      <abbr title="Component Repair Order">CRO</abbr> has been set up
      incorrectly. <br /><strong>Resolution</strong><br />
      Contact the <abbr title="Return Materials Authorization">RMA</abbr> team.
      To change them on the unit line select the box where it says company owned
      and change it to customer owned.
    </p>
    <div id="shipments"></div>
  </welcomeItem>
  <welcomeItem>
    <template #heading1>Shipments</template>
    <h3>Step by Step</h3>
    <br />
    <ol>
      <li>
        <p>
          Take the unit from the pre-shipments trolley. On the job conclusion
          sheet take the <abbr title="Component Repair Order">CRO</abbr> number
          and search using it, in the Component Repair Order Screen. Check the
          Serial number is on the
          <abbr title="Component Repair Order">CRO</abbr> and the Status is
          <strong>Completed</strong>. (<a href="#job-incomplete">If Not</a>)
        </p>
      </li>
      <br />
      <li>
        <p>
          In the header <abbr title="Right Mouse Button">RMB</abbr> and select
          <strong>go to customer order</strong>
        </p>
      </li>
      <blockquote>
        <p>
          If the <abbr title="Serial Number">S/N</abbr> of the unit is not in
          the Customer Order then go back to the
          <abbr title="Component Repair Order">CRO</abbr> and on the line of the
          unit <abbr title="Right Mouse Button">RMB</abbr> and select
          <strong>Customer Order Handling</strong> and <strong>View</strong>.
          you might want to query with the
          <abbr title="Return Materials Authorization">RMA</abbr> Team to make
          sure everything is correct.
        </p>
      </blockquote>
      <li>
        <p>
          Find the device or devices. Ensure that status of the unit is
          <strong>reserved</strong> and tick the
          <strong>Connect to shipments</strong> box for all the devices you have
          and Save.
          <a href="#not-reserved">If the unit is still showing as Released</a>
        </p>
        <blockquote>
          <p>
            Exchanged Units will have the original Line with
            <abbr title="Serial Number">S/N</abbr> of the devices that came in
            <strong>Cancelled</strong> and a replacement line with no
            <abbr title="Serial Number">S/N</abbr> on the line will appear. To
            check the correct device is selected,
            <abbr title="Right Mouse Button">RMB</abbr> the line and select
            <strong>Manual Reservations</strong> to see which device is
            allocated to the line.
          </p>
        </blockquote>
      </li>
      <li>
        <p>
          Now <abbr title="Right Mouse Button">RMB</abbr> in the header and
          Select <strong>Release</strong> if its an option.
        </p>
        <blockquote>
          <p>
            In the header of the Customer Order there is also a Status box, if
            this is planned then you need to <strong>Release</strong> the Order.
            if the Status is Blocked then you need to contact
            <a href="#accounts-receivables">Account Receivables</a>.<br />
            If the Status is <strong>Reserved</strong>,
            <strong>Picked</strong> or <strong>Partially Delivered</strong> Then
            the Customer Order has already been <strong>Released</strong> and so
            you can skip this step.
          </p>
        </blockquote>
      </li>
      <li>
        <p>
          <abbr title="Right Mouse Button">RMB</abbr> in the header and select
          <strong>Connect to Shipment</strong>. Then
          <abbr title="Right Mouse Button">RMB</abbr> in the header and select
          <strong>Shipment Info</strong>.
        </p>
      </li>
      <br />
      <li>
        <p>
          In the Shipment Lines Screen
          <abbr title="Right Mouse Button">RMB</abbr> the very bottom Line and
          select <strong>Shipment</strong>
        </p>
        <blockquote>
          <p>
            The very bottom line is the newest created shipment, so the shipment
            ID should also be the highest.<br />
            If you have connected multiple devices you do not need to select all
            the lines for that shipment in the Shipment Lines Screen, as this
            just opens the shipment that all the devices are on anyway.
          </p>
        </blockquote>
      </li>
      <li>
        <p>
          on the shipment screen, double click in the
          <strong>Planned Ship Date/Time</strong> box and press Enter. This will
          enter today’s date.
        </p>
      </li>
      <br />
      <li>
        <p>
          Then click in the <strong>Forward Agent ID</strong> box and bring up
          the List of Values(F8) and select <strong>Send To Receiver</strong>.
        </p>
      </li>
      <br />
      <li>
        <p>
          Now Save. Then Tick the <strong>Released For Stores</strong> Box and
          Save again.
        </p>
      </li>
      <br />
      <h4 id="picking">Picking</h4>
      <br />
      <li>
        <p>
          On the shipments screen
          <abbr title="Right Mouse Button">RMB</abbr> the first unit’s Line and
          select <strong>Manual reservations</strong>. In the header of the
          Manual Reservations Screen
          <abbr title="Right Mouse Button">RMB</abbr>, if the top option is
          <strong>Report Received Quantities as Picked</strong> then select it
          and click ok to all the dialog boxes. You Must Repeat this for all
          units on the shipment. If you do not have this option, then see Step
          11.
        </p>
      </li>
      <br />
      <li>
        <p>
          Go to the <strong>Report Picking of Pick List Lines</strong> Screen
          and press f2 (or Search with out any parameters). This may return many
          pick lists, Some of these are stores
          <strong>DO NOT DO ANYTHING WITH THESE</strong>. find the pick list
          that has the shipment ID on the line that is your Shipment. Then in
          the Header <abbr title="Right Mouse Button">RMB</abbr> and select
          <strong>Report Picking of Pick List Lines</strong> and then click ok
          to all the dialog boxes.
        </p>
      </li>
      <br />
      <li>
        <p>
          Now if you go back to the shipment screen and refresh. You should see
          the Status is <strong>Completed</strong> and the Next Step in Shipment
          Flow is <strong>Deliver</strong>.
        </p>
        <blockquote>
          <p>
            How to Know if you need Step 10 or Step 11.<br />
            If the Customer order had already been released when you started the
            shipment process then its likely you will need step 10.<br />
            If you released the Customer Order that cycle/Process, then you need
            step 11.<br />
            If the customer order was blocked when you released it the you need
            step 10
          </p>
        </blockquote>
      </li>
    </ol>
    <br />
    <hr />
    <h2 id="shipment-errors">Shipment Errors</h2>
    <br />
    <hr />
    <h3 id="job-incomplete">Job incomplete</h3>
    <p>
      If the Status on the <abbr title="Component Repair Order">CRO</abbr> line
      is still Released. then find out who was doing the job.<br />
      Using Clocking on shop floor work bench.<br />
      In <abbr title="Component Repair Order">CRO</abbr> repair lines, search
      <abbr title="Serial Number">S/N</abbr>,
      <abbr title="Right Mouse Button">RMB</abbr> line select
      <strong>Repair Order</strong> and <strong>Repair Shop Order</strong>,
      click on operations tab in shop order,
      <abbr title="Right Mouse Button">RMB</abbr> on the line select
      <strong>shop floor Clockings</strong><br />
      Then pass back to the engineer to complete the job
    </p>
    <br />
    <hr />
    <h3 id="not-reserved">Not Reserved</h3>
    <p>
      Try <abbr title="Right Mouse Button">RMB</abbr> on the units line and
      select <strong>Manual Reservations</strong> see if you can Reserve the
      unit.<br />
      (More Info to come)
    </p>
    <br />
    <hr />
    <h3 id="accounts-receivables">Accounts Receivables</h3>
    <p>
      If a Customer Order is blocked Then you need to Email Accounts Receivable
      with the Customer Order Number.<br />
      This Email can be as simple as
    </p>
    <pre><code>HI

Please Release 
O123456

Thanks
Name
</code></pre>
  </welcomeItem>
</template>
