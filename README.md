# User Guide

(1) download source using tar file 

(2) upload tar file at /home/gpadmin directory in the master node

(3) Uncompress tar file

$ tar -xvf hc_chk.tar

(4) run the diag shell script

$ cd /home/gpadmin/diag

$ sh 09_daily_db_hc_chk.sh

$ sh 10_weekly_db_hc_chk.sh

$ sh 11_monthly_db_chk.sh : 11_monthly_db_chk.sh File a is the same as 00_run_diag.sh file.

$ 00_run_diag.sh file : GPDB 6.x assessment report generate shell script.

-----------------------------------------------------------------
# Summary

#How to 

$ sh 09_daily_db_hc_chk.sh

$ sh 10_weekly_db_hc_chk.sh

# Report Results

/home/gpadmin/diag/hc_chk/daily

/home/gpadmin/diag/hc_chk/weekly


# Daily Items

1. Check resource usage by segment
2. All table list (except leaf partition table)
3. Size by schema
4. Each table size
5. Table list of frequent access
6. Check error message (by frequency)
7. Partitioned table list
8. Disk usage by segment (data file directory)
9. Check disk usage trends per hour
10. SQL list for a long time in the last week
11. Table list that needs to be updated for statistics (analyze)
12. Check mirror segment status (replication)

# Weekly items (last week, daily + weekly items included)

1. Check system resource usage (15 seconds, 1 minute, 10 minutes, 1 hour)
2. Usage by Resource Group (last week, 1 minute, 10 minutes)

# Monthly (OS, DB parameters, version, bloat, skew, daily + weekly items included)

1. Check OS kernel Parameters (Master, Standby Master, All Segments)
2. Check gpdb parameter setting value (Master, Standby Master, All Segments)
3. Check DB version and component module versions (bug fixed checks)
4. Check bloat table (catalog/user table)
5. Skew check (user table)
-----------------------------------------------------------------

# korean

-----------------------------------------------------------------

#설치 방법

gpdb_hc.tar 파일 /home/gpadmin/. 경로에 카피

tar -xvf gpdb_hc.tar

#실행 방법

sh 09_daily_db_hc_chk.sh

sh 10_weekly_db_hc_chk.sh

#리포트 결과 확인

/home/gpadmin/diag/hc_chk/daily

/home/gpadmin/diag/hc_chk/weekly


#daily 항목

1. 세그먼트 별 리소스 사용량 체크
2. 전체 테이블 리스트 (리프 파티션 테이블 제외)
3. 스키마별 사이즈
4. 각 테이블 사이즈
5. 엑세스가 빈번한 테이블 리스트
6. 에러 메세지 확인 (빈도별)
7. 파티션 테이블 리스트
8. 세그먼트 별 데이터 파일 디스크 사용량
9. 1시간 단위 디스크 사용량 추세 확인
10. 최근 일주일 동안 오랫동안 수행한 SQL 리스트
11. 통계 갱신이 필요한 테이블 리스트
12. 이중화 (mirror segment) 상태 체크

#weekly 항목 (최근 일주일, daily + weekly 항목 수행)

1. 시스템 리소스 사용량 체크 (15초,1분,10분,1시간)
2. 리소스 그룹별 사용량 (최근 일주일, 1분, 10분 단위)

#monthly

1. OS 파라미터 ( 마스터, 스탠바이 마스터,모든 세그먼트 )
2. gpdb 파라미터 설정 값 확인
3. DB 버젼 및 각종 컴포넌트 버젼 체크 ( 크리티컬 bug 확인 시 필요)
4. table bloat (catalog/사용자 테이블)확인
5. skew 체크

# Requirement

(1) gpadmin user should have privilege to use sudo command without password

(refernece url : https://docs.vmware.com/en/VMware-Greenplum/6/greenplum-database/install_guide-prep_os.html#topic23)

(2) A version of gpcc 6.x or higher must be installed.

If the gpcc is not installed or in a non-operating state, some of the report result are not generated.

------------------------------------------------------------------

(refernece url : https://docs.vmware.com/en/VMware-Greenplum/6/greenplum-database/install_guide-prep_os.html#topic23)
