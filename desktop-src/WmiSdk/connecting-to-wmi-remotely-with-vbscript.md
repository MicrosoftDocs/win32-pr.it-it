---
description: È possibile creare una connessione remota a WMI con VBScript creando un oggetto connessione. Questo oggetto contiene il nome del computer, lo spazio dei nomi WMI a cui si desidera connettersi, nonché le credenziali rilevanti e i livelli di autenticazione.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Connessione a WMI in modalità remota con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310409"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a><span data-ttu-id="e0db0-104">Connessione a WMI in modalità remota con VBScript</span><span class="sxs-lookup"><span data-stu-id="e0db0-104">Connecting to WMI Remotely with VBScript</span></span>

<span data-ttu-id="e0db0-105">È possibile creare una connessione remota a WMI con VBScript creando un oggetto connessione.</span><span class="sxs-lookup"><span data-stu-id="e0db0-105">You can create a remote connection to WMI with VBScript by creating a connection object.</span></span> <span data-ttu-id="e0db0-106">Questo oggetto contiene il nome del computer, lo spazio dei nomi WMI a cui si desidera connettersi, nonché le credenziali rilevanti e i livelli di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="e0db0-106">This object contains the name of the computer, the WMI namespace you want to connect to, as well as any relevant credentials and authentication levels.</span></span>

<span data-ttu-id="e0db0-107">**Per connettersi a un sistema remoto tramite VBScript**</span><span class="sxs-lookup"><span data-stu-id="e0db0-107">**To connect to a remote system using VBScript**</span></span>

1.  <span data-ttu-id="e0db0-108">Specificare le informazioni di connessione, ad esempio il nome del computer remoto, le credenziali e il livello di autenticazione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="e0db0-108">Specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span>

    <span data-ttu-id="e0db0-109">Se ci si connette a un computer remoto con le stesse credenziali (dominio e nome utente) con cui si è connessi, è possibile specificare le informazioni di connessione in un [moniker](constructing-a-moniker-string.md) [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), come descritto nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="e0db0-109">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the connection information in a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)[moniker](constructing-a-moniker-string.md), as described in the following code sample.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    <span data-ttu-id="e0db0-110">In generale, è necessario specificare lo spazio dei nomi WMI a cui connettersi nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="e0db0-110">Generally speaking, you should specify the WMI namespace to connect to on the remote computer.</span></span> <span data-ttu-id="e0db0-111">Questo perché è possibile che lo spazio dei nomi predefinito non sia lo stesso in computer diversi.</span><span class="sxs-lookup"><span data-stu-id="e0db0-111">This is because it is possible that the default namespace is not the same on different computers.</span></span> <span data-ttu-id="e0db0-112">Specificando lo spazio dei nomi si garantisce la connessione allo stesso spazio dei nomi in tutti i computer.</span><span class="sxs-lookup"><span data-stu-id="e0db0-112">Specifying the namespace ensures that you connect to the same namespace on all computers.</span></span>

    <span data-ttu-id="e0db0-113">Per ulteriori informazioni sulle costanti VBScript e sulle stringhe di scripting per l'utilizzo della connessione moniker, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="e0db0-113">For more information on VBScript constants and scripting strings for using the moniker connection, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

