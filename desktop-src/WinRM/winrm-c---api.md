---
title: API WinRM C++
description: Le interfacce Gestione remota Windows possono essere utilizzate per ottenere i dati o gestire le risorse in un computer remoto. Questa API è destinata principalmente all'uso interno. Quando possibile, è consigliabile usare l'API della shell client WinRM.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7cff2334d9839936d15f7258a70ce03f9751e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955628"
---
# <a name="winrm-c-api"></a><span data-ttu-id="e26ee-105">API WinRM C++</span><span class="sxs-lookup"><span data-stu-id="e26ee-105">WinRM C++ API</span></span>

<span data-ttu-id="e26ee-106">Le interfacce Gestione remota Windows possono essere utilizzate per ottenere i dati o gestire [*le risorse*](windows-remote-management-glossary.md) in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="e26ee-106">The Windows Remote Management interfaces can be used to obtain data or manage [*resources*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="e26ee-107">Questa API è destinata principalmente all'uso interno.</span><span class="sxs-lookup"><span data-stu-id="e26ee-107">This API is intended primarily for internal use.</span></span> <span data-ttu-id="e26ee-108">Quando possibile, è consigliabile usare l' [API della shell client WinRM](client-shell-api.md) .</span><span class="sxs-lookup"><span data-stu-id="e26ee-108">We recommend using the [WinRM Client Shell API](client-shell-api.md) instead whenever possible.</span></span> <span data-ttu-id="e26ee-109">Le interfacce corrispondono strettamente all' [API di scripting WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e26ee-109">The interfaces closely correspond to the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="e26ee-110">Le interfacce WinRM che ereditano direttamente da **IDispatch** hanno un oggetto di scripting corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e26ee-110">The WinRM interfaces that inherit directly from **IDispatch** each have a corresponding scripting object.</span></span> <span data-ttu-id="e26ee-111">Per ulteriori informazioni, vedere l' [API di scripting WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e26ee-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="e26ee-112">Per le applicazioni multithread, WinRM non supporta thread distinti che accedono allo stesso oggetto [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) .</span><span class="sxs-lookup"><span data-stu-id="e26ee-112">For multithreaded applications, WinRM does not support separate threads accessing the same [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) object.</span></span>

<span data-ttu-id="e26ee-113">Le interfacce seguenti sono fornite da WinRM.</span><span class="sxs-lookup"><span data-stu-id="e26ee-113">The following interfaces are provided by WinRM.</span></span>

<dl> <dt>

<span data-ttu-id="e26ee-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="e26ee-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="e26ee-115">Fornisce metodi e proprietà utilizzati per creare una nuova sessione e gestire una sessione stabilita.</span><span class="sxs-lookup"><span data-stu-id="e26ee-115">Provides methods and properties used to create a new session and manage an established session.</span></span> <span data-ttu-id="e26ee-116">[**WSMan**](wsman.md) è l'oggetto di scripting corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e26ee-116">[**WSMan**](wsman.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="e26ee-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="e26ee-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="e26ee-118">Fornisce metodi e proprietà utilizzati per creare un nuovo [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span><span class="sxs-lookup"><span data-stu-id="e26ee-118">Provides methods and properties used to create a new [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span> <span data-ttu-id="e26ee-119">Questo metodo è disponibile per l'oggetto di scripting [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="e26ee-119">This method is available for the [**WSMan**](wsman.md) scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="e26ee-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span><span class="sxs-lookup"><span data-stu-id="e26ee-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span></span>
</dt> <dd>

<span data-ttu-id="e26ee-121">Definisce il nome utente e la password utilizzati per le connessioni remote.</span><span class="sxs-lookup"><span data-stu-id="e26ee-121">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="e26ee-122">[**ConnectionOptions**](connectionoptions.md) è l'oggetto di scripting corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e26ee-122">[**ConnectionOptions**](connectionoptions.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="e26ee-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="e26ee-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span></span>
</dt> <dd>

<span data-ttu-id="e26ee-124">Definisce le operazioni di rete e le proprietà disponibili per la sessione.</span><span class="sxs-lookup"><span data-stu-id="e26ee-124">Defines the network operations and properties available for the session.</span></span> <span data-ttu-id="e26ee-125">[**Session**](session.md) è l'oggetto di scripting corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e26ee-125">[**Session**](session.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="e26ee-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span><span class="sxs-lookup"><span data-stu-id="e26ee-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span></span>
</dt> <dd>

<span data-ttu-id="e26ee-127">Rappresenta una raccolta di risultati restituiti dall'enumerazione di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="e26ee-127">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="e26ee-128">[**Enumerator**](enumerator.md) è l'oggetto di scripting corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e26ee-128">[**Enumerator**](enumerator.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="e26ee-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="e26ee-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span></span>
</dt> <dd>

<span data-ttu-id="e26ee-130">Fornisce il percorso di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="e26ee-130">Supplies the path to a resource.</span></span> <span data-ttu-id="e26ee-131">È possibile usare un oggetto [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) anziché un [*URI di risorsa*](windows-remote-management-glossary.md) nelle operazioni dell'oggetto [**Session**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="e26ee-131">You can use an [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="e26ee-132">[**ResourceLocator**](resourcelocator.md) è l'oggetto di scripting corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e26ee-132">[**ResourceLocator**](resourcelocator.md) is the corresponding scripting object.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="e26ee-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e26ee-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e26ee-134">Riferimento Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="e26ee-134">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




