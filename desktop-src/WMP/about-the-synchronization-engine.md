---
title: Informazioni sul motore di sincronizzazione
description: Informazioni sul motore di sincronizzazione
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player, motore di sincronizzazione
- Modello a oggetti di Windows Media Player, motore di sincronizzazione
- modello a oggetti, motore di sincronizzazione
- Controllo ActiveX di Windows Media Player, motore di sincronizzazione
- Controllo ActiveX, motore di sincronizzazione
- Controllo ActiveX Windows Media Player Mobile, motore di sincronizzazione
- Windows Media Player Mobile, motore di sincronizzazione
- sincronizzazione di dispositivi, motore di sincronizzazione
- sincronizzazione dei dispositivi, motore di sincronizzazione
- motore di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398602"
---
# <a name="about-the-synchronization-engine"></a><span data-ttu-id="66326-113">Informazioni sul motore di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="66326-113">About the Synchronization Engine</span></span>

<span data-ttu-id="66326-114">Il motore di sincronizzazione è il componente di Windows Media Player che gestisce la copia del contenuto multimediale digitale nei dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="66326-114">The synchronization engine is the component of Windows Media Player that manages copying digital media content to portable devices.</span></span> <span data-ttu-id="66326-115">Windows Media Player supporta una singola istanza del motore di sincronizzazione per ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66326-115">Windows Media Player supports a single instance of the synchronization engine for each device.</span></span> <span data-ttu-id="66326-116">Per eseguire attività di sincronizzazione a livello di programmazione, è necessario utilizzare un'istanza remota del controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="66326-116">You must use a remoted instance of the Windows Media Player control to perform synchronization tasks programmatically.</span></span> <span data-ttu-id="66326-117">In effetti, il programma condivide le istanze del motore di sincronizzazione con Windows Media Player e tutti gli altri programmi che usano le interfacce del lettore per la sincronizzazione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="66326-117">In effect, your program shares the synchronization engine instances with Windows Media Player and all other programs that use the Player interfaces for device synchronization.</span></span>

<span data-ttu-id="66326-118">È possibile usare [IWMPSyncDevice:: Start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) e [IWMPSyncDevice:: Stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) per controllare il momento in cui il motore di sincronizzazione esegue le operazioni.</span><span class="sxs-lookup"><span data-stu-id="66326-118">You can use [IWMPSyncDevice::start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) and [IWMPSyncDevice::stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) to control when the synchronization engine does its work.</span></span> <span data-ttu-id="66326-119">Nella maggior parte dei casi, non è consigliabile usare questi metodi.</span><span class="sxs-lookup"><span data-stu-id="66326-119">In most cases, you should not use these methods.</span></span> <span data-ttu-id="66326-120">Al contrario, è necessario consentire al motore di sincronizzazione di pianificare automaticamente il lavoro.</span><span class="sxs-lookup"><span data-stu-id="66326-120">Instead, you should let the synchronization engine schedule its work automatically.</span></span> <span data-ttu-id="66326-121">I metodi **Start** e **Stop** esistono per poterli utilizzare se il programma è stato progettato per sostituire l'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="66326-121">The **start** and **stop** methods exist so that you can use them if your program is designed to replace the Windows Media Player user interface.</span></span> <span data-ttu-id="66326-122">In questo caso, è possibile fornire un pulsante di avvio/arresto simile a quello di Windows Media Player disponibile nella scheda **dispositivi** .</span><span class="sxs-lookup"><span data-stu-id="66326-122">In this case, you might want to provide a start/stop button similar to the one Windows Media Player provides in the **Devices** tab.</span></span>

<span data-ttu-id="66326-123">È possibile monitorare lo stato di avanzamento della sincronizzazione per un dispositivo eseguendo il polling di [IWMPSyncDevice:: Get \_ Progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span><span class="sxs-lookup"><span data-stu-id="66326-123">You can monitor the synchronization progress for a device by polling [IWMPSyncDevice::get\_progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span></span> <span data-ttu-id="66326-124">Questo metodo recupera un valore di avanzamento per l'intero processo di sincronizzazione con un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="66326-124">This method retrieves a progress value for the entire synchronization process with a particular device.</span></span> <span data-ttu-id="66326-125">Il valore recuperato è un numero che rappresenta la percentuale di completamento della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="66326-125">The value retrieved is a number that represents the percentage of synchronization complete.</span></span> <span data-ttu-id="66326-126">Sono disponibili due eventi che è possibile ricevere correlati alla sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="66326-126">There are two events you can receive that are related to synchronization.</span></span> <span data-ttu-id="66326-127">L'evento **DeviceSyncError** informa l'utente quando si verifica un problema.</span><span class="sxs-lookup"><span data-stu-id="66326-127">The **DeviceSyncError** event notifies you when a problem occurs.</span></span> <span data-ttu-id="66326-128">L'evento **DeviceSyncStateChange** avvisa l'utente quando il motore di sincronizzazione ha modificato lo stato per il dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="66326-128">The **DeviceSyncStateChange** event alerts you when the synchronization engine has changed state for the current device.</span></span>

<span data-ttu-id="66326-129">È possibile limitare la quantità di archiviazione del dispositivo utilizzata da Windows Media Player per la sincronizzazione chiamando [IWMPSyncDevice2:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) con l'attributo **PercentSpaceReserved** .</span><span class="sxs-lookup"><span data-stu-id="66326-129">You can limit the amount of device storage that Windows Media Player uses for synchronization by calling [IWMPSyncDevice2::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) with the **PercentSpaceReserved** attribute.</span></span> <span data-ttu-id="66326-130">L'utilizzo di questa interfaccia richiede Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="66326-130">Using this interface requires Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66326-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66326-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66326-132">**Informazioni sulla sincronizzazione dei dispositivi**</span><span class="sxs-lookup"><span data-stu-id="66326-132">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="66326-133">**Interfaccia IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="66326-133">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="66326-134">**Visualizzazione dello stato di avanzamento della sincronizzazione**</span><span class="sxs-lookup"><span data-stu-id="66326-134">**Showing Synchronization Progress**</span></span>](showing-synchronization-progress.md)
</dt> </dl>

 

 