2.  <span data-ttu-id="e0db0-114">Se ci si connette a un computer remoto in un dominio diverso o si usano un nome utente e una password diversi, è necessario usare il metodo [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="e0db0-114">If you connect to a remote computer in a different domain or using a different user name and password, then you must use the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    <span data-ttu-id="e0db0-115">Come per un moniker, usare **ConnectServer** per specificare le credenziali, il livello di autenticazione e lo spazio dei nomi per la connessione remota.</span><span class="sxs-lookup"><span data-stu-id="e0db0-115">As with a moniker, you use **ConnectServer** to specify the credentials, authentication level, and namespace for the remote connection.</span></span> <span data-ttu-id="e0db0-116">Nell'esempio di codice seguente viene descritto l'utilizzo di ConnectServer per accedere a un computer remoto utilizzando un account amministratore e una password.</span><span class="sxs-lookup"><span data-stu-id="e0db0-116">The following code sample describes using ConnectServer to access a remote computer using an administrator account and password.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  <span data-ttu-id="e0db0-117">Quando si utilizza la funzione [**ConnectServer**](swbemlocator-connectserver.md) per le connessioni remote, impostare la rappresentazione e l'autenticazione sull'oggetto di sicurezza ottenuto tramite una chiamata a [**SWbemServices. Security**](swbemservices-security-.md).</span><span class="sxs-lookup"><span data-stu-id="e0db0-117">When using the [**ConnectServer**](swbemlocator-connectserver.md) function for remote connections, set impersonation and authentication on the security object obtained by a call to [**SWbemServices.Security**](swbemservices-security-.md).</span></span> <span data-ttu-id="e0db0-118">È possibile utilizzare l'enumerazione [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) per specificare il livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="e0db0-118">You can use the enumeration [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) to specify impersonation level.</span></span>

    <span data-ttu-id="e0db0-119">Nell'esempio di codice seguente viene impostato il livello di rappresentazione per l'esempio di codice VBScript precedente.</span><span class="sxs-lookup"><span data-stu-id="e0db0-119">The following code sample sets the impersonation level for the previous VBScript code sample.</span></span>

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    <span data-ttu-id="e0db0-120">Si noti che alcune connessioni richiedono un livello di autenticazione specifico.</span><span class="sxs-lookup"><span data-stu-id="e0db0-120">Note that some connections require a specific authentication level.</span></span> <span data-ttu-id="e0db0-121">Per ulteriori informazioni, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md) e [protezione dei client di scripting](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="e0db0-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md) and [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    <span data-ttu-id="e0db0-122">In particolare, è necessario impostare il livello di autenticazione **su \_ \_ \_ \_ PKT \_ privacy a livello** di autenticazione C o 6 se lo spazio dei nomi a cui ci si connette nel computer remoto richiede una connessione crittografata prima che restituisca dati.</span><span class="sxs-lookup"><span data-stu-id="e0db0-122">In particular, you should set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or 6 if the namespace to which you are connecting on the remote computer requires an encrypted connection before it will return data.</span></span> <span data-ttu-id="e0db0-123">È anche possibile usare questo livello di autenticazione, anche se lo spazio dei nomi non lo richiede.</span><span class="sxs-lookup"><span data-stu-id="e0db0-123">You can also use this authentication level, even if the namespace does not require it.</span></span> <span data-ttu-id="e0db0-124">In questo modo si garantisce che i dati vengano crittografati quando attraversa la rete.</span><span class="sxs-lookup"><span data-stu-id="e0db0-124">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="e0db0-125">Se si tenta di impostare un livello di autenticazione inferiore rispetto a quello consentito, verrà restituito un messaggio di accesso negato.</span><span class="sxs-lookup"><span data-stu-id="e0db0-125">If you attempt to set a lower authentication level than is allowed, an access denied message will be returned.</span></span> <span data-ttu-id="e0db0-126">Per ulteriori informazioni, vedere la pagina relativa [alla richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="e0db0-126">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="e0db0-127">Una volta effettuata la connessione, è possibile continuare ad accedere ai dati WMI.</span><span class="sxs-lookup"><span data-stu-id="e0db0-127">Once you have made your connection, you can continue to access WMI data.</span></span> <span data-ttu-id="e0db0-128">Per ulteriori informazioni, vedere [attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="e0db0-128">For more information, see [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e0db0-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="e0db0-129">Examples</span></span>

<span data-ttu-id="e0db0-130">Per un esempio VBScript più ampio, vedere la sezione Esempi nella pagina di riferimento [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="e0db0-130">For a larger VBScript sample, see the Examples section in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) reference page.</span></span>

<span data-ttu-id="e0db0-131">L'esempio di codice VBScript seguente consente di connettersi a un gruppo di computer remoti nello stesso dominio creando una matrice di nomi di computer remoti e visualizzando quindi i nomi dei dispositivi Plug and Play, ovvero le istanze di [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity), in ogni computer.</span><span class="sxs-lookup"><span data-stu-id="e0db0-131">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer.</span></span> <span data-ttu-id="e0db0-132">Per eseguire lo script seguente, è necessario essere un amministratore dei computer remoti.</span><span class="sxs-lookup"><span data-stu-id="e0db0-132">To run the script below, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="e0db0-133">Si noti che " \\ \\ " richiesto prima che il nome del computer remoto venga aggiunto dallo script che segue l'impostazione del livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="e0db0-133">Note that the "\\\\" required before the remote computer name is added by the script following the impersonation level setting.</span></span> <span data-ttu-id="e0db0-134">Per ulteriori informazioni sui percorsi WMI, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="e0db0-134">For more information about WMI paths, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



<span data-ttu-id="e0db0-135">L'esempio di codice VBScript seguente consente di connettersi a un computer remoto usando credenziali diverse.</span><span class="sxs-lookup"><span data-stu-id="e0db0-135">The following VBScript code example enables you to connect to a remote computer using different credentials.</span></span> <span data-ttu-id="e0db0-136">Ad esempio, un computer remoto in un dominio diverso o la connessione a un computer remoto che richiede un nome utente e una password diversi.</span><span class="sxs-lookup"><span data-stu-id="e0db0-136">For example, a remote computer in a different domain or connecting to a remote computer requiring a different user name and password.</span></span> <span data-ttu-id="e0db0-137">In questo caso, usare la connessione [**SWbemServices. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="e0db0-137">In this case, use the [**SWbemServices.ConnectServer**](swbemlocator-connectserver.md) connection.</span></span>


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a><span data-ttu-id="e0db0-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0db0-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0db0-139">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="e0db0-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
