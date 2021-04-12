---
title: Importazione del materiale della licenza e della chiave
description: Importazione del materiale della licenza e della chiave
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows Media Format SDK, importazione DRM
- Windows Media Format SDK, importazione
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), importazione
- DRM (Digital Rights Management), importazione
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), materiale della chiave
- DRM (Digital Rights Management), materiale della chiave
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, licenze
- API estese client, licenze
- API estese del client DRM, materiale della chiave
- API estese client, materiale della chiave
- licenze, importazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221975"
---
# <a name="importing-license-and-key-material"></a><span data-ttu-id="6d236-119">Importazione del materiale della licenza e della chiave</span><span class="sxs-lookup"><span data-stu-id="6d236-119">Importing License and Key Material</span></span>

<span data-ttu-id="6d236-120">Se si dispone di contenuto multimediale crittografato utilizzando un sistema di protezione del contenuto di terze parti e si desidera importare il materiale della licenza e della chiave in Windows Media DRM, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="6d236-120">If you have media content that was encrypted using a third-party content protection system and you want to import the license and key material into Windows Media DRM, follow these steps:</span></span>

1.  <span data-ttu-id="6d236-121">Recuperare la raccolta di certificati del computer Windows Media DRM chiamando il metodo [**IWMDRMSecurity:: GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="6d236-121">Retrieve the Windows Media DRM machine certificate collection by calling the [**IWMDRMSecurity::GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) method.</span></span>
2.  <span data-ttu-id="6d236-122">Analizzare la raccolta di certificati, assicurandosi che sia firmato correttamente e che venga convalidato con una chiave pubblica radice Microsoft nota.</span><span class="sxs-lookup"><span data-stu-id="6d236-122">Parse the certificate collection, ensuring that it is signed correctly and is validated to a known Microsoft root public key.</span></span> <span data-ttu-id="6d236-123">La raccolta di certificati è conforme allo schema XMR.</span><span class="sxs-lookup"><span data-stu-id="6d236-123">The certificate collection conforms to the XMR schema.</span></span> <span data-ttu-id="6d236-124">Per ulteriori informazioni, vedere la pagina relativa alla [compilazione di una licenza XMR](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="6d236-124">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>
3.  <span data-ttu-id="6d236-125">Facoltativo: estrarre l'elenco di revoche chiamando il metodo [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="6d236-125">Optional: Extract the revocation list by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
4.  <span data-ttu-id="6d236-126">Facoltativo: assicurarsi che non sia stato revocato alcun certificato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6d236-126">Optional: Insure that no certificate in the collection is revoked.</span></span> <span data-ttu-id="6d236-127">Per ulteriori informazioni, vedere [controllo della revoca del certificato](checking-certificate-revocation.md).</span><span class="sxs-lookup"><span data-stu-id="6d236-127">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
5.  <span data-ttu-id="6d236-128">Generare una licenza nel formato XMR che rappresenta i requisiti dei criteri per il contenuto di importazione e contiene il materiale della chiave DRM di Windows Media appropriato.</span><span class="sxs-lookup"><span data-stu-id="6d236-128">Generate a license in the XMR format that represents the policy requirements for the import content and contains the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="6d236-129">Per ulteriori informazioni, vedere l'argomento [compilazione di una licenza XMR](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="6d236-129">For more information, see the topic [Building an XMR License](building-an-xmr-license.md).</span></span>
6.  <span data-ttu-id="6d236-130">Passare la licenza XMR al sistema Windows Media DRM per l'elaborazione, usando il metodo [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="6d236-130">Pass the XMR license to the Windows Media DRM system for processing, by using the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="6d236-131">Informazioni dettagliate sullo schema XMR verranno fornite quando si esegue la licenza di Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="6d236-131">Details about the XMR schema will be provided to you when you license Windows Media DRM.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6d236-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d236-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d236-133">**Verifica della revoca dei certificati**</span><span class="sxs-lookup"><span data-stu-id="6d236-133">**Checking Certificate Revocation**</span></span>](checking-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="6d236-134">**Creazione di una licenza XMR**</span><span class="sxs-lookup"><span data-stu-id="6d236-134">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="6d236-135">**Importazione DRM**</span><span class="sxs-lookup"><span data-stu-id="6d236-135">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




