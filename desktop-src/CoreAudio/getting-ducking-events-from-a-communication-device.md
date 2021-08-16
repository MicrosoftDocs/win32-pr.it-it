---
description: Un'applicazione multimediale che vuole offrire un'esperienza di papera personalizzata deve restare in ascolto delle notifiche degli eventi quando un flusso di comunicazione viene aperto o chiuso nel sistema.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Recupero di eventi di ducking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5869aa02a64ef3b7d035743b9bee3c91d295448c4d89d659862c5efc81d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828262"
---
# <a name="getting-ducking-events"></a>Recupero di eventi di ducking

Un'applicazione multimediale che vuole offrire un'esperienza di papera personalizzata deve restare in ascolto delle notifiche degli eventi quando un flusso di comunicazione viene aperto o chiuso nel sistema. L'implementazione personalizzata può essere fornita usando MediaFoundation, DirectShow o DirectSound, che usano le API Audio core. Un client WASAPI diretto può anche eseguire l'override della gestione predefinita se sa quando viene avviata e terminata la sessione di comunicazione.

Per fornire un'implementazione personalizzata, un'applicazione multimediale deve ricevere notifiche dal sistema quando un'applicazione di comunicazione avvia o termina un flusso di comunicazione. L'applicazione multimediale deve [**implementare l'interfaccia IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) e registrare l'implementazione con il sistema audio. Al completamento della registrazione, l'applicazione multimediale riceve le notifiche degli eventi sotto forma di callback tramite i metodi nell'interfaccia . Per altre informazioni, vedere [Considerazioni sull'implementazione per l'applicazione di notifiche di tipo ducking.](handling-audio-ducking-events-from-communication-devices.md)

Per inviare notifiche di ducking, il sistema audio deve sapere quale sessione audio è in ascolto degli eventi di ducking. Ogni sessione audio viene identificata in modo univoco con un GUID, ovvero l'identificatore dell'istanza di sessione. La gestione sessione consente a un'applicazione di ottenere informazioni sulla sessione, ad esempio il titolo della sessione audio, lo stato di rendering e l'identificatore dell'istanza di sessione. L'identificatore può essere recuperato tramite l'interfaccia di controllo dei [**criteri, IAudioSessionControl2.**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)

I passaggi seguenti riepilogano il processo di recupero dell'identificatore dell'istanza di sessione dell'applicazione multimediale:

1.  Creare un'istanza dell'enumeratore del dispositivo e usarlo per ottenere un riferimento all'endpoint del dispositivo utilizzato dall'applicazione multimediale per eseguire il rendering del flusso non di comunicazione.
2.  Attivare la gestione sessione dall'endpoint del dispositivo e ottenere un riferimento [**all'interfaccia IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) della gestione sessione.
3.  Usando il [**puntatore IAudioSessionManager2,**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) ottenere un riferimento all'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) della gestione sessione.
4.  Eseguire una query [**per IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) [**dall'interfaccia IAudioSessionControl.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
5.  Chiamare [**IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) e recuperare una stringa contenente l'identificatore di sessione per la sessione audio corrente.

Per ottenere notifiche sui flussi di comunicazione, l'applicazione multimediale chiama [**IAudioSessionManager2::RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification). L'applicazione multimediale fornisce l'identificatore dell'istanza di sessione al sistema audio e un [**puntatore all'implementazione di IAudioVolumeDuckNotification.**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) L'applicazione può ora ricevere una notifica degli eventi all'apertura di un flusso nel dispositivo di comunicazione. Per arrestare la notifica, l'applicazione multimediale deve chiamare [**IAudioSessionManager2::UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).

Il codice seguente illustra come un'applicazione può registrarsi per ottenere notifiche di tipo ducking. La classe CMediaPlayer è definita in [Considerazioni sull'implementazione per le notifiche di papering.](handling-audio-ducking-events-from-communication-devices.md) [L'esempio DuckingMediaPlayer](duckingmediaplayer.md) implementa questa funzionalità.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di un dispositivo di comunicazione](using-the-communication-device.md)
</dt> <dt>

[Esperienza di paperino predefinita](stream-attenuation.md)
</dt> <dt>

[Disabilitazione dell'esperienza di ducking predefinita](disabling-the-ducking-experience.md)
</dt> <dt>

[Fornire un comportamento di papera personalizzato](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considerazioni sull'implementazione per l'abbassamento delle notifiche](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



