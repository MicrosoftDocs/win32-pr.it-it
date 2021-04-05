---
title: Visualizzazione degli attributi dei file protetti
description: Visualizzazione degli attributi dei file protetti
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows Media Format SDK, visualizzazione degli attributi dei file protetti
- Windows Media Format SDK, attributi dei file protetti
- Windows Media Format SDK, file protetti
- Formato di sistemi avanzati (ASF), visualizzazione degli attributi dei file protetti
- ASF (Advanced Systems Format), visualizzazione degli attributi dei file protetti
- ASF (Advanced Systems Format), attributi dei file protetti
- ASF (Advanced Systems Format), attributi dei file protetti
- ASF (Advanced Systems Format), file protetti
- ASF (Advanced Systems Format), file protetti
- Digital Rights Management (DRM), visualizzazione degli attributi dei file protetti
- DRM (Digital Rights Management), visualizzazione degli attributi dei file protetti
- Digital Rights Management (DRM), attributi dei file protetti
- DRM (Digital Rights Management), attributi dei file protetti
- Digital Rights Management (DRM), file protetti
- DRM (Digital Rights Management), file protetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723398"
---
# <a name="viewing-attributes-of-protected-files"></a><span data-ttu-id="1f8a1-118">Visualizzazione degli attributi dei file protetti</span><span class="sxs-lookup"><span data-stu-id="1f8a1-118">Viewing Attributes of Protected Files</span></span>

<span data-ttu-id="1f8a1-119">In alcuni scenari potrebbe essere necessario recuperare determinati attributi DRM in un file senza accedere effettivamente al contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-119">In some scenarios, you may need to retrieve certain DRM attributes in a file without actually accessing the contents of the file.</span></span> <span data-ttu-id="1f8a1-120">Questa funzionalità è utile, ad esempio, nelle applicazioni che elaborano batch di file in modi diversi in base alle informazioni contenute nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-120">This capability is useful, for example, in applications that process batches of files in different ways based on information in the file header.</span></span> <span data-ttu-id="1f8a1-121">Nelle versioni precedenti di Windows Media Format SDK, le applicazioni erano necessarie per il collegamento alla libreria statica DRM per poter aprire qualsiasi file protetto.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-121">In previous versions of the Windows Media Format SDK, applications were required to link to the DRM static library in order to open any protected file.</span></span> <span data-ttu-id="1f8a1-122">Le applicazioni che non hanno la libreria DRM possono usare l'interfaccia [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) nell'oggetto editor dei metadati per esaminare alcuni attributi DRM.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-122">Applications that do not have the DRM library can use the [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) interface on the metadata editor object to examine certain DRM attributes.</span></span>

> [!Note]  
> <span data-ttu-id="1f8a1-123">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1f8a1-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f8a1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f8a1-125">**Elenco attributi DRM**</span><span class="sxs-lookup"><span data-stu-id="1f8a1-125">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="1f8a1-126">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="1f8a1-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="1f8a1-127">**Interfaccia IWMDRMEditor**</span><span class="sxs-lookup"><span data-stu-id="1f8a1-127">**IWMDRMEditor Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




