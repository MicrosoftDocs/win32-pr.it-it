---
description: Informazioni sull'API MMDevice
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Informazioni sull'API MMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748778"
---
# <a name="about-mmdevice-api"></a><span data-ttu-id="61027-103">Informazioni sull'API MMDevice</span><span class="sxs-lookup"><span data-stu-id="61027-103">About MMDevice API</span></span>

<span data-ttu-id="61027-104">L'API Windows Multimedia Device (MMDevice) consente ai client audio di individuare i [dispositivi dell'endpoint audio](audio-endpoint-devices.md), determinarne le funzionalità e creare istanze di driver per tali dispositivi.</span><span class="sxs-lookup"><span data-stu-id="61027-104">The Windows Multimedia Device (MMDevice) API enables audio clients to discover [audio endpoint devices](audio-endpoint-devices.md), determine their capabilities, and create driver instances for those devices.</span></span>

<span data-ttu-id="61027-105">Il file di intestazione mmdeviceapi. h definisce le interfacce nell'API MMDevice.</span><span class="sxs-lookup"><span data-stu-id="61027-105">Header file Mmdeviceapi.h defines the interfaces in the MMDevice API.</span></span>

<span data-ttu-id="61027-106">L'API MMDevice è costituita da diverse interfacce.</span><span class="sxs-lookup"><span data-stu-id="61027-106">The MMDevice API consists of several interfaces.</span></span> <span data-ttu-id="61027-107">Il primo è l'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="61027-107">The first of these is the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="61027-108">Per accedere alle interfacce nell'API MMDevice, un client ottiene un riferimento all'interfaccia **IMMDeviceEnumerator** di un oggetto enumeratore del dispositivo chiamando la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , come illustrato nel frammento di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="61027-108">To access the interfaces in the MMDevice API, a client obtains a reference to the **IMMDeviceEnumerator** interface of a device-enumerator object by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, as shown in the following code fragment:</span></span>


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



<span data-ttu-id="61027-109">Nel frammento di codice precedente, CLSID \_ MMDeviceEnumerator ed IID \_ IMMDeviceEnumerator sono i valori GUID collegati come attributi all'oggetto della classe **MMDeviceEnumerator** e all'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="61027-109">In the preceding code fragment, CLSID\_MMDeviceEnumerator and IID\_IMMDeviceEnumerator are the GUID values that are attached as attributes to the **MMDeviceEnumerator** class object and to the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="61027-110">La chiamata [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) passa questi valori per riferimento.</span><span class="sxs-lookup"><span data-stu-id="61027-110">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call passes these values by reference.</span></span> <span data-ttu-id="61027-111">`hr`La variabile è di tipo **HRESULT** e la variabile `pEnumerator` è un puntatore all'interfaccia **IMMDeviceEnumerator** di un oggetto enumeratore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61027-111">Variable `hr` is of type **HRESULT**, and variable `pEnumerator` is a pointer to the **IMMDeviceEnumerator** interface of a device-enumerator object.</span></span> <span data-ttu-id="61027-112">**IMMDeviceEnumerator** fornisce metodi per l'enumerazione di dispositivi endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="61027-112">**IMMDeviceEnumerator** provides methods for enumerating audio endpoint devices.</span></span> <span data-ttu-id="61027-113">Per informazioni sull'operatore **\_ \_ uuidof** , sulla funzione **CoCreateInstance** e sulle costanti CLSCTX \_ *xxx* , vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="61027-113">For information about the **\_\_uuidof** operator, the **CoCreateInstance** function, and the CLSCTX\_*Xxx* constants, see the Windows SDK documentation.</span></span>

<span data-ttu-id="61027-114">Tramite l'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) , il client può ottenere riferimenti ad altre interfacce nell'API MMDevice.</span><span class="sxs-lookup"><span data-stu-id="61027-114">Through the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, the client can obtain references to the other interfaces in the MMDevice API.</span></span> <span data-ttu-id="61027-115">L'API MMDevice implementa le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="61027-115">The MMDevice API implements the following interfaces.</span></span>



| <span data-ttu-id="61027-116">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="61027-116">Interface</span></span>                                          | <span data-ttu-id="61027-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61027-117">Description</span></span>                                     |
|----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="61027-118">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="61027-118">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | <span data-ttu-id="61027-119">Rappresenta un dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="61027-119">Represents an audio device.</span></span>                     |
| [<span data-ttu-id="61027-120">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="61027-120">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | <span data-ttu-id="61027-121">Rappresenta una raccolta di dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="61027-121">Represents a collection of audio devices.</span></span>       |
| [<span data-ttu-id="61027-122">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="61027-122">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | <span data-ttu-id="61027-123">Fornisce metodi per l'enumerazione dei dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="61027-123">Provides methods for enumerating audio devices.</span></span> |
| [<span data-ttu-id="61027-124">**IMMEndpoint**</span><span class="sxs-lookup"><span data-stu-id="61027-124">**IMMEndpoint**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | <span data-ttu-id="61027-125">Rappresenta un dispositivo endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="61027-125">Represents an audio endpoint device.</span></span>            |



 

<span data-ttu-id="61027-126">Inoltre, i client dell'API MMDevice che richiedono la notifica delle modifiche di stato nei dispositivi dell'endpoint audio devono implementare la seguente interfaccia.</span><span class="sxs-lookup"><span data-stu-id="61027-126">In addition, clients of the MMDevice API that require notification of status changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="61027-127">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="61027-127">Interface</span></span>                                              | <span data-ttu-id="61027-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61027-128">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61027-129">**IMMNotificationClient**</span><span class="sxs-lookup"><span data-stu-id="61027-129">**IMMNotificationClient**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | <span data-ttu-id="61027-130">Fornisce notifiche quando viene aggiunto o rimosso un dispositivo endpoint audio, quando lo stato o le proprietà di un dispositivo cambiano oppure quando viene apportata una modifica al ruolo predefinito assegnato a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61027-130">Provides notifications when an audio endpoint device is added or removed, when the state or properties of a device change, or when there is a change in the default role assigned to a device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="61027-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61027-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61027-132">Dispositivi endpoint audio</span><span class="sxs-lookup"><span data-stu-id="61027-132">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="61027-133">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="61027-133">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 
