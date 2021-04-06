---
title: Enumerazione dei dispositivi (WMDM)
description: Enumerazione dei dispositivi
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Media Gestione dispositivi, enumerazione dei dispositivi
- Gestione dispositivi, enumerazione dei dispositivi
- Guida per programmatori, enumerazione dei dispositivi
- provider di servizi, enumerazione dei dispositivi
- creazione di provider di servizi, enumerazione dei dispositivi
- Enumerazione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316b87f6ad3f5680e0c22da832da7b1efec24629
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719552"
---
# <a name="enumerating-devices-wmdm"></a><span data-ttu-id="5528c-109">Enumerazione dei dispositivi (WMDM)</span><span class="sxs-lookup"><span data-stu-id="5528c-109">Enumerating devices (WMDM)</span></span>

<span data-ttu-id="5528c-110">Windows Media Gestione dispositivi gestisce una cache di dispositivi connessi che viene aggiornata all'avvio di un'applicazione Windows Media Gestione dispositivi, quando un dispositivo Plug and Play (PnP) si connette o si disconnette o quando l'applicazione chiama [**IWMDeviceManager2:: Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span><span class="sxs-lookup"><span data-stu-id="5528c-110">Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span></span> <span data-ttu-id="5528c-111">Questa cache viene esposta all'applicazione quando chiama [**IWMDeviceManager:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) o [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span><span class="sxs-lookup"><span data-stu-id="5528c-111">This cache is exposed to the application when it calls [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) or [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span></span> <span data-ttu-id="5528c-112">Ogni dispositivo viene esposto all'applicazione come un'interfaccia [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="5528c-112">Each device is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="5528c-113">Se il provider di servizi è registrato per gestire i dispositivi PnP, Windows Media Gestione dispositivi riconoscerà l'elenco corrente dei dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="5528c-113">If the service provider is registered to handle PnP devices, Windows Media Device Manager will be aware of the current list of connected devices.</span></span> <span data-ttu-id="5528c-114">Se il provider di servizi è registrato per gestire dispositivi non PnP, il provider di servizi è responsabile dell'individuazione dei dispositivi collegati.</span><span class="sxs-lookup"><span data-stu-id="5528c-114">If the service provider is registered to handle non-PnP devices, the service provider is responsible for discovering attached devices.</span></span> <span data-ttu-id="5528c-115">Un provider di servizi può essere registrato solo per dispositivi PnP o non PnP, mai entrambi.</span><span class="sxs-lookup"><span data-stu-id="5528c-115">A service provider can only be registered for PnP or non-PnP devices, never both.</span></span>

<span data-ttu-id="5528c-116">Le azioni seguenti illustrano come Windows Media Gestione dispositivi gestisce o aggiorna la cache.</span><span class="sxs-lookup"><span data-stu-id="5528c-116">The following actions show how Windows Media Device Manager maintains or updates its cache.</span></span> <span data-ttu-id="5528c-117">Si noti che la cache non viene mai aggiornata quando un dispositivo non PnP si connette o si disconnette.</span><span class="sxs-lookup"><span data-stu-id="5528c-117">Notice that the cache is never updated when a non-PnP device connects or disconnects.</span></span>

<span data-ttu-id="5528c-118">Viene avviata un'applicazione Windows Media Gestione dispositivi</span><span class="sxs-lookup"><span data-stu-id="5528c-118">A Windows Media Device Manager application starts</span></span>

-   <span data-ttu-id="5528c-119">Windows Media Gestione dispositivi recupera un elenco di dispositivi PnP collegati dal sottosistema PnP e chiama [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) sul SP registrato per ogni dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="5528c-119">Windows Media Device Manager retrieves a list of attached PnP devices from the PnP subsystem, and calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on the SP registered for each connected device.</span></span> <span data-ttu-id="5528c-120">(Individua il provider di servizi corretto eseguendo una query sul parametro di dispositivo WMDMSPCLSID per l'ID di classe del provider di servizi responsabile del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5528c-120">(It discovers the correct service provider by querying the WMDMSPCLSID device parameter for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="5528c-121">Per ulteriori informazioni, vedere [parametri del dispositivo](device-parameters.md) . Tutti i dispositivi restituiti vengono aggiunti alla cache Windows Media Gestione dispositivi dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="5528c-121">See [Device Parameters](device-parameters.md) for more information.) All devices returned are added to the Windows Media Device Manager cache of devices.</span></span>
-   <span data-ttu-id="5528c-122">Windows Media Gestione dispositivi trova tutti i provider di servizi non PnP registrati e chiama [**IMDServiceProvider:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) in ogni provider di servizi per ottenere un elenco di dispositivi da ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="5528c-122">Windows Media Device Manager finds all non-PnP service providers registered with it and calls [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) on each service provider to get a list devices from each one.</span></span> <span data-ttu-id="5528c-123">Tutti i dispositivi restituiti vengono aggiunti alla cache.</span><span class="sxs-lookup"><span data-stu-id="5528c-123">All devices returned are added to the cache.</span></span>

<span data-ttu-id="5528c-124">L'applicazione chiama IWMDeviceManager/2:: EnumDevices/2</span><span class="sxs-lookup"><span data-stu-id="5528c-124">The application calls IWMDeviceManager/2::EnumDevices/2</span></span>

-   <span data-ttu-id="5528c-125">Windows Media Gestione dispositivi restituisce l'elenco dei dispositivi memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="5528c-125">Windows Media Device Manager returns its cached device list.</span></span>

<span data-ttu-id="5528c-126">Connessione di un dispositivo PnP</span><span class="sxs-lookup"><span data-stu-id="5528c-126">A PnP device connects</span></span>

-   <span data-ttu-id="5528c-127">Windows Media Gestione dispositivi trova il provider di servizi pertinente e chiama **IMDServiceProvider2:: CreateDevice** e aggiunge il dispositivo alla relativa cache.</span><span class="sxs-lookup"><span data-stu-id="5528c-127">Windows Media Device Manager finds the relevant service provider and calls **IMDServiceProvider2::CreateDevice**, and adds the device to its cache.</span></span>
-   <span data-ttu-id="5528c-128">Se l'applicazione implementa [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Gestione dispositivi chiama [**IWMDMNotification:: WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) con una notifica di arrivo.</span><span class="sxs-lookup"><span data-stu-id="5528c-128">If the application implements [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Device Manager calls [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) with an arrival notification.</span></span>

<span data-ttu-id="5528c-129">Un dispositivo PnP si disconnette</span><span class="sxs-lookup"><span data-stu-id="5528c-129">A PnP device disconnects</span></span>

-   <span data-ttu-id="5528c-130">Windows Media Gestione dispositivi rimuove l'elemento dalla relativa cache.</span><span class="sxs-lookup"><span data-stu-id="5528c-130">Windows Media Device Manager removes the item from its cache.</span></span>
-   <span data-ttu-id="5528c-131">Se l'applicazione implementa IWMDMNotification, Windows Media Gestione dispositivi chiama IWMDMNotification:: WMDMMessage con una notifica di partenza.</span><span class="sxs-lookup"><span data-stu-id="5528c-131">If the application implements IWMDMNotification, Windows Media Device Manager calls IWMDMNotification::WMDMMessage with a departure notification.</span></span>

<span data-ttu-id="5528c-132">L'applicazione chiama IWMDeviceManager2:: Reinitialize</span><span class="sxs-lookup"><span data-stu-id="5528c-132">The application calls IWMDeviceManager2::Reinitialize</span></span>

-   <span data-ttu-id="5528c-133">Aggiorna la cache con tutti i dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="5528c-133">Refreshes the cache with all connected devices.</span></span>

<span data-ttu-id="5528c-134">Un dispositivo non PnP si connette o si disconnette</span><span class="sxs-lookup"><span data-stu-id="5528c-134">A non-PnP device connects or disconnects</span></span>

-   <span data-ttu-id="5528c-135">Windows Media Gestione dispositivi non viene informato dell'arrivo o della partenza e non esegue alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="5528c-135">Windows Media Device Manager is not informed of the arrival or departure, and takes no action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5528c-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5528c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5528c-137">**Creazione di un provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="5528c-137">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




