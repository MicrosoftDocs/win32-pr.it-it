---
title: Imposta il livello di sicurezza del processo predefinito con VBScript
description: Uno script può utilizzare le impostazioni predefinite di autenticazione WMI e di rappresentazione. Tuttavia, lo script potrebbe richiedere una connessione con una maggiore sicurezza o connettersi a uno spazio dei nomi che richiede una connessione crittografata.
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fe69228021fe8d3f36f03e60cb2366b6132f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233816"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a><span data-ttu-id="93c66-104">Imposta il livello di sicurezza del processo predefinito con VBScript</span><span class="sxs-lookup"><span data-stu-id="93c66-104">Set the default process security level with VBScript</span></span>

<span data-ttu-id="93c66-105">Uno script può utilizzare le impostazioni predefinite di autenticazione WMI e di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="93c66-105">A script can use the default WMI authentication and impersonation settings.</span></span> <span data-ttu-id="93c66-106">Tuttavia, lo script potrebbe richiedere una connessione con una maggiore sicurezza o connettersi a uno spazio dei nomi che richiede una connessione crittografata.</span><span class="sxs-lookup"><span data-stu-id="93c66-106">However, the script may need a connection with more security or may connect to a namespace that requires an encrypted connection.</span></span> <span data-ttu-id="93c66-107">Per ulteriori informazioni, vedere [impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md) e [richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="93c66-107">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md) and [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="93c66-108">Nel caso più semplice, uno script può utilizzare le impostazioni di autenticazione e rappresentazione predefinite.</span><span class="sxs-lookup"><span data-stu-id="93c66-108">In the simplest case, a script can use the default authentication and impersonation settings.</span></span> <span data-ttu-id="93c66-109">WMI viene in genere eseguito in un host del servizio condiviso e condivide la stessa autenticazione di altri processi nell'host.</span><span class="sxs-lookup"><span data-stu-id="93c66-109">WMI normally runs in a shared service host and shares the same authentication as other processes in the host.</span></span> <span data-ttu-id="93c66-110">Se si desidera eseguire il processo WMI con un livello di autenticazione diverso, eseguire WMI con il comando [**WinMgmt**](winmgmt.md) con l'opzione **/standalonehost** e impostare il livello di autenticazione per WMI in genere.</span><span class="sxs-lookup"><span data-stu-id="93c66-110">If you want to run the WMI process with a different level of authentication, run WMI with the [**winmgmt**](winmgmt.md) command with the **/standalonehost** switch and set the authentication level for WMI generally.</span></span> <span data-ttu-id="93c66-111">Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="93c66-111">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

<span data-ttu-id="93c66-112">Lo script seguente utilizza le impostazioni predefinite per i livelli di autenticazione e di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="93c66-112">The following script uses default settings for impersonation and authentication levels.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="93c66-113">È anche possibile usare un [moniker](constructing-a-moniker-string.md) in una chiamata a [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)e impostare le impostazioni di sicurezza predefinite, come nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="93c66-113">You can also use a [moniker](constructing-a-moniker-string.md) in a call to [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), and set the default security settings, as in the following example.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="93c66-114">Per ulteriori informazioni sull'impostazione di livelli di autenticazione o rappresentazione diversi in uno script o sull'impostazione dei valori predefiniti per un computer, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="93c66-114">For more information about setting different impersonation or authentication levels in a script, or for setting the default values for a computer, see the following topics:</span></span>

-   [<span data-ttu-id="93c66-115">Modifica delle credenziali di autenticazione predefinite tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="93c66-115">Changing the Default Authentication Credentials Using VBScript</span></span>](#changing-the-default-authentication-credentials-using-vbscript)
-   [<span data-ttu-id="93c66-116">Modifica delle impostazioni di rappresentazione predefinite tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="93c66-116">Changing the Default Impersonation Settings Using VBScript</span></span>](#changing-the-default-impersonation-levels-using-vbscript)
-   [<span data-ttu-id="93c66-117">Impostazione del livello di rappresentazione predefinito utilizzando il registro di sistema</span><span class="sxs-lookup"><span data-stu-id="93c66-117">Setting the Default Impersonation Level Using the Registry</span></span>](#setting-the-default-impersonation-level-using-the-registry)
-   [<span data-ttu-id="93c66-118">Accesso all'oggetto SWbemSecurity in VBScript</span><span class="sxs-lookup"><span data-stu-id="93c66-118">Accessing the SWbemSecurity Object in VBScript</span></span>](#accessing-the-swbemsecurity-object-in-vbscript)
-   [<span data-ttu-id="93c66-119">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="93c66-119">**SWbemSecurity**</span></span>](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a><span data-ttu-id="93c66-120">Modifica delle credenziali di autenticazione predefinite tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="93c66-120">Changing the Default Authentication Credentials Using VBScript</span></span>

<span data-ttu-id="93c66-121">È possibile modificare il livello di autenticazione in uno script utilizzando una stringa del [moniker](constructing-a-moniker-string.md) e gli oggetti [**SWbemLocator**](swbemlocator.md) e [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="93c66-121">You can change the authentication level in a script using a [moniker](constructing-a-moniker-string.md) string, and the [**SWbemLocator**](swbemlocator.md) and [**SWbemSecurity**](swbemsecurity.md) objects.</span></span>

<span data-ttu-id="93c66-122">Il livello di autenticazione deve essere impostato in base ai requisiti del sistema operativo di destinazione a cui ci si connette.</span><span class="sxs-lookup"><span data-stu-id="93c66-122">The authentication level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="93c66-123">Per ulteriori informazioni, vedere [connessione tra sistemi operativi diversi](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="93c66-123">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="93c66-124">Nell'esempio di codice VBScript riportato di seguito viene illustrato come modificare il livello di autenticazione in uno script che ottiene i dati di spazio libero da un computer remoto denominato "server1".</span><span class="sxs-lookup"><span data-stu-id="93c66-124">The following VBScript code example shows how to change the authentication level in a script that obtains the free space data from a remote computer named "Server1".</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



<span data-ttu-id="93c66-125">Nelle connessioni del moniker di script a WMI usare il nome breve visualizzato nella colonna "nome/descrizione del moniker" della tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="93c66-125">In script moniker connections to WMI, use the short name shown in the "Moniker name/description" column of the table below.</span></span> <span data-ttu-id="93c66-126">Nello script seguente, ad esempio, il livello di autenticazione è impostato su **WbemAuthenticationLevelPktIntegrity**.</span><span class="sxs-lookup"><span data-stu-id="93c66-126">For example, in the following script, the authentication level is set to **WbemAuthenticationLevelPktIntegrity**.</span></span>


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



<span data-ttu-id="93c66-127">Nella tabella seguente sono elencati i livelli di autenticazione che è possibile impostare.</span><span class="sxs-lookup"><span data-stu-id="93c66-127">The following table lists the authentication levels you can set.</span></span> <span data-ttu-id="93c66-128">Questi livelli sono definiti in wbemdisp. tlb nell'enumerazione [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="93c66-128">These levels are defined in Wbemdisp.tlb in the enumeration [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>



| <span data-ttu-id="93c66-129">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="93c66-129">Name/value</span></span>                                                      | <span data-ttu-id="93c66-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93c66-130">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93c66-131">**WbemAuthenticationLevelDefault**</span><span class="sxs-lookup"><span data-stu-id="93c66-131">**WbemAuthenticationLevelDefault**</span></span><br/> <span data-ttu-id="93c66-132">0</span><span class="sxs-lookup"><span data-stu-id="93c66-132">0</span></span><br/>      | <span data-ttu-id="93c66-133">Moniker: predefinito</span><span class="sxs-lookup"><span data-stu-id="93c66-133">Moniker: Default</span></span><br/> <span data-ttu-id="93c66-134">WMI utilizza l'impostazione predefinita di autenticazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="93c66-134">WMI uses the default Windows authentication setting.</span></span> <span data-ttu-id="93c66-135">Si tratta dell'impostazione consigliata che consente a WMI di negoziare il livello richiesto dal server per la restituzione di dati.</span><span class="sxs-lookup"><span data-stu-id="93c66-135">This is the recommended setting that allows WMI to negotiate to the level required by the server returning data.</span></span> <span data-ttu-id="93c66-136">Tuttavia, se lo spazio dei nomi richiede la crittografia, usare **WbemAuthenticationLevelPktPrivacy**.</span><span class="sxs-lookup"><span data-stu-id="93c66-136">However, if the namespace requires encryption, use **WbemAuthenticationLevelPktPrivacy**.</span></span><br/> |
| <span data-ttu-id="93c66-137">**WbemAuthenticationLevelNone**</span><span class="sxs-lookup"><span data-stu-id="93c66-137">**WbemAuthenticationLevelNone**</span></span><br/> <span data-ttu-id="93c66-138">1</span><span class="sxs-lookup"><span data-stu-id="93c66-138">1</span></span><br/>         | <span data-ttu-id="93c66-139">Moniker: None</span><span class="sxs-lookup"><span data-stu-id="93c66-139">Moniker: None</span></span><br/> <span data-ttu-id="93c66-140">Non usa alcuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="93c66-140">Uses no authentication.</span></span><br/>                                                                                                                                                                                                                                            |
| <span data-ttu-id="93c66-141">**WbemAuthenticationLevelConnect**</span><span class="sxs-lookup"><span data-stu-id="93c66-141">**WbemAuthenticationLevelConnect**</span></span><br/> <span data-ttu-id="93c66-142">2</span><span class="sxs-lookup"><span data-stu-id="93c66-142">2</span></span><br/>      | <span data-ttu-id="93c66-143">Moniker: Connetti</span><span class="sxs-lookup"><span data-stu-id="93c66-143">Moniker: Connect</span></span><br/> <span data-ttu-id="93c66-144">Autentica le credenziali del client solo quando il client stabilisce una relazione con il server.</span><span class="sxs-lookup"><span data-stu-id="93c66-144">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span><br/>                                                                                                                                                    |
| <span data-ttu-id="93c66-145">**WbemAuthenticationLevelCall**</span><span class="sxs-lookup"><span data-stu-id="93c66-145">**WbemAuthenticationLevelCall**</span></span><br/> <span data-ttu-id="93c66-146">3</span><span class="sxs-lookup"><span data-stu-id="93c66-146">3</span></span><br/>         | <span data-ttu-id="93c66-147">Chiamata</span><span class="sxs-lookup"><span data-stu-id="93c66-147">Call</span></span><br/> <span data-ttu-id="93c66-148">Esegue l'autenticazione solo all'inizio di ogni chiamata quando il server riceve la richiesta.</span><span class="sxs-lookup"><span data-stu-id="93c66-148">Authenticates only at the beginning of each call when the server receives the request.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="93c66-149">**WbemAuthenticationLevelPkt**</span><span class="sxs-lookup"><span data-stu-id="93c66-149">**WbemAuthenticationLevelPkt**</span></span><br/> <span data-ttu-id="93c66-150">4</span><span class="sxs-lookup"><span data-stu-id="93c66-150">4</span></span><br/>          | <span data-ttu-id="93c66-151">Moniker: PKT</span><span class="sxs-lookup"><span data-stu-id="93c66-151">Moniker: Pkt</span></span><br/> <span data-ttu-id="93c66-152">Autentica che tutti i dati ricevuti provengano dal client previsto.</span><span class="sxs-lookup"><span data-stu-id="93c66-152">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                                                                                   |
| <span data-ttu-id="93c66-153">**WbemAuthenticationLevelPktIntegrity**</span><span class="sxs-lookup"><span data-stu-id="93c66-153">**WbemAuthenticationLevelPktIntegrity**</span></span><br/> <span data-ttu-id="93c66-154">5</span><span class="sxs-lookup"><span data-stu-id="93c66-154">5</span></span><br/> | <span data-ttu-id="93c66-155">Moniker: PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="93c66-155">Moniker: PktIntegrity</span></span><br/> <span data-ttu-id="93c66-156">Autentica e verifica che nessuno dei dati trasferiti tra il client e il server sia stato modificato.</span><span class="sxs-lookup"><span data-stu-id="93c66-156">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="93c66-157">**WbemAuthenticationLevelPktPrivacy**</span><span class="sxs-lookup"><span data-stu-id="93c66-157">**WbemAuthenticationLevelPktPrivacy**</span></span><br/> <span data-ttu-id="93c66-158">6</span><span class="sxs-lookup"><span data-stu-id="93c66-158">6</span></span><br/>   | <span data-ttu-id="93c66-159">Moniker: su PktPrivacy</span><span class="sxs-lookup"><span data-stu-id="93c66-159">Moniker: PktPrivacy</span></span><br/> <span data-ttu-id="93c66-160">Autentica tutti i livelli di rappresentazione precedenti e crittografa il valore dell'argomento di ogni chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="93c66-160">Authenticates all previous impersonation levels and encrypts the argument value of each remote procedure call.</span></span> <span data-ttu-id="93c66-161">Usare questa impostazione se lo spazio dei nomi a cui ci si connette richiede una connessione crittografata.</span><span class="sxs-lookup"><span data-stu-id="93c66-161">Use this setting if the namespace to which you are connecting requires an encrypted connection.</span></span><br/>                                               |



 

<span data-ttu-id="93c66-162">Per determinare una chiamata con esito positivo, controllare il valore restituito dopo aver modificato il livello di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="93c66-162">To determine a successful call, check the return value after you change the authentication level.</span></span>

<span data-ttu-id="93c66-163">Ad esempio, poiché le connessioni locali hanno sempre un livello di autenticazione di **wbemAuthenticationLevelPktPrivacy**, l'esempio seguente non riesce a impostare il livello di autenticazione perché si connette al computer locale.</span><span class="sxs-lookup"><span data-stu-id="93c66-163">For example, because local connections always have an authentication level of **wbemAuthenticationLevelPktPrivacy**, the following example fails to set the authentication level because it connects to the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="93c66-164">Un provider può impostare la sicurezza su uno spazio dei nomi in modo che non venga restituito alcun dato, a meno che non si usi il pacchetto privacy (su PktPrivacy) nella connessione a tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="93c66-164">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (PktPrivacy) in your connection to that namespace.</span></span> <span data-ttu-id="93c66-165">In questo modo si garantisce che i dati vengano crittografati quando attraversa la rete.</span><span class="sxs-lookup"><span data-stu-id="93c66-165">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="93c66-166">Se si tenta di impostare un livello di autenticazione inferiore, si otterrà un messaggio di accesso negato.</span><span class="sxs-lookup"><span data-stu-id="93c66-166">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="93c66-167">Per ulteriori informazioni, vedere [protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="93c66-167">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a><span data-ttu-id="93c66-168">Modifica dei livelli di rappresentazione predefiniti tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="93c66-168">Changing the Default Impersonation Levels Using VBScript</span></span>

<span data-ttu-id="93c66-169">Quando si effettuano chiamate all'API di scripting per WMI, è consigliabile utilizzare le impostazioni predefinite fornite da WMI per il livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="93c66-169">When you make calls to the Scripting API for WMI, it is recommended that you use the defaults that WMI provides for the impersonation level.</span></span> <span data-ttu-id="93c66-170">Per le chiamate remote e alcuni provider con più hop di rete è necessario un livello di rappresentazione superiore rispetto a quello utilizzato da WMI.</span><span class="sxs-lookup"><span data-stu-id="93c66-170">Remote calls and some providers with more than one network hop require a higher impersonation level than WMI uses.</span></span> <span data-ttu-id="93c66-171">Se il livello di rappresentazione non è sufficiente, un provider potrebbe rifiutare una richiesta o fornire informazioni incomplete.</span><span class="sxs-lookup"><span data-stu-id="93c66-171">If the impersonation level is not sufficient, a provider might refuse a request or provide incomplete information.</span></span>

<span data-ttu-id="93c66-172">Se non si imposta il livello di rappresentazione in un moniker o impostando [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) su un oggetto a protezione diretta, impostare il livello di rappresentazione DCOM predefinito per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="93c66-172">If you do not set the impersonation level in either a moniker or by setting [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on a securable object, then set the default DCOM impersonation level for the operating system.</span></span> <span data-ttu-id="93c66-173">Il livello di rappresentazione deve essere impostato in base ai requisiti del sistema operativo di destinazione a cui ci si connette.</span><span class="sxs-lookup"><span data-stu-id="93c66-173">The impersonation level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="93c66-174">Per ulteriori informazioni, vedere [connessione tra sistemi operativi diversi](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="93c66-174">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="93c66-175">Nell'esempio di codice VBScript riportato di seguito viene illustrata la modifica del livello di rappresentazione nello stesso script illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="93c66-175">The following VBScript code example shows changing the impersonation level in the same script shown above.</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



<span data-ttu-id="93c66-176">La tabella seguente elenca i livelli di autenticazione in [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) che usano.</span><span class="sxs-lookup"><span data-stu-id="93c66-176">The following table lists the authentication levels in [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) that use.</span></span>



| <span data-ttu-id="93c66-177">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="93c66-177">Name/value</span></span>                                                    | <span data-ttu-id="93c66-178">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93c66-178">Description</span></span>                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93c66-179">**wbemImpersonationLevelAnonymous**</span><span class="sxs-lookup"><span data-stu-id="93c66-179">**wbemImpersonationLevelAnonymous**</span></span><br/> <span data-ttu-id="93c66-180">1</span><span class="sxs-lookup"><span data-stu-id="93c66-180">1</span></span><br/>   | <span data-ttu-id="93c66-181">Moniker: Anonimo</span><span class="sxs-lookup"><span data-stu-id="93c66-181">Moniker: Anonymous</span></span><br/> <span data-ttu-id="93c66-182">Nasconde le credenziali del chiamante.</span><span class="sxs-lookup"><span data-stu-id="93c66-182">Hides the credentials of the caller.</span></span> <span data-ttu-id="93c66-183">Le chiamate a WMI potrebbero non riuscire a questo livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="93c66-183">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                                  |
| <span data-ttu-id="93c66-184">**wbemImpersonationLevelIdentify**</span><span class="sxs-lookup"><span data-stu-id="93c66-184">**wbemImpersonationLevelIdentify**</span></span><br/> <span data-ttu-id="93c66-185">2</span><span class="sxs-lookup"><span data-stu-id="93c66-185">2</span></span><br/>    | <span data-ttu-id="93c66-186">Moniker: identificare</span><span class="sxs-lookup"><span data-stu-id="93c66-186">Moniker: Identify</span></span><br/> <span data-ttu-id="93c66-187">Consente agli oggetti di eseguire query sulle credenziali del chiamante.</span><span class="sxs-lookup"><span data-stu-id="93c66-187">Allows objects to query the credentials of the caller.</span></span> <span data-ttu-id="93c66-188">Le chiamate a WMI potrebbero non riuscire a questo livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="93c66-188">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                 |
| <span data-ttu-id="93c66-189">**wbemImpersonationLevelImpersonate**</span><span class="sxs-lookup"><span data-stu-id="93c66-189">**wbemImpersonationLevelImpersonate**</span></span><br/> <span data-ttu-id="93c66-190">3</span><span class="sxs-lookup"><span data-stu-id="93c66-190">3</span></span><br/> | <span data-ttu-id="93c66-191">Moniker: Impersonate</span><span class="sxs-lookup"><span data-stu-id="93c66-191">Moniker: Impersonate</span></span><br/> <span data-ttu-id="93c66-192">Consente agli oggetti di usare le credenziali del chiamante.</span><span class="sxs-lookup"><span data-stu-id="93c66-192">Allows objects to use the credentials of the caller.</span></span> <span data-ttu-id="93c66-193">Questo è il livello di rappresentazione consigliato per l'API di scripting per le chiamate WMI.</span><span class="sxs-lookup"><span data-stu-id="93c66-193">This is the recommended impersonation level for Scripting API for WMI calls.</span></span><br/>                                                        |
| <span data-ttu-id="93c66-194">**wbemImpersonationLevelDelegate**</span><span class="sxs-lookup"><span data-stu-id="93c66-194">**wbemImpersonationLevelDelegate**</span></span><br/> <span data-ttu-id="93c66-195">4</span><span class="sxs-lookup"><span data-stu-id="93c66-195">4</span></span><br/>    | <span data-ttu-id="93c66-196">Moniker: delegato</span><span class="sxs-lookup"><span data-stu-id="93c66-196">Moniker: Delegate</span></span><br/> <span data-ttu-id="93c66-197">Consente agli oggetti di permettere ad altri oggetti di usare le credenziali del chiamante.</span><span class="sxs-lookup"><span data-stu-id="93c66-197">Allows objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="93c66-198">Questa rappresentazione funzionerà con l'API di scripting per le chiamate WMI, ma potrebbe costituire un rischio di sicurezza non necessario.</span><span class="sxs-lookup"><span data-stu-id="93c66-198">This impersonation will work with Scripting API for WMI calls but may constitute an unnecessary security risk.</span></span><br/> |



 

<span data-ttu-id="93c66-199">Nell'esempio seguente viene illustrato come impostare la rappresentazione in una stringa del moniker quando si ottiene un'istanza specifica del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="93c66-199">The following example shows how to set the impersonation in a moniker string when obtaining a specific instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



<span data-ttu-id="93c66-200">Per ulteriori informazioni, vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="93c66-200">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

## <a name="setting-the-default-impersonation-level-using-the-registry"></a><span data-ttu-id="93c66-201">Impostazione del livello di rappresentazione predefinito utilizzando il registro di sistema</span><span class="sxs-lookup"><span data-stu-id="93c66-201">Setting the Default Impersonation Level Using the Registry</span></span>

<span data-ttu-id="93c66-202">Se si dispone dell'accesso al registro di sistema, è inoltre possibile impostare la chiave predefinita del registro di sistema livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="93c66-202">If you have access to the registry, you can also set the default impersonation level registry key.</span></span> <span data-ttu-id="93c66-203">Questa chiave specifica il livello di rappresentazione usato dall'API di scripting per WMI, se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="93c66-203">This key specifies which impersonation level the Scripting API for WMI uses unless otherwise specified.</span></span> <span data-ttu-id="93c66-204">Il percorso seguente identifica il percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="93c66-204">The following path identifies the registry path.</span></span>

<span data-ttu-id="93c66-205">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **predefinito livello di rappresentazione**</span><span class="sxs-lookup"><span data-stu-id="93c66-205">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Impersonation Level**</span></span>

<span data-ttu-id="93c66-206">Per impostazione predefinita, la chiave del registro di sistema è impostata su 3, specificando il livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="93c66-206">By default, the registry key is set to 3, specifying the Impersonate impersonation level.</span></span> <span data-ttu-id="93c66-207">Alcuni provider possono richiedere un livello di rappresentazione superiore.</span><span class="sxs-lookup"><span data-stu-id="93c66-207">Some providers may require a higher level of impersonation.</span></span>

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a><span data-ttu-id="93c66-208">Accesso all'oggetto SWbemSecurity in VBScript</span><span class="sxs-lookup"><span data-stu-id="93c66-208">Accessing the SWbemSecurity Object in VBScript</span></span>

<span data-ttu-id="93c66-209">In alternativa, è possibile impostare il livello di rappresentazione dall'oggetto di sicurezza [**SWbemSecurity**](swbemsecurity.md) , che viene visualizzato come proprietà di [**sicurezza \_**](swbemservices-security-.md) degli oggetti [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="93c66-209">The other way you can set the impersonation level is from the [**SWbemSecurity**](swbemsecurity.md) security object, which appears as the [**Security\_**](swbemservices-security-.md) property of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects.</span></span>

<span data-ttu-id="93c66-210">WMI passa l'impostazione di sicurezza di un oggetto padre ai discendenti dell'oggetto originale.</span><span class="sxs-lookup"><span data-stu-id="93c66-210">WMI passes the security setting of a parent object to the descendants of the original object.</span></span> <span data-ttu-id="93c66-211">Pertanto, è possibile impostare il livello di rappresentazione di un oggetto [**SWbemServices**](swbemservices.md) dopo l'accesso a WMI e alle chiamate API utilizzando questo oggetto o oggetti creati, ad esempio oggetti di tipo [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="93c66-211">Therefore, you can set the impersonation level of an [**SWbemServices**](swbemservices.md) object after logging on to WMI and API calls using this object or objects created from it, such as objects of type [**SWbemObject**](swbemobject.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="93c66-212">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="93c66-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93c66-213">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="93c66-213">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="93c66-214">Protezione dei client di scripting</span><span class="sxs-lookup"><span data-stu-id="93c66-214">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

