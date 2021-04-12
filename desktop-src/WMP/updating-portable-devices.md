---
title: Aggiornamento di dispositivi portatili
description: Aggiornamento di dispositivi portatili
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Windows Media Player Online Stores, aggiornamento di dispositivi portatili
- archivi online, aggiornamento di dispositivi portatili
- digitare 1 negozi online, aggiornamento di dispositivi portatili
- Windows Media Player Online Stores, dispositivi portatili
- negozi online, dispositivi portatili
- digitare 1 negozi online, dispositivi portatili
- aggiornamento di dispositivi portatili
- dispositivi portatili, aggiornamento
- dispositivi portatili, Windows Media Player Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29f5314f4eba1af43b3858304f02f8a7e0107df
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336265"
---
# <a name="updating-portable-devices"></a><span data-ttu-id="f20d0-112">Aggiornamento di dispositivi portatili</span><span class="sxs-lookup"><span data-stu-id="f20d0-112">Updating Portable Devices</span></span>

<span data-ttu-id="f20d0-113">Windows Media Player consente agli utenti di sincronizzare il contenuto multimediale digitale con i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="f20d0-113">Windows Media Player enables users to synchronize digital media content with portable devices.</span></span> <span data-ttu-id="f20d0-114">Questo può includere contenuto musicale acquistato o affittato da un negozio online.</span><span class="sxs-lookup"><span data-stu-id="f20d0-114">This can include music content purchased or rented from an online store.</span></span> <span data-ttu-id="f20d0-115">In alcune circostanze, i provider di archivio online potrebbero voler scrivere codice per lavorare su un dispositivo portatile connesso nell'ambito della gestione del contenuto fornito dallo Store.</span><span class="sxs-lookup"><span data-stu-id="f20d0-115">Under some circumstances, online store providers might want to write code to work on a connected portable device as part of managing content provided by the store.</span></span> <span data-ttu-id="f20d0-116">Per concedere al plug-in Online Store la possibilità di usare un dispositivo connesso, Windows Media Player chiama [IWMPContentPartner:: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) e fornisce il nome canonico del dispositivo portatile.</span><span class="sxs-lookup"><span data-stu-id="f20d0-116">To give the online store plug-in the opportunity to work with a connected device, Windows Media Player calls [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) and provides the canonical name of the portable device.</span></span> <span data-ttu-id="f20d0-117">Se il codice del plug-in determina che alcune operazioni devono essere eseguite con il dispositivo connesso, deve restituire immediatamente S \_ OK dalla chiamata a **UpdateDevice** prima di procedere con l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f20d0-117">If the plug-in code determines that some work must be done with the connected device, it must immediately return S\_OK from the call to **UpdateDevice** before proceeding to do the work.</span></span> <span data-ttu-id="f20d0-118">Se non è necessario eseguire alcuna operazione, il plug-in deve restituire un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="f20d0-118">If there is no work to do, the plug-in should return an error code.</span></span>

<span data-ttu-id="f20d0-119">Al termine dell'uso del dispositivo da parte del plug-in, è necessario chiamare [IWMPContentPartnerCallback:: UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) per notificare a Windows Media Player che il dispositivo è disponibile.</span><span class="sxs-lookup"><span data-stu-id="f20d0-119">When the plug-in has finished using the device, it must call [IWMPContentPartnerCallback::UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) to notify Windows Media Player that the device is available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f20d0-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f20d0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f20d0-121">**Guida per programmatori per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="f20d0-121">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




