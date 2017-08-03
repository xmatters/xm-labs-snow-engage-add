
# Engage with xMatters - Add to Call for the ServiceNow integration

The [xMatters integration for ServiceNow](https://store.servicenow.com/sn_appstore_store.do#!/store/application/5950d7444f2231000e9fa88ca310c78c) provides the ability to quickly assemble an xMatters-hosted conference bridge using the Engage with xMatters feature. However, there is no ability to add additional groups/useres to an existing xMatters-hosted conference bridge using that feature. This was due to limitations of the xMatters REST API. The API has now been updated to support the underlying requirements and the update set provided here allows the Engage with xMatters feature to take advantage in order to supporting adding groups/users to an existing xMatters-hosted conference bridge.

# Pre-Requisites
* ServiceNow Geneva or later
* ServiceNow integration to [xMatters v3.7.11+](https://store.servicenow.com/sn_appstore_store.do#!/store/application/5950d7444f2231000e9fa88ca310c78c/3.7.12)
* xMatters account - If you don't have one, [get one](https://www.xmatters.com)!

# Files
* [Engage with xMatters - Add to Call.xml](https://github.com/tkouhsari/xm-labs-snow-engage-add/blob/master/Engage%20with%20xMatters%20-%20Add%20to%20Call.xml) - Update set for ServiceNow.

# Installation
To import the update set into ServiceNow:
1. Download [Engage with xMatters - Add to Call.xml](https://github.com/tkouhsari/xm-labs-snow-engage-add/blob/master/Engage%20with%20xMatters%20-%20Add%20to%20Call.xml). 
2. Login to ServiceNow and navigate to Retrieved Update Sets.
3. Click on the **Import Update Set from XML** link.
4. Select the XML file you just downloaded and click **Upload**.
5. Click into the Engage with xMatters - Add to Call update set.
6. Click the **Preview Update Set** button.
7. Click the **Commit Update Set** button.

The update set introduces a new Script Include (xMattersAjaxExtended) and updates two UI Scripts (xm_mod_options_provider and xm_app_engage_xmatters). If you have modified the out-of-the-box UI Scripts, you may need to merge your changes into the update set. 	

That's it! There's no additional installation or configuration steps necessary.

# Testing
Login to ServiceNow and find an open Incident. Start an xMatters-hosted conference bridge using the Engage with xMatters feature. After that call is active (it may take 30 seconds to a minute), use the Engage with xMatters feature again from the same incident. This time, your Conference Bridge select box should give you your previous conference bridge number as an option. Selecting that number will allow you to add additional groups/users to that existing call.

# Troubleshooting
If the Conference Bridge select box does not show numbers for existing calls, check the System Logs in ServiceNow for any errors. 

