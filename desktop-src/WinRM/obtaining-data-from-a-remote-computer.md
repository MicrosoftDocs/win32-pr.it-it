---
title: Recupero di dati da un computer remoto
description: È possibile ottenere dati o gestire le risorse in computer remoti e nel computer locale. La connessione a un computer remoto in uno script Gestione remota Windows è molto simile all'esecuzione di una connessione locale.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cfc95a73dab4c9a0f19481b7ba41f3c40a3862d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872545"
---
# <a name="obtaining-data-from-a-remote-computer"></a><span data-ttu-id="f92d8-104">Recupero di dati da un computer remoto</span><span class="sxs-lookup"><span data-stu-id="f92d8-104">Obtaining Data from a Remote Computer</span></span>

<span data-ttu-id="f92d8-105">È possibile ottenere dati o gestire le risorse in computer remoti e nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="f92d8-105">You can obtain data or manage resources on remote computers as well as the local computer.</span></span> <span data-ttu-id="f92d8-106">La connessione a un computer remoto in uno script Gestione remota Windows è molto simile all'esecuzione di una connessione locale.</span><span class="sxs-lookup"><span data-stu-id="f92d8-106">Connecting to a remote computer in a Windows Remote Management script is very similar to making a local connection.</span></span> <span data-ttu-id="f92d8-107">I dati dell'istanza WMI sono disponibili e, se il computer remoto dispone di hardware BMC in grado di comunicare utilizzando il protocollo di WS-Management, sono disponibili anche i dati dell' [interfaccia di gestione piattaforma intelligente (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) .</span><span class="sxs-lookup"><span data-stu-id="f92d8-107">WMI instance data is available and, if the remote computer has BMC hardware that can communicate using the WS-Management protocol, then [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) data is also available.</span></span> <span data-ttu-id="f92d8-108">Per ulteriori informazioni, vedere [gestione remota Windows e WMI](windows-remote-management-and-wmi.md) e [gestione hardware remota](remote-hardware-management.md).</span><span class="sxs-lookup"><span data-stu-id="f92d8-108">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md) and [Remote Hardware Management](remote-hardware-management.md).</span></span>

<span data-ttu-id="f92d8-109">Potrebbe essere necessario creare un oggetto [**ConnectionOptions**](connectionoptions.md) per specificare le informazioni sul tipo di autenticazione richiesto per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="f92d8-109">You may need to create a [**ConnectionOptions**](connectionoptions.md) object to specify information about the type of authentication requested for the logon.</span></span>

<span data-ttu-id="f92d8-110">Se l'account del computer remoto ha lo stesso nome utente e la stessa password di accesso, le uniche informazioni aggiuntive necessarie sono il trasporto, il nome di dominio e il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="f92d8-110">If the account on the remote computer has the same logon username and password, the only extra information you need is the transport, the domain name, and the computer name.</span></span> <span data-ttu-id="f92d8-111">A causa del [controllo dell'account utente](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), l'account remoto deve essere un account di dominio e un membro del gruppo Administrators del computer remoto.</span><span class="sxs-lookup"><span data-stu-id="f92d8-111">Because of [User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), the remote account must be a domain account and a member of the remote computer Administrators group.</span></span> <span data-ttu-id="f92d8-112">Se l'account è un membro del computer locale del gruppo Administrators, il controllo dell'account utente non consente l'accesso al servizio WinRM.</span><span class="sxs-lookup"><span data-stu-id="f92d8-112">If the account is a local computer member of the Administrators group, then UAC does not allow access to the WinRM service.</span></span> <span data-ttu-id="f92d8-113">Per accedere a un servizio WinRM remoto in un gruppo di lavoro, è necessario disabilitare il filtro UAC per gli account locali creando la seguente voce del registro di sistema DWORD e impostandone il valore su 1: **\[ HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \] LocalAccountTokenFilterPolicy**.</span><span class="sxs-lookup"><span data-stu-id="f92d8-113">To access a remote WinRM service in a workgroup, UAC filtering for local accounts must be disabled by creating the following DWORD registry entry and setting its value to 1: **\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\System\] LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="f92d8-114">**Per connettersi a un computer remoto usando il nome utente e la password di accesso**</span><span class="sxs-lookup"><span data-stu-id="f92d8-114">**To connect to a remote computer using your logon username and password**</span></span>

1.  <span data-ttu-id="f92d8-115">Specificare il computer di destinazione con un nome di dominio completo o un indirizzo IP e assegnarlo a una costante.</span><span class="sxs-lookup"><span data-stu-id="f92d8-115">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="f92d8-116">Se viene specificato un indirizzo IPv6, l'indirizzo deve essere racchiuso tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="f92d8-116">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="f92d8-117">Creare un oggetto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="f92d8-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  <span data-ttu-id="f92d8-118">Creare la sessione, specificando il trasporto, HTTP o HTTPS, e concatenarla con la costante che rappresenta il computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f92d8-118">Create the session, specifying the transport, HTTP or HTTPS, and concatenating it with the constant representing the target computer.</span></span>

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

