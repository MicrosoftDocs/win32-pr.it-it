---
description: In Windows 7, le API della piattaforma di alto livello che usano le API audio principali, ad esempio Media Foundation, DirectSound e Wave, implementano la funzionalità di routing dei flussi gestendo il passaggio da un dispositivo esistente a un nuovo endpoint audio predefinito.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Recupero dell'endpoint del dispositivo per il routing del flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877850"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a><span data-ttu-id="54587-103">Recupero dell'endpoint del dispositivo per il routing del flusso</span><span class="sxs-lookup"><span data-stu-id="54587-103">Getting the Device Endpoint for Stream Routing</span></span>

<span data-ttu-id="54587-104">In Windows 7, le API della piattaforma di alto livello che usano le API audio principali, ad esempio Media Foundation, DirectSound e Wave, implementano la funzionalità di routing dei flussi gestendo il passaggio da un dispositivo esistente a un nuovo endpoint audio predefinito.</span><span class="sxs-lookup"><span data-stu-id="54587-104">In Windows 7, high-level platform APIs that use Core Audio APIs such as Media Foundation, DirectSound, and Wave APIs, implement the stream routing feature by handling stream switching from an existing device to a new default audio endpoint.</span></span> <span data-ttu-id="54587-105">Le applicazioni multimediali che usano queste API (ad esempio, un'applicazione che attiva un oggetto **IDirectSound** o **IBaseFilter** su un oggetto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) ) usano il comportamento di routing del flusso senza apportare alcuna modifica all'origine.</span><span class="sxs-lookup"><span data-stu-id="54587-105">Media applications that use these APIs (for example, an application activating an **IDirectSound** or **IBaseFilter** object on an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object) use the stream routing behavior without any modifications to the source.</span></span>

<span data-ttu-id="54587-106">Le API di alto livello implementano il routing del flusso per l'endpoint del dispositivo ottenuto tramite [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="54587-106">The high-level APIs implement stream routing for the device endpoint that is obtained through [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="54587-107">Se un'applicazione esegue il flusso al dispositivo predefinito, la funzionalità di routing del flusso funziona come definito.</span><span class="sxs-lookup"><span data-stu-id="54587-107">If an application streams to the default device, the stream routing feature operates as defined.</span></span> <span data-ttu-id="54587-108">I flussi non vengono passati al nuovo dispositivo se vengono recuperati da qualsiasi altro meccanismo anche se corrisponde al dispositivo predefinito.</span><span class="sxs-lookup"><span data-stu-id="54587-108">Streams are not switched to the new device if it is retrieved by any other mechanism even if it is the same as the default device.</span></span>

<span data-ttu-id="54587-109">Un'applicazione multimediale che usa direttamente le API audio principali (client WASAPI) può fornire un'implementazione di routing del flusso personalizzata per qualsiasi dispositivo di rendering o acquisizione.</span><span class="sxs-lookup"><span data-stu-id="54587-109">A media application that uses Core Audio APIs directly (WASAPI client) can provide a custom stream routing implementation for any rendering or capture device.</span></span> <span data-ttu-id="54587-110">Un client WASAPI può replicare il implementazione fornito dalle API di alto livello limitandosi ai flussi aperti nei dispositivi impostati come dispositivo predefinito.</span><span class="sxs-lookup"><span data-stu-id="54587-110">A WASAPI client can replicate the implemetation provided by the high-level APIs by restricting it to streams that are opened on devices that are set as the default device.</span></span> <span data-ttu-id="54587-111">Per ottenere un riferimento all'endpoint del dispositivo predefinito, il client deve chiamare [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="54587-111">To get a reference to the default device's endpoint, the client must call [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="54587-112">In questa chiamata il client deve indicare se è necessario un puntatore al dispositivo predefinito di rendering o alla periferica di acquisizione predefinita specificando il parametro *dataflow* .</span><span class="sxs-lookup"><span data-stu-id="54587-112">In this call, the client must indicate whether it requires a pointer to the rendering default device or the capture default device by specifying the *dataFlow* parameter.</span></span> <span data-ttu-id="54587-113">Il client deve inoltre specificare il ruolo appropriato per l'endpoint nell'attributo **ERole** (**eConsole** o **comunicazioni elettroniche**).</span><span class="sxs-lookup"><span data-stu-id="54587-113">The client must also specify the appropriate role for the endpoint in the **ERole** attribute (**eConsole** or **eCommunications**).</span></span> <span data-ttu-id="54587-114">Non usare **eMultimedia**.</span><span class="sxs-lookup"><span data-stu-id="54587-114">Do not use **eMultimedia**.</span></span>

<span data-ttu-id="54587-115">Se l'applicazione viene trascinata in qualsiasi altro dispositivo, l'applicazione può ottenere il dispositivo specificando una stringa ID endpoint (chiamando [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span><span class="sxs-lookup"><span data-stu-id="54587-115">If the application streams to any other device, the application can get the device by specifying an endpoint ID string (by calling [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span></span>

<span data-ttu-id="54587-116">Dopo che il dispositivo è stato identificato, il client WASAPI può fornire l'implementazione per il routing del flusso gestendo le notifiche della sessione audio e del dispositivo inviate per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="54587-116">After the device is identified, the WASAPI client can provide the implementation for stream routing by handling the device and audio session notifications sent for the device.</span></span> <span data-ttu-id="54587-117">Per ulteriori informazioni su queste notifiche, vedere [notifiche rilevanti per il routing del flusso](relevant-device-notifications-for-stream-routing.md).</span><span class="sxs-lookup"><span data-stu-id="54587-117">For more information about these notifications, see [Relevant Notifications for Stream Routing](relevant-device-notifications-for-stream-routing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="54587-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54587-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54587-119">Informazioni sull'API MMDevice</span><span class="sxs-lookup"><span data-stu-id="54587-119">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="54587-120">Informazioni su WASAPI</span><span class="sxs-lookup"><span data-stu-id="54587-120">About WASAPI</span></span>](wasapi.md)
</dt> <dt>

[<span data-ttu-id="54587-121">Routing del flusso</span><span class="sxs-lookup"><span data-stu-id="54587-121">Stream Routing</span></span>](stream-routing.md)
</dt> </dl>

 

 



