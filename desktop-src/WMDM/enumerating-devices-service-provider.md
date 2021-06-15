---
title: Enumerazione dei dispositivi (WMDM)
description: Gestione dispositivi Windows Media gestisce una cache di dispositivi connessi. Informazioni su come Gestione dispositivi Windows Media gestisce o aggiorna la cache.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Gestione dispositivi Windows Media, enumerazione dei dispositivi
- Gestione dispositivi, enumerazione dei dispositivi
- guida per programmatori, enumerazione di dispositivi
- provider di servizi, enumerazione di dispositivi
- creazione di provider di servizi, enumerazione dei dispositivi
- enumerazione di dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9b2fd3a891e2c52710bd9a2f6d46a78e9eb238
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112067908"
---
# <a name="enumerating-devices-wmdm"></a><span data-ttu-id="1d123-110">Enumerazione dei dispositivi (WMDM)</span><span class="sxs-lookup"><span data-stu-id="1d123-110">Enumerating devices (WMDM)</span></span>

<span data-ttu-id="1d123-111">Gestione dispositivi Windows Media gestisce una cache di dispositivi connessi che viene aggiornata all'avvio di un'applicazione Gestione dispositivi Windows Media, quando un dispositivo Plug and Play (PnP) si connette o si disconnette o quando l'applicazione chiama [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span><span class="sxs-lookup"><span data-stu-id="1d123-111">Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span></span> <span data-ttu-id="1d123-112">Questa cache viene esposta all'applicazione quando chiama [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) o [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span><span class="sxs-lookup"><span data-stu-id="1d123-112">This cache is exposed to the application when it calls [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) or [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span></span> <span data-ttu-id="1d123-113">Ogni dispositivo viene esposto all'applicazione come [**interfaccia IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)</span><span class="sxs-lookup"><span data-stu-id="1d123-113">Each device is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="1d123-114">Se il provider di servizi è registrato per gestire i dispositivi PnP, Gestione dispositivi Windows Media sarà a conoscenza dell'elenco corrente dei dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="1d123-114">If the service provider is registered to handle PnP devices, Windows Media Device Manager will be aware of the current list of connected devices.</span></span> <span data-ttu-id="1d123-115">Se il provider di servizi è registrato per gestire dispositivi non PnP, il provider di servizi è responsabile dell'individuazione dei dispositivi collegati.</span><span class="sxs-lookup"><span data-stu-id="1d123-115">If the service provider is registered to handle non-PnP devices, the service provider is responsible for discovering attached devices.</span></span> <span data-ttu-id="1d123-116">Un provider di servizi può essere registrato solo per dispositivi PnP o non PnP, mai entrambi.</span><span class="sxs-lookup"><span data-stu-id="1d123-116">A service provider can only be registered for PnP or non-PnP devices, never both.</span></span>

<span data-ttu-id="1d123-117">Le azioni seguenti mostrano come Gestione dispositivi Windows Media gestisce o aggiorna la cache.</span><span class="sxs-lookup"><span data-stu-id="1d123-117">The following actions show how Windows Media Device Manager maintains or updates its cache.</span></span> <span data-ttu-id="1d123-118">Si noti che la cache non viene mai aggiornata quando un dispositivo non PnP si connette o si disconnette.</span><span class="sxs-lookup"><span data-stu-id="1d123-118">Notice that the cache is never updated when a non-PnP device connects or disconnects.</span></span>

<span data-ttu-id="1d123-119">Viene avviata un'applicazione Gestione dispositivi Windows Media</span><span class="sxs-lookup"><span data-stu-id="1d123-119">A Windows Media Device Manager application starts</span></span>

-   <span data-ttu-id="1d123-120">Gestione dispositivi Windows Media recupera un elenco di dispositivi PnP collegati dal sottosistema PnP e chiama [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) nel sp registrato per ogni dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="1d123-120">Windows Media Device Manager retrieves a list of attached PnP devices from the PnP subsystem, and calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on the SP registered for each connected device.</span></span> <span data-ttu-id="1d123-121">Individua il provider di servizi corretto tramite una query sul parametro del dispositivo WMDMSPCLSID per l'ID classe del provider di servizi responsabile del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d123-121">(It discovers the correct service provider by querying the WMDMSPCLSID device parameter for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="1d123-122">Per [altre informazioni, vedere](device-parameters.md) Parametri del dispositivo. Tutti i dispositivi restituiti vengono aggiunti alla cache dei dispositivi di Gestione dispositivi Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1d123-122">See [Device Parameters](device-parameters.md) for more information.) All devices returned are added to the Windows Media Device Manager cache of devices.</span></span>
-   <span data-ttu-id="1d123-123">Gestione dispositivi Windows Media trova tutti i provider di servizi non PnP registrati con esso e chiama [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) in ogni provider di servizi per ottenere un elenco di dispositivi da ognuno.</span><span class="sxs-lookup"><span data-stu-id="1d123-123">Windows Media Device Manager finds all non-PnP service providers registered with it and calls [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) on each service provider to get a list devices from each one.</span></span> <span data-ttu-id="1d123-124">Tutti i dispositivi restituiti vengono aggiunti alla cache.</span><span class="sxs-lookup"><span data-stu-id="1d123-124">All devices returned are added to the cache.</span></span>

<span data-ttu-id="1d123-125">L'applicazione chiama IWMDeviceManager/2::EnumDevices/2</span><span class="sxs-lookup"><span data-stu-id="1d123-125">The application calls IWMDeviceManager/2::EnumDevices/2</span></span>

-   <span data-ttu-id="1d123-126">Gestione dispositivi Windows Media restituisce il relativo elenco di dispositivi memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="1d123-126">Windows Media Device Manager returns its cached device list.</span></span>

<span data-ttu-id="1d123-127">Un dispositivo PnP si connette</span><span class="sxs-lookup"><span data-stu-id="1d123-127">A PnP device connects</span></span>

-   <span data-ttu-id="1d123-128">Gestione dispositivi Windows Media trova il provider di servizi pertinente e chiama **IMDServiceProvider2::CreateDevice** e aggiunge il dispositivo alla cache.</span><span class="sxs-lookup"><span data-stu-id="1d123-128">Windows Media Device Manager finds the relevant service provider and calls **IMDServiceProvider2::CreateDevice**, and adds the device to its cache.</span></span>
-   <span data-ttu-id="1d123-129">Se l'applicazione implementa [**IWMDMNotification,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)Gestione dispositivi Windows Media chiama [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) con una notifica di arrivo.</span><span class="sxs-lookup"><span data-stu-id="1d123-129">If the application implements [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Device Manager calls [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) with an arrival notification.</span></span>

<span data-ttu-id="1d123-130">Un dispositivo PnP si disconnette</span><span class="sxs-lookup"><span data-stu-id="1d123-130">A PnP device disconnects</span></span>

-   <span data-ttu-id="1d123-131">Gestione dispositivi Windows Media rimuove l'elemento dalla cache.</span><span class="sxs-lookup"><span data-stu-id="1d123-131">Windows Media Device Manager removes the item from its cache.</span></span>
-   <span data-ttu-id="1d123-132">Se l'applicazione implementa IWMDMNotification, Gestione dispositivi Windows Media chiama IWMDMNotification::WMDMMessage con una notifica di partenza.</span><span class="sxs-lookup"><span data-stu-id="1d123-132">If the application implements IWMDMNotification, Windows Media Device Manager calls IWMDMNotification::WMDMMessage with a departure notification.</span></span>

<span data-ttu-id="1d123-133">L'applicazione chiama IWMDeviceManager2::Reinitialize</span><span class="sxs-lookup"><span data-stu-id="1d123-133">The application calls IWMDeviceManager2::Reinitialize</span></span>

-   <span data-ttu-id="1d123-134">Aggiorna la cache con tutti i dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="1d123-134">Refreshes the cache with all connected devices.</span></span>

<span data-ttu-id="1d123-135">Un dispositivo non PnP si connette o si disconnette</span><span class="sxs-lookup"><span data-stu-id="1d123-135">A non-PnP device connects or disconnects</span></span>

-   <span data-ttu-id="1d123-136">Gestione dispositivi Windows Media non è informato dell'arrivo o della partenza e non prende alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="1d123-136">Windows Media Device Manager is not informed of the arrival or departure, and takes no action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d123-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d123-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d123-138">**Creazione di un provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="1d123-138">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




