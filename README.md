# User Guide

(1) download source using tar file 

(2) upload tar file at /home/gpadmin directory in the master node

(3) change the directory name

$ tar -xvf hc_chk.tar

(4) run the diag shell script

$ cd /home/gpadmin/diag

$ sh 09_daily_db_hc_chk.sh
$ sh 10_weekly_db_hc_chk.sh
$ sh 11_monthly_db_chk.sh : 11_monthly_db_chk.sh File a is the same as 00_run_diag.sh file.
$ 00_run_diag.sh file : GPDB 6.x assessment report generate shell script.

-----------------------------------------------------------------
# Summary

How to 
$ sh 09_daily_db_hc_chk.sh
$ sh 10_weekly_db_hc_chk.sh

#Review Report Results
/home/gpadmin/diag/hc_chk/daily
/home/gpadmin/diag/hc_chk/weekly


#Daily Items
1. Check resource usage by segment
2. Full table list (except leaf partition table)
3. Size by schema
4. Each table size
5. Table list with frequent access
6. Check error message (by frequency)
7. partition table list
8. Data file disk usage by segment
9. Check disk usage trends per hour
10. SQL list performed for a long time in the last week
11. Table list that needs to be updated for statistics
12. Check mirror segment status

#Weekly items (last week, daily + weekly items performed)
1. Check system resource usage (15 seconds, 1 minute, 10 minutes, 1 hour)
2. Usage by Resource Group (last week, 1 minute, 10 minutes)

#monthly
1. OS Parameters (Master, Standby Master, All Segments)
2. Check gpdb parameter setting value
3. Check DB version and various component versions (required for critical bug checks)
4. Check table blot (catalog/user table)
5. Skew check


-----------------------------------------------------------------

# Requirement

(1) gpadmin user should have privilege to use sudo command without password

(refernece url : https://docs.vmware.com/en/VMware-Greenplum/6/greenplum-database/install_guide-prep_os.html#topic23)

(2) A version of gpcc 6.x or higher must be installed.

If the gpcc is not installed or in a non-operating state, some of the report result are not generated.

------------------------------------------------------------------

(refernece url : https://docs.vmware.com/en/VMware-Greenplum/6/greenplum-database/install_guide-prep_os.html#topic23)
