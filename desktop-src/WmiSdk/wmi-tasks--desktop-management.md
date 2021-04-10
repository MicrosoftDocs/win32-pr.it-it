---
description: Le attività WMI per gestione desktop possono esercitare il controllo e ottenere dati da un desktop remoto o da un computer locale.
ms.assetid: bb8356bf-de38-4925-a501-6ad47d23ea8f
ms.tgt_platform: multiple
title: 'Attività WMI: gestione desktop '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33f027c808a30463f2747d11020f45d1b8d40edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880653"
---
# <a name="wmi-tasks-desktop-management"></a><span data-ttu-id="ee84b-103">Attività WMI: gestione desktop </span><span class="sxs-lookup"><span data-stu-id="ee84b-103">WMI Tasks: Desktop Management</span></span>

<span data-ttu-id="ee84b-104">Le attività WMI per gestione desktop possono esercitare il controllo e ottenere dati da un desktop remoto o da un computer locale.</span><span class="sxs-lookup"><span data-stu-id="ee84b-104">WMI tasks for desktop management can exert control and obtain data from either a remote desktop or a local computer.</span></span> <span data-ttu-id="ee84b-105">Ad esempio, è possibile determinare se lo screensaver in un computer locale richiede una password.</span><span class="sxs-lookup"><span data-stu-id="ee84b-105">For example, you can determine whether the screensaver on a local computer requires a password.</span></span> <span data-ttu-id="ee84b-106">WMI offre inoltre la possibilità di arrestare un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="ee84b-106">WMI also gives you the ability shut down a remote computer.</span></span> <span data-ttu-id="ee84b-107">Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ee84b-107">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="ee84b-108">Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="ee84b-108">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="ee84b-109">Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="ee84b-109">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="ee84b-110">Nella procedura riportata di seguito viene descritto come eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="ee84b-110">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="ee84b-111">**Per eseguire uno script**</span><span class="sxs-lookup"><span data-stu-id="ee84b-111">**To run a script**</span></span>

