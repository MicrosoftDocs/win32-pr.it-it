---
title: Informazioni sulle relazioni
description: Informazioni sulle relazioni
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, relazioni
- Modello a oggetti di Windows Media Player, relazioni
- modello a oggetti, relazioni
- Controllo ActiveX Windows Media Player, relazioni
- Controllo ActiveX, relazioni
- Controllo ActiveX Windows Media Player Mobile, relazioni
- Windows Media Player Mobile, relazioni
- sincronizzazione di dispositivi, relazioni
- sincronizzazione dei dispositivi, relazioni
- partenariati tra dispositivi e Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104472243"
---
# <a name="about-partnerships"></a><span data-ttu-id="0e245-113">Informazioni sulle relazioni</span><span class="sxs-lookup"><span data-stu-id="0e245-113">About Partnerships</span></span>

<span data-ttu-id="0e245-114">Una partnership è una relazione speciale tra un dispositivo portatile e Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0e245-114">A partnership is a special relationship between a portable device and Windows Media Player.</span></span> <span data-ttu-id="0e245-115">Gli utenti possono stabilire una relazione per un particolare dispositivo usando l'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0e245-115">Users can establish a partnership for a particular device by using the Windows Media Player user interface.</span></span> <span data-ttu-id="0e245-116">È possibile gestire le relazioni a livello di codice usando [IWMPSyncDevice:: createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) e [IWMPSyncDevice::d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span><span class="sxs-lookup"><span data-stu-id="0e245-116">You can programmatically manage partnerships by using [IWMPSyncDevice::createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) and [IWMPSyncDevice::deletePartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span></span> <span data-ttu-id="0e245-117">Il metodo **createPartnership** avvia un processo asincrono che termina quando viene ricevuto l'evento **CreatePartnershipComplete** tramite l'interfaccia **IWMPEvents2** .</span><span class="sxs-lookup"><span data-stu-id="0e245-117">The **createPartnership** method starts an asynchronous process that ends when the **CreatePartnershipComplete** event is received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="0e245-118">Windows Media Player 10 o versioni successive supporta la creazione di relazioni con un massimo di 16 dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0e245-118">Windows Media Player 10 or later supports creating partnerships with up to 16 devices.</span></span> <span data-ttu-id="0e245-119">A ogni relazione è associato un indice di relazione.</span><span class="sxs-lookup"><span data-stu-id="0e245-119">Each partnership has an associated partnership index.</span></span> <span data-ttu-id="0e245-120">È possibile recuperare l'indice di relazione per un determinato dispositivo chiamando [IWMPSyncDevice:: Get \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span><span class="sxs-lookup"><span data-stu-id="0e245-120">You can retrieve the partnership index for a particular device by calling [IWMPSyncDevice::get\_partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span></span> <span data-ttu-id="0e245-121">Gli indici di partnership sono numerati da 1 a 16.</span><span class="sxs-lookup"><span data-stu-id="0e245-121">Partnership indices are numbered from 1 to 16.</span></span> <span data-ttu-id="0e245-122">Quando un particolare dispositivo non dispone di una relazione con Windows Media Player, **getPartnershipIndex** restituisce zero per l'indice.</span><span class="sxs-lookup"><span data-stu-id="0e245-122">When a particular device does not have a partnership with Windows Media Player, **getPartnershipIndex** returns zero for the index.</span></span>

<span data-ttu-id="0e245-123">È possibile recuperare lo stato della partnership di un determinato dispositivo chiamando [IWMPSyncDevice:: Get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) ed esaminando il valore [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperato.</span><span class="sxs-lookup"><span data-stu-id="0e245-123">You can retrieve the partnership status of a particular device by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="0e245-124">Windows Media Player consente la collaborazione con una libreria di un utente in un computer per ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e245-124">Windows Media Player allows one partnership with one user's library on one computer for each device.</span></span> <span data-ttu-id="0e245-125">Ciò significa che la creazione di una nuova partnership elimina qualsiasi relazione esistente che il dispositivo corrente potrebbe avere con un altro computer.</span><span class="sxs-lookup"><span data-stu-id="0e245-125">This means that creating a new partnership destroys any existing partnership the current device might have with another computer.</span></span> <span data-ttu-id="0e245-126">Per capire quando lo stato cambia per un dispositivo, è possibile ricevere l'evento **DeviceStatusChange** .</span><span class="sxs-lookup"><span data-stu-id="0e245-126">To know when the status changes for a device, you can receive the **DeviceStatusChange** event.</span></span>

<span data-ttu-id="0e245-127">Windows Media Player non è in grado di creare una relazione con un dispositivo con lo stato **wmpdsManualDevice**.</span><span class="sxs-lookup"><span data-stu-id="0e245-127">Windows Media Player cannot create a partnership with a device having the status **wmpdsManualDevice**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e245-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e245-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e245-129">**Informazioni sulla sincronizzazione dei dispositivi**</span><span class="sxs-lookup"><span data-stu-id="0e245-129">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="0e245-130">**Interfaccia IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="0e245-130">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="0e245-131">**Uso dei dispositivi portatili**</span><span class="sxs-lookup"><span data-stu-id="0e245-131">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




