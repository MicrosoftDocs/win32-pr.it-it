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
# <a name="disabling-the-default-ducking-experience"></a>Disabilitazione dell'esperienza di ducking predefinita

Un utente può disabilitare l' [esperienza di ducking predefinita](stream-attenuation.md) fornita dal sistema utilizzando le opzioni disponibili nella scheda **comunicazioni** del pannello di controllo multimediale di Windows, Mmsys.cpl.

Quando si applica il ducking, viene usato un effetto di dissolvenza e dissolvenza per un periodo di 1 secondo. Un'applicazione di gioco potrebbe non voler interferire con il flusso di comunicazione con l'audio del gioco. Alcune applicazioni multimediali potrebbero scoprire che l'esperienza di riproduzione è stridente quando la musica si dissolve nuovamente. Questi tipi di applicazioni possono scegliere di non partecipare all'esperienza ducking.

A livello di codice, un client WASAPI diretto può rifiutare esplicitamente l'uso di gestione sessioni per la sessione audio che fornisce il controllo del volume per i flussi non di comunicazione. Si noti che anche se un client rifiuta l'abbassamento di ducking, riceve comunque notifiche di ducking dal sistema.

Per rifiutare esplicitamente il ducking, il client deve ottenere un riferimento all'interfaccia [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) del gestore sessioni. Per rifiutare esplicitamente l'esperienza ducking, attenersi alla procedura seguente:

1.  Creare un'istanza dell'enumeratore Device e usarlo per ottenere un riferimento all'endpoint del dispositivo usato dall'applicazione multimediale per eseguire il rendering del flusso non di comunicazione.
2.  Attivare Gestione sessioni dall'endpoint del dispositivo e ottenere un riferimento all'interfaccia [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) del gestore sessioni.
3.  Utilizzando il puntatore [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , ottenere un riferimento all'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) di gestione sessioni.
4.  Eseguire una query per [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) dall'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .
5.  Chiamare [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) e passare **true** o **false** per specificare la preferenza ducking. La preferenza specificata può essere modificata dinamicamente durante la sessione. Si noti che la modifica del rifiuto esplicito non viene applicata fino a quando il flusso non viene interrotto e non viene riavviato.

Il codice seguente illustra come un'applicazione può specificare la propria preferenza di ducking. Il chiamante della funzione deve passare **true** o **false** nel parametro DuckingOptOutChecked. A seconda del valore passato, ducking viene abilitato o disabilitato tramite [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di un dispositivo di comunicazione](using-the-communication-device.md)
</dt> <dt>

[Esperienza di ducking predefinita](stream-attenuation.md)
</dt> <dt>

[Fornire un comportamento di ducking personalizzato](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considerazioni sull'implementazione per le notifiche di ducking](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Recupero di eventi ducking](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



