---
title: Verifica della revoca dei certificati
description: Verifica della revoca dei certificati
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- Windows Media Format SDK, importazione DRM
- Windows Media Format SDK, importazione
- Windows Media Format SDK, revoca di certificati
- Windows Media Format SDK, revoca dei certificati
- Digital Rights Management (DRM), importazione
- DRM (Digital Rights Management), importazione
- Digital Rights Management (DRM), revoca dei certificati
- DRM (Digital Rights Management), revoca dei certificati
- Digital Rights Management (DRM), revoca dei certificati
- DRM (Digital Rights Management), revoca dei certificati
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, revoca dei certificati
- API estese client, revoca di certificati
- API estese del client DRM, revoca dei certificati
- API estese client, revoca dei certificati
- certificati, revoca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbb72dd52870437ef9b69b30cc36a57725abe09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710234"
---
# <a name="checking-certificate-revocation"></a><span data-ttu-id="60f4c-120">Verifica della revoca dei certificati</span><span class="sxs-lookup"><span data-stu-id="60f4c-120">Checking Certificate Revocation</span></span>

<span data-ttu-id="60f4c-121">Quando si importa il contenuto in Windows Media DRM, è necessario assicurarsi che nessun certificato in una raccolta di certificati sia stato revocato verificando che nessun certificato nella raccolta sia presente nell'elenco di revoche.</span><span class="sxs-lookup"><span data-stu-id="60f4c-121">When importing content into Windows Media DRM, you must ensure that no certificate in a certificate collection has been revoked by verifying that no certificate in the collection is in the revocation list.</span></span> <span data-ttu-id="60f4c-122">L'elenco di revoche viene estratto usando il metodo [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="60f4c-122">The revocation list is extracted by using the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>

<span data-ttu-id="60f4c-123">Si usa quindi il metodo [**IWMDRMSecurity:: CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) per verificare che il certificato non sia stato revocato.</span><span class="sxs-lookup"><span data-stu-id="60f4c-123">You then use the [**IWMDRMSecurity::CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) method to verify that the certificate is not revoked.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60f4c-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60f4c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60f4c-125">**Importazione DRM**</span><span class="sxs-lookup"><span data-stu-id="60f4c-125">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




