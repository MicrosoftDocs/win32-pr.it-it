---
title: Importazione DRM
description: Importazione DRM
ms.assetid: 5e67a721-830b-4d99-9f90-4cb2d7c61104
keywords:
- Windows Media Format SDK, API client DRM estese
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, API estese
- Windows Media Format SDK, API
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, importazione DRM
- Windows Media Format SDK, importazione
- Windows Media Format SDK, sistema di protezione del contenuto (CPS)
- Digital Rights Management (DRM), API estese del client
- DRM (Digital Rights Management), API estese client
- Digital Rights Management (DRM), API estese
- DRM (Digital Rights Management), API estese
- Digital Rights Management (DRM), API
- DRM (Digital Rights Management), API
- Digital Rights Management (DRM), importazione
- DRM (Digital Rights Management), importazione
- Digital Rights Management (DRM), sistema di protezione del contenuto (CPS)
- DRM (Digital Rights Management), sistema di protezione del contenuto (CPS)
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, sistema di protezione del contenuto (CPS)
- API estese client, sistema di protezione del contenuto (CPS)
- sistema di protezione del contenuto (CPS)
- CPS (sistema di protezione del contenuto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fc20cfd682df975c10a8f39785c0e8d69610d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711128"
---
# <a name="drm-import"></a><span data-ttu-id="0208b-127">Importazione DRM</span><span class="sxs-lookup"><span data-stu-id="0208b-127">DRM Import</span></span>

<span data-ttu-id="0208b-128">Le sezioni seguenti illustrano come convertire il contenuto multimediale da un sistema di protezione del contenuto di terze parti (CPS) a Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="0208b-128">The following sections explain how to convert media content from a third-party content protection system (CPS) to Windows Media DRM.</span></span> <span data-ttu-id="0208b-129">Questo processo è noto come importazione DRM ed è costituito essenzialmente dai passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0208b-129">This process is known as DRM Import and consists essentially of the following steps:</span></span>

1.  <span data-ttu-id="0208b-130">Creazione del file ASF.</span><span class="sxs-lookup"><span data-stu-id="0208b-130">Creating the ASF file.</span></span>
2.  <span data-ttu-id="0208b-131">Creazione della licenza.</span><span class="sxs-lookup"><span data-stu-id="0208b-131">Creating the license.</span></span>
3.  <span data-ttu-id="0208b-132">Facoltativamente, eliminare la licenza.</span><span class="sxs-lookup"><span data-stu-id="0208b-132">Optionally deleting the license.</span></span>

<span data-ttu-id="0208b-133">L'importazione DRM è illustrata nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="0208b-133">DRM Import is explained in the following sections.</span></span>



| <span data-ttu-id="0208b-134">Sezione</span><span class="sxs-lookup"><span data-stu-id="0208b-134">Section</span></span>                                                                              | <span data-ttu-id="0208b-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0208b-135">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0208b-136">Importazione del materiale della licenza e della chiave</span><span class="sxs-lookup"><span data-stu-id="0208b-136">Importing License and Key Material</span></span>](importing-license-and-key-material.md)         | <span data-ttu-id="0208b-137">Viene descritto come rilasciare le licenze in locale e importarle in Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="0208b-137">Describes how to issue licenses locally and import them into Windows Media DRM.</span></span>      |
| [<span data-ttu-id="0208b-138">Verifica della revoca dei certificati</span><span class="sxs-lookup"><span data-stu-id="0208b-138">Checking Certificate Revocation</span></span>](checking-certificate-revocation.md)               | <span data-ttu-id="0208b-139">Viene descritto come controllare la revoca dei certificati.</span><span class="sxs-lookup"><span data-stu-id="0208b-139">Describes how to check certificate revocation.</span></span>                                       |
| [<span data-ttu-id="0208b-140">Creazione di una licenza XMR</span><span class="sxs-lookup"><span data-stu-id="0208b-140">Building an XMR License</span></span>](building-an-xmr-license.md)                               | <span data-ttu-id="0208b-141">Viene descritto come creare una licenza XMR e passarla al sottosistema DRM.</span><span class="sxs-lookup"><span data-stu-id="0208b-141">Describes how to create an XMR license and pass it to the DRM subsystem.</span></span>             |
| [<span data-ttu-id="0208b-142">Creazione e inizializzazione di un writer DRM</span><span class="sxs-lookup"><span data-stu-id="0208b-142">Creating and Initializing a DRM Writer</span></span>](creating-and-initializing-a-drm-writer.md) | <span data-ttu-id="0208b-143">Viene descritto come inizializzare un oggetto writer ASF per preparare l'importazione DRM.</span><span class="sxs-lookup"><span data-stu-id="0208b-143">Describes how to initialize an ASF writer object to prepare for DRM Import.</span></span>          |
| [<span data-ttu-id="0208b-144">Crittografia e importazione di esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="0208b-144">Encrypting and Importing Media Samples</span></span>](encrypting-and-importing-media-samples.md) | <span data-ttu-id="0208b-145">Viene descritto come crittografare e importare singoli esempi di supporti in Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="0208b-145">Describes how to encrypt and import individual media samples into Windows Media DRM.</span></span> |
| [<span data-ttu-id="0208b-146">Eliminazione della licenza</span><span class="sxs-lookup"><span data-stu-id="0208b-146">License Deletion</span></span>](license-deletion.md)                                             | <span data-ttu-id="0208b-147">Viene descritto come eliminare le licenze create localmente.</span><span class="sxs-lookup"><span data-stu-id="0208b-147">Describes how to delete locally created licenses.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="0208b-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0208b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0208b-149">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="0208b-149">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




