---
title: Informazioni di riferimento su WMDM
description: Windows Media Device Manager SDK è costituito da una raccolta di interfacce, strutture, enumerazioni e costanti. Usare questi articoli di riferimento.
ms.assetid: 1d2260a8-bc9f-41b3-a3b0-0176b45fff1f
keywords:
- Gestione dispositivi Windows Media, informazioni di riferimento sulla programmazione
- Gestione dispositivi, informazioni di riferimento sulla programmazione
- Gestione dispositivi Windows Media, applicazioni desktop
- Gestione dispositivi, applicazioni desktop
- Gestione dispositivi Windows Media, provider di servizi
- Gestione dispositivi, provider di servizi
- applicazioni desktop, informazioni di riferimento sulla programmazione
- provider di servizi, informazioni di riferimento sulla programmazione
- informazioni di riferimento sulla programmazione, applicazioni desktop
- informazioni di riferimento sulla programmazione, provider di servizi
- informazioni di riferimento sulla programmazione, Gestione dispositivi Windows Media
- informazioni di riferimento su Gestione dispositivi Windows Media
- informazioni di riferimento per Gestione dispositivi Windows Media, applicazioni desktop
- informazioni di riferimento per Gestione dispositivi Windows Media, provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e624bbc445d5d5e376cad926248ae4ee4db17a6e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406524"
---
# <a name="wmdm-reference"></a><span data-ttu-id="f3538-118">Informazioni di riferimento su WMDM</span><span class="sxs-lookup"><span data-stu-id="f3538-118">WMDM reference</span></span>

<span data-ttu-id="f3538-119">Windows Media Device Manager SDK è costituito da una raccolta di interfacce, strutture, enumerazioni e costanti.</span><span class="sxs-lookup"><span data-stu-id="f3538-119">The Windows Media Device Manager SDK consists of a collection of interfaces, structures, enumerations, and constants.</span></span> <span data-ttu-id="f3538-120">La sezione di riferimento divide le interfacce in gruppi in base al tipo di oggetto che le usa.</span><span class="sxs-lookup"><span data-stu-id="f3538-120">The reference section divides the interfaces into groups according to the type of object that uses them.</span></span>



| <span data-ttu-id="f3538-121">Sezione</span><span class="sxs-lookup"><span data-stu-id="f3538-121">Section</span></span>                                                                                                    | <span data-ttu-id="f3538-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3538-122">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3538-123">Interfacce per le applicazioni</span><span class="sxs-lookup"><span data-stu-id="f3538-123">Interfaces for Applications</span></span>](interfaces-for-applications.md)                                             | <span data-ttu-id="f3538-124">Descrive le interfacce usate o implementate solo da applicazioni desktop, Windows Media Player plug-in o oggetti COM che necessitano di un accesso di alto livello a un dispositivo portatile.</span><span class="sxs-lookup"><span data-stu-id="f3538-124">Describes interfaces that are used or implemented only by desktop applications, Windows Media Player plug-ins, or COM objects that need high-level access to a portable device.</span></span>                     |
| [<span data-ttu-id="f3538-125">Interfacce per i provider di servizi</span><span class="sxs-lookup"><span data-stu-id="f3538-125">Interfaces for Service Providers</span></span>](interfaces-for-service-providers.md)                                   | <span data-ttu-id="f3538-126">Descrive le interfacce usate o implementate solo dai provider di servizi, che gestiscono la comunicazione effettiva di basso livello con un dispositivo portatile.</span><span class="sxs-lookup"><span data-stu-id="f3538-126">Describes interfaces that are used or implemented only by service providers, which handle the actual low-level communication with a portable device.</span></span>                                                |
| [<span data-ttu-id="f3538-127">Interfacce DRM-Implemented Windows Media</span><span class="sxs-lookup"><span data-stu-id="f3538-127">Windows Media DRM-Implemented Interfaces</span></span>](windows-media-drm-implemented-interfaces.md)                   | <span data-ttu-id="f3538-128">Descrive le interfacce che non devono essere implementate da provider di servizi di terze parti, ma che vengono implementate e chiamate internamente da Gestione dispositivi Windows Media e Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f3538-128">Describes interfaces that are not intended to be implemented by third-party service providers, but are implemented and called internally by the Windows Media DRM and Windows Media Device Manager.</span></span> |
| [<span data-ttu-id="f3538-129">Interfacce per provider di servizi e applicazioni</span><span class="sxs-lookup"><span data-stu-id="f3538-129">Interfaces for Service Providers and Applications</span></span>](interfaces-for-service-providers-and-applications.md) | <span data-ttu-id="f3538-130">Vengono descritte le interfacce che possono essere usate dalle applicazioni o dai provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="f3538-130">Describes interfaces that can be used either by applications or by service providers.</span></span>                                                                                                               |
| [<span data-ttu-id="f3538-131">Interfacce per provider di contenuti sicuri</span><span class="sxs-lookup"><span data-stu-id="f3538-131">Interfaces for Secure Content Providers</span></span>](interfaces-for-secure-content-providers.md)                     | <span data-ttu-id="f3538-132">Descrive le interfacce che devono essere implementate da un dispositivo o un'applicazione che userà contenuto protetto da DRM.</span><span class="sxs-lookup"><span data-stu-id="f3538-132">Describes interfaces that must be implemented by a device or application that will use DRM-protected content.</span></span>                                                                                       |
| [<span data-ttu-id="f3538-133">Strutture</span><span class="sxs-lookup"><span data-stu-id="f3538-133">Structures</span></span>](structures.md)                                                                               | <span data-ttu-id="f3538-134">Descrive le strutture usate per i metodi di Gestione dispositivi Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f3538-134">Describes structures used for Windows Media Device Manager methods.</span></span>                                                                                                                                 |
| [<span data-ttu-id="f3538-135">Tipi di enumerazione</span><span class="sxs-lookup"><span data-stu-id="f3538-135">Enumeration Types</span></span>](enumeration-types.md)                                                                 | <span data-ttu-id="f3538-136">Descrive le enumerazioni usate per i metodi di Gestione dispositivi Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f3538-136">Describes enumerations used for Windows Media Device Manager methods.</span></span>                                                                                                                               |
| [<span data-ttu-id="f3538-137">Costanti dei metadati</span><span class="sxs-lookup"><span data-stu-id="f3538-137">Metadata Constants</span></span>](metadata-constants.md)                                                               | <span data-ttu-id="f3538-138">Descrive le costanti definite da Windows Media Device Manager SDK per l'impostazione o il recupero di varie proprietà dei metadati per un dispositivo o un oggetto nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3538-138">Describes the constants defined by the Windows Media Device Manager SDK for setting or retrieving various metadata properties for a device or object on the device.</span></span>                                 |
| [<span data-ttu-id="f3538-139">Codici errore</span><span class="sxs-lookup"><span data-stu-id="f3538-139">Error Codes</span></span>](error-codes.md)                                                                             | <span data-ttu-id="f3538-140">Descrive i codici di errore che possono essere restituiti dai metodi sdk di Gestione dispositivi Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f3538-140">Describes the error codes that can be returned by Windows Media Device Manager SDK methods.</span></span>                                                                                                         |



 

 

 




