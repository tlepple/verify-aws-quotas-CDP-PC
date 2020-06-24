#  AWS Pre-Reqs

---
---
### Notes:
---

*  The below videos were recorded in 30 second segments to keep file sizes small (a requirement from github).
*  Follow the instructions in order.

---
---

1.  Navigate to the AWS service `IAM`:

---

![](https//github.com/tlepple/horizon-public-how2/provider/aws/images/nav2usersLarge.gif)

---


2.  Create an AWS User:

*  Make sure that the user name is only created in lower case

---

![](./images/createUserLarge.gif)

---

3. Save user credentials to your computer.

---

![](./images/saveCredLarge.gif)

---

4.  Add new user to the `Admins` group

*  This step will appear to fail.  The root cause is that we do not have the IAM Permission to list users part of the group `Admins`

![](./images/addUser2AdminsGroupLarge.gif)

---

5.  Verify that your user is part of group `Admins`

![](./images/verifyUserGroupLarge.gif)

---

6.  Create a Key Pair in the EC2 Service

![](./images/createKPlarge.gif)

---
---

