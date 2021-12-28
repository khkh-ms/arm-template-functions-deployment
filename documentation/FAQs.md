# Frequently Asked Questions (FAQs)

Q : When is dependsOn required?

A : Dependencies are required for resources that are deployed within the same template, especially when the order of creation matters. For Example: If function app site and ZipDeploy extension are being deployed in the same template, then it is important to declare that the ZipDeploy resource depends on the site. Because only after the creation of the site, we want to create ZipDeploy extension for deployment.
<br /><br />

Q : What type of value is required for dependsOn?

A : Its value is a JavaScript Object Notation (JSON) array of strings, each of which is a resource name or ID. A full `resourceId` can also be used for the dependency but is only necessary when two or more resources share the same name (which should be avoided).
<br /><br />

Q : Can we use the appSetting `WEBSITE_RUN_FROM_PACKAGE=1` with MSDeploy?

A : No. The appSetting `WEBSITE_RUN_FROM_PACKAGE=1` is only available with ZipDeploy. This is the recommended path of deployment.
<br /><br />