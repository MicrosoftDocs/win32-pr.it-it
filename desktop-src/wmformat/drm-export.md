---
title: Esportazione DRM
description: Esportazione DRM
ms.assetid: 0b44f2e5-e63c-4bdb-8123-097a5d5e3756
keywords:
- Windows Media Format SDK, API client DRM estese
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, API estese
- Windows Media Format SDK, API
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, esportazione DRM
- Windows Media Format SDK, esportazione
- Digital Rights Management (DRM), API estese del client
- DRM (Digital Rights Management), API estese client
- Digital Rights Management (DRM), API estese
- DRM (Digital Rights Management), API estese
- Digital Rights Management (DRM), API
- DRM (Digital Rights Management), API
- Digital Rights Management (DRM), esportazione
- DRM (Digital Rights Management), esportazione
- API estese del client DRM, esportazione
- API estese client, esportazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2917cfd0c9042f4547540618b44ed4c2f324edb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330263"
---
# <a name="drm-export"></a><span data-ttu-id="b42db-120">Esportazione DRM</span><span class="sxs-lookup"><span data-stu-id="b42db-120">DRM Export</span></span>

<span data-ttu-id="b42db-121">La funzionalità di esportazione DRM di Windows Media consente di creare applicazioni con licenza che decrittografano il contenuto protetto da DRM di Windows Media e di eseguire nuovamente la crittografia in uno schema di protezione del contenuto (CPS) di output specificato in modo esplicito dall'emittente di licenze associato.</span><span class="sxs-lookup"><span data-stu-id="b42db-121">Windows Media DRM export functionality enables you to create licensed applications that decrypt content protected by Windows Media DRM, and re-encrypt in an output content protection scheme (CPS) explicitly specified by the associated license issuer.</span></span> <span data-ttu-id="b42db-122">L'autorità emittente di licenze autorizza in modo esplicito l'esportazione del contenuto a un determinato CPS tramite un elenco di inclusione.</span><span class="sxs-lookup"><span data-stu-id="b42db-122">The license issuer explicitly authorizes the export of content to a specific CPS through an inclusion list.</span></span>

> [!Note]  
> <span data-ttu-id="b42db-123">Per accedere alla funzionalità di esportazione, è necessario richiedere un [certificato di esportazione dell'applicazione](export-application-certificate.md) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b42db-123">To access export functionality, you must apply for an [Export Application Certificate](export-application-certificate.md) from Microsoft.</span></span>

 

<span data-ttu-id="b42db-124">La funzionalità di esportazione di Windows Media DRM è illustrata nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b42db-124">Windows Media DRM export functionality is explained in the following sections.</span></span>



| <span data-ttu-id="b42db-125">Sezione</span><span class="sxs-lookup"><span data-stu-id="b42db-125">Section</span></span>                                                                                      | <span data-ttu-id="b42db-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b42db-126">Description</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b42db-127">Esportare il certificato dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b42db-127">Export Application Certificate</span></span>](export-application-certificate.md)                         | <span data-ttu-id="b42db-128">Descrive un certificato dell'applicazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="b42db-128">Describes an export application certificate.</span></span>                                                        |
| [<span data-ttu-id="b42db-129">Elenchi di inclusione e autorizzazione esplicita</span><span class="sxs-lookup"><span data-stu-id="b42db-129">Explicit Authorization and Inclusion Lists</span></span>](explicit-authorization-and-inclusion-lists.md) | <span data-ttu-id="b42db-130">Viene illustrato il processo di autorizzazione esplicita e il funzionamento degli elenchi di inclusione.</span><span class="sxs-lookup"><span data-stu-id="b42db-130">Explains the process of explicit authorization, and how inclusions lists work.</span></span>                      |
| [<span data-ttu-id="b42db-131">Esportazione di contenuto compresso</span><span class="sxs-lookup"><span data-stu-id="b42db-131">Exporting Compressed Content</span></span>](exporting-compressed-content.md)                             | <span data-ttu-id="b42db-132">Viene descritto come esportare contenuto compresso da contenuti audio o video protetti da DRM di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b42db-132">Describes how to export compressed content from Windows Media DRM protected audio or video content.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b42db-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b42db-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b42db-134">**Elenchi di inclusione e autorizzazione esplicita**</span><span class="sxs-lookup"><span data-stu-id="b42db-134">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="b42db-135">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="b42db-135">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




