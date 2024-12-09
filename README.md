# Initial Access-Stage2 execution

## Malicious Document - Stage 2
Based on the initial findings, we discovered that there is a stage 2 execution:

    The document has successfully executed an encoded base64 command.
    Decoding this string reveals the exact command chain executed by the malicious document.

## Investigation Guide
With the following discoveries, we may refer again to the cheatsheet to continue with the investigation:

    The Autostart execution reflects explorer.exe as its parent process ID.
    Child processes of explorer.exe within the event timeframe could be significant.
    Process Creation (Event ID 1) and File Creation (Event ID 11) succeeding the document execution are worth checking.

Significant Data Sources:

    Sysmon
