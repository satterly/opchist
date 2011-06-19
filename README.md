HP Operations Manager Message History Script
============================================

Usage: opchist 
        [-server <server>] 
        [-minutes <mins>] [-hours <hours>] [-days <days>] [-all] 
        [-from <dd/mm/yy> [hh:mm]] [-to <dd/mm/yy> [hh:mm]] [-count <num>]
        [-id <msg_id>] [-severity critical,normal,unknown,warning,minor,all,major] 
        [-node <node>] [-application <app>] [-group <msg_g>] [-object <obj>]
        [-text <text>] [-service <svc_id>] 
        [-source <source>] [-type <msg_type>] [-key <msg_key>] 
        [-nocase] [-notrunc] [-dupl <min>[,<max>]] [-latency <num>] [-ackd-by <user>]
        [-log-only] [-unmatched] [-notif] [-misc] [-cma] [-esc] [-owned] [-read-only]
        [-ackn] [-fwdto] [-fwdfrom] [-fromovow] [-ovowserver <ovowserver>] 
        [-show [attributes,text,original,details,flags,times,latency,forwards,cma,actions,anno,tickets,some,all,none]]
        [-region <code>] [-csv [-separator <sep>]] [-opcmsg]
        [-noheader] [-nofooter] 
        [-not] [-sort [first,last,node,dupl,severity,application,group,object,text,type,service]] [-reverse]
        [-history] 
        [-debug] [-version] [-help] 

       -server  HPOM database (default: )
      -minutes  show messages from last <x> minutes 
        -hours  show messages from last <x> hours 
         -days  show messages from last <x> days 
          -all  show all available messages 
         -from  date-time (default: 2 hours) 
           -to  date-time (default: NOW) 
           -id  message id 
         -node% nodename 
     -severity  critical,normal,unknown,warning,minor,all,major (default: all) 
  -application% application name 
        -group% message group 
       -object% message object 
         -text  message text (text is automatically surrounded by % wildcards) 

      -service% service name 
       -source% message source 
         -type% message type 
          -key% message key 
       -nocase  case-insensitive searches for node,application,group,object and text (default: case-sensitive) 
      -notrunc  do not truncate message text or annotations (default: trunc) 
         -dupl  only show messages with number of duplicates >= min, and optionally <= max. 
      -latency  show messages with latency >= min 
      -ackd-by  show messages acknowledged by <user> 
     -log-only! only show log only messages 
    -unmatched! only show unmatched messages 
        -notif! only show messages forwarded to notification service 
         -misc! only show messages in miscellaneous message group 
          -cma! only show messages with cma's 
          -esc! only show messages that were escalated 
        -owned! only show messages that are owned 
    -read-only! only show messages that are read only
         -ackn  only show message acknowledged but not yet moved to history
        -fwdto  only show messages that have been forwarded to another HPOV server 
      -fwdfrom  only show messages that have been forwarded from another HPOV server 
     -fromovow  only show messages that have been forwarded from OVOW server (can be defined in $HOME/.opchist file) 
   -ovowserver  nodename of OVOW server (or define '$ovowserver = <ovowserver>', in config file) 
         -show  attributes,text,original,details,flags,times,latency,forwards,cma,actions,anno,tickets,some,all,none (default: attributes) 
       -region  override region (default: EU)
          -csv  output in comma separated variable format
    -separator  change the default separator from comma to <sep>
       -opcmsg  output in format that can be run as opcmsgs
     -noheader  turn off header 
     -nofooter  turn off footer 
          -not  negate pattern matching for message text and all fields that support percent wildcards (%)
         -sort  first,last,node,dupl,severity,application,group,object,text,type,service (default: last) 
      -reverse  reverse the sort order (default: descending) 
      -history  run query against history messages 
        -debug  debug mode 
      -version  show version information 
         -help  this help 

             !  option may be negated eg. '-nounmatched' or '-nonotif' 
             %  fields support percent wildcards eg. '-node lon%' or '-obj %SPI%' 

    Files: 
        /Users/nicholas/.opchist
    TWiki: 
        http://yourserverhere/twiki/bin/view/HPOM/Opchist

opchist,v10
