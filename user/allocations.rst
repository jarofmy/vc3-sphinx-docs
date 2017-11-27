.. _allocations:

==========================
5. Connect an Allocation
==========================

After updating your profile, you can connect an allocation to the VC3 service.
An allocation, in VC3, is defined as combination of a username and resource
target that consumes some type of compute unit - regardless of whether it is
billed as Service Units (many HPC centers), dollars (AWS, GCE), or priority
(HTCondor and other opportunistic systems).

Clicking *My Allocations* on the left shows all allocations currently
associated with your account. You may select a new one by clicking
*Connect Allocation*.

.. image:: /image/screenshot_277.png

You will be able to select a resource target from the drop down menu, and enter
an account name for the resource. This is the same account name that you use to
SSH to the remote system.
.. image:: /image/screenshot_278.png

Once you've connected your allocation, the system will validate it.
.. image:: /image/screenshot_279.png

In order to create a virtual cluster, the VC3 software needs to be able to SSH
to the remote resource. If you click your allocation, you should see a section
titled *Public Token*.

.. image:: /image/screenshot_281.png

You will need to add this token to your Unix account, in the file
`~/.ssh/authorized_keys`. You can either edit this file with your favorite
editor (such as `nano`, `vim,` or `emacs`), or use the `echo` command to append
it to the authorized keys file.

.. image:: /image/screenshot_282.png

This token allows the VC3 system to SSH into a cluster _as you_ and submit jobs
on your, or your project's, behalf.
