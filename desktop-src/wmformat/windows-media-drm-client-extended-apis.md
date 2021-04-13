---
title: API estese del client Windows Media DRM
description: API estese del client Windows Media DRM
ms.assetid: c0397aa8-1f5a-48f5-a96b-555079e9a292
keywords:
- Windows Media Format SDK, API client DRM estese
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, API estese
- Windows Media Format SDK, API
- Windows Media Format SDK, Digital Rights Management (DRM)
- Digital Rights Management (DRM), API estese del client
- DRM (Digital Rights Management), API estese client
- Digital Rights Management (DRM), API estese
- DRM (Digital Rights Management), API estese
- Digital Rights Management (DRM), API
- DRM (Digital Rights Management), API
- API estese del client DRM, informazioni
- API estese client, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c33ef3649f2cda63713ebd22a0116fdd025144
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399104"
---
# <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="7c8dd-116">API estese del client Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="7c8dd-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="7c8dd-117">\[La funzionalità DRM di Windows Media è deprecata e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c8dd-117">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="7c8dd-118">In alternativa, usare [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="7c8dd-118">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="7c8dd-119">In questa documentazione vengono descritte le API (Application Programming Interface) del client Microsoft Windows Media Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="7c8dd-119">This documentation describes the Microsoft Windows Media Digital Rights Management (DRM) Client Extended Application Programming Interfaces (APIs).</span></span> <span data-ttu-id="7c8dd-120">Le API estese del client Windows Media DRM includono oggetti che possono essere usati per gestire le operazioni di Windows Media Digital Rights Management (DRM) in un computer client.</span><span class="sxs-lookup"><span data-stu-id="7c8dd-120">The Windows Media DRM Client Extended APIs include objects that can be used to manage Windows Media Digital Rights Management (DRM) operations on a client computer.</span></span>

<span data-ttu-id="7c8dd-121">L'obiettivo principale di queste API è la gestione delle licenze per i contenuti multimediali digitali protetti.</span><span class="sxs-lookup"><span data-stu-id="7c8dd-121">The primary focus of these APIs is the management of licenses for protected digital media content.</span></span> <span data-ttu-id="7c8dd-122">Inoltre, le API possono essere utilizzate per aggiornare i componenti di DRM nel computer client e per creare applicazioni che trasmettono contenuto mediante Windows Media DRM per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="7c8dd-122">In addition, the APIs can be used to update the DRM components on the client computer and to create applications that transmit content using Windows Media DRM for Network Devices.</span></span>

<span data-ttu-id="7c8dd-123">Queste API costituiscono la controparte lato client di Windows Media Rights Manager SDK.</span><span class="sxs-lookup"><span data-stu-id="7c8dd-123">These APIs constitute the client-side counterpart to the Windows Media Rights Manager SDK.</span></span> <span data-ttu-id="7c8dd-124">Dove Windows Media Rights Manager viene usato per creare Servizi online che proteggono i file e emettono licenze, le API estese del client Windows Media DRM vengono usate per creare applicazioni che utilizzano tale contenuto.</span><span class="sxs-lookup"><span data-stu-id="7c8dd-124">Where Windows Media Rights Manager is used to create online services that protect files and issue licenses, the Windows Media DRM Client Extended APIs are used to create applications that consume that content.</span></span>

<span data-ttu-id="7c8dd-125">Questo documento include le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7c8dd-125">This document includes the following sections.</span></span>



| <span data-ttu-id="7c8dd-126">Sezione</span><span class="sxs-lookup"><span data-stu-id="7c8dd-126">Section</span></span>                                                                                                  | <span data-ttu-id="7c8dd-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c8dd-127">Description</span></span>                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c8dd-128">Informazioni sulle API estese del client Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="7c8dd-128">About the Windows Media DRM Client Extended APIs</span></span>](about-the-windows-media-drm-client-extended-apis.md) | <span data-ttu-id="7c8dd-129">Vengono fornite informazioni generali e informazioni di base che è necessario conoscere prima di sviluppare applicazioni che utilizzano le API di.</span><span class="sxs-lookup"><span data-stu-id="7c8dd-129">Provides overview and background information that you should be familiar with before developing applications that use the APIs.</span></span>                                                        |
| [<span data-ttu-id="7c8dd-130">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="7c8dd-130">Programming Guide</span></span>](drm-programming-guide.md)                                                           | <span data-ttu-id="7c8dd-131">Vengono fornite istruzioni dettagliate per l'esecuzione di diverse operazioni DRM sul lato client.</span><span class="sxs-lookup"><span data-stu-id="7c8dd-131">Provides detailed instructions for performing various client-side DRM operations.</span></span>                                                                                                      |
| [<span data-ttu-id="7c8dd-132">Guida di riferimento alla programmazione</span><span class="sxs-lookup"><span data-stu-id="7c8dd-132">Programming Reference</span></span>](drm-programming-reference.md)                                                   | <span data-ttu-id="7c8dd-133">Fornisce informazioni di riferimento su interfacce, metodi, funzioni, strutture, tipi di enumerazione e costanti incluse nelle API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="7c8dd-133">Provides reference information about the interfaces, methods, functions, structures, enumeration types, and constants that are included in the Windows Media DRM Client Extended APIs.</span></span> |



 

 

 