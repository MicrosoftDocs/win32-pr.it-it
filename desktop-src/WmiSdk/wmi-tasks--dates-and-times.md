---
description: Esistono diverse classi WMI e un oggetto di scripting per analizzare o convertire il formato datetime CIM. Per altri esempi, vedere TechNet ScriptCenter all'indirizzo https://www.microsoft.com/technet .
ms.assetid: dd01a732-5c88-4c24-a551-4d5452e712cc
ms.tgt_platform: multiple
title: 'Attività WMI: date e ore'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 46e8c850ffd04fe4ac5bc9af1b130632338b61ec79c92d154f5769ffd54cb2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739447"
---
# <a name="wmi-tasks-dates-and-times"></a>Attività WMI: date e ore

Esistono diverse classi WMI e un oggetto di scripting per analizzare o convertire il [formato datetime CIM.](date-and-time-format.md) Per altri esempi, vedere TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale. Per altre informazioni su come usare lo script per ottenere dati da computer remoti, vedere [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

## <a name="to-run-a-script"></a>Per eseguire uno script

La procedura seguente descrive come eseguire uno script.

1.  Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*. Assicurarsi che l'editor di testo non aggiunge un'.txt al file.
2.  Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.
3.  Digitare **cscript filename.vbs** al prompt dei comandi.
4.  Se non è possibile accedere a un registro eventi, verificare se si è in esecuzione da un prompt dei comandi con privilegi elevati. Alcuni registri eventi, ad esempio il registro eventi di sicurezza, possono essere protetti dai controlli di accesso utente.

> [!Note]  
> Per impostazione predefinita, cscript visualizza l'output di uno script nella finestra del prompt dei comandi. Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file. Digitare **cscript filename.vbs > outfile.txt** prompt dei comandi per reindirizzare l'output dello *script* filename.vbsa *outfile.txt*.

 

Nella tabella seguente sono elencati esempi di script che possono essere usati per ottenere vari tipi di dati dal computer locale.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ricerca per categorie</th>
<th>Classi o metodi WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... convertire le date WMI in date e ore standard?<br/></td>
<td>Usare <a href="swbemdatetime.md"><strong>l'oggetto SWbemDateTime</strong></a> per convertirli in date e ore regolari.<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Set dtmInstallDate = CreateObject(&quot;WbemScripting.SWbemDateTime&quot;)
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objOS = objWMIService.ExecQuery(&quot;Select * from Win32_OperatingSystem&quot;)
For Each strOS in objOS
    dtmInstallDate.Value = strOS.InstallDate
    Wscript.Echo dtmInstallDate.GetVarDate
Next</code></pre></td>
</tr>
</tbody>
</table>

<p>In caso di codice, eseguire l'attività manualmente.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Function WMIDateStringToDate(dtmInstallDate) 
    WMIDateStringToDate = CDate(Mid(dtmInstallDate, 5, 2) & &quot;/&quot; & Mid(dtmInstallDate, 7, 2) _
                        & &quot;/&quot; & Left(dtmInstallDate, 4) & &quot; &quot; & Mid (dtmInstallDate, 9, 2) & &quot;:&quot; _
                        & Mid(dtmInstallDate, 11, 2) & &quot;:&quot; & Mid(dtmInstallDate,13, 2)) 
End Function </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p>... determinare l'ora attualmente configurata in un computer?</p></td>
<td><p>Usare la <a href="/previous-versions/windows/desktop/wmitimepprov/win32-localtime"><strong>Win32_LocalTime</strong></a> classe .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_LocalTime&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Day:           &quot; & objItem.Day & VBNewLine _
               & &quot;Day Of Week:   &quot; & objItem.DayOfWeek & VBNewLine _
               & &quot;Hour:          &quot; & objItem.Hour & VBNewLine _
               & &quot;Minute:        &quot; & objItem.Minute & VBNewLine _
               & &quot;Month:         &quot; & objItem.Month & VBNewLine _
               & &quot;Quarter:       &quot; & objItem.Quarter & VBNewLine _
               & &quot;Second:        &quot; & objItem.Second & VBNewLine _
               & &quot;Week In Month: &quot; & objItem.WeekInMonth & VBNewLine _
               & &quot;Year:          &quot; & objItem.Year 
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Specify computer and get Local Time
$Computer = &quot;.&quot;
$times = Get-WmiObject Win32_LocalTime -computer $computer

<# Now display the result #>

Foreach ($time in $times) {
    &quot;Day : {0}&quot; -f $Time.Day
    &quot;Day Of Week : {0}&quot; -f $Time.DayOfWeek
    &quot;Hour : {0}&quot; -f $Time.Hour
    &quot;Minute : {0}&quot; -f $Time.Minute
    &quot;Month : {0}&quot; -f $Time.Month
    &quot;Quarter : {0}&quot; -f $Time.Quarter
    &quot;Second : {0}&quot; -f $time.Second 
    &quot;Week In Month: {0}&quot; -f $Time.WeekInMonth 
    &quot;Year : {0}&quot; -f $Time.Year 
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><p>... determinare il nome del fuso orario in cui è in esecuzione un computer?</p></td>
<td><p>Usare la <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> classe e controllare il valore della <strong>proprietà Description.</strong></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_TimeZone&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Description:   &quot; & objItem.Description
    Wscript.Echo &quot;Daylight Name: &quot; & objItem.DaylightName
    Wscript.Echo &quot;Standard Name: &quot; & objItem.StandardName
    Wscript.Echo
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;  
$timezone = Get-WMIObject -class Win32_TimeZone -ComputerName $computer  
  
<# Display details  #>
if ($computer -eq &quot;.&quot;) {$computer = Hostname}  
&quot;Time zone information on computer `&quot;{0}`&quot;&quot; -f $computer  
&quot;Time Zone Description   : {0}&quot; -f $timezone.Description  
&quot;Daylight Name           : {0}&quot; -f $timezone.DaylightName  
&quot;Standard Name           : {0}&quot; -f $timezone.StandardName  </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p>... assicurarsi che &quot; il 02/10/2000 venga interpretato come 2 ottobre &quot; 2000, non &quot; 10 febbraio 2000? &quot;</p></td>
<td><p>Gestire le <a href="gloss-c.md"><em></em></a> date in formato <a href="datetime.md">CIM DATETIME</a> e usare i metodi <a href="swbemdatetime.md"><strong>SWbemDateTime,</strong></a> ad esempio <a href="swbemdatetime-getvardate.md"><strong>GetVarDate,</strong></a> per convertirle in formati <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a> <strong>o VT_Date.</strong> Poiché il formato DATETIME è indipendente dalle impostazioni locali, è possibile scrivere uno script che viene eseguito in qualsiasi computer. Usare <strong>l'oggetto SWbemDateTime</strong> per convertirli in date e ore regolari. Per <a href="date-and-time-format.md">altre informazioni sulla conversione</a> di date e ore, vedere Formato di data e ora.</p></td>
</tr>
<tr class="odd">
<td><p>... convertire un valore datetime WMI in un valore DateTime .NET?</p></td>
<td><p>Analizzare manualmente la stringa e quindi inserire i valori recuperati in un <a href="/dotnet/api/system.datetime">oggetto DateTime.</a></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>function WMIDateStringToDateTime( [String] $strWmiDate ) 
{ 
    $strWmiDate.Trim() > $null 
    $iYear   = [Int32]::Parse($strWmiDate.SubString( 0, 4)) 
    $iMonth  = [Int32]::Parse($strWmiDate.SubString( 4, 2)) 
    $iDay    = [Int32]::Parse($strWmiDate.SubString( 6, 2)) 
    $iHour   = [Int32]::Parse($strWmiDate.SubString( 8, 2)) 
    $iMinute = [Int32]::Parse($strWmiDate.SubString(10, 2)) 
    $iSecond = [Int32]::Parse($strWmiDate.SubString(12, 2)) 
<# decimal point is at $strWmiDate.Substring(14, 1) #> 
    $iMicroseconds = [Int32]::Parse($strWmiDate.Substring(15, 6)) 
    $iMilliseconds = $iMicroseconds / 1000 
    $iUtcOffsetMinutes = [Int32]::Parse($strWmiDate.Substring(21, 4)) 
    if ( $iUtcOffsetMinutes -ne 0 ) 
    { 
        $dtkind = [DateTimeKind]::Local 
    } 
    else 
    { 
        $dtkind = [DateTimeKind]::Utc 
    } 
    return New-Object -TypeName DateTime ` 
                      -ArgumentList $iYear, $iMonth, $iDay, ` 
                                    $iHour, $iMinute, $iSecond, ` 
                                    $iMilliseconds, $dtkind 
} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Esempi di applicazioni C++ WMI](wmi-c---application-examples.md)
</dt> <dt>

[Formato di data e ora](date-and-time-format.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
