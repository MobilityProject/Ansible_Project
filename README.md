Ansible을 이용한 클라우드 취약점 분석 

![시스템 구성도 drawio](https://github.com/user-attachments/assets/b7512b0e-1e45-40f3-9dae-61f93f80934b)

![상세 구성도 drawio](https://github.com/user-attachments/assets/658cabcc-9577-4bb6-9fa8-1ae2b3915b26)
< 상세 구성도 >

Master
│
├── Apache
│   ├── tasks
│   │   ├── access_control
│   │   │   └── process_directory.yml
│   │   └── security
│   │       ├── limit_upload_download.yml
│   │       └── web_service_separation.yml
│   └── main.yml
│
├── IIS
│   ├── defaults
│   │   └── main.yml
│   ├── files
│   │   └── logs
│   ├── handlers
│   │   └── main.yml
│   ├── meta
│   │   └── main.yml
│   ├── tasks
│   │   └── main.yml
│   ├── tests
│   │   ├── test.yml
│   │   └── inventory
│   └── vars
│       └── main.yml
│
├── Linux-server
│   ├── tasks
│   │   ├── Account_Management
│   │   │   ├── server_account.yml
│   │   │   ├── server_password.yml
│   │   │   ├── server_password_max.yml
│   │   │   ├── server_password_max_sol.yml
│   │   │   ├── server_password_protect.yml
│   │   │   ├── server_password_protect_sol.yml
│   │   │   ├── server_password_sol.yml
│   │   │   └── server_threshold.yml
│   │   ├── File_Directory_Management
│   │   │   ├── FileDirectory.yml
│   │   │   └── StickbitCheck.yml
│   │   ├── System_Management
│   │   │   ├── DNS.yml
│   │   │   ├── FTP.yml
│   │   │   ├── NFS.yml
│   │   │   ├── Sendmail.yml
│   │   │   ├── ServiceFinger.yml
│   │   │   └── automountd.yml
│   │   └── main.yml
│   └── vars
│       ├── file_check_list.yml
│       ├── ssh_key_deploy.yml
│       └── vulnerability_rtype_services.yml
│
├── MySQL
│   ├── tasks
│   │   ├── main.yml
│   │   ├── Account_Management_Security_Setting
│   │   │   ├── mysql_account.yml
│   │   │   ├── mysql_confpriv.yml
│   │   │   ├── mysql_confpriv_sol.yml
│   │   │   ├── mysql_passwd_escrypt.yml
│   │   │   ├── mysql_password.yml
│   │   │   ├── mysql_password_sol.yml
│   │   │   ├── mysql_priv.yml
│   │   │   ├── mysql_rootpriv.yml
│   │   │   └── mysql_rootpriv_sol.yml
│   │   └── Patch_Log_Management
│   │       ├── mysql_log.yml
│   │       ├── mysql_log_sol.yml
│   │       └── mysql_ver_check.yml
│
├── Redis
│   ├── tasks
│   │   ├── main.yml
│   │   ├── Account_Security_Setting
│   │   │   └── redis_account_security.yml
│   │   └── Patch_Log_Management
│   │       └── redis_Log.yml
│   └── vars
│
└── windows
    ├── defaults
    │   └── main.yml
    ├── handlers
    │   └── main.yml
    ├── meta
    │   └── main.yml
    ├── tasks
    │   ├── main.yml
    │   ├── Account_Management
    │   │   ├── Id_Locked_Check.yml
    │   │   └── Pwd_period_Check.yml
    │   ├── Patch_Log_Management
    │   │   ├── Remote_Registry_Check.yml
    │   │   ├── Save_Log.yml
    │   │   ├── Servicepack_Check.yml
    │   │   └── logs
    │   ├── Security_Management
    │   │   ├── Autologin_control.yml
    │   │   ├── Notlogin_Systemoff.yml
    │   │   └── Systemoff_by_Remote.yml
    │   └── Service_Management
    │       └── Anonymous_Ftp_Forbid.yml
    ├── tests
    │   └── main.yml
    └── vars
        └── main.yml
