# Deploying a Conformance Pack Using the AWS Config Console<a name="conformance-pack-console"></a>

On the **Conformance packs** page, you can deploy a conformance pack for an account in a Region\. You can also edit and delete the deployed conformance pack\. 

## Deploy a Conformance Pack Using Templates<a name="deploy-cpack-using-sample-template"></a>

You can deploy a conformance pack using AWS Config sample templates or your own custom template\. For instructions on how to create personalized conformance packs, see [Custom Conformance Pack](https://docs.aws.amazon.com/config/latest/developerguide/custom-conformance-pack.html)\.

1. Sign in to the AWS Management Console and open the AWS Config console at [https://console\.aws\.amazon\.com/config/](https://console.aws.amazon.com/config/)\.

1. Navigate to the **Conformance packs** page and choose **Deploy conformance pack**\.

1. On the **Specify template** page, either choose a sample template or use an existing template\. 
   + If you choose **Use sample template**, select a **Sample template** from the dropdown list of sample templates\.

     For information about the contents of each template, see Conformance Pack Sample Templates\.
   + If you choose **Template is ready**, specify the template source\. It is either an Amazon S3 URI, an AWS Systems Manager document \(SSM document\), or a template that you upload\.

     If your template is more than 50 KB, upload it to the S3 bucket and select that S3 bucket location\. For example: s3://*bucketname/prefix*\.
**Important**  
Choose **Template is ready** if you created your conformance pack YAML file from scratch based on [Custom Conformance Pack](https://docs.aws.amazon.com/config/latest/developerguide/custom-conformance-pack.html)\.

1. Choose **Next**\.

1. On the **Specify conformance pack details** page, type the name for your conformance pack\.

   The conformance pack name must be a unique name with a maximum of 256 alphanumeric characters\. The name can contain hyphens but cannot contain spaces\. 

1. Optional: Add a parameter\. 

   Parameters are defined in your template and help you manage and organize your resources\.

1. Choose **Next**\.

1. On the **Review and deploy** page, review all of the information\. 

   You can edit the template details and conformance pack details by choosing **Edit**\.

1. Choose **Deploy conformance pack**\.

   AWS Config displays the conformance pack on the conformance pack page with the appropriate status\. 

   If your conformance pack deployment fails, check your permissions, verify that you did the prerequisite steps, and try again\. Or you can contact AWS Support\.

To deploy a **conformance pack using sample template with remediations**, see the [Prerequisites for Using a Conformance Pack With Remediation](cpack-prerequisites.md#cpack-prerequisites-remediations) and then use the preceding procedure\.

To deploy a **conformance pack with one or more AWS Config rules**, see the [Prerequisites for Using a Conformance Pack With One or More AWS Config Rules](cpack-prerequisites.md#cpack-prerequisites-oneormorerules)\.

## Edit a Conformance Pack<a name="edit-conformance-pack"></a>

1. To edit a conformance pack, select the conformance pack from the table\.

1. Choose **Actions** and then choose **Edit**\.

1. On the **Edit conformance pack** page, you can edit the template details, sample template, conformance pack, and parameters section\. 

   You cannot change the name of the conformance pack\.

1. Choose **Save changes**\.

   The conformance pack is displayed with the AWS Config rules\.

## Delete a Conformance Pack<a name="delete-conformance-pack"></a>

1. To delete a conformance pack, select the conformance pack from the table\.

1. Choose **Actions** and then choose **Delete**\.

1. On the delete *conformance pack* dialog box, confirm if you would like to permanently delete this conformance pack\. 
**Important**  
You cannot revert this action\. When you delete a conformance pack, you delete all of the AWS Config rules and remediation actions in that conformance pack\.

1. Enter **Delete** and choose **Delete**\.

   On the **Conformance packs** page, you can see the deployment status as **Deleting** until the conformance pack is completely deleted\.