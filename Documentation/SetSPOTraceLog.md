#Set-SPOTraceLog
*Topic automatically generated on: 2015-08-27*

Defines if tracing should be turned on. PnP Core, which is the foundation of these cmdlets utilizes the standard Trace functionality of .NET. With this cmdlet you can turn capturing of this trace to a log file on or off.
##Syntax
```powershell
Set-SPOTraceLog -Off [<SwitchParameter>]
```


```powershell
Set-SPOTraceLog -On [<SwitchParameter>] [-LogFile <String>] [-Level <LogLevel>] [-Delimiter <String>] [-IndentSize <Int32>] [-AutoFlush <Boolean>]
```


##Parameters
Parameter|Type|Required|Description
---------|----|--------|-----------
|AutoFlush|Boolean|False|Auto flush the trace log. Defaults to true.|
|Delimiter|String|False|If specified the trace log entries will be delimited with this value.|
|IndentSize|Int32|False|Indents in the tracelog will be with this amount of characters. Defaults to 4.|
|Level|LogLevel|False|The level of events to capture. Possible values are 'Debug', 'Error', 'Warning', 'Information'. Defaults to 'Information'.|
|LogFile|String|False|The path and filename of the file to write the trace log to.|
|Off|SwitchParameter|True|Turn off tracing to log file.|
|On|SwitchParameter|True|Turn on tracing to log file|
##Examples

###Example 1
    PS:> Set-SPOTraceLog -On -LogFile traceoutput.txt
This turns on trace logging to the file 'traceoutput.txt' and will capture events of at least 'Information' level.

###Example 2
    PS:> Set-SPOTraceLog -On -LogFile traceoutput.txt -Level Debug
This turns on trace logging to the file 'traceoutput.txt' and will capture debug events.

###Example 3
    PS:> Set-SPOTraceLog -On -LogFile traceoutput.txt -Level Debug -Delimiter ","
This turns on trace logging to the file 'traceoutput.txt' and will write the entries as comma separated. Debug events are captured.

###Example 4
    PS:> Set-SPOTraceLog -Off
This turns off trace logging. It will flush any remaining messages to the log file.
<!-- Ref: FF10B9D26546C73A2B0417DD65D80203 -->