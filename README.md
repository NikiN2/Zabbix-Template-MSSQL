# Zabbix-Template-MSSQL

Microsoft SQL Server 2012 monitoring. For English and Russian version. With LLD. �hecked in 2.4.8 and 3.0.0
Based on Anton Golubkin's "Template MS SQL 2012" at 
https://share.zabbix.com/databases/microsoft-sql-server/template-ms-sql-2012


# Changelog
* ��������� ����������� ��������� ������ ��� ������, ������� ���� ���������� ��� LLD, �������� $DB_to_skip � SQLBaseName_To_Zabbix.ps1 
* �������� {HOST.NAME} � ����� ��������� (����� �������� ���������, �������, � ������ �� �������� ��� ���������)
* �������� ����������� ����� �� ������� "Top 10 SQL Server Counters for Monitoring SQL Server Performance" (http://www.databasejournal.com/features/mssql/article.php/3932406/Top-10-SQL-Server-Counters-for-Monitoring-SQL-Server-Performance.htm)
* ������ ��� �������� MSSQL.
* ������� "Access Methods Page Splits / Sec" 
    {MS SQL 2012:perf_counter["\SQLServer:Access Methods\Page Splits/sec",30].last()}>
    {MS SQL 2012:perf_counter["\SQLServer:SQL Statistics\Batch Requests/sec",30].last()}/20
��������� � ���� ����������, Anton Golubkin �������������� �� ����� "Ideally this counter should be less than 20% of the batch requests per second." �� ����������, ��� ������� �����������, ����� PageSplits > 5% Batch Requests. ��� ��������� ������� ���� :) ������� �� 20% (�.�. "/5")
# ��� ������� ������ ��� Express �������� (��� ��� ������, ����� � ������� ����������� ��������� ����������� MSSQL)
  1. �������� ������ �� ������� ������ � Zabbix
  2. ������������� ��� ������������ ������ (��������, ������� " Express" � ��������)
  3. ������������� ������ ��� ��������� ������ "���� Express" � ������� ���
  4. ������� ���������������� .xls � ��������� ��������� � �������� ��� ��������� "SQLServer:" �� "MSSQL$SQLEXPRESS:". ���� �������� ������ ��� ���������� MSSQL � ������������ ������ - ������� ��� ���. ���������� ��� ����� ��� ���������� ��������� � perfmon.exe
  5. ��������� � ������������� ��������� ������. ��� ������� ����� ������� �� ������� "�������� ������������"


# English
* LLD : now you can skip some databases from LLD, check $DB_to_skip in SQLBaseName_To_Zabbix.ps1 
* Add "{HOST.NAME}" to trigger name
* Screen with "Top 10 SQL Server Counters for Monitoring SQL Server Performance" (http://www.databasejournal.com/features/mssql/article.php/3932406/Top-10-SQL-Server-Counters-for-Monitoring-SQL-Server-Performance.htm)
* Template for Russian MSSQL server
* Howto add Express server



