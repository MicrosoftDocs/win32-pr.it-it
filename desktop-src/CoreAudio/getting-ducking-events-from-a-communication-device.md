---
description: Un'applicazione multimediale che desidera fornire un'esperienza di ducking personalizzata deve restare in ascolto delle notifiche degli eventi quando un flusso di comunicazione viene aperto o chiuso nel sistema.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Recupero di eventi ducking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e45557c25570a89452a39683a0b6732b9632129
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523722"
---
# <a name="getting-ducking-events"></a><span data-ttu-id="49009-103">Recupero di eventi ducking</span><span class="sxs-lookup"><span data-stu-id="49009-103">Getting Ducking Events</span></span>

<span data-ttu-id="49009-104">Un'applicazione multimediale che desidera fornire un'esperienza di ducking personalizzata deve restare in ascolto delle notifiche degli eventi quando un flusso di comunicazione viene aperto o chiuso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="49009-104">A media application that wants to provide a customised ducking experience must listen for the event notifications when a communication stream is opened or closed in the system.</span></span> <span data-ttu-id="49009-105">È possibile fornire l'implementazione personalizzata usando MediaFoundation, DirectShow o DirectSound, che usano le API di base di audio.</span><span class="sxs-lookup"><span data-stu-id="49009-105">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="49009-106">Un client WASAPI diretto può anche eseguire l'override della gestione predefinita se sa quando inizia e termina la sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="49009-106">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="49009-107">Per fornire un'implementazione personalizzata, un'applicazione multimediale deve ricevere notifiche dal sistema quando un'applicazione di comunicazione avvia o termina un flusso di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="49009-107">To provide a custom implementation, a media application needs to get notifications from the system when a communication application starts or ends a communication stream.</span></span> <span data-ttu-id="49009-108">L'applicazione multimediale deve implementare l'interfaccia [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) e registrare l'implementazione con il sistema audio.</span><span class="sxs-lookup"><span data-stu-id="49009-108">The media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="49009-109">Al completamento della registrazione, l'applicazione multimediale riceve le notifiche degli eventi sotto forma di callback tramite i metodi dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="49009-109">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="49009-110">Per ulteriori informazioni, vedere [considerazioni sull'implementazione per le notifiche di ducking](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="49009-110">For more information, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

<span data-ttu-id="49009-111">Per inviare notifiche di ducking, è necessario che il sistema audio conosca la sessione audio in ascolto degli eventi ducking.</span><span class="sxs-lookup"><span data-stu-id="49009-111">To send ducking notifications, the audio system must know which audio session is listening for the ducking events.</span></span> <span data-ttu-id="49009-112">Ogni sessione audio viene identificata in modo univoco con un GUID, ovvero l'identificatore dell'istanza di sessione.</span><span class="sxs-lookup"><span data-stu-id="49009-112">Each audio session is uniquely identified with a GUID—session instance identifier.</span></span> <span data-ttu-id="49009-113">Gestione sessioni consente a un'applicazione di ottenere informazioni sulla sessione, ad esempio il titolo della sessione audio, lo stato di rendering e l'identificatore dell'istanza della sessione.</span><span class="sxs-lookup"><span data-stu-id="49009-113">The session manager allows an application to get information about the session such as title of audio session, the rendering state, and the session instance identifier.</span></span> <span data-ttu-id="49009-114">L'identificatore può essere recuperato tramite l'interfaccia di controllo dei criteri [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span><span class="sxs-lookup"><span data-stu-id="49009-114">The identifier can be retrieved by using the policy control interface, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span></span>

<span data-ttu-id="49009-115">I passaggi seguenti riepilogano il processo di recupero dell'identificatore dell'istanza di sessione dell'applicazione multimediale:</span><span class="sxs-lookup"><span data-stu-id="49009-115">The following steps summarize the process of getting the session instance identifier of the media application:</span></span>

1.  <span data-ttu-id="49009-116">Creare un'istanza dell'enumeratore Device e usarlo per ottenere un riferimento all'endpoint del dispositivo usato dall'applicazione multimediale per eseguire il rendering del flusso non di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="49009-116">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="49009-117">Attivare Gestione sessioni dall'endpoint del dispositivo e ottenere un riferimento all'interfaccia [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) del gestore sessioni.</span><span class="sxs-lookup"><span data-stu-id="49009-117">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="49009-118">Utilizzando il puntatore [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , ottenere un riferimento all'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) di gestione sessioni.</span><span class="sxs-lookup"><span data-stu-id="49009-118">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="49009-119">Eseguire una query per [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) dall'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .</span><span class="sxs-lookup"><span data-stu-id="49009-119">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="49009-120">Chiamare [**IAudioSessionControl2:: GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) e recuperare una stringa che contiene l'identificatore di sessione per la sessione audio corrente.</span><span class="sxs-lookup"><span data-stu-id="49009-120">Call [**IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) and retrieve a string that contains the session identifier for the current audio session.</span></span>

<span data-ttu-id="49009-121">Per ricevere notifiche di ducking sui flussi di comunicazione, l'applicazione multimediale chiama [**IAudioSessionManager2:: RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span><span class="sxs-lookup"><span data-stu-id="49009-121">To get ducking notifications about communication streams, the media application calls [**IAudioSessionManager2::RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span></span> <span data-ttu-id="49009-122">L'applicazione multimediale fornisce l'identificatore dell'istanza di sessione al sistema audio e un puntatore all'implementazione di [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) .</span><span class="sxs-lookup"><span data-stu-id="49009-122">The media application supplies its session instance identifier to the audio system and a pointer to the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) implementation.</span></span> <span data-ttu-id="49009-123">L'applicazione può ora ricevere una notifica degli eventi quando un flusso viene aperto nel dispositivo di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="49009-123">The application can now receive event notification when a stream opened on the communication device.</span></span> <span data-ttu-id="49009-124">Per arrestare il recupero della notifica, l'applicazione multimediale deve chiamare [**IAudioSessionManager2:: UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span><span class="sxs-lookup"><span data-stu-id="49009-124">To stop getting notification, the media application must call [**IAudioSessionManager2::UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span></span>

<span data-ttu-id="49009-125">Il codice seguente illustra come è possibile registrare un'applicazione per ottenere notifiche di ducking.</span><span class="sxs-lookup"><span data-stu-id="49009-125">The following code shows how an application can register to get ducking notifications.</span></span> <span data-ttu-id="49009-126">La classe CMediaPlayer è definita in [considerazioni sull'implementazione per le notifiche di ducking](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="49009-126">The CMediaPlayer class is defined in [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span> <span data-ttu-id="49009-127">Questa funzionalità è implementata nell'esempio [DuckingMediaPlayer](duckingmediaplayer.md) .</span><span class="sxs-lookup"><span data-stu-id="49009-127">The [DuckingMediaPlayer](duckingmediaplayer.md) sample implements this functionality.</span></span>


```C++
////////////////////////////////////////////////////////////////////
//Description: Registers for duck notifications depending on the 
//             the ducking options specified by the caller.
//Parameters: 
//    If DuckingOptOutChecked is TRUE, the client is registered for
//    to receive ducking notifications; 
//    FALSE, the client's registration is deleted.
////////////////////////////////////////////////////////////////////

HRESULT CMediaPlayer::DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;

    LPWSTR sessionId = NULL;

    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(
              eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate the session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>
                                 (&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(
                                  NULL, 0, &pSessionControl);
        
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                               IID_PPV_ARGS(&pSessionControl2));
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    // Get the session instance identifier.
    
    if (SUCCEEDED(hr))
    {
        hr = pSessionControl2->GetSessionInstanceIdentifier(
                                 sessionId);
                
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }

    //  Register for ducking events depending on 
    //  the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionManager2->RegisterDuckNotification(
                                    sessionId, this);
        }
        else
        {
            hr = pSessionManager2->UnregisterDuckNotification
                                      (FALSE);
        }
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="49009-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="49009-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49009-129">Uso di un dispositivo di comunicazione</span><span class="sxs-lookup"><span data-stu-id="49009-129">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="49009-130">Esperienza di ducking predefinita</span><span class="sxs-lookup"><span data-stu-id="49009-130">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="49009-131">Disabilitazione dell'esperienza di ducking predefinita</span><span class="sxs-lookup"><span data-stu-id="49009-131">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="49009-132">Fornire un comportamento di ducking personalizzato</span><span class="sxs-lookup"><span data-stu-id="49009-132">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="49009-133">Considerazioni sull'implementazione per le notifiche di ducking</span><span class="sxs-lookup"><span data-stu-id="49009-133">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



