---
description: Per ottenere dati da WMI, sia nel computer locale che in un computer remoto, è necessario connettersi al servizio WMI connettendosi a uno spazio dei nomi specifico.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: 'Attività WMI: connessione al servizio WMI'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 751c6c0802c30e113f4a2b7ddc646cdf5646b7dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310328"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a><span data-ttu-id="f49ab-103">Attività WMI: connessione al servizio WMI</span><span class="sxs-lookup"><span data-stu-id="f49ab-103">WMI Tasks: Connecting to the WMI Service</span></span>

<span data-ttu-id="f49ab-104">Per ottenere dati da WMI, sia nel computer locale che in un computer remoto, è necessario connettersi al servizio WMI connettendosi a uno [*spazio dei nomi*](gloss-n.md)specifico.</span><span class="sxs-lookup"><span data-stu-id="f49ab-104">To get data from WMI, either on the local computer or from a remote computer, you must connect to the WMI service by connecting to a specific [*namespace*](gloss-n.md).</span></span> <span data-ttu-id="f49ab-105">Nella maggior parte dei casi, usare la connessione del [moniker](creating-a-wmi-script.md) abbreviato o la connessione del [**localizzatore**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="f49ab-105">In most cases, use either the shorthand [moniker](creating-a-wmi-script.md) connection or the [**Locator**](swbemlocator-connectserver.md) connection.</span></span> <span data-ttu-id="f49ab-106">Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f49ab-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="f49ab-107">Per le connessioni remote sono necessarie le impostazioni appropriate per il Windows Firewall e DCOM.</span><span class="sxs-lookup"><span data-stu-id="f49ab-107">Remote connections require proper settings for the Windows Firewall and DCOM.</span></span> <span data-ttu-id="f49ab-108">Per ulteriori informazioni, vedere [la pagina relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md) e alla [connessione tramite Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="f49ab-108">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span> <span data-ttu-id="f49ab-109">A partire da Windows Vista, il controllo dell'account utente (UAC) può influire sull'accesso WMI.</span><span class="sxs-lookup"><span data-stu-id="f49ab-109">Starting with Windows Vista, User Account Control (UAC) can affect WMI access.</span></span> <span data-ttu-id="f49ab-110">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f49ab-110">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="f49ab-111">Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="f49ab-111">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="f49ab-112">Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="f49ab-112">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="f49ab-113">Nella procedura riportata di seguito viene descritto come eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="f49ab-113">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="f49ab-114">**Per eseguire uno script**</span><span class="sxs-lookup"><span data-stu-id="f49ab-114">**To run a script**</span></span>

1.  <span data-ttu-id="f49ab-115">Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="f49ab-115">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="f49ab-116">Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.</span><span class="sxs-lookup"><span data-stu-id="f49ab-116">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="f49ab-117">Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.</span><span class="sxs-lookup"><span data-stu-id="f49ab-117">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="f49ab-118">Digitare **cscript filename.vbs** al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="f49ab-118">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="f49ab-119">Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="f49ab-119">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="f49ab-120">Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="f49ab-120">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="f49ab-121">Per impostazione predefinita, cscript Visualizza l'output di uno script nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="f49ab-121">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="f49ab-122">Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="f49ab-122">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="f49ab-123">Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="f49ab-123">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="f49ab-124">Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="f49ab-124">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f49ab-125">Ricerca per categorie</span><span class="sxs-lookup"><span data-stu-id="f49ab-125">How do I...</span></span></th>
<th><span data-ttu-id="f49ab-126">Classi o metodi WMI</span><span class="sxs-lookup"><span data-stu-id="f49ab-126">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f49ab-127">... connettersi a un computer remoto tramite WMI?</span><span class="sxs-lookup"><span data-stu-id="f49ab-127">...connect to a remote computer using WMI?</span></span></td>
<td><span data-ttu-id="f49ab-128">Specificare una delle opzioni seguenti come parte della stringa di connessione del <a href="constructing-a-moniker-string.md">moniker</a> :</span><span class="sxs-lookup"><span data-stu-id="f49ab-128">Specify one of the following as part of your <a href="constructing-a-moniker-string.md">moniker</a> connection string:</span></span><br/>
<ul>
<li><span data-ttu-id="f49ab-129">Nome del computer NetBIOS, ad esempio &quot; ATL-DC-01&quot;</span><span class="sxs-lookup"><span data-stu-id="f49ab-129">A NetBIOS computer name, such as &quot;atl-dc-01&quot;</span></span></li>
<li><span data-ttu-id="f49ab-130">Un nome di dominio completo, ad esempio &quot; ATL-DC-01.fabrikam.com&quot;</span><span class="sxs-lookup"><span data-stu-id="f49ab-130">A fully qualified domain name, such as &quot;atl-dc-01.fabrikam.com&quot;</span></span></li>
<li><span data-ttu-id="f49ab-131">Un indirizzo IPv4, ad esempio &quot; 192.168.1.1&quot;</span><span class="sxs-lookup"><span data-stu-id="f49ab-131">An IPv4 address, such as &quot;192.168.1.1&quot;</span></span></li>
<li><span data-ttu-id="f49ab-132">A partire da Windows Vista, è possibile specificare un indirizzo IPv6 se il computer di destinazione e il computer da cui si sta effettuando la connessione eseguono entrambi IPv6.</span><span class="sxs-lookup"><span data-stu-id="f49ab-132">Starting with Windows Vista, you can specify an IPv6 address if the target computer and the computer from which you are making the connection both run IPv6.</span></span><br/></li>
</ul>
<span data-ttu-id="f49ab-133">Per ulteriori informazioni, vedere <a href="connecting-to-wmi-on-a-remote-computer.md">connessione a WMI in un computer remoto</a> e <a href="ipv6-and-ipv4-support-in-wmi.md">supporto per IPv6 e IPv4 in WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="f49ab-133">For more information, see <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a> and <a href="ipv6-and-ipv4-support-in-wmi.md">IPv6 and IPv4 Support in WMI</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f49ab-134">VB</span><span class="sxs-lookup"><span data-stu-id="f49ab-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<th><span data-ttu-id="f49ab-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f49ab-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f49ab-136">... eseguire uno script WMI con credenziali alternative?</span><span class="sxs-lookup"><span data-stu-id="f49ab-136">...run a WMI script under alternate credentials?</span></span></td>
<td><p><span data-ttu-id="f49ab-137">Usare il metodo <a href="swbemlocator-connectserver.md"><strong>SWbemLocator. ConnectServer</strong></a> o <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator:: ConnectServer</strong></a> in C++ e includere il nome utente e la password appropriati.</span><span class="sxs-lookup"><span data-stu-id="f49ab-137">Use the <a href="swbemlocator-connectserver.md"><strong>SWbemLocator.ConnectServer</strong></a> method, or <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator::ConnectServer</strong></a> in C++, and include the appropriate user name and password.</span></span> <span data-ttu-id="f49ab-138">Non è possibile modificare le credenziali durante la connessione al computer locale.</span><span class="sxs-lookup"><span data-stu-id="f49ab-138">You cannot change credentials when connecting to the local computer.</span></span> <span data-ttu-id="f49ab-139">Per ulteriori informazioni, vedere <a href="creating-a-wmi-script.md">creazione di uno script WMI</a> e <a href="connecting-to-wmi-on-a-remote-computer.md">connessione a WMI in un computer remoto</a>.</span><span class="sxs-lookup"><span data-stu-id="f49ab-139">For more information, see <a href="creating-a-wmi-script.md">Creating a WMI Script</a> and <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f49ab-140">VB</span><span class="sxs-lookup"><span data-stu-id="f49ab-140">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<th><span data-ttu-id="f49ab-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f49ab-141">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f49ab-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f49ab-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f49ab-143">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="f49ab-143">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="f49ab-144">Esempi di applicazioni WMI C++</span><span class="sxs-lookup"><span data-stu-id="f49ab-144">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="f49ab-145">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="f49ab-145">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
