# dyalog_linux_odbc

Steps on how to connect to sql with ODBC from Dyalog. (using arch linux)

Example files have been provided.

Make sure to have correct ODBC driver installed for your sql.

## dyalog.dcfg
default path : $HOME/.dyalog/
Assign property ODBCINI: "<path-to>/odbc.ini"

## odbc.ini
default path : /etc/odbc.ini
Create sql connections here. Settings are dependent on flavor of sql.

## odbcinst.ini
default path : /etc/odbcinst.ini
Declare drivers here.

## dyalog session
)load sqapl
SQA.Init ''
SQA.Connect 'C1' 'DSNName' 'passwd' 'username'
SQA.Tables 'C1'
