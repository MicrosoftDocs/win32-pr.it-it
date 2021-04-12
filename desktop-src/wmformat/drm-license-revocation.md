---
title: Revoca delle licenze (client Microsoft Windows Media DRM)
description: Revoca delle licenze (client Microsoft Windows Media DRM)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows Media Format SDK, licenze
- Windows Media Format SDK, revoca delle licenze
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), revoca delle licenze
- DRM (Digital Rights Management), revoca delle licenze
- API estese del client DRM, licenze
- API estese client, licenze
- API estese del client DRM, revoca delle licenze
- API estese client, revoca delle licenze
- licenze, revoca
- revoca delle licenze, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234432"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a><span data-ttu-id="e8b05-115">Revoca delle licenze (client Microsoft Windows Media DRM)</span><span class="sxs-lookup"><span data-stu-id="e8b05-115">License Revocation (Microsoft Windows Media DRM Client)</span></span>

<span data-ttu-id="e8b05-116">La revoca delle licenze si riferisce alla rimozione delle licenze da un archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="e8b05-116">License revocation refers to the removal of licenses from a local license store.</span></span> <span data-ttu-id="e8b05-117">Uno scenario comune per la revoca delle licenze si verifica quando un provider di servizi, ad esempio un servizio di abbonamento musicale, deve disattivare il servizio nel computer di un utente.</span><span class="sxs-lookup"><span data-stu-id="e8b05-117">A common scenario for license revocation occurs when a service provider, such as a music subscription service, must deactivate the service on a user's computer.</span></span>

<span data-ttu-id="e8b05-118">Il processo di revoca della licenza viene avviato da un servizio fornito dall'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="e8b05-118">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="e8b05-119">L'applicazione può ospitare questo servizio o può essere un'applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="e8b05-119">Your application can host this service or it can be a Web application.</span></span> <span data-ttu-id="e8b05-120">In entrambi i casi, l'applicazione deve essere in grado di ricevere una richiesta di licenza creata dal servizio.</span><span class="sxs-lookup"><span data-stu-id="e8b05-120">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="e8b05-121">Per rimuovere le licenze dall'archivio licenze, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e8b05-121">To remove licenses from the license store, do the following:</span></span>

1.  <span data-ttu-id="e8b05-122">Quando si riceve una richiesta di licenza dall'emittente della licenza, creare una richiesta di revoca usando il metodo [**IWMDRMLicenseManagement:: CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b05-122">Upon receiving a license challenge from the license issuer, create a revocation challenge using the [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) method.</span></span> <span data-ttu-id="e8b05-123">Questo metodo consente di allocare un buffer contenente i dati di una richiesta di revoca, che vengono passati all'applicazione tramite il parametro *ppbChallengeOutput* .</span><span class="sxs-lookup"><span data-stu-id="e8b05-123">This method will allocate a buffer containing a revocation challenge data, which is passed to your application through the *ppbChallengeOutput* parameter.</span></span>
2.  <span data-ttu-id="e8b05-124">Inviare la richiesta di revoca della licenza a un servizio di revoca delle licenze.</span><span class="sxs-lookup"><span data-stu-id="e8b05-124">Send the license revocation challenge to a license revocation service.</span></span> <span data-ttu-id="e8b05-125">Il server genererà un BLOB di revoca delle licenze (LRB) in risposta.</span><span class="sxs-lookup"><span data-stu-id="e8b05-125">The server will generate a license revocation BLOB (LRB) in response.</span></span>
3.  <span data-ttu-id="e8b05-126">Rimuovere la licenza dall'archivio locale usando il metodo [**IWMDRMLicenseManagement::P rocesslicenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) , passando il LRB restituito dal server licenze.</span><span class="sxs-lookup"><span data-stu-id="e8b05-126">Remove the license from the local store using the [**IWMDRMLicenseManagement::ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) method, passing the LRB returned by license server.</span></span>
4.  <span data-ttu-id="e8b05-127">Deallocare il buffer allocato da **CreateLicenseRevocationChallenge** tramite la funzione **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="e8b05-127">Deallocate the buffer allocated by **CreateLicenseRevocationChallenge** by using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="e8b05-128">Per ulteriori informazioni sul funzionamento della revoca delle licenze o su come scrivere un servizio di revoca, vedere Implementazione della revoca delle [licenze](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span><span class="sxs-lookup"><span data-stu-id="e8b05-128">For more information on how license revocation works or on how to write a revocation service, see [Implementing License Revocation](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8b05-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8b05-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8b05-130">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="e8b05-130">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="e8b05-131">**Archivio licenze locale**</span><span class="sxs-lookup"><span data-stu-id="e8b05-131">**Local License Store**</span></span>](local-license-store.md)
</dt> <dt>

[<span data-ttu-id="e8b05-132">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="e8b05-132">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 