---
title: Acquisizione di licenza non invisibile all'utente
description: Acquisizione di licenza non invisibile all'utente
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows Media Format SDK, acquisizione di licenze non invisibile all'utente
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), acquisizione di licenze non invisibile all'utente
- DRM (Digital Rights Management), acquisizione di licenze non invisibile all'utente
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- API estese del client DRM, acquisizione di licenze non invisibile all'utente
- API estese client, acquisizione di licenze non invisibile all'utente
- acquisizione di licenza non invisibile all'utente
- licenze, acquisizione di licenze non Silent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516057"
---
# <a name="non-silent-license-acquisition"></a><span data-ttu-id="14f71-113">Acquisizione di licenza non invisibile all'utente</span><span class="sxs-lookup"><span data-stu-id="14f71-113">Non-Silent License Acquisition</span></span>

<span data-ttu-id="14f71-114">L'acquisizione di licenze non Silent consente al provider di licenze di interagire con l'utente finale tramite una pagina Web, come un passaggio intermedio del processo di acquisizione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="14f71-114">Non-silent license acquisition enables the license provider to interact with the end user through a Web page, as an intermediate step in the license acquisition process.</span></span> <span data-ttu-id="14f71-115">L'acquisizione di una licenza non invisibile all'utente viene avviata in risposta a un utente che tenta di accedere al contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="14f71-115">Non-silent license acquisition is initiated in response to a user trying to access protected content.</span></span>

<span data-ttu-id="14f71-116">Per eseguire l'acquisizione di una licenza non invisibile all'utente, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="14f71-116">To perform non-silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="14f71-117">Chiamare il metodo [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="14f71-117">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="14f71-118">Passare l'intestazione DRM dal file protetto come parametro *bstrHeaderData* .</span><span class="sxs-lookup"><span data-stu-id="14f71-118">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="14f71-119">Specificare i diritti che si desidera concedere alla licenza nel parametro *bstrActions* .</span><span class="sxs-lookup"><span data-stu-id="14f71-119">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="14f71-120">Infine, impostare il parametro *dwFlags* su WMDRM \_ acquisisce \_ licenza non \_ invisibile.</span><span class="sxs-lookup"><span data-stu-id="14f71-120">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_NONSILENT.</span></span>
2.  <span data-ttu-id="14f71-121">Eventi trap per l'interfaccia **IWMDRMLicenseManagement** .</span><span class="sxs-lookup"><span data-stu-id="14f71-121">Trap events for the **IWMDRMLicenseManagement** interface.</span></span> <span data-ttu-id="14f71-122">Quando si riceve l'evento **MEWMDRMLicenseAcquisitionCompleted** , ottenere il valore associato chiamando **IMFMediaEvent:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="14f71-122">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, get its associated value by calling **IMFMediaEvent::GetValue**.</span></span> <span data-ttu-id="14f71-123">Il valore deve essere di tipo VT \_ Unknown, un puntatore a un'interfaccia **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="14f71-123">The value should be of type VT\_UNKNOWN, a pointer to an **IUnknown** interface.</span></span>
3.  <span data-ttu-id="14f71-124">Chiamare il metodo **QueryInterface** dell'interfaccia **IUnknown** recuperata nel passaggio 2 per ottenere l'interfaccia [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .</span><span class="sxs-lookup"><span data-stu-id="14f71-124">Call the **QueryInterface** method of the **IUnknown** interface retrieved in step 2 to get the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>
4.  <span data-ttu-id="14f71-125">Chiamare [**IWMDRMNonSilentLicenseAquisition:: getchallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) per recuperare la richiesta di licenza.</span><span class="sxs-lookup"><span data-stu-id="14f71-125">Call [**IWMDRMNonSilentLicenseAquisition::GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) to retrieve the license challenge.</span></span> <span data-ttu-id="14f71-126">Chiamare anche [**IWMDRMNonSilentLicenseAquisition:: getURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) se non si ha già l'URL del server licenze.</span><span class="sxs-lookup"><span data-stu-id="14f71-126">Also call [**IWMDRMNonSilentLicenseAquisition::GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) if you do not have the URL of the license server already.</span></span>
5.  <span data-ttu-id="14f71-127">Invia la richiesta di verifica alla pagina Web specificata dall'URL.</span><span class="sxs-lookup"><span data-stu-id="14f71-127">Send the challenge to the Web page specified by the URL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14f71-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14f71-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14f71-129">**Acquisizione di licenze**</span><span class="sxs-lookup"><span data-stu-id="14f71-129">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="14f71-130">**Uso del modello di eventi Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="14f71-130">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




