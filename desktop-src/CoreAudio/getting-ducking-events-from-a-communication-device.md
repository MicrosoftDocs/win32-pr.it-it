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
# <a name="getting-ducking-events"></a>Recupero di eventi ducking

Un'applicazione multimediale che desidera fornire un'esperienza di ducking personalizzata deve restare in ascolto delle notifiche degli eventi quando un flusso di comunicazione viene aperto o chiuso nel sistema. È possibile fornire l'implementazione personalizzata usando MediaFoundation, DirectShow o DirectSound, che usano le API di base di audio. Un client WASAPI diretto può anche eseguire l'override della gestione predefinita se sa quando inizia e termina la sessione di comunicazione.

Per fornire un'implementazione personalizzata, un'applicazione multimediale deve ricevere notifiche dal sistema quando un'applicazione di comunicazione avvia o termina un flusso di comunicazione. L'applicazione multimediale deve implementare l'interfaccia [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) e registrare l'implementazione con il sistema audio. Al completamento della registrazione, l'applicazione multimediale riceve le notifiche degli eventi sotto forma di callback tramite i metodi dell'interfaccia. Per ulteriori informazioni, vedere [considerazioni sull'implementazione per le notifiche di ducking](handling-audio-ducking-events-from-communication-devices.md).

Per inviare notifiche di ducking, è necessario che il sistema audio conosca la sessione audio in ascolto degli eventi ducking. Ogni sessione audio viene identificata in modo univoco con un GUID, ovvero l'identificatore dell'istanza di sessione. Gestione sessioni consente a un'applicazione di ottenere informazioni sulla sessione, ad esempio il titolo della sessione audio, lo stato di rendering e l'identificatore dell'istanza della sessione. L'identificatore può essere recuperato tramite l'interfaccia di controllo dei criteri [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).

I passaggi seguenti riepilogano il processo di recupero dell'identificatore dell'istanza di sessione dell'applicazione multimediale:

1.  Creare un'istanza dell'enumeratore Device e usarlo per ottenere un riferimento all'endpoint del dispositivo usato dall'applicazione multimediale per eseguire il rendering del flusso non di comunicazione.
2.  Attivare Gestione sessioni dall'endpoint del dispositivo e ottenere un riferimento all'interfaccia [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) del gestore sessioni.
3.  Utilizzando il puntatore [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , ottenere un riferimento all'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) di gestione sessioni.
4.  Eseguire una query per [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) dall'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .
5.  Chiamare [**IAudioSessionControl2:: GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) e recuperare una stringa che contiene l'identificatore di sessione per la sessione audio corrente.

Per ricevere notifiche di ducking sui flussi di comunicazione, l'applicazione multimediale chiama [**IAudioSessionManager2:: RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification). L'applicazione multimediale fornisce l'identificatore dell'istanza di sessione al sistema audio e un puntatore all'implementazione di [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) . L'applicazione può ora ricevere una notifica degli eventi quando un flusso viene aperto nel dispositivo di comunicazione. Per arrestare il recupero della notifica, l'applicazione multimediale deve chiamare [**IAudioSessionManager2:: UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).

Il codice seguente illustra come è possibile registrare un'applicazione per ottenere notifiche di ducking. La classe CMediaPlayer è definita in [considerazioni sull'implementazione per le notifiche di ducking](handling-audio-ducking-events-from-communication-devices.md). Questa funzionalità è implementata nell'esempio [DuckingMediaPlayer](duckingmediaplayer.md) .


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

[Esperienza di ducking predefinita](stream-attenuation.md)
</dt> <dt>

[Disabilitazione dell'esperienza di ducking predefinita](disabling-the-ducking-experience.md)
</dt> <dt>

[Fornire un comportamento di ducking personalizzato](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considerazioni sull'implementazione per le notifiche di ducking](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



