---
title: Pre-distribuzione della licenza
description: Pre-distribuzione della licenza
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- Windows Media Format SDK, pre-distribuzione delle licenze
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), pre-distribuzione delle licenze
- DRM (Digital Rights Management), pre-distribuzione delle licenze
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- API estese del client DRM, pre-distribuzione delle licenze
- API estese del client, pre-distribuzione delle licenze
- pre-distribuzione delle licenze
- licenze, pre-consegna delle licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300276"
---
# <a name="license-pre-delivery"></a><span data-ttu-id="0e29b-113">Pre-distribuzione della licenza</span><span class="sxs-lookup"><span data-stu-id="0e29b-113">License Pre-Delivery</span></span>

<span data-ttu-id="0e29b-114">Il pre-recapito della licenza è il processo usato per effettuare il pull delle licenze in un computer client in modo preemptive.</span><span class="sxs-lookup"><span data-stu-id="0e29b-114">License pre-delivery is the process used to pull licenses to a client computer preemptively.</span></span> <span data-ttu-id="0e29b-115">Uno scenario comune per l'uso del pre-recapito è quando un utente sottoscrive un servizio musicale.</span><span class="sxs-lookup"><span data-stu-id="0e29b-115">A common scenario for using pre-delivery is when a user subscribes to a music service.</span></span> <span data-ttu-id="0e29b-116">Senza dover consegnare le licenze prima che siano necessarie, l'utente deve attendere l'acquisizione delle licenze per ogni nuova canzone.</span><span class="sxs-lookup"><span data-stu-id="0e29b-116">Without delivering licenses before they are needed, the user would have to wait for license acquisition for each new song.</span></span>

<span data-ttu-id="0e29b-117">Poiché il pre-recapito non viene eseguito come risposta a un tentativo di accesso, viene in genere eseguito solo dal proprietario del contenuto.</span><span class="sxs-lookup"><span data-stu-id="0e29b-117">Because pre-delivery is not done as a response to attempted access, it is typically performed only by the content owner.</span></span> <span data-ttu-id="0e29b-118">Ovvero è possibile predisporre solo le licenze per il contenuto controllato.</span><span class="sxs-lookup"><span data-stu-id="0e29b-118">That is, you can only pre-deliver licenses for content that you control.</span></span> <span data-ttu-id="0e29b-119">Il processo di pre-distribuzione è un coordinamento tra un componente client e un server licenze compilato utilizzando gli oggetti di Windows Media Digital Rights Management SDK.</span><span class="sxs-lookup"><span data-stu-id="0e29b-119">The pre-delivery process is a coordination between a client component and a license server built by using the objects of the Windows Media Digital Rights Management SDK.</span></span>

<span data-ttu-id="0e29b-120">Il pre-recapito della licenza è simile all'acquisizione di una [licenza non invisibile all'utente](non-silent-license-acquisition.md).</span><span class="sxs-lookup"><span data-stu-id="0e29b-120">License pre-delivery is similar to [Non-Silent License Acquisition](non-silent-license-acquisition.md).</span></span> <span data-ttu-id="0e29b-121">Seguire gli stessi passaggi, ad eccezione del fatto che non si ha un'intestazione DRM da passare a [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span><span class="sxs-lookup"><span data-stu-id="0e29b-121">Follow the same steps, except that you don't have a DRM header to pass to [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span></span> <span data-ttu-id="0e29b-122">Il metodo genererà una richiesta di verifica non specifica del contenuto che è possibile inviare al server licenze.</span><span class="sxs-lookup"><span data-stu-id="0e29b-122">The method will generate a challenge that is not content-specific that you can send to your license server.</span></span>

<span data-ttu-id="0e29b-123">In alternativa, è possibile usare [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) per la pre-distribuzione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="0e29b-123">Alternatively you can use the [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) to pre-deliver licenses.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e29b-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e29b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e29b-125">**Acquisizione di licenze**</span><span class="sxs-lookup"><span data-stu-id="0e29b-125">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="0e29b-126">**Uso del modello di eventi Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="0e29b-126">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 