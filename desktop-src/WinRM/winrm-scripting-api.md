---
title: API di scripting WinRM
description: Gestione remota Windows gli oggetti di scripting sono implementati come livello superiore al protocollo di WS-Management.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7910213487f525b74c3d1a8819a450f95336aba1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298613"
---
# <a name="winrm-scripting-api"></a><span data-ttu-id="54eef-103">API di scripting WinRM</span><span class="sxs-lookup"><span data-stu-id="54eef-103">WinRM Scripting API</span></span>

<span data-ttu-id="54eef-104">Gestione remota Windows gli oggetti di scripting sono implementati come livello superiore al [protocollo WS-Management](ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="54eef-104">Windows Remote Management scripting objects are implemented as a layer above the [WS-Management Protocol](ws-management-protocol.md).</span></span> <span data-ttu-id="54eef-105">Gli oggetti di scripting consentono di ottenere dati o gestire [*risorse*](windows-remote-management-glossary.md) in computer locali e remoti.</span><span class="sxs-lookup"><span data-stu-id="54eef-105">The scripting objects enable you to obtain data or manage [*resources*](windows-remote-management-glossary.md) on local and remote computers.</span></span>

## <a name="ws-management-objects"></a><span data-ttu-id="54eef-106">Oggetti WS-Management</span><span class="sxs-lookup"><span data-stu-id="54eef-106">WS-Management Objects</span></span>

<span data-ttu-id="54eef-107">Ogni oggetto di scripting dispone di un'interfaccia C++ corrispondente.</span><span class="sxs-lookup"><span data-stu-id="54eef-107">Each scripting object has a corresponding C++ interface.</span></span> <span data-ttu-id="54eef-108">Per ulteriori informazioni, vedere l' [API C++ WinRM](winrm-c---api.md) e [scripting in gestione remota Windows](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="54eef-108">For more information, see [WinRM C++ API](winrm-c---api.md) and [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="54eef-109">Gli oggetti seguenti vengono forniti dall'API di scripting di WinRM.</span><span class="sxs-lookup"><span data-stu-id="54eef-109">The following objects are provided by the WinRM Scripting API.</span></span>

<dl> <dt>

<span data-ttu-id="54eef-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span><span class="sxs-lookup"><span data-stu-id="54eef-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span></span>
</dt> <dd>

<span data-ttu-id="54eef-111">Definisce il nome utente e la password utilizzati per le connessioni remote.</span><span class="sxs-lookup"><span data-stu-id="54eef-111">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="54eef-112">Il nome utente e la password vengono passati quando si chiama il metodo [**CreateConnectionOptions**](wsman-createconnectionoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="54eef-112">The user name and password are passed when calling the [**CreateConnectionOptions**](wsman-createconnectionoptions.md) method.</span></span> <span data-ttu-id="54eef-113">Per ulteriori informazioni, vedere [recupero di dati da un computer remoto](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="54eef-113">For more information, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span> <span data-ttu-id="54eef-114">L'interfaccia C++ corrispondente è [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span><span class="sxs-lookup"><span data-stu-id="54eef-114">The corresponding C++ interface is [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span></span>

</dd> <dt>

<span data-ttu-id="54eef-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumeratore**](enumerator.md)</span><span class="sxs-lookup"><span data-stu-id="54eef-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumerator**](enumerator.md)</span></span>
</dt> <dd>

<span data-ttu-id="54eef-116">Rappresenta una raccolta di risultati restituiti dall'enumerazione di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="54eef-116">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="54eef-117">Per altre informazioni, vedere [enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="54eef-117">For more information, see [Enumerating or Listing All the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span> <span data-ttu-id="54eef-118">L'interfaccia C++ corrispondente è [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span><span class="sxs-lookup"><span data-stu-id="54eef-118">The corresponding C++ interface is [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="54eef-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span><span class="sxs-lookup"><span data-stu-id="54eef-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span></span>
</dt> <dd>

<span data-ttu-id="54eef-120">Fornisce il percorso di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="54eef-120">Supplies the path to a resource.</span></span> <span data-ttu-id="54eef-121">È possibile usare un oggetto [**resourceLocator**](resourcelocator.md) anziché un [*URI di risorsa*](windows-remote-management-glossary.md) nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="54eef-121">You can use a [**ResourceLocator**](resourcelocator.md) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations, such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="54eef-122">L'interfaccia C++ corrispondente è [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span><span class="sxs-lookup"><span data-stu-id="54eef-122">The corresponding C++ interface is [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span>

</dd> <dt>

<span data-ttu-id="54eef-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Sessione**](session.md)</span><span class="sxs-lookup"><span data-stu-id="54eef-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Session**](session.md)</span></span>
</dt> <dd>

<span data-ttu-id="54eef-124">Definisce le operazioni di rete e le proprietà disponibili per la sessione, ad esempio [**Session. Get**](session-get.md), [**Session. enumerate**](session-enumerate.md), [**Session. Invoke**](session-invoke.md).</span><span class="sxs-lookup"><span data-stu-id="54eef-124">Defines the network operations and properties available for the session, such as [**Session.Get**](session-get.md), [**Session.Enumerate**](session-enumerate.md), [**Session.Invoke**](session-invoke.md).</span></span> <span data-ttu-id="54eef-125">Per ulteriori informazioni, vedere [recupero di dati dal computer locale](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="54eef-125">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span> <span data-ttu-id="54eef-126">L'interfaccia C++ corrispondente è [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span><span class="sxs-lookup"><span data-stu-id="54eef-126">The corresponding C++ interface is [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span></span>

</dd> <dt>

<span data-ttu-id="54eef-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span><span class="sxs-lookup"><span data-stu-id="54eef-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span></span>
</dt> <dd>

<span data-ttu-id="54eef-128">Fornisce metodi e proprietà utilizzati per creare una nuova sessione o gestire una sessione stabilita.</span><span class="sxs-lookup"><span data-stu-id="54eef-128">Provides methods and properties used to create a new session or manage an established session.</span></span> <span data-ttu-id="54eef-129">Per ulteriori informazioni, vedere [utilizzo di gestione remota Windows](using-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="54eef-129">For more information see, [Using Windows Remote Management](using-windows-remote-management.md).</span></span> <span data-ttu-id="54eef-130">Le interfacce C++ corrispondenti sono [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) e [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span><span class="sxs-lookup"><span data-stu-id="54eef-130">The corresponding C++ interfaces are [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="54eef-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54eef-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54eef-132">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="54eef-132">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="54eef-133">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="54eef-133">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="54eef-134">Creazione di script in Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="54eef-134">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="54eef-135">Riferimento Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="54eef-135">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




