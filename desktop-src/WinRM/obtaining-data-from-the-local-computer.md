---
title: Recupero di dati dal computer locale
description: Sebbene Gestione remota Windows e il protocollo di WS-Management siano progettati in modo esplicito per la comunicazione remota, è il caso più semplice stabilire una sessione nel computer locale.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727407"
---
# <a name="obtaining-data-from-the-local-computer"></a><span data-ttu-id="5613f-103">Recupero di dati dal computer locale</span><span class="sxs-lookup"><span data-stu-id="5613f-103">Obtaining Data from the Local Computer</span></span>

<span data-ttu-id="5613f-104">Sebbene Gestione remota Windows e il protocollo di WS-Management siano progettati in modo esplicito per la comunicazione remota, è il caso più semplice stabilire una sessione nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="5613f-104">Although Windows Remote Management and WS-Management protocol are explicitly designed for remote communication, establishing a session on the local computer is the simplest case.</span></span> <span data-ttu-id="5613f-105">È possibile che alcuni script richiedano l'accesso ai dati nel computer locale e nei computer remoti.</span><span class="sxs-lookup"><span data-stu-id="5613f-105">Some scripts may require access data on the local computer as well as remote computers.</span></span>

<span data-ttu-id="5613f-106">**WinRM versione 2,0:  **</span><span class="sxs-lookup"><span data-stu-id="5613f-106">**WinRM version 2.0:  **</span></span>

<span data-ttu-id="5613f-107">Tutte le operazioni sono considerate remote e il servizio gestione remota Windows deve essere avviato prima dell'esecuzione di qualsiasi operazione.</span><span class="sxs-lookup"><span data-stu-id="5613f-107">All operations are considered remote and the WinRM service must be started before any operation is performed.</span></span> <span data-ttu-id="5613f-108">Se non viene specificata una destinazione remota, il localhost viene usato per impostazione predefinita e tutte le operazioni verranno inviate al servizio gestione remota Windows locale.</span><span class="sxs-lookup"><span data-stu-id="5613f-108">If a remote destination is not specified, then the localhost is used by default, and all operations will be sent to the local WinRM service.</span></span> <span data-ttu-id="5613f-109">Per ulteriori informazioni sull'avvio del servizio gestione remota Windows, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="5613f-109">For more information about starting the WinRM service, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="5613f-110">Quando si utilizza il servizio gestione remota Windows per le operazioni locali, è necessario considerare i fattori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5613f-110">When using the WinRM service for local operations, the following factors should be considered:</span></span>

