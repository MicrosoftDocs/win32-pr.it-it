---
description: Viene descritto in che modo gli script, le applicazioni e i provider possono stabilire connessioni a WMI in computer remoti per ottenere dati o controllare hardware e software.
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: Connessione a WMI in un computer remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d581d1be73013e57ef2193102f6e8afc287b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315236"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a><span data-ttu-id="148fd-103">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="148fd-103">Connecting to WMI on a Remote Computer</span></span>

<span data-ttu-id="148fd-104">WMI può essere utilizzato per gestire e accedere ai dati WMI nei computer remoti.</span><span class="sxs-lookup"><span data-stu-id="148fd-104">WMI can be used to manage and access WMI data on remote computers.</span></span> <span data-ttu-id="148fd-105">Le connessioni remote in WMI sono interessate dalle impostazioni [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) e DCOM.</span><span class="sxs-lookup"><span data-stu-id="148fd-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) and DCOM settings.</span></span> <span data-ttu-id="148fd-106">Il [controllo dell'account utente (UAC)](/previous-versions/aa905108(v=msdn.10)) può richiedere anche modifiche ad alcune impostazioni.</span><span class="sxs-lookup"><span data-stu-id="148fd-106">[User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)) may also require changes to some settings.</span></span> <span data-ttu-id="148fd-107">Tuttavia, una volta corrette le impostazioni, la chiamata a un sistema remoto è molto simile a una chiamata WMI locale.</span><span class="sxs-lookup"><span data-stu-id="148fd-107">However, once your have your settings correct, the call to a remote system is very similar to a local WMI call.</span></span> <span data-ttu-id="148fd-108">È possibile scegliere di renderlo più complesso, tuttavia, usando credenziali diverse, protocolli di autenticazione alternativi e altre funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="148fd-108">You may choose to make it more complex however, by using different credentials, alternate authentication protocols, and other security features.</span></span>

## <a name="configuring-a-computer-for-a-remote-connection"></a><span data-ttu-id="148fd-109">Configurazione di un computer per una connessione remota</span><span class="sxs-lookup"><span data-stu-id="148fd-109">Configuring a Computer for a Remote Connection</span></span>

<span data-ttu-id="148fd-110">Prima di poter accedere a un sistema remoto con WMI, potrebbe essere necessario controllare alcune impostazioni di sicurezza per confermare di avere accesso.</span><span class="sxs-lookup"><span data-stu-id="148fd-110">Before you can access a remote system with WMI, you may need to check some security settings to confirm that you have access.</span></span> <span data-ttu-id="148fd-111">In particolare:</span><span class="sxs-lookup"><span data-stu-id="148fd-111">Specifically:</span></span>

