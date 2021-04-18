---
title: Interfacce per i provider di contenuti sicuri
description: Interfacce per i provider di contenuti sicuri
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Media Gestione dispositivi, contenuto protetto da DRM
- Gestione dispositivi, contenuto protetto da DRM
- Guida di riferimento alla programmazione, contenuto protetto da DRM
- informazioni di riferimento per Windows Media Gestione dispositivi, contenuto protetto da DRM
- Contenuto protetto da DRM
- Windows Media Gestione dispositivi, Secure Content Provider (SCP)
- Gestione dispositivi, Secure Content Provider (SCP)
- Guida di riferimento alla programmazione, Secure Content Provider (SCP)
- informazioni di riferimento su Windows Media Gestione dispositivi, Secure Content Provider (SCP)
- provider di contenuti protetti (SCP)
- SCP (provider di contenuti protetto)
- Windows Media Gestione dispositivi, interfacce SCP
- Interfacce di Gestione dispositivi, SCP
- Guida di riferimento alla programmazione, interfacce SCP
- informazioni di riferimento sulle interfacce SCP di Windows Media Gestione dispositivi
- Interfacce SCP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298333"
---
# <a name="interfaces-for-secure-content-providers"></a><span data-ttu-id="1db77-119">Interfacce per i provider di contenuti sicuri</span><span class="sxs-lookup"><span data-stu-id="1db77-119">Interfaces for Secure Content Providers</span></span>

<span data-ttu-id="1db77-120">Un provider di contenuti protetto (SCP) è un componente plug-in che consente a Windows Media Gestione dispositivi di trasferire e richiedere informazioni sui diritti da contenuto protetto da DRM.</span><span class="sxs-lookup"><span data-stu-id="1db77-120">A secure content provider (SCP) is a plug-in component that enables Windows Media Device Manager to transfer and request rights information from DRM-protected content.</span></span> <span data-ttu-id="1db77-121">Microsoft fornisce un componente SCP in grado di gestire file WMA e WMV protetti da DRM.</span><span class="sxs-lookup"><span data-stu-id="1db77-121">Microsoft provides an SCP component that can handle DRM-protected WMA and WMV files.</span></span> <span data-ttu-id="1db77-122">Se il dispositivo o l'applicazione userà contenuto protetto da DRM di altri formati, deve creare un componente SCP implementando tutte le interfacce.</span><span class="sxs-lookup"><span data-stu-id="1db77-122">If your device or application will use DRM-protected content of other formats, it should create an SCP component by implementing all of these interfaces.</span></span> <span data-ttu-id="1db77-123">In caso contrario, non sarà necessario utilizzare tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="1db77-123">Otherwise, you will not need to use these interfaces.</span></span>



| <span data-ttu-id="1db77-124">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="1db77-124">Interface</span></span>                                                  | <span data-ttu-id="1db77-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1db77-125">Description</span></span>                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1db77-126">**ISCPSecureAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="1db77-126">**ISCPSecureAuthenticate**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | <span data-ttu-id="1db77-127">Interfaccia principale del provider di contenuti protetti.</span><span class="sxs-lookup"><span data-stu-id="1db77-127">The primary interface of the secure content provider.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="1db77-128">**ISCPSecureAuthenticate2**</span><span class="sxs-lookup"><span data-stu-id="1db77-128">**ISCPSecureAuthenticate2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | <span data-ttu-id="1db77-129">Estende **ISCPSecureAuthenticate** fornendo un metodo per ottenere un oggetto Session.</span><span class="sxs-lookup"><span data-stu-id="1db77-129">Extends **ISCPSecureAuthenticate** by providing a way to get a session object.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="1db77-130">**ISCPSecureExchange**</span><span class="sxs-lookup"><span data-stu-id="1db77-130">**ISCPSecureExchange**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | <span data-ttu-id="1db77-131">Utilizzato per scambiare il contenuto protetto e i diritti associati al contenuto.</span><span class="sxs-lookup"><span data-stu-id="1db77-131">Used to exchange secured content and rights associated with content.</span></span>                                                                                                                                                                                 |
| [<span data-ttu-id="1db77-132">**ISCPSecureExchange2**</span><span class="sxs-lookup"><span data-stu-id="1db77-132">**ISCPSecureExchange2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | <span data-ttu-id="1db77-133">Estende **ISCPSecureExchange** fornendo una nuova versione del metodo **TransferContainerData** .</span><span class="sxs-lookup"><span data-stu-id="1db77-133">Extends **ISCPSecureExchange** by providing a new version of the **TransferContainerData** method.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="1db77-134">**ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="1db77-134">**ISCPSecureExchange3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | <span data-ttu-id="1db77-135">Estende **ISCPSecureExchange2** fornendo prestazioni di scambio dei dati migliorate e un metodo di callback completo del trasferimento.</span><span class="sxs-lookup"><span data-stu-id="1db77-135">Extends **ISCPSecureExchange2** by providing improved data exchange performance, and a transfer complete callback method.</span></span>                                                                                                                            |
| [<span data-ttu-id="1db77-136">**ISCPSecureQuery**</span><span class="sxs-lookup"><span data-stu-id="1db77-136">**ISCPSecureQuery**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | <span data-ttu-id="1db77-137">Sottoposta a query da Windows Media Gestione dispositivi per determinare la proprietà del contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="1db77-137">Queried by Windows Media Device Manager to determine ownership of secured content.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="1db77-138">**ISCPSecureQuery2**</span><span class="sxs-lookup"><span data-stu-id="1db77-138">**ISCPSecureQuery2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | <span data-ttu-id="1db77-139">Estende **ISCPSecureQuery** tramite la funzionalità che determina se il provider di contenuti protetti è responsabile del contenuto e, in tal caso, fornisce un URL per l'aggiornamento dei componenti revocati e per determinare quali componenti sono stati revocati.</span><span class="sxs-lookup"><span data-stu-id="1db77-139">Extends **ISCPSecureQuery** through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.</span></span> |
| [<span data-ttu-id="1db77-140">**ISCPSecureQuery3**</span><span class="sxs-lookup"><span data-stu-id="1db77-140">**ISCPSecureQuery3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | <span data-ttu-id="1db77-141">Estende **ISCPSecureQuery2** fornendo un set di nuovi metodi per recuperare i diritti e prendere decisioni su un canale non crittografato.</span><span class="sxs-lookup"><span data-stu-id="1db77-141">Extends **ISCPSecureQuery2** by providing a set of new methods for retrieving the rights and making decision on a clear channel.</span></span>                                                                                                                     |
| [<span data-ttu-id="1db77-142">**ISCPSession**</span><span class="sxs-lookup"><span data-stu-id="1db77-142">**ISCPSession**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | <span data-ttu-id="1db77-143">Fornisce una gestione efficiente dello stato comune per più operazioni.</span><span class="sxs-lookup"><span data-stu-id="1db77-143">Provides efficient common state management for multiple operations.</span></span>                                                                                                                                                                                  |



 

 

 




