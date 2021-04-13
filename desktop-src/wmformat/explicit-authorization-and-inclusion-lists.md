---
title: Elenchi di inclusione e autorizzazione esplicita
description: Elenchi di inclusione e autorizzazione esplicita
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows Media Format SDK, esportazione DRM
- Windows Media Format SDK, esportazione
- Windows Media Format SDK, elenco di autorizzazioni esplicite e di inclusione
- Windows Media Format SDK, elenchi di autorizzazione
- Windows Media Format SDK, elenchi di inclusione
- Digital Rights Management (DRM), esportazione
- DRM (Digital Rights Management), esportazione
- Digital Rights Management (DRM), esplicito autorizzazione e inclusione elenchi
- DRM (Digital Rights Management), autorizzazione esplicita e elenchi di inclusione
- Digital Rights Management (DRM), elenchi di autorizzazioni
- DRM (Digital Rights Management), elenchi di autorizzazioni
- Digital Rights Management (DRM), elenchi di inclusione
- DRM (Digital Rights Management), elenchi di inclusione
- API estese del client DRM, elenchi di autorizzazioni esplicite e di inclusione
- API estese client, elenco di autorizzazioni esplicite e di inclusione
- API estese del client DRM, elenchi di autorizzazioni
- API estese client, elenchi di autorizzazioni
- API estese del client DRM, elenchi di inclusione
- API estese client, elenchi di inclusione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2309bed28ffd3add2a75c1cd90488b9ef454659b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398558"
---
# <a name="explicit-authorization-and-inclusion-lists"></a><span data-ttu-id="847fd-122">Elenchi di inclusione e autorizzazione esplicita</span><span class="sxs-lookup"><span data-stu-id="847fd-122">Explicit Authorization and Inclusion Lists</span></span>

<span data-ttu-id="847fd-123">Le licenze possono contenere un elenco di inclusione per autorizzare in modo esplicito l'esportazione di contenuto protetto da DRM di Windows Media ad altri schemi di protezione del contenuto (CPS).</span><span class="sxs-lookup"><span data-stu-id="847fd-123">Licenses can contain an inclusion list to explicitly authorize the exporting of content protected by Windows Media DRM to other content protection schemes (CPS).</span></span> <span data-ttu-id="847fd-124">In base ai termini del contratto di licenza stipulato con Microsoft per abilitare l'esportazione DRM, è possibile esportare solo in un CPS valido identificato nell'elenco di inclusione di una licenza.</span><span class="sxs-lookup"><span data-stu-id="847fd-124">As per the terms of the license agreement you enter into with Microsoft to enable DRM Export you can export only to a valid CPS that is identified in the inclusion list of a license.</span></span>

<span data-ttu-id="847fd-125">Un elenco di inclusione è una matrice limitata di identificatori univoci globali (GUID) che ognuno rappresenta un CPS autorizzato specifico in cui il contenuto può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="847fd-125">An inclusion list is a bounded array of globally unique identifiers (GUIDs) that each represents a specific authorized CPS to which the content can be exported.</span></span> <span data-ttu-id="847fd-126">I GUID elencati in un elenco di inclusione sono indipendenti dai livelli di protezione dell'output (OPL) e dai livelli di protezione del contenuto (CPL).</span><span class="sxs-lookup"><span data-stu-id="847fd-126">The GUIDs listed in an inclusion list are independent of the output protection levels (OPL) and content protection levels (CPL).</span></span> <span data-ttu-id="847fd-127">Applicare queste restrizioni è responsabilità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="847fd-127">Enforcing these restrictions is the responsibility of your application.</span></span>

> [!Note]  
> <span data-ttu-id="847fd-128">Quando si esegue l'esportazione DRM di Windows Media sui contenuti compressi, è possibile accedere all'elenco di inclusione tramite il metodo [**IWMDRMLicense:: Getinclusivion**](iwmdrmlicense-getinclusionlist.md) .</span><span class="sxs-lookup"><span data-stu-id="847fd-128">When performing Windows Media DRM Export on compressed content, you access the inclusion list through the [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) method.</span></span> <span data-ttu-id="847fd-129">Quando si esegue l'esportazione DRM di Windows Media su contenuto non compresso, usare il metodo [**IWMDRMReader3:: Getinclusive**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) .</span><span class="sxs-lookup"><span data-stu-id="847fd-129">When performing Windows Media DRM Export on uncompressed content, use the [**IWMDRMReader3::GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) method.</span></span>

 

<span data-ttu-id="847fd-130">Per registrare un nuovo sistema di protezione del contenuto come Windows Media DRM Export consentito nelle regole di conformità per l'esportazione di Windows Media DRM, contattare wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="847fd-130">To register a new content protection system as a Windows Media DRM Permitted Export in the Windows Media DRM export compliance rules, please contact wmla@microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="847fd-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="847fd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="847fd-132">**Esportazione DRM**</span><span class="sxs-lookup"><span data-stu-id="847fd-132">**DRM Export**</span></span>](drm-export.md)
</dt> </dl>

 

 