-   <span data-ttu-id="5613f-111">La configurazione locale di WinRM può essere letta solo dagli amministratori.</span><span class="sxs-lookup"><span data-stu-id="5613f-111">The local WinRM configuration can only be read by administrators.</span></span>
-   <span data-ttu-id="5613f-112">Per gli spazi dei nomi WMI è necessario impostare autorizzazioni Remote Enable.</span><span class="sxs-lookup"><span data-stu-id="5613f-112">WMI namespaces must have remote enable permissions set.</span></span> <span data-ttu-id="5613f-113">Per ulteriori informazioni, vedere [protezione di una connessione WMI remota](../wmisdk/securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5613f-113">For more information, see [Securing a Remote WMI Connection](../wmisdk/securing-a-remote-wmi-connection.md).</span></span>
-   <span data-ttu-id="5613f-114">Se non viene creato un [*listener*](windows-remote-management-glossary.md) WinRM, il servizio WinRM è in ascolto delle richieste locali sulla porta 47001.</span><span class="sxs-lookup"><span data-stu-id="5613f-114">If a WinRM [*listener*](windows-remote-management-glossary.md) is not created, then the WinRM service listens for local requests on port 47001.</span></span>

<span data-ttu-id="5613f-115">Ogni script WinRM deve iniziare stabilendo una sessione o una connessione a un computer creando un oggetto [**sessione**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="5613f-115">Every WinRM script must start by establishing a session or connection to a computer by creating a [**Session**](session.md) object.</span></span> <span data-ttu-id="5613f-116">Dopo aver creato la sessione, è possibile utilizzare i metodi dell'oggetto **sessione** , ad esempio [**Session. enumerate**](session-enumerate.md) o [**Session. Invoke**](session-invoke.md) , per ottenere i dati o per eseguire metodi.</span><span class="sxs-lookup"><span data-stu-id="5613f-116">After the session is created, you can use the **Session** object methods, such as [**Session.Enumerate**](session-enumerate.md) or [**Session.Invoke**](session-invoke.md) to obtain data or to execute methods.</span></span>

<span data-ttu-id="5613f-117">La creazione di una sessione è piuttosto simile alla [connessione](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) a uno spazio dei nomi di Strumentazione gestione Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page)).</span><span class="sxs-lookup"><span data-stu-id="5613f-117">The creation of a session is somewhat similar to [connecting](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) to a Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page)) namespace.</span></span> <span data-ttu-id="5613f-118">La sessione è essenzialmente un livello che consente di inviare e ricevere dati tramite messaggi [*SOAP*](windows-remote-management-glossary.md) e il protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="5613f-118">The session is essentially a layer that allows you to send and receive data through [*SOAP*](windows-remote-management-glossary.md) messages and the WS-Management protocol.</span></span> <span data-ttu-id="5613f-119">Per ulteriori informazioni, vedere [protocollo WS-Management](ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="5613f-119">For more information, see [WS-Management Protocol](ws-management-protocol.md).</span></span>

<span data-ttu-id="5613f-120">Chiamando il metodo [**WSMan. CreateSession**](wsman-createsession.md) per creare un oggetto [**sessione**](session.md) , viene avviata una [*sessione*](windows-remote-management-glossary.md) di che si connette alla gestione remota Windows locale.</span><span class="sxs-lookup"><span data-stu-id="5613f-120">Calling the [**WSMan.CreateSession**](wsman-createsession.md) method to create a [**Session**](session.md) object will start a [*session*](windows-remote-management-glossary.md) that connects to the local WinRM.</span></span>

<span data-ttu-id="5613f-121">**Per creare una sessione WSMan e ottenere i dati**</span><span class="sxs-lookup"><span data-stu-id="5613f-121">**To Create a WSMan Session and Obtain Data**</span></span>

1.  <span data-ttu-id="5613f-122">Creare un oggetto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="5613f-122">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="5613f-123">Creare una sessione chiamando il metodo [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="5613f-123">Create a session by calling the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="5613f-124">Questa sessione viene eseguita con il nome utente e la password di accesso e può ottenere dati tramite la gestione remota Windows locale.</span><span class="sxs-lookup"><span data-stu-id="5613f-124">This session runs under your logon username and password and can obtain data through the local WinRM.</span></span>

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  <span data-ttu-id="5613f-125">Creare un [*URI*](windows-remote-management-glossary.md) di risorsa per identificare la [*risorsa*](windows-remote-management-glossary.md) che si vuole gestire o per cui si desidera ottenere i dati.</span><span class="sxs-lookup"><span data-stu-id="5613f-125">Create a resource [*URI*](windows-remote-management-glossary.md) to identify the [*resource*](windows-remote-management-glossary.md) you want to manage or for which you want to obtain data.</span></span> <span data-ttu-id="5613f-126">Per altre informazioni sulla formattazione di un URI, vedere [URI di risorsa](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="5613f-126">For more information about formatting a URI, see [Resource URIs](resource-uris.md).</span></span> <span data-ttu-id="5613f-127">Questo URI di risorsa è relativo a un'istanza specifica della classe del [**\_ servizio WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) , il servizio Winmgmt.</span><span class="sxs-lookup"><span data-stu-id="5613f-127">This resource URI is for a specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the Winmgmt service.</span></span> <span data-ttu-id="5613f-128">Per ulteriori informazioni, vedere [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="5613f-128">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  <span data-ttu-id="5613f-129">Chiamare i metodi di [**sessione**](session.md) che ottengono o enumerano i dati usando l'URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5613f-129">Call [**Session**](session.md) methods that get or enumerate data using the resource URI.</span></span> <span data-ttu-id="5613f-130">Per ulteriori informazioni, vedere [API di scripting WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5613f-130">For more information, see [WinRM Scripting API](winrm-scripting-api.md).</span></span>

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  <span data-ttu-id="5613f-131">Per ottenere o gestire i dati da un altro computer o usare metodi di autenticazione diversi, vedere [recupero di dati da un computer remoto](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="5613f-131">To get or manage data from another computer or use different methods of authentication, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span>

<span data-ttu-id="5613f-132">Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo che consente di ottenere l'istanza specifica del [**\_ servizio WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) denominato "WinMgmt".</span><span class="sxs-lookup"><span data-stu-id="5613f-132">The following VBScript code example shows the complete script that obtains the specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) named "Winmgmt".</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



<span data-ttu-id="5613f-133">Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo con la trasformazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="5613f-133">The following VBScript code example shows the complete script with the data transform.</span></span> <span data-ttu-id="5613f-134">Per ulteriori informazioni, vedere [visualizzazione dell'output XML dagli script WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="5613f-134">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a><span data-ttu-id="5613f-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5613f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5613f-136">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="5613f-136">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="5613f-137">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="5613f-137">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="5613f-138">Riferimento Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="5613f-138">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 