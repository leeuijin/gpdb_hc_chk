# User Guide

(1) download source using zip file 

(2) upload zip file at /home/gpadmin directory in the master node

(3) change the directory name

$ tar -xvf xxx.tar

(4) run the diag shell script

$ cd /home/gpadmin/diag

$ sh 00_run_diag.sh

-----------------------------------------------------------------

# Requirement

(1) gpadmin user should have privilege to use sudo command without password

(refernece url : https://docs.vmware.com/en/VMware-Greenplum/6/greenplum-database/install_guide-prep_os.html#topic23)

(2) A version of gpcc 6.x or higher must be installed.

If the gpcc is not installed or in a non-operating state, some of the report result are not generated.

------------------------------------------------------------------

(refernece url : https://docs.vmware.com/en/VMware-Greenplum/6/greenplum-database/install_guide-prep_os.html#topic23)
