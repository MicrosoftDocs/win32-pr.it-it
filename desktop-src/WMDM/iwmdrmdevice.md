---
title: Interfaccia IWMDRMDevice
description: Questa interfaccia non è progettata per essere implementata da un provider di servizi, ma viene fornita ai fini della documentazione completa. L'interfaccia IWMDRMDevice consente a un provider di contenuti protetto di comunicare con i dispositivi che usano Windows Media DRM 10 per i dispositivi portatili.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, descritta
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337927"
---
# <a name="iwmdrmdevice-interface"></a><span data-ttu-id="7ea91-105">Interfaccia IWMDRMDevice</span><span class="sxs-lookup"><span data-stu-id="7ea91-105">IWMDRMDevice interface</span></span>

<span data-ttu-id="7ea91-106">Questa interfaccia non è progettata per essere implementata da un provider di servizi, ma viene fornita ai fini della documentazione completa.</span><span class="sxs-lookup"><span data-stu-id="7ea91-106">This interface is not intended to be implemented by a service provider, but is provided for purposes of complete documentation.</span></span>

<span data-ttu-id="7ea91-107">L'interfaccia **IWMDRMDevice** consente a un provider di contenuti protetto di comunicare con i dispositivi che usano Windows Media DRM 10 per i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="7ea91-107">The **IWMDRMDevice** interface enables a secure content provider to communicate with devices that use Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="members"></a><span data-ttu-id="7ea91-108">Membri</span><span class="sxs-lookup"><span data-stu-id="7ea91-108">Members</span></span>

<span data-ttu-id="7ea91-109">L'interfaccia **IWMDRMDevice** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7ea91-109">The **IWMDRMDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7ea91-110">**IWMDRMDevice** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7ea91-110">**IWMDRMDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="7ea91-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="7ea91-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7ea91-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="7ea91-112">Methods</span></span>

<span data-ttu-id="7ea91-113">L'interfaccia **IWMDRMDevice** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7ea91-113">The **IWMDRMDevice** interface has these methods.</span></span>



| <span data-ttu-id="7ea91-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="7ea91-114">Method</span></span>                                                                  | <span data-ttu-id="7ea91-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ea91-115">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ea91-116">**CleanDataStore**</span><span class="sxs-lookup"><span data-stu-id="7ea91-116">**CleanDataStore**</span></span>](iwmdrmdevice-cleandatastore.md)                   | <span data-ttu-id="7ea91-117">Avvia il processo di pulizia dell'archivio dati DRM sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ea91-117">Starts the process of cleaning the DRM data store on the device.</span></span><br/>                  |
| [<span data-ttu-id="7ea91-118">**GetDeviceCertificate**</span><span class="sxs-lookup"><span data-stu-id="7ea91-118">**GetDeviceCertificate**</span></span>](iwmdrmdevice-getdevicecertificate.md)       | <span data-ttu-id="7ea91-119">Recupera il certificato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ea91-119">Retrieves the device certificate.</span></span><br/>                                                 |
| [<span data-ttu-id="7ea91-120">**GetMeterChallenge**</span><span class="sxs-lookup"><span data-stu-id="7ea91-120">**GetMeterChallenge**</span></span>](iwmdrmdevice-getmeterchallenge.md)             | <span data-ttu-id="7ea91-121">Recupera la richiesta di misurazione.</span><span class="sxs-lookup"><span data-stu-id="7ea91-121">Retrieves the metering challenge.</span></span><br/>                                                 |
| [<span data-ttu-id="7ea91-122">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="7ea91-122">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)                   | <span data-ttu-id="7ea91-123">Recupera il clock protetto.</span><span class="sxs-lookup"><span data-stu-id="7ea91-123">Retrieves the secure clock.</span></span><br/>                                                       |
| [<span data-ttu-id="7ea91-124">**GetSecureClockChallenge**</span><span class="sxs-lookup"><span data-stu-id="7ea91-124">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md) | <span data-ttu-id="7ea91-125">Recupera la richiesta di clock sicura.</span><span class="sxs-lookup"><span data-stu-id="7ea91-125">Retrieves the secure clock challenge.</span></span><br/>                                             |
| [<span data-ttu-id="7ea91-126">**Getsynct**</span><span class="sxs-lookup"><span data-stu-id="7ea91-126">**GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)                         | <span data-ttu-id="7ea91-127">Recupera l'elenco di sincronizzazione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="7ea91-127">Retrieves the license synchronization list.</span></span><br/>                                       |
| [<span data-ttu-id="7ea91-128">**IsWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="7ea91-128">**IsWMDRMDevice**</span></span>](iwmdrmdevice-iswmdrmdevice.md)                     | <span data-ttu-id="7ea91-129">Determina se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="7ea91-129">Determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span><br/> |
| [<span data-ttu-id="7ea91-130">**Viene chiamato SetLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="7ea91-130">**SetLicenseResponse**</span></span>](iwmdrmdevice-setlicenseresponse.md)           | <span data-ttu-id="7ea91-131">Imposta la risposta della licenza.</span><span class="sxs-lookup"><span data-stu-id="7ea91-131">Sets the license response.</span></span><br/>                                                        |
| [<span data-ttu-id="7ea91-132">**SetMeterResponse**</span><span class="sxs-lookup"><span data-stu-id="7ea91-132">**SetMeterResponse**</span></span>](iwmdrmdevice-setmeterresponse.md)               | <span data-ttu-id="7ea91-133">Imposta la risposta di misurazione.</span><span class="sxs-lookup"><span data-stu-id="7ea91-133">Sets the metering response.</span></span><br/>                                                       |
| [<span data-ttu-id="7ea91-134">**SetSecureClockResponse**</span><span class="sxs-lookup"><span data-stu-id="7ea91-134">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)   | <span data-ttu-id="7ea91-135">Imposta la risposta del clock protetto.</span><span class="sxs-lookup"><span data-stu-id="7ea91-135">Sets the secure clock response.</span></span><br/>                                                   |



 

## <a name="see-also"></a><span data-ttu-id="7ea91-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ea91-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea91-137">**Interfacce per i provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="7ea91-137">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> </dl>

 

