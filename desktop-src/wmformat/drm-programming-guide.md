---
title: Guida alla programmazione del client Microsoft Windows Media DRM
description: Guida alla programmazione del client Microsoft Windows Media DRM
ms.assetid: e7b179b3-ed14-4ea0-9a00-9d96557a2e2e
keywords:
- Windows Media Format SDK, API client DRM estese
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, API estese
- Windows Media Format SDK, API
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, guida per programmatori
- Digital Rights Management (DRM), API estese del client
- DRM (Digital Rights Management), API estese client
- Digital Rights Management (DRM), API estese
- DRM (Digital Rights Management), API estese
- Digital Rights Management (DRM), API
- DRM (Digital Rights Management), API
- Digital Rights Management (DRM), Guida alla programmazione
- DRM (Digital Rights Management), Guida alla programmazione
- API estese del client DRM, informazioni
- API estese client, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b338ea6ebd9cb132c8e6b1c76c8e1d7f6c6aa182
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474885"
---
# <a name="microsoft-windows-media-drm-client-programming-guide"></a><span data-ttu-id="13f99-119">Guida alla programmazione del client Microsoft Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="13f99-119">Microsoft Windows Media DRM Client Programming Guide</span></span>

<span data-ttu-id="13f99-120">Questa guida fornisce informazioni sull'uso delle funzionalità delle API estese del client Windows Media DRM nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="13f99-120">This guide provides information about using the features of the Windows Media DRM Client Extended APIs in your applications.</span></span> <span data-ttu-id="13f99-121">Le sezioni seguenti illustrano in dettaglio i passaggi necessari per implementare le funzionalità di DRM.</span><span class="sxs-lookup"><span data-stu-id="13f99-121">The following sections explain, in detail, the steps involved in implementing DRM features.</span></span>



| <span data-ttu-id="13f99-122">Sezione</span><span class="sxs-lookup"><span data-stu-id="13f99-122">Section</span></span>                                                                                                                          | <span data-ttu-id="13f99-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13f99-123">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13f99-124">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="13f99-124">Getting Started</span></span>](drm-getting-started.md)                                                                                       | <span data-ttu-id="13f99-125">Vengono fornite informazioni sulla configurazione di progetti C++ che utilizzano le API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="13f99-125">Provides information about setting up C++ projects that use the Windows Media DRM Client Extended APIs.</span></span>    |
| [<span data-ttu-id="13f99-126">Acquisizione di licenze</span><span class="sxs-lookup"><span data-stu-id="13f99-126">Acquiring Licenses</span></span>](acquiring-licenses.md)                                                                                     | <span data-ttu-id="13f99-127">Viene descritto come ottenere le licenze nel computer client.</span><span class="sxs-lookup"><span data-stu-id="13f99-127">Describes how to get licenses on the client computer.</span></span>                                                      |
| [<span data-ttu-id="13f99-128">Recupero di informazioni dalle licenze nell'archivio licenze locale</span><span class="sxs-lookup"><span data-stu-id="13f99-128">Getting Information from Licenses in the Local License Store</span></span>](getting-information-from-licenses-in-the-local-license-store.md) | <span data-ttu-id="13f99-129">Viene descritto come ottenere informazioni sui diritti per il contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="13f99-129">Describes how to get information about rights for protected content.</span></span>                                       |
| [<span data-ttu-id="13f99-130">Esecuzione dell'individualizzazione DRM</span><span class="sxs-lookup"><span data-stu-id="13f99-130">Performing DRM Individualization</span></span>](performing-drm-individualization.md)                                                         | <span data-ttu-id="13f99-131">Viene descritto come aggiornare e individuare il componente DRM nel computer client per renderlo più sicuro.</span><span class="sxs-lookup"><span data-stu-id="13f99-131">Describes how to update and individualize the DRM component on the client computer to make it more secure.</span></span> |
| [<span data-ttu-id="13f99-132">Esportazione DRM</span><span class="sxs-lookup"><span data-stu-id="13f99-132">DRM Export</span></span>](drm-export.md)                                                                                                     | <span data-ttu-id="13f99-133">Viene descritto come esportare contenuti protetti da Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="13f99-133">Describes how to export content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="13f99-134">Importazione DRM</span><span class="sxs-lookup"><span data-stu-id="13f99-134">DRM Import</span></span>](drm-import.md)                                                                                                     | <span data-ttu-id="13f99-135">Viene descritto come importare contenuti protetti da Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="13f99-135">Describes how to import content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="13f99-136">Revoca delle licenze</span><span class="sxs-lookup"><span data-stu-id="13f99-136">License Revocation</span></span>](drm-license-revocation.md)                                                                                 | <span data-ttu-id="13f99-137">Viene descritto come rimuovere le licenze dall'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="13f99-137">Describes how to remove licenses from the local license store.</span></span>                                             |
| [<span data-ttu-id="13f99-138">Revoca e rinnovo automatici dei componenti</span><span class="sxs-lookup"><span data-stu-id="13f99-138">Automated Component Revocation and Renewal</span></span>](automated-component-revocation-and-renewal.md)                                     | <span data-ttu-id="13f99-139">Descrive il sistema di revoca e rinnovo automatico di DRM di Windows Media usando gli abilitatori del contenuto.</span><span class="sxs-lookup"><span data-stu-id="13f99-139">Describes the Windows Media DRM automated revocation and renewal system using content enablers.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="13f99-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13f99-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13f99-141">**API estese del client Windows Media DRM**</span><span class="sxs-lookup"><span data-stu-id="13f99-141">**Windows Media DRM Client Extended APIs**</span></span>](windows-media-drm-client-extended-apis.md)
</dt> <dt>

<span data-ttu-id="13f99-142">[Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="13f99-142">[Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10))</span></span>
</dt> </dl>

 

 