<span data-ttu-id="f92d8-119">Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo.</span><span class="sxs-lookup"><span data-stu-id="f92d8-119">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="f92d8-120">Lo script include una subroutine per trasformare i dati da XML non elaborato a formato leggibile.</span><span class="sxs-lookup"><span data-stu-id="f92d8-120">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="f92d8-121">Per ulteriori informazioni, vedere [visualizzazione dell'output XML dagli script WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="f92d8-121">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



<span data-ttu-id="f92d8-122">**Per connettersi a un computer remoto usando un account diverso**</span><span class="sxs-lookup"><span data-stu-id="f92d8-122">**To connect to a remote computer using a different account**</span></span>

1.  <span data-ttu-id="f92d8-123">Specificare il computer di destinazione con un nome di dominio completo o un indirizzo IP e assegnarlo a una costante.</span><span class="sxs-lookup"><span data-stu-id="f92d8-123">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="f92d8-124">Se viene specificato un indirizzo IPv6, l'indirizzo deve essere racchiuso tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="f92d8-124">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="f92d8-125">Creare un oggetto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="f92d8-125">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  <span data-ttu-id="f92d8-126">Chiamare il metodo [**WSMan. CreateConnectionOptions**](wsman-createconnectionoptions.md) per creare un oggetto [**ConnectionOptions**](connectionoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="f92d8-126">Call the [**WSMan.CreateConnectionOptions**](wsman-createconnectionoptions.md) method to create a [**ConnectionOptions**](connectionoptions.md) object.</span></span> <span data-ttu-id="f92d8-127">L'account nel computer remoto deve essere un membro del gruppo Administrators del computer locale.</span><span class="sxs-lookup"><span data-stu-id="f92d8-127">The account on the remote computer must be a member of the local computer administrators group.</span></span>

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  <span data-ttu-id="f92d8-128">Nella chiamata [**WSMan. CreateSession**](wsman-createsession.md) specificare i flag di connessione di sessione appropriati nel parametro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="f92d8-128">On the [**WSman.CreateSession**](wsman-createsession.md) call, specify the appropriate session connection flags in the *flags* parameter.</span></span> <span data-ttu-id="f92d8-129">Per altre informazioni, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f92d8-129">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="f92d8-130">Specificare il computer di destinazione con un nome di computer completo o un indirizzo IP e il trasporto, ovvero http o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f92d8-130">Specify the target computer with a fully qualified computer name or an IP address and the transport—http or https.</span></span> <span data-ttu-id="f92d8-131">Questo script richiede l'autenticazione [*Kerberos*](windows-remote-management-glossary.md) dal servizio WinRM remoto.</span><span class="sxs-lookup"><span data-stu-id="f92d8-131">This script requests [*Kerberos*](windows-remote-management-glossary.md) authentication from the remote WinRM service.</span></span>

    <span data-ttu-id="f92d8-132">Diversamente dagli script WMI, è possibile utilizzare diversi metodi di autenticazione negli script WinRM.</span><span class="sxs-lookup"><span data-stu-id="f92d8-132">Unlike WMI scripts, you can use several methods of authentication in WinRM scripts.</span></span> <span data-ttu-id="f92d8-133">Per altre informazioni, vedere [autenticazione per le connessioni remote](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="f92d8-133">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  <span data-ttu-id="f92d8-134">Quando l'oggetto Session è disponibile, è possibile chiamare qualsiasi metodo dell'oggetto [**Session**](session.md) per ottenere i dati per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="f92d8-134">After the session object is available, you can call any of the [**Session**](session.md) object methods to obtain data for a resource.</span></span> <span data-ttu-id="f92d8-135">È possibile ottenere dati per qualsiasi risorsa disponibile nel computer in cui è in esecuzione la sessione.</span><span class="sxs-lookup"><span data-stu-id="f92d8-135">You can get data for any resource that is available on the computer on which the session is running.</span></span> <span data-ttu-id="f92d8-136">Per ulteriori informazioni, vedere [recupero di dati dal computer locale](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="f92d8-136">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span>

<span data-ttu-id="f92d8-137">Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo.</span><span class="sxs-lookup"><span data-stu-id="f92d8-137">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="f92d8-138">Lo script include una subroutine per trasformare i dati da XML non elaborato a formato leggibile.</span><span class="sxs-lookup"><span data-stu-id="f92d8-138">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="f92d8-139">Per ulteriori informazioni, vedere [visualizzazione dell'output XML dagli script WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="f92d8-139">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span> <span data-ttu-id="f92d8-140">Lo script specifica l'autenticazione Kerberos, ma se il computer remoto si trova in un gruppo di lavoro anziché in un dominio, specificando Kerberos viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="f92d8-140">The script specifies Kerberos authentication, but if the remote computer is in a workgroup rather than a domain, specifying Kerberos generates an error.</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("Wsman.Automation")
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "Username"
objConnectionOptions.Password = "Password"
iFlags = objWsman.SessionFlagUseKerberos Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
  iFlags, objConnectionOptions)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="f92d8-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f92d8-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f92d8-142">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="f92d8-142">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="f92d8-143">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="f92d8-143">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="f92d8-144">Riferimento Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="f92d8-144">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 