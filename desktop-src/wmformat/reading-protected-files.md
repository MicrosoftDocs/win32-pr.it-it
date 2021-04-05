---
title: Lettura di file protetti
description: Lettura di file protetti
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media Format SDK, lettura di file protetti
- Windows Media Format SDK, file protetti
- ASF (Advanced Systems Format), lettura di file protetti
- ASF (Advanced Systems Format), lettura di file protetti
- ASF (Advanced Systems Format), file protetti
- ASF (Advanced Systems Format), file protetti
- Formato Advanced Systems (ASF), WMStubDRM. lib
- ASF (formato avanzato dei sistemi), WMStubDRM. lib
- WMStubDRM. lib, lettura di file protetti
- WMStubDRM. lib, file protetti
- Digital Rights Management (DRM), WMStubDRM. lib
- DRM (Digital Rights Management), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723407"
---
# <a name="reading-protected-files"></a><span data-ttu-id="a6dbf-115">Lettura di file protetti</span><span class="sxs-lookup"><span data-stu-id="a6dbf-115">Reading Protected Files</span></span>

<span data-ttu-id="a6dbf-116">La lettura di un file o di un flusso di rete protetto da DRM comporta fondamentalmente il tentativo di aprire il file (o connettersi al flusso) e quindi di gestire gli eventi che potrebbero essere inviati dai componenti di DRM.</span><span class="sxs-lookup"><span data-stu-id="a6dbf-116">Reading a DRM-protected file or network stream basically involves attempting to open the file (or connect to the stream) and then handling any events that might be sent from the DRM components.</span></span>

<span data-ttu-id="a6dbf-117">Se un lettore non è abilitato per il DRM (non si collega a una libreria WMStubDRM. lib valida), la chiamata [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) non riesce quando tenta di aprire un file protetto e restituisce \_ contenuto protetto da NS e \_ \_ o un errore correlato.</span><span class="sxs-lookup"><span data-stu-id="a6dbf-117">If a player is not DRM-enabled (does not link to a valid wmstubdrm.lib library) the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) call fails when it tries to open a protected file and returns NS\_E\_PROTECTED\_CONTENT or some related error.</span></span>

<span data-ttu-id="a6dbf-118">Quando un'applicazione abilitata per DRM tenta di aprire un file protetto da DRM, il componente DRM cerca automaticamente nel sistema locale una licenza valida.</span><span class="sxs-lookup"><span data-stu-id="a6dbf-118">When a DRM-enabled application attempts to open a DRM-protected file, the DRM component automatically searches the local system for a valid license.</span></span> <span data-ttu-id="a6dbf-119">Se ne viene individuato uno, il componente DRM decrittografa automaticamente il file in modo completamente trasparente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a6dbf-119">If one is found, the DRM component automatically decrypts the file in a way that is completely transparent to the application.</span></span> <span data-ttu-id="a6dbf-120">L'azione che un'applicazione può eseguire sul file decrittografato dipende dai diritti specificati nella licenza.</span><span class="sxs-lookup"><span data-stu-id="a6dbf-120">The action that an application may perform on the decrypted file depends on the rights specified in the license.</span></span> <span data-ttu-id="a6dbf-121">Per una descrizione completa dei diritti possibili, vedere la documentazione di Windows Media Rights Manager SDK.</span><span class="sxs-lookup"><span data-stu-id="a6dbf-121">For a full description of possible rights, see the Windows Media Rights Manager SDK documentation.</span></span>

<span data-ttu-id="a6dbf-122">Se l'applicazione non dispone di una licenza valida per un file, il lettore riceve una notifica di stato dal componente DRM.</span><span class="sxs-lookup"><span data-stu-id="a6dbf-122">If the application does not have a valid license for a file, the player receives a status notification from the DRM component.</span></span> <span data-ttu-id="a6dbf-123">L'applicazione Player può quindi avviare il processo di [*acquisizione delle licenze*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a6dbf-123">The player application can then initiate the [*license acquisition*](wmformat-glossary.md) process.</span></span> <span data-ttu-id="a6dbf-124">Dopo la ricezione di una licenza valida, è possibile accedere al file.</span><span class="sxs-lookup"><span data-stu-id="a6dbf-124">After a valid license has been received, the file can be accessed.</span></span> <span data-ttu-id="a6dbf-125">Nelle sezioni seguenti vengono descritte le attività di base che un'applicazione deve eseguire durante l'implementazione del processo di acquisizione della licenza:</span><span class="sxs-lookup"><span data-stu-id="a6dbf-125">The following sections describe the basic tasks that an application must perform in implementing the license acquisition process:</span></span>

-   [<span data-ttu-id="a6dbf-126">Specifica delle azioni da eseguire</span><span class="sxs-lookup"><span data-stu-id="a6dbf-126">Specifying the Actions To Be Performed</span></span>](specifying-the-actions-to-be-performed.md)
-   [<span data-ttu-id="a6dbf-127">Gestione degli eventi di acquisizione delle licenze</span><span class="sxs-lookup"><span data-stu-id="a6dbf-127">Handling License Acquisition Events</span></span>](handling-license-acquisition-events.md)
-   [<span data-ttu-id="a6dbf-128">Applicazioni DRM individualizzazione</span><span class="sxs-lookup"><span data-stu-id="a6dbf-128">Individualizing DRM Applications</span></span>](individualizing-drm-applications.md)
-   [<span data-ttu-id="a6dbf-129">Gestione degli eventi di individualizzazione</span><span class="sxs-lookup"><span data-stu-id="a6dbf-129">Handling Individualization Events</span></span>](handling-individualization-events.md)

> [!Note]  
> <span data-ttu-id="a6dbf-130">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="a6dbf-130">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a6dbf-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6dbf-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6dbf-132">**Funzionalità di Rights Management digitali**</span><span class="sxs-lookup"><span data-stu-id="a6dbf-132">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="a6dbf-133">**Elenco attributi DRM**</span><span class="sxs-lookup"><span data-stu-id="a6dbf-133">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="a6dbf-134">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="a6dbf-134">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="a6dbf-135">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="a6dbf-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




