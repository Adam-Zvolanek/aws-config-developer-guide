# iam\-role\-managed\-policy\-check<a name="iam-role-managed-policy-check"></a>

Checks if all AWS managed policies specified in the list of managed policies are attached to the AWS Identity and Access Management \(IAM\) role\. The rule is NON\_COMPLIANT if an AWS managed policy is not attached to the IAM role\. 

**Identifier:** IAM\_ROLE\_MANAGED\_POLICY\_CHECK

**Trigger type:** Configuration changes

**AWS Region:** All supported AWS regions except Middle East \(UAE\), Europe \(Spain\), Europe \(Zurich\) Region

**Parameters:**

managedPolicyArnsType: CSV  
Comma\-separated list of AWS managed policy ARNs\.

## AWS CloudFormation template<a name="w2aac12c31c27b9d339c15"></a>

To create AWS Config managed rules with AWS CloudFormation templates, see [Creating AWS Config Managed Rules With AWS CloudFormation Templates](aws-config-managed-rules-cloudformation-templates.md)\.