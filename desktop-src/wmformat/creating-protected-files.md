---
title: Creazione di file protetti
description: Creazione di file protetti
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows Media Format SDK, creazione di file protetti
- Windows Media Format SDK, file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- ASF (Advanced Systems Format), file protetti
- ASF (Advanced Systems Format), file protetti
- Formato Advanced Systems (ASF), WMStubDRM. lib
- ASF (formato avanzato dei sistemi), WMStubDRM. lib
- WMStubDRM. lib, creazione di file protetti
- WMStubDRM. lib, file protetti
- Digital Rights Management (DRM), WMStubDRM. lib
- DRM (Digital Rights Management), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a14d96da924bdb2a307bc804514a1ec3de083
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336313"
---
# <a name="creating-protected-files"></a><span data-ttu-id="51e7d-115">Creazione di file protetti</span><span class="sxs-lookup"><span data-stu-id="51e7d-115">Creating Protected Files</span></span>

<span data-ttu-id="51e7d-116">Per creare file multimediali digitali protetti usando DRM versione 1 o DRM 7 e versioni successive, eseguire il collegamento al file WMStubDRM. lib ottenuto da Microsoft e creare l'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="51e7d-116">To create protected digital media files using either DRM version 1 or DRM versions 7 and later, link to the WMStubDRM.lib file that you obtained from Microsoft, and create the writer object.</span></span> <span data-ttu-id="51e7d-117">Per la protezione della versione 1, utilizzare l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) per impostare gli attributi DRM che si desidera applicare.</span><span class="sxs-lookup"><span data-stu-id="51e7d-117">For version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface to set the DRM attributes you want to apply.</span></span> <span data-ttu-id="51e7d-118">Per le versioni 7 e successive, usare i metodi di interfaccia [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) .</span><span class="sxs-lookup"><span data-stu-id="51e7d-118">For versions 7 and later, use the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface methods.</span></span>

<span data-ttu-id="51e7d-119">Negli argomenti seguenti viene descritto in dettaglio come proteggere i file.</span><span class="sxs-lookup"><span data-stu-id="51e7d-119">The following topics describe in detail how to protect files.</span></span>

-   [<span data-ttu-id="51e7d-120">Protezione dei file con DRM versione 1</span><span class="sxs-lookup"><span data-stu-id="51e7d-120">Protecting Files with DRM Version 1</span></span>](protecting-files-with-drm-version-1.md)
-   [<span data-ttu-id="51e7d-121">Protezione dei file con DRM 7 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="51e7d-121">Protecting Files with DRM Version 7 or Later</span></span>](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> <span data-ttu-id="51e7d-122">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="51e7d-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="51e7d-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51e7d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51e7d-124">**Elenco attributi DRM**</span><span class="sxs-lookup"><span data-stu-id="51e7d-124">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="51e7d-125">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="51e7d-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="51e7d-126">**Versioni DRM**</span><span class="sxs-lookup"><span data-stu-id="51e7d-126">**DRM Versions**</span></span>](drm-versions.md)
</dt> <dt>

[<span data-ttu-id="51e7d-127">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="51e7d-127">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="51e7d-128">**Ottenere la libreria DRM necessaria**</span><span class="sxs-lookup"><span data-stu-id="51e7d-128">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> <dt>

[<span data-ttu-id="51e7d-129">**Lettura di file protetti**</span><span class="sxs-lookup"><span data-stu-id="51e7d-129">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




