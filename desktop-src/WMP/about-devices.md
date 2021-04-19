---
title: Informazioni sui dispositivi
description: Informazioni sui dispositivi
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Windows Media Player, sincronizzazione dei dispositivi
- Modello a oggetti di Windows Media Player, sincronizzazione dei dispositivi
- modello a oggetti, sincronizzazione dei dispositivi
- Controllo ActiveX di Windows Media Player, sincronizzazione dei dispositivi
- Controllo ActiveX, sincronizzazione dei dispositivi
- Controllo ActiveX Windows Media Player Mobile, sincronizzazione dei dispositivi
- Windows Media Player Mobile, sincronizzazione dei dispositivi
- sincronizzazione dei dispositivi, informazioni
- sincronizzazione dei dispositivi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89a074e4edb5bdbc7d90391398d5e0e4133505a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299375"
---
# <a name="about-devices"></a><span data-ttu-id="b6f21-112">Informazioni sui dispositivi</span><span class="sxs-lookup"><span data-stu-id="b6f21-112">About Devices</span></span>

<span data-ttu-id="b6f21-113">I dispositivi portatili sono dispositivi hardware che gli utenti portano a utilizzare contenuti multimediali digitali quando sono lontani dal computer.</span><span class="sxs-lookup"><span data-stu-id="b6f21-113">Portable devices are hardware devices that users carry to enjoy digital media content when they are away from their computer.</span></span> <span data-ttu-id="b6f21-114">In genere, i dispositivi portatili vengono usati a batteria.</span><span class="sxs-lookup"><span data-stu-id="b6f21-114">Typically, portable devices are battery operated.</span></span> <span data-ttu-id="b6f21-115">Alcuni dispositivi possono riprodurre solo musica.</span><span class="sxs-lookup"><span data-stu-id="b6f21-115">Some devices can play music only.</span></span> <span data-ttu-id="b6f21-116">Altri dispositivi possono riprodurre video e musica.</span><span class="sxs-lookup"><span data-stu-id="b6f21-116">Other devices can play video and music.</span></span>

<span data-ttu-id="b6f21-117">Alcuni dispositivi supportano la sincronizzazione automatica del contenuto multimediale digitale con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b6f21-117">Some devices support automatic synchronization of digital media content with Windows Media Player.</span></span> <span data-ttu-id="b6f21-118">Altri dispositivi supportano solo il trasferimento manuale.</span><span class="sxs-lookup"><span data-stu-id="b6f21-118">Other devices support only manual transfer.</span></span> <span data-ttu-id="b6f21-119">È possibile determinare se un determinato dispositivo supporta la sincronizzazione automatica chiamando [IWMPSyncDevice:: Get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) e quindi controllando il valore [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperato.</span><span class="sxs-lookup"><span data-stu-id="b6f21-119">You can determine whether a particular device supports automatic synchronization by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="b6f21-120">Se il valore recuperato è **wmpdsManualDevice**, il dispositivo non supporta la sincronizzazione automatica.</span><span class="sxs-lookup"><span data-stu-id="b6f21-120">If the retrieved value is **wmpdsManualDevice**, the device does not support automatic synchronization.</span></span>

<span data-ttu-id="b6f21-121">È possibile enumerare i dispositivi connessi al computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b6f21-121">You can enumerate the devices connected to the user's computer.</span></span> <span data-ttu-id="b6f21-122">A tale scopo, usare prima [IWMPSyncServices:: Get \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) per recuperare il conteggio dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b6f21-122">To do this, first use [IWMPSyncServices::get\_deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) to retrieve the count of devices.</span></span> <span data-ttu-id="b6f21-123">Quindi, in un ciclo, chiamare [IWMPSyncServices:: GetDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passando ogni volta il valore di indice appropriato.</span><span class="sxs-lookup"><span data-stu-id="b6f21-123">Then, in a loop, call [IWMPSyncServices::getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passing the appropriate index value each time.</span></span> <span data-ttu-id="b6f21-124">È possibile usare [IWMPSyncDevice:: Get \_ Connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) per valutare se un determinato dispositivo è attualmente connesso.</span><span class="sxs-lookup"><span data-stu-id="b6f21-124">You can use [IWMPSyncDevice::get\_connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) to evaluate whether a particular device is currently connected.</span></span>

<span data-ttu-id="b6f21-125">Per informazioni su quando i dispositivi si connettono o si disconnettono, è possibile ricevere gli eventi **DeviceConnect** e **DeviceDisconnect** .</span><span class="sxs-lookup"><span data-stu-id="b6f21-125">To know when devices connect or disconnect, you can receive the **DeviceConnect** and **DeviceDisconnect** events.</span></span> <span data-ttu-id="b6f21-126">Questi eventi vengono ricevuti tramite l'interfaccia **IWMPEvents2** .</span><span class="sxs-lookup"><span data-stu-id="b6f21-126">These events are received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="b6f21-127">L'interfaccia **IWMPSyncDevice** fornisce metodi aggiuntivi che consentono di ottenere o impostare informazioni su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6f21-127">The **IWMPSyncDevice** interface provides additional methods to enable you to get or set information about a device.</span></span> <span data-ttu-id="b6f21-128">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="b6f21-128">For example:</span></span>

-   <span data-ttu-id="b6f21-129">I metodi **get \_ FriendlyName** e **put \_ FriendlyName** consentono di recuperare e specificare il nome del dispositivo definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b6f21-129">The **get\_FriendlyName** and **put\_FriendlyName** methods enable you to retrieve and specify the user-defined device name.</span></span>
-   <span data-ttu-id="b6f21-130">Il metodo **get \_ DeviceName** consente di recuperare il nome del dispositivo visualizzato dagli utenti nella shell di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b6f21-130">The **get\_deviceName** method enables you to retrieve the device name that users see in the Windows XP shell.</span></span>
-   <span data-ttu-id="b6f21-131">Il metodo **GetItemInfo** consente di recuperare i metadati dai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b6f21-131">The **getItemInfo** method enables you to retrieve metadata from devices.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6f21-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6f21-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6f21-133">**Informazioni sulla sincronizzazione dei dispositivi**</span><span class="sxs-lookup"><span data-stu-id="b6f21-133">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="b6f21-134">**Interfaccia IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="b6f21-134">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="b6f21-135">**Interfaccia IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="b6f21-135">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="b6f21-136">**Uso dei dispositivi portatili**</span><span class="sxs-lookup"><span data-stu-id="b6f21-136">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