-   <span data-ttu-id="148fd-112">Windows contiene una serie di funzionalità di sicurezza che possono bloccare l'accesso agli script nei sistemi remoti.</span><span class="sxs-lookup"><span data-stu-id="148fd-112">Windows contains a number of security features that may block access to scripts on remote systems.</span></span> <span data-ttu-id="148fd-113">Di conseguenza, potrebbe essere necessario modificare le impostazioni di Active Directory e Windows Firewall del sistema prima di effettuare una chiamata WMI.</span><span class="sxs-lookup"><span data-stu-id="148fd-113">As such, you may need to modify your system's Active Directory and Windows Firewall settings before making a WMI call.</span></span> <span data-ttu-id="148fd-114">Per ulteriori informazioni, vedere [configurazione di una connessione WMI remota](connecting-to-wmi-remotely-starting-with-vista.md) e [risoluzione dei problemi di una connessione WMI remota](troubleshooting-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="148fd-114">For more information, see [Setting up a Remote WMI Connection](connecting-to-wmi-remotely-starting-with-vista.md) and [Troubleshooting a Remote WMI Connection](troubleshooting-a-remote-wmi-connection.md).</span></span>

-   <span data-ttu-id="148fd-115">Per il funzionamento di una connessione remota, è necessario abilitare le impostazioni DCOM corrette.</span><span class="sxs-lookup"><span data-stu-id="148fd-115">The correct DCOM settings must be enabled for a remote connection to work.</span></span> <span data-ttu-id="148fd-116">La modifica delle impostazioni DCOM può consentire a utenti con diritti limitati di accedere a un computer per una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="148fd-116">Changing DCOM settings can allow low rights users access to a computer for a remote connection.</span></span> <span data-ttu-id="148fd-117">Per ulteriori informazioni, vedere [protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="148fd-117">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="148fd-118">Inoltre, in alcuni casi potrebbe essere necessario eseguire WMI tramite una porta fissa.</span><span class="sxs-lookup"><span data-stu-id="148fd-118">In addition, there may be some circumstances in which you may wish to run WMI though a fixed port.</span></span> <span data-ttu-id="148fd-119">A tale scopo, sarà necessario modificare anche le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="148fd-119">To do this, you will also need to change your settings.</span></span> <span data-ttu-id="148fd-120">Per ulteriori informazioni, vedere [configurazione di una porta fissa per WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="148fd-120">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

## <a name="connecting-to-a-remote-computer"></a><span data-ttu-id="148fd-121">Connessione a un computer remoto</span><span class="sxs-lookup"><span data-stu-id="148fd-121">Connecting to a Remote Computer</span></span>

<span data-ttu-id="148fd-122">Al suo cuore, la connessione a un sistema remoto con WMI consiste nel garantire che siano disponibili le autorizzazioni appropriate per accedere al sistema e che la connessione sia configurata correttamente.</span><span class="sxs-lookup"><span data-stu-id="148fd-122">At its heart, connecting to a remote system with WMI consists of making sure that you have the appropriate permissions to access the system, and that your connection is properly configured.</span></span> <span data-ttu-id="148fd-123">Una volta che si dispone di questi due elementi, la connessione stessa è relativamente semplice.</span><span class="sxs-lookup"><span data-stu-id="148fd-123">Once you have those two elements, the connection itself is relatively simple.</span></span> <span data-ttu-id="148fd-124">Se ad esempio si usano le credenziali di sicurezza predefinite, è possibile accedere a WMI in un sistema remoto usando il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="148fd-124">For example, if you are using your default security credentials, you can access WMI on a remote system using the following code:</span></span>

<dl> <dt>

<span data-ttu-id="148fd-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Connessione a WMI in modalità remota con PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="148fd-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span></span>
</dt> <dd>

<span data-ttu-id="148fd-126">Usare il parametro *-ComputerName* comune alla maggior parte dei cmdlet WMI, ad esempio [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="148fd-126">Use the *-ComputerName* parameter common to most WMI cmdlets, such as [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span></span>


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span data-ttu-id="148fd-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Connessione a WMI in modalità remota con VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span><span class="sxs-lookup"><span data-stu-id="148fd-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span></span>
</dt> <dd>

<span data-ttu-id="148fd-128">Usare un moniker contenente il nome del sistema remoto nella chiamata a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="148fd-128">Use a moniker that contains the name of the remote system in the call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span data-ttu-id="148fd-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connessione a WMI in modalità remota con C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="148fd-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="148fd-130">Per la versione corrente dell'interfaccia gestita WMI ([Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), utilizzare l'oggetto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) per rappresentare una connessione a un host remoto.</span><span class="sxs-lookup"><span data-stu-id="148fd-130">For the current version of the WMI managed interface ([Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), use the [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object to represent a connection to a remote host.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span data-ttu-id="148fd-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connessione a WMI in modalità remota con C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="148fd-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="148fd-132">Per la versione V1 dell'interfaccia gestita WMI ([System. Management](/dotnet/api/system.management)), utilizzare l'oggetto [ManagementScope](/dotnet/api/system.management.managementscope) per rappresentare una connessione a un host remoto.</span><span class="sxs-lookup"><span data-stu-id="148fd-132">For the v1 version of the WMI managed interface ([System.Management](/dotnet/api/system.management)), use the [ManagementScope](/dotnet/api/system.management.managementscope) object to represent a connection to a remote host.</span></span>


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span data-ttu-id="148fd-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Esempio: recupero di dati WMI da un computer remoto (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span><span class="sxs-lookup"><span data-stu-id="148fd-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Example: Getting WMI Data from a Remote Computer (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span></span>
</dt> <dd>

<span data-ttu-id="148fd-134">Usare il metodo [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) per specificare il nome del computer remoto nel parametro *strNetworkResource* .</span><span class="sxs-lookup"><span data-stu-id="148fd-134">Use the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method to specify the name of the remote computer in the *strNetworkResource* parameter.</span></span>


```CSharp
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTER_B\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
```



</dd> </dl>

<span data-ttu-id="148fd-135">Gli esempi di codice precedenti rappresentano probabilmente la connessione remota più semplice che è possibile eseguire con WMI.</span><span class="sxs-lookup"><span data-stu-id="148fd-135">The previous code samples are arguably the most basic remote connection you can perform with WMI.</span></span> <span data-ttu-id="148fd-136">In particolare, gli esempi presuppongono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="148fd-136">Specifically, the samples assume the following:</span></span>

-   <span data-ttu-id="148fd-137">Si è un amministratore del computer remoto.</span><span class="sxs-lookup"><span data-stu-id="148fd-137">You are an administrator on the remote machine.</span></span> <span data-ttu-id="148fd-138">A causa del [controllo dell'account utente](/previous-versions/aa905108(v=msdn.10)), l'account nel sistema remoto deve essere un account di dominio nel gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="148fd-138">Due to [User Account Control](/previous-versions/aa905108(v=msdn.10)), the account on the remote system must be a domain account in the Administrators group.</span></span> <span data-ttu-id="148fd-139">Per ulteriori informazioni, vedere controllo dell'account utente e WMI.</span><span class="sxs-lookup"><span data-stu-id="148fd-139">For more information, see User Account Control and WMI.</span></span>
-   <span data-ttu-id="148fd-140">La password nel computer locale corrente non è vuota.</span><span class="sxs-lookup"><span data-stu-id="148fd-140">The password on your current local machine is not blank.</span></span> <span data-ttu-id="148fd-141">Si tratta essenzialmente di un requisito di sicurezza di Windows che è necessario avere eseguito l'accesso al sistema con una password.</span><span class="sxs-lookup"><span data-stu-id="148fd-141">This is essentially a Windows security requirement that you must have logged onto your system with a password.</span></span>
-   <span data-ttu-id="148fd-142">Sia il computer locale che quello remoto si trovano nello stesso dominio.</span><span class="sxs-lookup"><span data-stu-id="148fd-142">Both your local and remote computers are within the same domain.</span></span> <span data-ttu-id="148fd-143">Se è necessario superare i limiti di dominio, è necessario fornire informazioni aggiuntive o utilizzare un modello di programmazione leggermente diverso.</span><span class="sxs-lookup"><span data-stu-id="148fd-143">If you need to cross domain boundaries, you would need to supply additional information or use a slightly different programming model.</span></span>
-   <span data-ttu-id="148fd-144">Si usa il proprio account per accedere al computer remoto.</span><span class="sxs-lookup"><span data-stu-id="148fd-144">You are using your own account to access the remote machine.</span></span> <span data-ttu-id="148fd-145">Se si sta tentando di accedere a un account diverso, è necessario fornire credenziali aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="148fd-145">If you were trying to access a different account, you would need to supply additional credentials.</span></span> <span data-ttu-id="148fd-146">Si noti che il tentativo di accedere a WMI localmente con credenziali diverse dall'account corrente non è consentito.</span><span class="sxs-lookup"><span data-stu-id="148fd-146">(Note that trying to access WMI locally with credentials different than your current account is not permitted.)</span></span>
-   <span data-ttu-id="148fd-147">Entrambi i computer eseguono IPv6.</span><span class="sxs-lookup"><span data-stu-id="148fd-147">Both computers are running IPv6.</span></span> <span data-ttu-id="148fd-148">WMI supporta le connessioni ai computer che eseguono IPv6.</span><span class="sxs-lookup"><span data-stu-id="148fd-148">WMI supports connections to computers running IPv6.</span></span> <span data-ttu-id="148fd-149">Tuttavia, sia il computer locale che il "computer \_ B" devono eseguire IPv6.</span><span class="sxs-lookup"><span data-stu-id="148fd-149">However, both your local machine and "Computer\_B" must be running IPv6.</span></span> <span data-ttu-id="148fd-150">È anche possibile che in entrambi i computer sia in esecuzione IPv4.</span><span class="sxs-lookup"><span data-stu-id="148fd-150">Either computer may be running IPv4 also.</span></span> <span data-ttu-id="148fd-151">Per ulteriori informazioni, vedere [supporto di IPv6 e IPv4 in WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="148fd-151">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>
-   <span data-ttu-id="148fd-152">Non è necessario delegare lo script, ovvero non è necessario accedere a computer remoti aggiuntivi tramite il computer remoto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="148fd-152">Your script does not need to delegate - that is, it does not need to access additional remote computers through the targeted remote computer.</span></span> <span data-ttu-id="148fd-153">Per ulteriori informazioni, vedere [delega con WMI](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="148fd-153">For more information, see [Delegating with WMI](connecting-to-a-3rd-computer-delegation.md).</span></span>
-   <span data-ttu-id="148fd-154">Si sta provando a effettuare una chiamata specifica, anziché creare un processo remoto.</span><span class="sxs-lookup"><span data-stu-id="148fd-154">You are trying to make a specific call, rather than creating a remote process.</span></span> <span data-ttu-id="148fd-155">Per ulteriori informazioni, vedere [creazione di processi in modalità remota tramite WMI](creating-processes-remotely.md).</span><span class="sxs-lookup"><span data-stu-id="148fd-155">For more information, see [Creating Processes Remotely using WMI](creating-processes-remotely.md).</span></span>

<span data-ttu-id="148fd-156">Tenendo conto di queste limitazioni, una chiamata WMI remota è molto simile a una chiamata WMI locale. l'unica differenza consiste nel fatto che è necessario specificare il nome del sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="148fd-156">With those restrictions in mind, a remote WMI call is very similar to a local WMI call - the only difference being that you must specify the name of the remote system.</span></span> <span data-ttu-id="148fd-157">Tuttavia, è possibile scegliere di modificare molte di queste funzionalità: usando credenziali diverse o indirizzando la chiamata attraverso un computer di terze parti o accedendo a un dominio diverso.</span><span class="sxs-lookup"><span data-stu-id="148fd-157">However, you may choose to change many of those features: using different credentials, or routing your call through a 3rd party computer, or accessing a different domain.</span></span>

 

 
