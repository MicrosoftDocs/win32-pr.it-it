---
title: Riferimento a WMDM
description: Guida di riferimento alla programmazione
ms.assetid: 1d2260a8-bc9f-41b3-a3b0-0176b45fff1f
keywords:
- Windows Media Gestione dispositivi, riferimento per la programmazione
- Gestione dispositivi, riferimento per la programmazione
- Windows Media Gestione dispositivi, applicazioni desktop
- Gestione dispositivi, applicazioni desktop
- Windows Media Gestione dispositivi, provider di servizi
- Gestione dispositivi, provider di servizi
- applicazioni desktop, riferimenti per la programmazione
- provider di servizi, riferimento per la programmazione
- Guida di riferimento alla programmazione, applicazioni desktop
- Guida di riferimento alla programmazione, provider di servizi
- Guida di riferimento alla programmazione, Windows Media Gestione dispositivi
- informazioni di riferimento su Windows Media Gestione dispositivi, informazioni
- informazioni di riferimento su Windows Media Gestione dispositivi, applicazioni desktop
- informazioni di riferimento su Windows Media Gestione dispositivi, provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1498d42e65de99abc1d32895f3628d93502c70f
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104398330"
---
# <a name="wmdm-reference"></a><span data-ttu-id="d0da7-117">Riferimento a WMDM</span><span class="sxs-lookup"><span data-stu-id="d0da7-117">WMDM reference</span></span>

<span data-ttu-id="d0da7-118">Windows Media Gestione dispositivi SDK è costituito da una raccolta di interfacce, strutture, enumerazioni e costanti.</span><span class="sxs-lookup"><span data-stu-id="d0da7-118">The Windows Media Device Manager SDK consists of a collection of interfaces, structures, enumerations, and constants.</span></span> <span data-ttu-id="d0da7-119">La sezione di riferimento divide le interfacce in gruppi in base al tipo di oggetto che li utilizza.</span><span class="sxs-lookup"><span data-stu-id="d0da7-119">The reference section divides the interfaces into groups according to the type of object that uses them.</span></span>



| <span data-ttu-id="d0da7-120">Sezione</span><span class="sxs-lookup"><span data-stu-id="d0da7-120">Section</span></span>                                                                                                    | <span data-ttu-id="d0da7-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0da7-121">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0da7-122">Interfacce per le applicazioni</span><span class="sxs-lookup"><span data-stu-id="d0da7-122">Interfaces for Applications</span></span>](interfaces-for-applications.md)                                             | <span data-ttu-id="d0da7-123">Vengono descritte le interfacce utilizzate o implementate solo da applicazioni desktop, plug-in di Windows Media Player o oggetti COM che richiedono l'accesso di alto livello a un dispositivo portatile.</span><span class="sxs-lookup"><span data-stu-id="d0da7-123">Describes interfaces that are used or implemented only by desktop applications, Windows Media Player plug-ins, or COM objects that need high-level access to a portable device.</span></span>                     |
| [<span data-ttu-id="d0da7-124">Interfacce per i provider di servizi</span><span class="sxs-lookup"><span data-stu-id="d0da7-124">Interfaces for Service Providers</span></span>](interfaces-for-service-providers.md)                                   | <span data-ttu-id="d0da7-125">Descrive le interfacce utilizzate o implementate solo dai provider di servizi, che gestiscono la comunicazione effettiva di basso livello con un dispositivo portatile.</span><span class="sxs-lookup"><span data-stu-id="d0da7-125">Describes interfaces that are used or implemented only by service providers, which handle the actual low-level communication with a portable device.</span></span>                                                |
| [<span data-ttu-id="d0da7-126">Interfacce DRM-Implemented Windows Media</span><span class="sxs-lookup"><span data-stu-id="d0da7-126">Windows Media DRM-Implemented Interfaces</span></span>](windows-media-drm-implemented-interfaces.md)                   | <span data-ttu-id="d0da7-127">Descrive le interfacce che non sono progettate per essere implementate da provider di servizi di terze parti, ma che vengono implementate e chiamate internamente da Windows Media DRM e Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d0da7-127">Describes interfaces that are not intended to be implemented by third-party service providers, but are implemented and called internally by the Windows Media DRM and Windows Media Device Manager.</span></span> |
| [<span data-ttu-id="d0da7-128">Interfacce per provider di servizi e applicazioni</span><span class="sxs-lookup"><span data-stu-id="d0da7-128">Interfaces for Service Providers and Applications</span></span>](interfaces-for-service-providers-and-applications.md) | <span data-ttu-id="d0da7-129">Descrive le interfacce che possono essere utilizzate dalle applicazioni o dai provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="d0da7-129">Describes interfaces that can be used either by applications or by service providers.</span></span>                                                                                                               |
| [<span data-ttu-id="d0da7-130">Interfacce per i provider di contenuti sicuri</span><span class="sxs-lookup"><span data-stu-id="d0da7-130">Interfaces for Secure Content Providers</span></span>](interfaces-for-secure-content-providers.md)                     | <span data-ttu-id="d0da7-131">Descrive le interfacce che devono essere implementate da un dispositivo o un'applicazione che utilizzerà contenuto protetto da DRM.</span><span class="sxs-lookup"><span data-stu-id="d0da7-131">Describes interfaces that must be implemented by a device or application that will use DRM-protected content.</span></span>                                                                                       |
| [<span data-ttu-id="d0da7-132">Strutture</span><span class="sxs-lookup"><span data-stu-id="d0da7-132">Structures</span></span>](structures.md)                                                                               | <span data-ttu-id="d0da7-133">Descrive le strutture utilizzate per i metodi Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d0da7-133">Describes structures used for Windows Media Device Manager methods.</span></span>                                                                                                                                 |
| [<span data-ttu-id="d0da7-134">Tipi di enumerazione</span><span class="sxs-lookup"><span data-stu-id="d0da7-134">Enumeration Types</span></span>](enumeration-types.md)                                                                 | <span data-ttu-id="d0da7-135">Descrive le enumerazioni utilizzate per i metodi Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d0da7-135">Describes enumerations used for Windows Media Device Manager methods.</span></span>                                                                                                                               |
| [<span data-ttu-id="d0da7-136">Costanti dei metadati</span><span class="sxs-lookup"><span data-stu-id="d0da7-136">Metadata Constants</span></span>](metadata-constants.md)                                                               | <span data-ttu-id="d0da7-137">Descrive le costanti definite da Windows Media Gestione dispositivi SDK per l'impostazione o il recupero di varie proprietà dei metadati per un dispositivo o un oggetto nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0da7-137">Describes the constants defined by the Windows Media Device Manager SDK for setting or retrieving various metadata properties for a device or object on the device.</span></span>                                 |
| [<span data-ttu-id="d0da7-138">Codici errore</span><span class="sxs-lookup"><span data-stu-id="d0da7-138">Error Codes</span></span>](error-codes.md)                                                                             | <span data-ttu-id="d0da7-139">Vengono descritti i codici di errore che possono essere restituiti dai metodi Windows Media Gestione dispositivi SDK.</span><span class="sxs-lookup"><span data-stu-id="d0da7-139">Describes the error codes that can be returned by Windows Media Device Manager SDK methods.</span></span>                                                                                                         |



 

 

 




