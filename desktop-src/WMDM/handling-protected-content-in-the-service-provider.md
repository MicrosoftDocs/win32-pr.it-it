---
title: Gestione del contenuto protetto nel provider di servizi
description: Gestione del contenuto protetto nel provider di servizi
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Windows Media Gestione dispositivi, certificati
- Gestione dispositivi, certificati
- Guida per programmatori, certificati
- provider di servizi, certificati
- creazione di provider di servizi, certificati
- certificates
- Windows Media Gestione dispositivi, contenuto protetto da DRM
- Gestione dispositivi, contenuto protetto da DRM
- Guida per programmatori, contenuto protetto da DRM
- provider di servizi, contenuto protetto da DRM
- creazione di provider di servizi, contenuto protetto da DRM
- Contenuto protetto da DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298041"
---
# <a name="handling-protected-content-in-the-service-provider"></a><span data-ttu-id="7fd64-115">Gestione del contenuto protetto nel provider di servizi</span><span class="sxs-lookup"><span data-stu-id="7fd64-115">Handling Protected Content in the Service Provider</span></span>

<span data-ttu-id="7fd64-116">È possibile creare un provider di servizi in grado di inviare contenuto protetto da DRM a un dispositivo basato su DRM (PDDRM) di dispositivi portatili, ma non è possibile creare un provider di servizi in grado di inviare contenuto protetto da DRM ai dispositivi basati su Windows Media DRM 10 per i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="7fd64-116">You can build a service provider that can send DRM-protected content to a device built on Portable Device DRM (PDDRM), but you cannot build a service provider that can send DRM-protected content to devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="7fd64-117">Questi dispositivi usano MTP e non è possibile creare un provider di servizi MTP personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7fd64-117">These devices use MTP, and you cannot build your own MTP service provider.</span></span>

<span data-ttu-id="7fd64-118">L'unico passaggio aggiuntivo che un provider di servizi deve eseguire per inviare materiale DRM a un dispositivo PDDRM consiste nell'ottenere una coppia di certificati/chiavi rilasciata da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7fd64-118">The only extra step that a service provider must take to send DRM material to a PDDRM device is to get a Microsoft-issued certificate/key pair.</span></span> <span data-ttu-id="7fd64-119">Vedere [gli strumenti per lo sviluppo](tools-for-development.md) per informazioni su dove ottenere questo certificato/chiave.</span><span class="sxs-lookup"><span data-stu-id="7fd64-119">See [Tools for Development](tools-for-development.md) to learn where to get this certificate/key.</span></span> <span data-ttu-id="7fd64-120">Le licenze rilasciate a questi dispositivi saranno licenze semplificate che supportano solo la riproduzione semplice dei contenuti acquistati; non supporteranno le licenze in scadenza.</span><span class="sxs-lookup"><span data-stu-id="7fd64-120">The licenses issued to these devices will be simplified licenses that only support simple playback of purchased content; they will not support time-expiring licenses.</span></span> <span data-ttu-id="7fd64-121">Questa licenza verrà creata automaticamente dal provider di contenuti protetti (fornito da Microsoft per i file WMA/WMV) e archiviata nell'intestazione del file inviato al provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="7fd64-121">This license will be created for you by the secure content provider (provided by Microsoft for WMA/WMV files) and stored in the header of the file sent to the service provider.</span></span> <span data-ttu-id="7fd64-122">Non sarà necessario eseguire alcun passaggio speciale per i file protetti.</span><span class="sxs-lookup"><span data-stu-id="7fd64-122">You will not have to take any special steps for protected files.</span></span>

<span data-ttu-id="7fd64-123">Dopo l'invio del file protetto, Windows Media Gestione dispositivi chiamerà il provider di servizi per richiedere un file di archiviazione licenze speciale dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7fd64-123">After sending the protected file, Windows Media Device Manager will call the service provider to request a special license storage file from the device.</span></span> <span data-ttu-id="7fd64-124">Windows Media Gestione dispositivi aggiungerà una copia della nuova licenza a questo file e lo restituirà al provider di servizi per inviare di nuovo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7fd64-124">Windows Media Device Manager will add a copy of the new license to this file, and return it to the service provider to send back to the device.</span></span> <span data-ttu-id="7fd64-125">Tuttavia, anche se il provider di servizi non riesce a trovare o a restituire questo file, il dispositivo deve comunque essere in grado di riprodurre il file protetto usando la copia della licenza nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="7fd64-125">However, even if the service provider fails to find or return this file, the device should still be able to play the protected file by using the license copy in the file header.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fd64-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fd64-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fd64-127">**Creazione di un provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="7fd64-127">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="7fd64-128">**Gestione del contenuto protetto**</span><span class="sxs-lookup"><span data-stu-id="7fd64-128">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 




