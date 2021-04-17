---
title: Interfaccia IWMDRMDeviceApp
description: L'interfaccia IWMDRMDeviceApp consente a un'applicazione di misurare, sincronizzare le licenze e aggiornare i componenti DRM di un dispositivo.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi, descritta
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300308"
---
# <a name="iwmdrmdeviceapp-interface"></a><span data-ttu-id="e7565-105">Interfaccia IWMDRMDeviceApp</span><span class="sxs-lookup"><span data-stu-id="e7565-105">IWMDRMDeviceApp interface</span></span>

<span data-ttu-id="e7565-106">\[La funzionalità DRM di Windows Media è deprecata e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e7565-106">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="e7565-107">In alternativa, usare [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="e7565-107">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="e7565-108">L'interfaccia **IWMDRMDeviceApp** consente a un'applicazione di misurare, sincronizzare le licenze e aggiornare i componenti DRM di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7565-108">The **IWMDRMDeviceApp** interface enables an application to meter, synchronize licenses, and update a device's DRM components.</span></span> <span data-ttu-id="e7565-109">Questa interfaccia funziona solo con i dispositivi che supportano Windows Media DRM 10 per i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="e7565-109">This interface will only work with devices that support Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="e7565-110">Per ottenere questa interfaccia, chiamare **CoCreateInstance**, passando CLSID \_ WMDRMDeviceApp.</span><span class="sxs-lookup"><span data-stu-id="e7565-110">To get this interface, call **CoCreateInstance**, passing in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="e7565-111">Questa interfaccia viene definita nel file di intestazione compilato da WMDRMDeviceApp. idl.</span><span class="sxs-lookup"><span data-stu-id="e7565-111">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="e7565-112">Questa intestazione **\# include** s "WMDM. h".</span><span class="sxs-lookup"><span data-stu-id="e7565-112">This header **\#include** s "wmdm.h".</span></span> <span data-ttu-id="e7565-113">Potrebbe essere necessario modificare il nome del file in modo che corrisponda all'intestazione compilata da WMDM. idl.</span><span class="sxs-lookup"><span data-stu-id="e7565-113">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="e7565-114">Membri</span><span class="sxs-lookup"><span data-stu-id="e7565-114">Members</span></span>

<span data-ttu-id="e7565-115">L'interfaccia **IWMDRMDeviceApp** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e7565-115">The **IWMDRMDeviceApp** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e7565-116">**IWMDRMDeviceApp** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e7565-116">**IWMDRMDeviceApp** also has these types of members:</span></span>

-   [<span data-ttu-id="e7565-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="e7565-117">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e7565-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="e7565-118">Methods</span></span>

<span data-ttu-id="e7565-119">L'interfaccia **IWMDRMDeviceApp** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e7565-119">The **IWMDRMDeviceApp** interface has these methods.</span></span>



| <span data-ttu-id="e7565-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="e7565-120">Method</span></span>                                                                   | <span data-ttu-id="e7565-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7565-121">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7565-122">**AcquireDeviceData**</span><span class="sxs-lookup"><span data-stu-id="e7565-122">**AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)           | <span data-ttu-id="e7565-123">Inizializza o reimposta un clock sicuro del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e7565-123">Initializes or resets a device secure clock</span></span><br/>                                                                                     |
| [<span data-ttu-id="e7565-124">**GenerateMeterChallenge**</span><span class="sxs-lookup"><span data-stu-id="e7565-124">**GenerateMeterChallenge**</span></span>](iwmdrmdeviceapp-generatemeterchallenge.md) | <span data-ttu-id="e7565-125">Acquisisce i dati di misurazione da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7565-125">Acquires metering data from a device.</span></span><br/>                                                                                           |
| [<span data-ttu-id="e7565-126">**ProcessMeterResponse**</span><span class="sxs-lookup"><span data-stu-id="e7565-126">**ProcessMeterResponse**</span></span>](iwmdrmdeviceapp-processmeterresponse.md)     | <span data-ttu-id="e7565-127">Reimposta alcuni o tutti i conteggi di misurazione in un dispositivo, dopo che i dati del dispositivo sono stati inviati ed elaborati dal server.</span><span class="sxs-lookup"><span data-stu-id="e7565-127">Resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span><br/> |
| [<span data-ttu-id="e7565-128">**QueryDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="e7565-128">**QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)           | <span data-ttu-id="e7565-129">Esegue una query su un dispositivo per lo stato e le funzionalità DRM correnti.</span><span class="sxs-lookup"><span data-stu-id="e7565-129">Queries a device for its current DRM status and capabilities.</span></span><br/>                                                                   |
| [<span data-ttu-id="e7565-130">**SynchronizeLicenses**</span><span class="sxs-lookup"><span data-stu-id="e7565-130">**SynchronizeLicenses**</span></span>](iwmdrmdeviceapp-synchronizelicenses.md)       | <span data-ttu-id="e7565-131">Aggiorna le licenze in un dispositivo quando la scadenza è prossima.</span><span class="sxs-lookup"><span data-stu-id="e7565-131">Updates licenses on a device when they are close to expiring.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="e7565-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7565-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7565-133">**Gestione del contenuto protetto nell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="e7565-133">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="e7565-134">**Interfacce per le applicazioni**</span><span class="sxs-lookup"><span data-stu-id="e7565-134">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="e7565-135">**Misurazione dell'utilizzo del contenuto**</span><span class="sxs-lookup"><span data-stu-id="e7565-135">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

