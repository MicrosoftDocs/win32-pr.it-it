---
title: Creazione di una licenza XMR
description: Creazione di una licenza XMR
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows Media Format SDK, importazione DRM
- Windows Media Format SDK, importazione
- Windows Media Format SDK, licenze XMR
- Windows Media Format SDK, licenze
- Windows Media Format SDK, diritti multimediali estendibili (XMR)
- Digital Rights Management (DRM), importazione
- DRM (Digital Rights Management), importazione
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), licenze XMR
- DRM (Digital Rights Management), licenze XMR
- Digital Rights Management (DRM), diritti multimediali estendibili (XMR)
- DRM (Digital Rights Management), diritti multimediali estendibili (XMR)
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, licenze XMR
- API estese client, licenze XMR
- API estese del client DRM, licenze
- API estese client, licenze
- API estese del client DRM, diritti multimediali estendibili (XMR)
- API estese client, diritti multimediali estendibili (XMR)
- licenze, XMR
- Diritti multimediali estendibili (XMR)
- XMR (diritti multimediali estendibili)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc275419116362c08cabe4dc70aa227687705fdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395323"
---
# <a name="building-an-xmr-license"></a><span data-ttu-id="0a187-127">Creazione di una licenza XMR</span><span class="sxs-lookup"><span data-stu-id="0a187-127">Building an XMR License</span></span>

<span data-ttu-id="0a187-128">Per generare una licenza per Windows Media DRM da elaborare, è necessario utilizzare lo schema binario XMR (Extensible Media Rights).</span><span class="sxs-lookup"><span data-stu-id="0a187-128">To generate a license for Windows Media DRM to process, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="0a187-129">XMR è uno schema per la trasmissione dei diritti e delle restrizioni di utilizzo dei supporti e deve essere concesso in licenza separatamente.</span><span class="sxs-lookup"><span data-stu-id="0a187-129">XMR is a schema for conveying media usage rights and restrictions and needs to be licensed separately.</span></span>

<span data-ttu-id="0a187-130">Il materiale importante in una licenza viene crittografato con la chiave pubblica nella raccolta di certificati DRM di Windows Media, quindi è visibile solo al sottosistema API client Windows Media DRM esteso.</span><span class="sxs-lookup"><span data-stu-id="0a187-130">The important material in a license is encrypted using the public key in the Windows Media DRM certificate collection, so it is visible only to the Windows Media DRM Client Extended API subsystem.</span></span> <span data-ttu-id="0a187-131">.</span><span class="sxs-lookup"><span data-stu-id="0a187-131">.</span></span>

<span data-ttu-id="0a187-132">È responsabilità dell'utente assicurarsi che le impostazioni relative alla struttura e ai criteri di licenza siano valide e coerenti con l'intento dell'emittente di licenze e che siano conformi alle regole di conformità.</span><span class="sxs-lookup"><span data-stu-id="0a187-132">It is your responsibility to ensure that the license structure and policy settings are valid and consistent with the license issuer's intent, and that they conform to the compliance rules.</span></span>

<span data-ttu-id="0a187-133">È necessario leggere le regole di conformità dell'importazione DRM di Windows Media per apprendere il set completo di oggetti XMR che devono essere presenti nella licenza.</span><span class="sxs-lookup"><span data-stu-id="0a187-133">You should read the Windows Media DRM import compliance rules to learn the complete set of XMR objects that must be present in the license.</span></span>

<span data-ttu-id="0a187-134">Per passare la licenza XMR al sottosistema DRM, chiamare il metodo [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="0a187-134">To pass the XMR license to the DRM subsystem, call the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span> <span data-ttu-id="0a187-135">Usare il formato seguente per passare la licenza nel parametro *bstrLicenseResponse* :</span><span class="sxs-lookup"><span data-stu-id="0a187-135">Use the following format to pass the license in the *bstrLicenseResponse* parameter:</span></span>


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



<span data-ttu-id="0a187-136">Questa stringa deve essere in formato Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="0a187-136">This string must be in Unicode format (UTF-16).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a187-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a187-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a187-138">**Importazione DRM**</span><span class="sxs-lookup"><span data-stu-id="0a187-138">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




