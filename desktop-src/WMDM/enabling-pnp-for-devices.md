---
title: Abilitazione di PnP per i dispositivi
description: Abilitazione di PnP per i dispositivi
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Media Gestione dispositivi, dispositivi PnP
- Dispositivi Gestione dispositivi, PnP
- Guida per programmatori, dispositivi PnP
- provider di servizi, dispositivi PnP
- creazione di provider di servizi, dispositivi PnP
- Dispositivi PnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855890"
---
# <a name="enabling-pnp-for-devices"></a><span data-ttu-id="ff816-109">Abilitazione di PnP per i dispositivi</span><span class="sxs-lookup"><span data-stu-id="ff816-109">Enabling PnP for Devices</span></span>

<span data-ttu-id="ff816-110">Windows Media Gestione dispositivi monitora le notifiche relative all'arrivo e alla rimozione dei dispositivi che annunciano un'interfaccia del dispositivo lettore audio portatile.</span><span class="sxs-lookup"><span data-stu-id="ff816-110">Windows Media Device Manager monitors arrival and removal notifications of devices that advertise a Portable Audio Player device interface.</span></span> <span data-ttu-id="ff816-111">All'arrivo di un dispositivo di questo tipo, Windows Media Gestione dispositivi esegue una query su un parametro di dispositivo denominato *WMDMSPCLSID* per l'ID di classe del provider di servizi responsabile del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff816-111">On the arrival of such a device, Windows Media Device Manager queries a device parameter named *WMDMSPCLSID* for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="ff816-112">Windows Media Gestione dispositivi chiama [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) su questo provider di servizi per creare un oggetto dispositivo, esposto all'applicazione come oggetto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="ff816-112">Windows Media Device Manager calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on this service provider to create a device object, which is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

<span data-ttu-id="ff816-113">Un provider di servizi può gestire dispositivi PnP o dispositivi non PnP. non è in grado di gestire entrambi i tipi.</span><span class="sxs-lookup"><span data-stu-id="ff816-113">A service provider can either handle PnP devices, or non-PnP devices; it cannot handle both types.</span></span>

<span data-ttu-id="ff816-114">Per consentire a un dispositivo di usare il meccanismo precedente (e quindi abilitare le notifiche di arrivo e rimozione per il dispositivo in Windows Media Gestione dispositivi applicazioni), devono essere soddisfatti i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff816-114">For a device to work with the preceding mechanism (and thus enable arrival and removal notifications for the device under Windows Media Device Manager applications), the following requirements must be met:</span></span>

-   <span data-ttu-id="ff816-115">Il driver di dispositivo di questo dispositivo deve annunciare l'interfaccia del dispositivo Windows Media Gestione dispositivi Portable Audio Player.</span><span class="sxs-lookup"><span data-stu-id="ff816-115">The device driver of this device must advertise the Windows Media Device Manager Portable Audio Player device interface.</span></span> <span data-ttu-id="ff816-116">Il GUID per questa interfaccia del dispositivo è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="ff816-116">The GUID for this device interface is defined as:</span></span>

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > <span data-ttu-id="ff816-117">Un dispositivo non deve annunciare questa interfaccia se il dispositivo annuncia l'interfaccia del volume (definita come VolumeClassGuid o GUID \_ DEVINTERFACE \_ volume in winioctl. h).</span><span class="sxs-lookup"><span data-stu-id="ff816-117">A device should not advertise this interface if the device advertises the Volume interface (defined as VolumeClassGuid or GUID\_DEVINTERFACE\_VOLUME in winioctl.h).</span></span> <span data-ttu-id="ff816-118">Se il dispositivo annuncia l'interfaccia del volume, è già abilitato per la funzionalità PnP in Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="ff816-118">If the device advertises the Volume Interface, it is already PnP-enabled under Windows Media Device Manager.</span></span>

     

    <span data-ttu-id="ff816-119">-AND/OR-</span><span class="sxs-lookup"><span data-stu-id="ff816-119">-AND/OR-</span></span>

    <span data-ttu-id="ff816-120">È necessario creare una nuova sottochiave del registro di sistema per il provider di servizi nella sottochiave HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows Media Gestione dispositivi \\ KnownDevices.</span><span class="sxs-lookup"><span data-stu-id="ff816-120">A new registry subkey for the service provider must be created inside the subkey HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\KnownDevices.</span></span> <span data-ttu-id="ff816-121">Questa chiave deve avere il nome del provider di servizi e deve avere le due voci di \_ valore reg SZ seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff816-121">This key should have the name of your service provider and must have the following two Reg\_SZ value entries:</span></span>

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   <span data-ttu-id="ff816-122">Il dispositivo deve avere un parametro di dispositivo denominato WMDMSPCLSID.</span><span class="sxs-lookup"><span data-stu-id="ff816-122">The device must have a device parameter named WMDMSPCLSID.</span></span> <span data-ttu-id="ff816-123">Il valore di questo parametro deve essere impostato come CLSID del provider di servizi in un formato stringa.</span><span class="sxs-lookup"><span data-stu-id="ff816-123">The value of this parameter should be set as the CLSID of the service provider in a string form.</span></span> <span data-ttu-id="ff816-124">Per altre informazioni sui parametri del dispositivo, vedere [parametri del dispositivo](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ff816-124">For more information about device parameters, see [Device Parameters](device-parameters.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="ff816-125">Il valore del parametro deve essere CLSID, non il ProgID del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="ff816-125">The parameter value must be the CLSID, not the ProgID of the service provider.</span></span>

     

-   <span data-ttu-id="ff816-126">Il provider di servizi per questo dispositivo deve implementare l'interfaccia IMDServiceProvider2.</span><span class="sxs-lookup"><span data-stu-id="ff816-126">The service provider for this device must implement the IMDServiceProvider2 interface.</span></span>
-   <span data-ttu-id="ff816-127">La chiave del provider di servizi in HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows Media Gestione dispositivi \\ plugins \\ SP \\ spName deve contenere il valore DWORD seguente</span><span class="sxs-lookup"><span data-stu-id="ff816-127">The service provider key under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\Plugins\\SP\\SPName must contain the following DWORD value</span></span>
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a><span data-ttu-id="ff816-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff816-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff816-129">**Creazione di un provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="ff816-129">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




