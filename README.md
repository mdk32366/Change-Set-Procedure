# Change-Set-Procedure
Process to Follow in Performing Change Sets

##Before Deployment


+ You want to ensure no changes are made in production as you roll yours out, as deploying a change set will overwrite any changes to production.

+ You want to give yourself enough time to test your changes in production so you can ensure everything is working correctly before your users get in.

+ You don’t want users starting to work in it before it is fully deployed, or before you’ve had a chance to brief them fully.

+ Check the audit trail Check the audit trail in production to ensure no changes have been made that will be overwritten by your deployment. If they have, you may want to delay your deployment in order to get these changes copied over to the sandbox, or speak to the stakeholders involved.

+ Prepare your change set Prepare and validate your change set in advance. This can take a significant amount of time if you have to match things up between the sandbox and production, and you don’t want to miss your deployment window because you hadn’t prepared. There are a few things that may catch you out in validation, such as renaming standard fields and any changes to API names, so watch out for these!

+ Do a Full Export Do a full export of production data before deployment. If anything goes wrong, you want to make sure that your data remains intact, so a backup is essential before any big changes.

+ Build a Sandbox Copy Create another sandbox that’s a copy of your production org, so you’ve got a record of your existing setup and metadata. Again, if anything goes wrong, you want to be able to revert back to the current state of play if necessary.

+ Prepare test scripts Prepare the tests you will run after deployment to ensure everything is working correctly. Of course, as a good admin you’ll have already done your testing in your sandbox before creating the change set, but you should repeat it again in production to check everything has deployed as it should. Have these test scripts (step-by-step instructions on what to test and how) prepared in advance, so you and then your users can run through these tests quickly to check everything is functioning as expected.

+ Disable Email Deliverability Mass changes can trigger lots of system emails and notifications, so disable email deliverability while you deploy to ensure your users aren’t bombarded with an avalanche of mail. 

+ Deactivate Rules Deactivate validation rules, workflow rules, flows, process builders – anything that might impact changes or prevent them from deploying correctly. Make a note of what you’ve deactivated so you can reactivate it once your change set has deployed. Make sure that you run tests after you’ve reactivated these (and your new ones!), to ensure you have a fully functioning environment.

## After Deployment

### Data and Undeployed Changes 

+ Reactivate Anything Paused If you paused your workflows and validation rules during deployment, now is the time to reactivate them. Activate Workflows When deployed, rules and automations are not automatically activated. Activate your new Process Builders, workflows, validation rules – anything that might not be active on deployment. Test

+ Test your changes – Use the ‘log in as user’ feature to log in as different users and check their profile access and preferences – are you seeing what you’d expect to? Ask your champion users to help you test too, if possible.

+ Switch Email Deliverability Back On Now that testing is complete and you’re satisfied everything is working, you can enable email deliverability so your users can receive emails again.

