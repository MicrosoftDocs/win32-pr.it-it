---
title: Panoramica di Windows Media DRM
description: Panoramica di Windows Media DRM
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- Digital Rights Management (DRM), informazioni
- DRM (Digital Rights Management), informazioni
- Digital Rights Management (DRM), creazione di pacchetti di file Windows Media
- DRM (Digital Rights Management), creazione di pacchetti di file Windows Media
- Digital Rights Management (DRM), licenze file protette
- DRM (Digital Rights Management), licenze file protette
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), lettura di file protetti
- DRM (Digital Rights Management), lettura di file protetti
- ASF (Advanced Systems Format), Digital Rights Management (DRM)
- ASF (formato avanzato dei sistemi), Digital Rights Management (DRM)
- licenze, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297835"
---
# <a name="overview-of-windows-media-drm"></a><span data-ttu-id="d4f5c-119">Panoramica di Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="d4f5c-119">Overview of Windows Media DRM</span></span>

<span data-ttu-id="d4f5c-120">Windows Media Digital Rights Management (DRM) è un sistema per la protezione del contenuto nei file di Windows Media, in modo che gli utenti non autorizzati non possano accedervi.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-120">Windows Media Digital Rights Management (DRM) is a system for protecting the content in Windows Media files so that unauthorized users cannot access it.</span></span> <span data-ttu-id="d4f5c-121">Il ciclo DRM di base prevede tre fasi: creazione di pacchetti, licenze e lettura.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-121">There are three phases to the basic DRM cycle: packaging, licensing, and reading.</span></span>

## <a name="packaging-windows-media-files"></a><span data-ttu-id="d4f5c-122">Creazione di pacchetti di file Windows Media</span><span class="sxs-lookup"><span data-stu-id="d4f5c-122">Packaging Windows Media Files</span></span>

<span data-ttu-id="d4f5c-123">Windows Media DRM è progettato per funzionare con i file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-123">Windows Media DRM is designed to work with Windows Media files.</span></span> <span data-ttu-id="d4f5c-124">Un file di Windows Media è un file che è conforme alla specifica ASF (Advanced Systems Format) e contiene solo audio e video compressi con i codec Windows Media Audio e video.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-124">A Windows Media file is a file that conforms to the Advanced Systems Format (ASF) specification and only contains Audio and Video that has been compressed by using the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="d4f5c-125">Quando si crea un pacchetto di un file ASF, all'intestazione viene aggiunta una sezione specifica di DRM.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-125">When an ASF file is packaged, a DRM-specific section is added to the header.</span></span> <span data-ttu-id="d4f5c-126">L'intestazione DRM contiene un ID chiave, che identifica il contenuto a scopo di gestione delle licenze e un URL di acquisizione della licenza, ovvero l'indirizzo di una pagina Web che può emettere licenze per la lettura del contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-126">The DRM header contains a Key ID, which identifies the content for the purposes of licensing, and a license acquisition URL, which is the address of a Web page that can issue licenses to read the protected content.</span></span> <span data-ttu-id="d4f5c-127">Sono disponibili molte altre informazioni che possono essere inserite nell'intestazione DRM, ma è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-127">There is much more information that can be put in the DRM header, but it is optional.</span></span> <span data-ttu-id="d4f5c-128">L'intestazione DRM è firmata in modo che sia possibile verificare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-128">The DRM header is signed so that the packager can be verified.</span></span>

<span data-ttu-id="d4f5c-129">Il contenuto del file ASF viene crittografato durante il processo di compressione.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-129">The content in the ASF file is encrypted during the packing process.</span></span> <span data-ttu-id="d4f5c-130">Tuttavia, le informazioni riportate di seguito nel file in pacchetto sono disponibili anche per i client che non dispongono di una licenza:</span><span class="sxs-lookup"><span data-stu-id="d4f5c-130">However, the following information in the packaged file is available even to clients that do not have a license:</span></span>

-   <span data-ttu-id="d4f5c-131">Metadati archiviati nell'intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-131">Metadata that is stored in the ASF header.</span></span>
-   <span data-ttu-id="d4f5c-132">Alcuni metadati archiviati nell'intestazione DRM (ad esempio, è sempre possibile ottenere l'URL di acquisizione della licenza).</span><span class="sxs-lookup"><span data-stu-id="d4f5c-132">Some metadata that is stored in the DRM header (for example, you can always get the license acquisition URL).</span></span>

## <a name="licensing-protected-files"></a><span data-ttu-id="d4f5c-133">File protetti con licenza</span><span class="sxs-lookup"><span data-stu-id="d4f5c-133">Licensing Protected Files</span></span>

<span data-ttu-id="d4f5c-134">Per la lettura di un file in pacchetto, è necessario emettere una licenza per il computer client.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-134">For a packaged file to be read, a license must be issued to the client computer.</span></span> <span data-ttu-id="d4f5c-135">Una licenza è un set di dati che descrive le condizioni in base alle quali è possibile leggere i dati nei file protetti.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-135">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="d4f5c-136">In genere, viene emessa una licenza per un file protetto in risposta all'utente che tenta di eseguire un'operazione sul file.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-136">Most often, a license is issued for a protected file in response to the user trying to perform some operation on the file.</span></span> <span data-ttu-id="d4f5c-137">È anche possibile, tuttavia, che un emittente di licenze fornisca licenze a un client prima che venga richiesto in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-137">It is also possible, however, for a license issuer to deliver licenses to a client before it is explicitly requested.</span></span> <span data-ttu-id="d4f5c-138">Per ulteriori informazioni sulle licenze, vedere [licenze](licenses.md).</span><span class="sxs-lookup"><span data-stu-id="d4f5c-138">For more information about licenses, see [Licenses](licenses.md).</span></span>

## <a name="reading-data-from-protected-files"></a><span data-ttu-id="d4f5c-139">Lettura di dati da file protetti</span><span class="sxs-lookup"><span data-stu-id="d4f5c-139">Reading Data from Protected Files</span></span>

<span data-ttu-id="d4f5c-140">Quando un utente tenta di eseguire un'operazione su un file protetto (riproduzione, masterizzazione su CD, copia in un dispositivo e così via), l'applicazione deve verificare la presenza di licenze per il contenuto nel computer client.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-140">When a user tries to perform an operation on a protected file (play, burn to CD, copy to a device, and so on), the application must check for licenses for the content on the client computer.</span></span> <span data-ttu-id="d4f5c-141">Se nel computer client è presente una licenza valida, l'operazione può proseguire.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-141">If a valid license exists on the client computer, the operation can proceed.</span></span> <span data-ttu-id="d4f5c-142">Se non è disponibile una licenza per il contenuto o se nessuna licenza per il contenuto presente nel computer client consente l'azione richiesta, è necessario acquisire una licenza.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-142">If there isn't a license for the content, or if no license for the content that is on the client computer allows the requested action, then a license must be acquired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4f5c-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d4f5c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4f5c-144">**Informazioni sulle API estese del client Windows Media DRM**</span><span class="sxs-lookup"><span data-stu-id="d4f5c-144">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