1.  <span data-ttu-id="ee84b-112">Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="ee84b-112">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="ee84b-113">Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.</span><span class="sxs-lookup"><span data-stu-id="ee84b-113">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="ee84b-114">Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.</span><span class="sxs-lookup"><span data-stu-id="ee84b-114">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="ee84b-115">Digitare **cscript filename.vbs** al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="ee84b-115">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="ee84b-116">Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="ee84b-116">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="ee84b-117">Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="ee84b-117">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="ee84b-118">Per impostazione predefinita, cscript Visualizza l'output di uno script nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="ee84b-118">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="ee84b-119">Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="ee84b-119">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="ee84b-120">Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="ee84b-120">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="ee84b-121">Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="ee84b-121">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-122">Ricerca per categorie</span><span class="sxs-lookup"><span data-stu-id="ee84b-122">How do I...</span></span></th>
<th><span data-ttu-id="ee84b-123">Classi o metodi WMI</span><span class="sxs-lookup"><span data-stu-id="ee84b-123">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee84b-124">... determinare se un computer remoto è stato avviato in modalità provvisoria con lo stato di rete?</span><span class="sxs-lookup"><span data-stu-id="ee84b-124">...determine if a remote computer has booted up in the Safe Mode with Networking state?</span></span></td>
<td><span data-ttu-id="ee84b-125">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e controllare il valore della proprietà <strong>PrimaryOwnerName</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee84b-125">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and check the value of the <strong>PrimaryOwnerName</strong> property.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-126">VB</span><span class="sxs-lookup"><span data-stu-id="ee84b-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery (&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Registered owner: &quot; & objComputer.PrimaryOwnerName
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee84b-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSettings = Get-WmiObject -Class Win32_ComputerSystem
foreach ($objComputer in $colSettings)
{
    &quot;System Name: &quot; + $objComputer.Name
    &quot;Registered owner: &quot; + $objComputer.PrimaryOwnerName
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee84b-128">... determinare se lo screensaver del computer richiede una password.</span><span class="sxs-lookup"><span data-stu-id="ee84b-128">...determine if a computer screensaver requires a password?</span></span></td>
<td><p><span data-ttu-id="ee84b-129">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong>Win32_Desktop</strong></a> e controllare il valore della proprietà <strong>ScreenSaverSecure</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee84b-129">Use the <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong>Win32_Desktop</strong></a> class and check the value of the <strong>ScreenSaverSecure</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-130">VB</span><span class="sxs-lookup"><span data-stu-id="ee84b-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_Desktop&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Screen Saver Secure: &quot; & objItem.ScreenSaverSecure
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee84b-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$Desktops = Get-WMIObject -class Win32_Desktop -ComputerName $computer
&quot;{0} desktops found as follows&quot; -f $desktops.count
foreach ($desktop in $desktops) {
     &quot;Desktop      : {0}&quot;  -f $Desktop.Name
     &quot;Screen Saver : {0}&quot;  -f $desktop.ScreensaverExecutable
     &quot;Secure       : {0} &quot; -f $desktop.ScreenSaverSecure
     &quot;&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee84b-132">... Verificare che sia stata impostata una schermata del computer per 800 pixel di 600 pixel?</span><span class="sxs-lookup"><span data-stu-id="ee84b-132">...verify that a computer screen has been set for 800 pixels by 600 pixels?</span></span></td>
<td><p><span data-ttu-id="ee84b-133">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong>Win32_DesktopMonitor</strong></a> e verificare i valori delle proprietà <strong>ScreenHeight</strong> e <strong>ScreenWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="ee84b-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong>Win32_DesktopMonitor</strong></a> class and check the values of the properties <strong>ScreenHeight</strong> and <strong>ScreenWidth</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-134">VB</span><span class="sxs-lookup"><span data-stu-id="ee84b-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_DesktopMonitor&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Screen Height: &quot; & objItem.ScreenHeight
    Wscript.Echo &quot;Screen Width: &quot; & objItem.ScreenWidth
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee84b-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><# Get desktop information #>
$computer = &quot;.&quot;
$desktops = Get-WmiObject -Class Win32_DesktopMonitor
$hostname = hostname

<span data-ttu-id="ee84b-136">< # Visualizza i dettagli sul desktop # > &quot; sono presenti {0} desktop in {1} , come indicato di seguito: &quot; -f $desktops. Conteggio, $hostname &quot; &quot; $i = 1 # numero di desktop in questo sistema</span><span class="sxs-lookup"><span data-stu-id="ee84b-136"><# Display desktop details #> &quot;There are {0} Desktops on {1} as follows:&quot; -f $desktops.Count, $hostname &quot;&quot; $i=1 # count of desktops on this system</span></span>

<span data-ttu-id="ee84b-137">foreach ($desktop in $desktops) { &quot; Desktop {0} : {1} &quot; -f $i + +, $desktop. Caption &quot; Altezza schermo: {0} &quot; -f $desktop. &quot;Larghezza schermo ScreenHeight: {0} &quot; -f $desktop. ScreenWidth &quot; &quot; }</code></span><span class="sxs-lookup"><span data-stu-id="ee84b-137">foreach ($desktop in $desktops) { &quot;Desktop {0}: {1}&quot; -f  $i++, $Desktop.Caption &quot;Screen Height : {0}&quot; -f $desktop.ScreenHeight &quot;Screen Width  : {0}&quot; -f $desktop.ScreenWidth &quot;&quot; }</code></span></span></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee84b-138">... determinare il tempo di esecuzione di un computer</span><span class="sxs-lookup"><span data-stu-id="ee84b-138">...determine how long a computer has been running?</span></span></td>
<td><p><span data-ttu-id="ee84b-139">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e la proprietà <strong>LastBootUpTime</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee84b-139">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <strong>LastBootUpTime</strong> property.</span></span> <span data-ttu-id="ee84b-140">Sottrarre tale valore dall'ora corrente per ottenere il tempo di esecuzione del sistema.</span><span class="sxs-lookup"><span data-stu-id="ee84b-140">Subtract that value from the current time to get the system uptime.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-141">VB</span><span class="sxs-lookup"><span data-stu-id="ee84b-141">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
 
For Each objOS in colOperatingSystems
    dtmBootup = objOS.LastBootUpTime
    dtmLastBootUpTime = WMIDateStringToDate(dtmBootup)
    dtmSystemUptime = DateDiff(&quot;h&quot;, dtmLastBootUpTime, Now)
    Wscript.Echo dtmSystemUptime 
Next
 
Function WMIDateStringToDate(dtmBootup)
    WMIDateStringToDate =  CDate(Mid(dtmBootup, 5, 2) & &quot;/&quot; & _
        Mid(dtmBootup, 7, 2) & &quot;/&quot; & Left(dtmBootup, 4) & &quot; &quot; & Mid (dtmBootup, 9, 2) & &quot;:&quot; & _
        Mid(dtmBootup, 11, 2) & &quot;:&quot; & Mid(dtmBootup, 13, 2))
End Function</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee84b-142">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>function WMIDateStringToDate($Bootup) {
[System.Management.ManagementDateTimeconverter]::ToDateTime($Bootup)
}

<# Main script #>
$Computer = &quot;.&quot; # adjust as needed
$computers = Get-WMIObject -class Win32_OperatingSystem -computer $computer

foreach ($system in $computers) {
    $Bootup = $system.LastBootUpTime
    $LastBootUpTime = WMIDateStringToDate($Bootup)
    $now = Get-Date
 $Uptime = $now-$lastBootUpTime
    &quot;System Up for: {0}&quot; -f $UpTime
} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee84b-143">... riavviare o arrestare un computer remoto?</span><span class="sxs-lookup"><span data-stu-id="ee84b-143">...reboot or shut down a remote computer?</span></span></td>
<td><p><span data-ttu-id="ee84b-144">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ee84b-144">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown</strong></a> method.</span></span> <span data-ttu-id="ee84b-145">È necessario includere il privilegio <a href="privilege-constants.md">RemoteShutdown</a> durante la connessione a WMI.</span><span class="sxs-lookup"><span data-stu-id="ee84b-145">You must include the <a href="privilege-constants.md">RemoteShutdown</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="ee84b-146">Per ulteriori informazioni, vedere <a href="executing-privileged-operations-using-vbscript.md">esecuzione di operazioni con privilegi tramite VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="ee84b-146">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span> <span data-ttu-id="ee84b-147">A differenza del metodo <a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>Shutdown</strong></a> su <strong>Win32_OperatingSystem</strong>, il metodo <strong>Win32Shutdown</strong> consente di impostare i flag per controllare il comportamento di arresto.</span><span class="sxs-lookup"><span data-stu-id="ee84b-147">Unlike the <a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>Shutdown</strong></a> method on <strong>Win32_OperatingSystem</strong>, the <strong>Win32Shutdown</strong> method allows you to set flags to control the shutdown behavior.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-148">VB</span><span class="sxs-lookup"><span data-stu-id="ee84b-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Shutdown)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    ObjOperatingSystem.Shutdown(1)
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee84b-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
$colOperatingSystem = Get-WmiObject -Class Win32_OperatingSystem -ComputerName $strComputer -Namespace &quot;wmi\cimv2&quot;
foreach ($objOperatingSystem in $colOperatingSystem)
{
    [void]$objOperatingSystem.Shutdown()
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee84b-150">... determinare quali applicazioni vengono eseguite automaticamente ogni volta che si avvia Windows?</span><span class="sxs-lookup"><span data-stu-id="ee84b-150">...determine what applications automatically run each time I start Windows?</span></span></td>
<td><p><span data-ttu-id="ee84b-151">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong>Win32_StartupCommand</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ee84b-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong>Win32_StartupCommand</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-152">VB</span><span class="sxs-lookup"><span data-stu-id="ee84b-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colStartupCommands = objWMIService.ExecQuery _
    (&quot;Select * from Win32_StartupCommand&quot;)
For Each objStartupCommand in colStartupCommands
    Wscript.Echo &quot;Command: &quot; & objStartupCommand.Command & VBNewLine _
    & &quot;Description: &quot; & objStartupCommand.Description & VBNewLine _
    & &quot;Location: &quot; & objStartupCommand.Location & VBNewLine _
    & &quot;Name: &quot; & objStartupCommand.Name & VBNewLine _
    & &quot;SettingID: &quot; & objStartupCommand.SettingID & VBNewLine _
    & &quot;User: &quot; & objStartupCommand.User
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee84b-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee84b-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_StartupCommand -ComputerName $strComputer
foreach ($objStartupCommand in $colItems) 
{ 
    &quot;Command: &quot; + $objStartupCommand.Command
    &quot;Description: &quot; + $objStartupCommand.Description 
    &quot;Location: &quot; + $objStartupCommand.Location 
    &quot;Name: &quot; + $objStartupCommand.Name 
    &quot;SettingID: &quot; + $objStartupCommand.SettingID 
    &quot;User: &quot; + $objStartupCommand.User
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ee84b-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee84b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee84b-155">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="ee84b-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="ee84b-156">Esempi di applicazioni WMI C++</span><span class="sxs-lookup"><span data-stu-id="ee84b-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="ee84b-157">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="ee84b-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

