---
title: Implementazione della revoca delle licenze
description: Implementazione della revoca delle licenze
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- Windows Media Format SDK, implementazione della revoca delle licenze
- Windows Media Format SDK, revoca delle licenze
- Windows Media Format SDK, revoca delle licenze
- ASF (Advanced Systems Format), implementazione della revoca delle licenze
- ASF (Advanced Systems Format), implementazione della revoca delle licenze
- ASF (Advanced Systems Format), revoca delle licenze
- ASF (formato avanzato dei sistemi), revoca delle licenze
- ASF (Advanced Systems Format), revoca delle licenze
- ASF (formato avanzato dei sistemi), revoca delle licenze
- Digital Rights Management (DRM), implementazione della revoca delle licenze
- DRM (Digital Rights Management), implementazione della revoca delle licenze
- Digital Rights Management (DRM), revoca delle licenze
- DRM (Digital Rights Management), revoca delle licenze
- Digital Rights Management (DRM), revoca delle licenze
- DRM (Digital Rights Management), revoca delle licenze
- revoca delle licenze, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83bfb1a512b031f5b7c297ecede4ed33fba8f2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723567"
---
# <a name="implementing-license-revocation"></a><span data-ttu-id="376b1-119">Implementazione della revoca delle licenze</span><span class="sxs-lookup"><span data-stu-id="376b1-119">Implementing License Revocation</span></span>

<span data-ttu-id="376b1-120">Windows Media Rights Manager 10 SDK include una funzionalità denominata revoca delle licenze.</span><span class="sxs-lookup"><span data-stu-id="376b1-120">The Windows Media Rights Manager 10 SDK includes a feature called license revocation.</span></span> <span data-ttu-id="376b1-121">Questa funzionalità consente ai server licenze di richiedere la rimozione delle licenze dal computer client.</span><span class="sxs-lookup"><span data-stu-id="376b1-121">This feature enables license servers to request that licenses be removed from the client computer.</span></span> <span data-ttu-id="376b1-122">Windows Media Format SDK fornisce metodi che elaborano i messaggi di revoca e rimuovono le licenze dall'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="376b1-122">The Windows Media Format SDK provides methods that process revocation messages and remove the licenses from the local license store.</span></span>

<span data-ttu-id="376b1-123">Il processo di revoca della licenza viene avviato da un servizio fornito dall'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="376b1-123">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="376b1-124">L'applicazione può ospitare questo servizio o può essere un'applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="376b1-124">Your application can host this service, or it can be a Web application.</span></span> <span data-ttu-id="376b1-125">In entrambi i casi, l'applicazione deve essere in grado di ricevere una richiesta di licenza creata dal servizio.</span><span class="sxs-lookup"><span data-stu-id="376b1-125">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="376b1-126">Per rimuovere le licenze dall'archivio licenze, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="376b1-126">To remove licenses from the license store, perform the following steps:</span></span>

1.  <span data-ttu-id="376b1-127">Quando si riceve una richiesta di licenza dall'autorità emittente della licenza, chiamare la funzione [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) per creare un oggetto agente di revoca delle licenze e ottenere un puntatore all'interfaccia [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .</span><span class="sxs-lookup"><span data-stu-id="376b1-127">Upon receiving a license challenge from the license issuer, call the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function to create a license revocation agent object and obtain a pointer to the [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span>
2.  <span data-ttu-id="376b1-128">Chiamare il metodo [**IWMLicenseRevocationAgent:: GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) per generare la risposta alla richiesta di verifica.</span><span class="sxs-lookup"><span data-stu-id="376b1-128">Call the [**IWMLicenseRevocationAgent::GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) method to generate the challenge response.</span></span>
3.  <span data-ttu-id="376b1-129">Inviare la risposta alla richiesta di verifica al componente del servizio licenze dal quale è stata ricevuta la richiesta di verifica.</span><span class="sxs-lookup"><span data-stu-id="376b1-129">Send the challenge response back to the license service component from which you received the challenge.</span></span>
4.  <span data-ttu-id="376b1-130">Il componente del servizio licenze invia un BLOB di revoche di licenze firmato (LRB) all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="376b1-130">The license service component sends a signed license revocation blob (LRB) to your application.</span></span> <span data-ttu-id="376b1-131">Quando viene ricevuta, chiamare il metodo [**IWMLicenseRevocationAgent::P rocesslrb**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) .</span><span class="sxs-lookup"><span data-stu-id="376b1-131">When you receive it, call the [**IWMLicenseRevocationAgent::ProcessLRB**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) method.</span></span> <span data-ttu-id="376b1-132">**ProcessLRB** crea un messaggio di riconoscimento che è necessario restituire al servizio licenze per verificare che le licenze siano state rimosse.</span><span class="sxs-lookup"><span data-stu-id="376b1-132">**ProcessLRB** creates an acknowledgement message that you must send back to the license service to verify that the licenses were removed.</span></span>

> [!Note]  
> <span data-ttu-id="376b1-133">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="376b1-133">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="376b1-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="376b1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="376b1-135">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="376b1-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="376b1-136">**Interfaccia IWMLicenseRevocationAgent**</span><span class="sxs-lookup"><span data-stu-id="376b1-136">**IWMLicenseRevocationAgent Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




