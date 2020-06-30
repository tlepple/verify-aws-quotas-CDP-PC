#  AWS Pre-Reqs

---
---
### Notes:
---

*  Follow the instructions in order.

---
---

1.  Navigate to the AWS service `IAM` and create the user:
* Make sure that the user name is only created in lower case

---

![](./images/createAwsUser2.gif)

---

2. Save user credentials to your computer.

* TBD - Record steps video

---

![](./images/saveCredLarge.gif)

---

3.  Create a Key Pair in the EC2 Service

* TBD - Record steps video
![](./images/createKPlarge.gif)

---

4.  Export your AWS security credentials:

```
export AWS_ACCESS_KEY_ID=<Your AWS Access Key>
export AWS_SECRET_ACCESS_KEY=<Your AWS Secret Access Key>
export AWS_DEFAULT_REGION=<Your AWS Region>

```

---

*  TBD  Code Rest commands to check prereqs:

### Examples:

```
aws service-quotas get-service-quota     --service-code ec2     --quota-code L-1216C47A

aws service-quotas list-service-quotas \
    --service-code vpc

# list security group info for a tag
aws ec2 describe-security-groups \
    --filters Name=tag:owner,Values=tlepple
```

