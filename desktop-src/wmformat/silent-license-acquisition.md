---
title: Acquisizione di una licenza invisibile all'utente
description: Acquisizione di una licenza invisibile all'utente
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows Media Format SDK, acquisizione di una licenza invisibile all'utente
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), acquisizione di licenze Silent
- DRM (Digital Rights Management), acquisizione di licenze Silent
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- API estese del client DRM, acquisizione di licenze Silent
- API estese client, acquisizione di licenze Silent
- acquisizione di una licenza invisibile all'utente
- licenze, acquisizione di licenze Silent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045002"
---
# <a name="silent-license-acquisition"></a><span data-ttu-id="aa485-113">Acquisizione di una licenza invisibile all'utente</span><span class="sxs-lookup"><span data-stu-id="aa485-113">Silent License Acquisition</span></span>

<span data-ttu-id="aa485-114">L'acquisizione di una licenza invisibile all'utente richiede solo una singola chiamata al metodo che gestisce in modo asincrono tutte le comunicazioni di rete con il server licenze.</span><span class="sxs-lookup"><span data-stu-id="aa485-114">Silent license acquisition requires only a single method call that handles all of the network communications with the license server asynchronously.</span></span>

<span data-ttu-id="aa485-115">Questo tipo di acquisizione della licenza viene in genere usato come risposta all'utente finale che tenta di accedere al contenuto protetto, ad esempio, tentando di riprodurre un file protetto in un'applicazione di Media Player.</span><span class="sxs-lookup"><span data-stu-id="aa485-115">This type of license acquisition is usually used as a response to the end user trying to access protected content—for example, trying to play a protected file in a media player application.</span></span> <span data-ttu-id="aa485-116">Poiché l'acquisizione di una licenza invisibile all'utente ottiene la licenza con una singola chiamata, non può essere usata se è necessario un input aggiuntivo da parte dell'utente, ad esempio il pagamento per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="aa485-116">Because silent license acquisition gets the license with a single call, it cannot be used if additional input from the user, such as payment for the content, is required.</span></span>

<span data-ttu-id="aa485-117">Per eseguire l'acquisizione di una licenza invisibile all'utente, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="aa485-117">To perform silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="aa485-118">Chiamare il metodo [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="aa485-118">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="aa485-119">Passare l'intestazione DRM dal file protetto come parametro *bstrHeaderData* .</span><span class="sxs-lookup"><span data-stu-id="aa485-119">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="aa485-120">Specificare i diritti che si desidera concedere alla licenza nel parametro *bstrActions* .</span><span class="sxs-lookup"><span data-stu-id="aa485-120">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="aa485-121">Infine, impostare il parametro *dwFlags* su WMDRM \_ acquisisce \_ licenza invisibile all' \_ utente.</span><span class="sxs-lookup"><span data-stu-id="aa485-121">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_SILENT.</span></span>
2.  <span data-ttu-id="aa485-122">Eventi trap per l'interfaccia [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .</span><span class="sxs-lookup"><span data-stu-id="aa485-122">Trap events for the [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span> <span data-ttu-id="aa485-123">Quando si riceve l'evento **MEWMDRMLicenseAcquisitionCompleted** , controllare il codice restituito chiamando il metodo **IMFMediaEvent:: GetStatus** , che è documentato nella documentazione di Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="aa485-123">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, check its return code by calling the **IMFMediaEvent::GetStatus** method, which is documented in the Media Foundation documentation.</span></span> <span data-ttu-id="aa485-124">Se il valore **HRESULT** recuperato è un codice di esito positivo, la licenza è stata scaricata correttamente e si trova nell'archivio licenze locale pronto per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="aa485-124">If the retrieved **HRESULT** value is a success code, then the license was successfully downloaded and is in the local license store ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa485-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa485-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa485-126">**Acquisizione di licenze**</span><span class="sxs-lookup"><span data-stu-id="aa485-126">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="aa485-127">**Uso del modello di eventi Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="aa485-127">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




