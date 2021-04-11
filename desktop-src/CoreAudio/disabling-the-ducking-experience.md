---
description: Un utente può disabilitare l'esperienza di ducking predefinita fornita dal sistema utilizzando le opzioni disponibili nella scheda comunicazioni del pannello di controllo multimediale di Windows, Mmsys.cpl.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Disabilitazione dell'esperienza di ducking predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed33fa7d9473cb5c68a018b98bff8a826612387e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127667"
---
# <a name="disabling-the-default-ducking-experience"></a><span data-ttu-id="5f648-103">Disabilitazione dell'esperienza di ducking predefinita</span><span class="sxs-lookup"><span data-stu-id="5f648-103">Disabling the Default Ducking Experience</span></span>

<span data-ttu-id="5f648-104">Un utente può disabilitare l' [esperienza di ducking predefinita](stream-attenuation.md) fornita dal sistema utilizzando le opzioni disponibili nella scheda **comunicazioni** del pannello di controllo multimediale di Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="5f648-104">A user can disable the [Default Ducking Experience](stream-attenuation.md) provided by the system by using the options that are available on the **Communications** tab of the Windows multimedia control panel, Mmsys.cpl.</span></span>

<span data-ttu-id="5f648-105">Quando si applica il ducking, viene usato un effetto di dissolvenza e dissolvenza per un periodo di 1 secondo.</span><span class="sxs-lookup"><span data-stu-id="5f648-105">When ducking is applied, a fade-out and fade-in effect is used for a period of 1 second.</span></span> <span data-ttu-id="5f648-106">Un'applicazione di gioco potrebbe non voler interferire con il flusso di comunicazione con l'audio del gioco.</span><span class="sxs-lookup"><span data-stu-id="5f648-106">A game application might not want the communication stream to interfere with the game audio.</span></span> <span data-ttu-id="5f648-107">Alcune applicazioni multimediali potrebbero scoprire che l'esperienza di riproduzione è stridente quando la musica si dissolve nuovamente.</span><span class="sxs-lookup"><span data-stu-id="5f648-107">Some media applications might find that the playback experience is jarring when music fades back in.</span></span> <span data-ttu-id="5f648-108">Questi tipi di applicazioni possono scegliere di non partecipare all'esperienza ducking.</span><span class="sxs-lookup"><span data-stu-id="5f648-108">These types of applications can choose not to participate in the ducking experience.</span></span>

<span data-ttu-id="5f648-109">A livello di codice, un client WASAPI diretto può rifiutare esplicitamente l'uso di gestione sessioni per la sessione audio che fornisce il controllo del volume per i flussi non di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="5f648-109">Programmatically, a direct WASAPI client can opt out by using the session manager for the audio session that provides volume control for the non-communication streams.</span></span> <span data-ttu-id="5f648-110">Si noti che anche se un client rifiuta l'abbassamento di ducking, riceve comunque notifiche di ducking dal sistema.</span><span class="sxs-lookup"><span data-stu-id="5f648-110">Note that even if an client opts out of ducking, it still receives ducking notifications from the system.</span></span>

<span data-ttu-id="5f648-111">Per rifiutare esplicitamente il ducking, il client deve ottenere un riferimento all'interfaccia [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) del gestore sessioni.</span><span class="sxs-lookup"><span data-stu-id="5f648-111">To opt out of ducking, the client must get a reference to the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) interface of the session manager.</span></span> <span data-ttu-id="5f648-112">Per rifiutare esplicitamente l'esperienza ducking, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="5f648-112">To opt out of the ducking experience, use the following steps:</span></span>

1.  <span data-ttu-id="5f648-113">Creare un'istanza dell'enumeratore Device e usarlo per ottenere un riferimento all'endpoint del dispositivo usato dall'applicazione multimediale per eseguire il rendering del flusso non di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="5f648-113">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="5f648-114">Attivare Gestione sessioni dall'endpoint del dispositivo e ottenere un riferimento all'interfaccia [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) del gestore sessioni.</span><span class="sxs-lookup"><span data-stu-id="5f648-114">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="5f648-115">Utilizzando il puntatore [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , ottenere un riferimento all'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) di gestione sessioni.</span><span class="sxs-lookup"><span data-stu-id="5f648-115">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="5f648-116">Eseguire una query per [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) dall'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .</span><span class="sxs-lookup"><span data-stu-id="5f648-116">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="5f648-117">Chiamare [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) e passare **true** o **false** per specificare la preferenza ducking.</span><span class="sxs-lookup"><span data-stu-id="5f648-117">Call [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) and pass **TRUE** or **FALSE** to specify the ducking preference.</span></span> <span data-ttu-id="5f648-118">La preferenza specificata può essere modificata dinamicamente durante la sessione.</span><span class="sxs-lookup"><span data-stu-id="5f648-118">The specified preference can be changed dynamically during the session.</span></span> <span data-ttu-id="5f648-119">Si noti che la modifica del rifiuto esplicito non viene applicata fino a quando il flusso non viene interrotto e non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="5f648-119">Note that the opt-out change does not take effect until the stream is stopped and started again.</span></span>

<span data-ttu-id="5f648-120">Il codice seguente illustra come un'applicazione può specificare la propria preferenza di ducking.</span><span class="sxs-lookup"><span data-stu-id="5f648-120">The following code shows how an application can specify its ducking preference.</span></span> <span data-ttu-id="5f648-121">Il chiamante della funzione deve passare **true** o **false** nel parametro DuckingOptOutChecked.</span><span class="sxs-lookup"><span data-stu-id="5f648-121">The caller of the function must pass **TRUE** or **FALSE** in the DuckingOptOutChecked parameter.</span></span> <span data-ttu-id="5f648-122">A seconda del valore passato, ducking viene abilitato o disabilitato tramite [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span><span class="sxs-lookup"><span data-stu-id="5f648-122">Depending on the value passed, ducking is enabled or disabled through the [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span></span>


```C++
////////////////////////////////////////////////////////////////////
//Description: Specifies the ducking options for the application.
//Parameters: 
//    If DuckingOptOutChecked is TRUE system ducking is disabled; 
//    FALSE, system ducking is enabled.
////////////////////////////////////////////////////////////////////

HRESULT DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;


    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>(&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(NULL, 0, &pSessionControl);
        
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                  __uuidof(IAudioSessionControl2),
                  (void**)&pSessionControl2);
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    //  Sync the ducking state with the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionControl2->SetDuckingPreference(TRUE);
        }
        else
        {
            hr = pSessionControl2->SetDuckingPreference(FALSE);
        }
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5f648-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f648-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f648-124">Uso di un dispositivo di comunicazione</span><span class="sxs-lookup"><span data-stu-id="5f648-124">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="5f648-125">Esperienza di ducking predefinita</span><span class="sxs-lookup"><span data-stu-id="5f648-125">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="5f648-126">Fornire un comportamento di ducking personalizzato</span><span class="sxs-lookup"><span data-stu-id="5f648-126">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="5f648-127">Considerazioni sull'implementazione per le notifiche di ducking</span><span class="sxs-lookup"><span data-stu-id="5f648-127">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="5f648-128">Recupero di eventi ducking</span><span class="sxs-lookup"><span data-stu-id="5f648-128">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



