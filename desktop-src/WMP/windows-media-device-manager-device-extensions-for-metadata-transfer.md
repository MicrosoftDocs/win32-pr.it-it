---
title: Estensioni del dispositivo Windows Media Gestione dispositivi per il trasferimento dei metadati
description: Estensioni del dispositivo Windows Media Gestione dispositivi per il trasferimento dei metadati
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player, estensioni del dispositivo
- Windows Media Player, estensioni
- Media Player di Windows, metadati
- Windows Media Player, trasferimento di metadati accelerato
- Windows Media Player, trasferimento accelerato dei metadati
- metadati, estensioni del dispositivo
- metadati, estensioni
- estensioni del dispositivo, trasferimento di metadati
- estensioni, trasferimento di metadati
- trasferimento di metadati accelerato
- metadati, trasferimento accelerato
- estensioni del dispositivo, trasferimento di metadati accelerato
- estensioni, trasferimento di metadati accelerato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471438"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a><span data-ttu-id="d2151-116">Estensioni del dispositivo Windows Media Gestione dispositivi per il trasferimento dei metadati</span><span class="sxs-lookup"><span data-stu-id="d2151-116">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>

<span data-ttu-id="d2151-117">Per consentire il trasferimento di metadati accelerati, i produttori di dispositivi che non supportano MTP devono eseguire le operazioni seguenti nel codice sorgente:</span><span class="sxs-lookup"><span data-stu-id="d2151-117">To enable accelerated metadata transfer, manufacturers of devices that do not support MTP must do the following in source code:</span></span>

-   <span data-ttu-id="d2151-118">Definire **il \_ \_ \_ supporto del dispositivo WMDM di WMP**.</span><span class="sxs-lookup"><span data-stu-id="d2151-118">Define **WMP\_WMDM\_DEVICE\_SUPPORT**.</span></span>
-   <span data-ttu-id="d2151-119">Includere wmpdevices. h, che viene installato come parte di Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="d2151-119">Include wmpdevices.h, which is installed as part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="d2151-120">Wmpdevices. h definisce le strutture seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2151-120">Wmpdevices.h defines the following structures.</span></span>



| <span data-ttu-id="d2151-121">Struttura</span><span class="sxs-lookup"><span data-stu-id="d2151-121">Structure</span></span>                                                                                 | <span data-ttu-id="d2151-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2151-122">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2151-123">WMP \_ WMDM \_ metadati \_ round \_ Trip \_ PC2DEVICE</span><span class="sxs-lookup"><span data-stu-id="d2151-123">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | <span data-ttu-id="d2151-124">Struttura utilizzata da Windows Media Player per richiedere informazioni di sincronizzazione dei metadati accelerate da dispositivi portatili che non supportano MTP.</span><span class="sxs-lookup"><span data-stu-id="d2151-124">Structure used by Windows Media Player to request accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |
| [<span data-ttu-id="d2151-125">WMP \_ WMDM \_ metadati \_ round \_ Trip \_ DEVICE2PC</span><span class="sxs-lookup"><span data-stu-id="d2151-125">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | <span data-ttu-id="d2151-126">Struttura utilizzata da Windows Media Player per ricevere informazioni di sincronizzazione dei metadati accelerate dai dispositivi portatili che non supportano MTP.</span><span class="sxs-lookup"><span data-stu-id="d2151-126">Structure used by Windows Media Player to receive accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |



 

<span data-ttu-id="d2151-127">Per richiedere informazioni dal dispositivo sui metadati che sono stati modificati, Windows Media Player 10 o versione successiva chiama il metodo Windows Media Gestione dispositivi **IWMDMDevice3::D eviceiocontrol**.</span><span class="sxs-lookup"><span data-stu-id="d2151-127">To request information from the device about metadata that has changed, Windows Media Player 10 or later calls the Windows Media Device Manager method **IWMDMDevice3::DeviceIoControl**.</span></span> <span data-ttu-id="d2151-128">Quando si effettua questa chiamata, il giocatore segue passaggi specifici, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="d2151-128">When making this call, the Player follows specific steps, as follows:</span></span>

-   <span data-ttu-id="d2151-129">Il primo parametro, *dwIoControlCode*, contiene la costante **\_ \_ \_ round \_ trip dei metadati IOCTL WMP**.</span><span class="sxs-lookup"><span data-stu-id="d2151-129">The first parameter, *dwIoControlCode*, contains the constant **IOCTL\_WMP\_METADATA\_ROUND\_TRIP**.</span></span> <span data-ttu-id="d2151-130">Questa costante è definita in wmpdevices. h.</span><span class="sxs-lookup"><span data-stu-id="d2151-130">This constant is defined in wmpdevices.h.</span></span>
-   <span data-ttu-id="d2151-131">Il secondo parametro, *lpInBuffer*, punta a una struttura di **\_ \_ round trip dei metadati di WMP WMDM \_ \_ \_ PC2DEVICE** .</span><span class="sxs-lookup"><span data-stu-id="d2151-131">The second parameter, *lpInBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE** structure.</span></span>
-   <span data-ttu-id="d2151-132">Il terzo parametro, *nInBufferSize*, contiene la dimensione del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="d2151-132">The third parameter, *nInBufferSize*, contains the size of the input buffer.</span></span>
-   <span data-ttu-id="d2151-133">Il quarto parametro, *lpOutBuffer*, punta a una struttura di **\_ \_ round trip dei metadati di WMP WMDM \_ \_ \_ DEVICE2PC** .</span><span class="sxs-lookup"><span data-stu-id="d2151-133">The fourth parameter, *lpOutBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC** structure.</span></span> <span data-ttu-id="d2151-134">Il dispositivo deve compilare questa struttura con le informazioni sulle modifiche.</span><span class="sxs-lookup"><span data-stu-id="d2151-134">The device must fill in this structure with information about changes.</span></span>
-   <span data-ttu-id="d2151-135">Il quinto parametro, *pnOutBufferSize*, riceve la dimensione del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="d2151-135">The fifth parameter, *pnOutBufferSize*, receives the size of the output buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2151-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2151-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2151-137">**Estensioni del dispositivo per il trasferimento di metadati accelerati**</span><span class="sxs-lookup"><span data-stu-id="d2151-137">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




