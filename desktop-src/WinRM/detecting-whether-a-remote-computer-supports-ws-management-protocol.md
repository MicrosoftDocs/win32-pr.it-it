---
title: Rilevamento dell'eventuale supporto di WS-Management protocollo da un computer remoto
description: È possibile utilizzare i metodi Session. identifi o IWSManSession. identifi per determinare se il computer remoto dispone di un servizio che supporta il protocollo WS-Management.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298309"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a><span data-ttu-id="23be6-103">Rilevamento dell'eventuale supporto di WS-Management protocollo da un computer remoto</span><span class="sxs-lookup"><span data-stu-id="23be6-103">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>

<span data-ttu-id="23be6-104">È possibile utilizzare i metodi [**Session. identifi**](session-identify.md) o [**IWSManSession. identifi**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) per determinare se il computer remoto dispone di un servizio che supporta il protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="23be6-104">You can use the [**Session.Identify**](session-identify.md) or [**IWSManSession.Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) methods to determine if the remote computer has a service that supports the WS-Management protocol.</span></span>

<span data-ttu-id="23be6-105">Se nel computer remoto è configurato un servizio di WS-Management protocollo ed è in attesa di richieste, il servizio può rilevare una richiesta di identificazione in base al codice XML seguente nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="23be6-105">If a WS-Management protocol service is configured on the remote computer and is listening for requests, the service can detect an Identify request by the following XML in the header.</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



<span data-ttu-id="23be6-106">Il servizio del protocollo WS-Management che riceve la richiesta restituisce le informazioni contenute nell'elenco seguente nel corpo del messaggio:</span><span class="sxs-lookup"><span data-stu-id="23be6-106">The WS-Management protocol service that receives the request returns the information, contained in the following list, in the body of the message:</span></span>

-   <span data-ttu-id="23be6-107">Versione del protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="23be6-107">The WS-Management protocol version.</span></span> <span data-ttu-id="23be6-108">Ad esempio, "https://schemas.dmtf.org/wbem/wsman/1/wsman".</span><span class="sxs-lookup"><span data-stu-id="23be6-108">For example, "https://schemas.dmtf.org/wbem/wsman/1/wsman".</span></span>
-   <span data-ttu-id="23be6-109">Il fornitore del prodotto, ad esempio, "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="23be6-109">The product vendor, for example, "Microsoft Corporation".</span></span>
-   <span data-ttu-id="23be6-110">Versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="23be6-110">The product version.</span></span> <span data-ttu-id="23be6-111">Se la richiesta viene inviata con **WSManFlagUseNoAuthentication** nel parametro *Flags* , non vengono restituite informazioni sulla versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="23be6-111">If the request is sent with **WSManFlagUseNoAuthentication** in the *flags* parameter, then no product version information is returned.</span></span> <span data-ttu-id="23be6-112">Se la richiesta viene inviata con l'autenticazione predefinita attiva o con un'altra modalità di autenticazione specificata, è possibile che vengano restituite le informazioni sulla versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="23be6-112">If the request is sent with either the default authentication in effect or with another authentication mode specified, then the product version information can be returned.</span></span>

<span data-ttu-id="23be6-113">La richiesta di rilevare se il computer remoto dispone di un servizio di protocollo configurato e in ascolto WS-Management può essere eseguito all'inizio di uno script con altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="23be6-113">The request to detect whether the remote computer has a configured and listening WS-Management protocol service can be performed at the beginning of a script with other operations.</span></span> <span data-ttu-id="23be6-114">In questo modo si verificherà che il computer o i computer di destinazione possano rispondere a ulteriori WS-Management richieste di protocollo.</span><span class="sxs-lookup"><span data-stu-id="23be6-114">This will verify that the target computer or computers can respond to further WS-Management protocol requests.</span></span> <span data-ttu-id="23be6-115">La verifica può essere eseguita anche in uno script separato.</span><span class="sxs-lookup"><span data-stu-id="23be6-115">The verification also can be done in a separate script.</span></span>

<span data-ttu-id="23be6-116">**Per rilevare un servizio del protocollo di WS-Management**</span><span class="sxs-lookup"><span data-stu-id="23be6-116">**To detect a WS-Management protocol service**</span></span>

1.  <span data-ttu-id="23be6-117">Creare un oggetto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="23be6-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="23be6-118">Determinare se la richiesta deve essere inviata autenticata o non autenticata e impostare di conseguenza il parametro dei *flag* nella chiamata a [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="23be6-118">Determine whether the request should be sent authenticated or unauthenticated and set the *flags* parameter accordingly in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  <span data-ttu-id="23be6-119">Chiamare [**Session. identifi**](session-identify.md).</span><span class="sxs-lookup"><span data-stu-id="23be6-119">Call [**Session.Identify**](session-identify.md).</span></span>

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a><span data-ttu-id="23be6-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="23be6-120">Examples</span></span>

<span data-ttu-id="23be6-121">L'esempio di codice VBScript seguente invia una richiesta di identificazione non autenticata al computer remoto denominato "REMOTE1" nello stesso dominio.</span><span class="sxs-lookup"><span data-stu-id="23be6-121">The following VBScript code example sends an unauthenticated Identify request to the remote computer named "Remote1" in the same domain.</span></span>


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



<span data-ttu-id="23be6-122">Nella risposta seguente viene illustrato il codice XML restituito dal computer remoto.</span><span class="sxs-lookup"><span data-stu-id="23be6-122">The following response shows the XML returned by the remote computer.</span></span> <span data-ttu-id="23be6-123">La versione del protocollo WS-Management (" https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ") e il fornitore del sistema operativo ("Microsoft Corporation") vengono specificati nel codice XML restituito.</span><span class="sxs-lookup"><span data-stu-id="23be6-123">The WS-Management protocol version ("https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd") and the operating system vendor ("Microsoft Corporation") are specified in the returned XML.</span></span> <span data-ttu-id="23be6-124">Poiché il messaggio viene inviato senza autenticazione, la versione del prodotto non viene restituita dal servizio Gestione remota Windows.</span><span class="sxs-lookup"><span data-stu-id="23be6-124">Because the message is sent unauthenticated, the product version is not returned by the Windows Remote Management service.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



<span data-ttu-id="23be6-125">Nell'esempio di codice VBScript seguente viene inviata una richiesta di identificazione autenticata al computer remoto.</span><span class="sxs-lookup"><span data-stu-id="23be6-125">The following VBScript code example sends an authenticated Identify request to the remote computer.</span></span>


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



<span data-ttu-id="23be6-126">Poiché la richiesta è stata inviata con l'autenticazione, vengono restituite le informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="23be6-126">Because the request was sent with authentication, the version information is returned.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a><span data-ttu-id="23be6-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23be6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23be6-128">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="23be6-128">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="23be6-129">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="23be6-129">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="23be6-130">Riferimento Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="23be6-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




