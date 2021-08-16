---
description: Un utente può disabilitare l'esperienza di papera predefinita fornita dal sistema usando le opzioni disponibili nella scheda Comunicazioni del pannello di controllo multimediale di Windows, Mmsys.cpl.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Disabilitazione dell'esperienza di ducking predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473b0bab8c3575d416cc72b7e931b4c85160bdaacc6031611ad80394f44b9098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828552"
---
# <a name="disabling-the-default-ducking-experience"></a>Disabilitazione dell'esperienza di ducking predefinita

Un utente può disabilitare l'esperienza [di papera](stream-attenuation.md) predefinita fornita  dal sistema usando le opzioni disponibili nella scheda Comunicazioni del pannello di controllo multimediale di Windows, Mmsys.cpl.

Quando si applica la dissolvenza, per un periodo di 1 secondo vengono usati un effetto dissolvenza in uscita e dissolvenza in entrata. Un'applicazione di gioco potrebbe non volere che il flusso di comunicazione interferisca con l'audio del gioco. Alcune applicazioni multimediali potrebbero scoprire che l'esperienza di riproduzione è in jarring quando la musica torna in dissolvenza. Questi tipi di applicazioni possono scegliere di non partecipare all'esperienza di papera.

A livello di codice, un client WASAPI diretto può rifiutare esplicitamente usando la gestione sessione per la sessione audio che fornisce il controllo del volume per i flussi non di comunicazione. Si noti che anche se un client rifiuta esplicitamente l'uso di ducking, riceve comunque notifiche di rifiuto dal sistema.

Per rifiutare esplicitamente l'applicazione, il client deve ottenere un riferimento [**all'interfaccia IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) della gestione sessione. Per rifiutare esplicitamente l'esperienza di papera, seguire questa procedura:

1.  Creare un'istanza dell'enumeratore del dispositivo e usarlo per ottenere un riferimento all'endpoint del dispositivo utilizzato dall'applicazione multimediale per eseguire il rendering del flusso non di comunicazione.
2.  Attivare la gestione sessione dall'endpoint del dispositivo e ottenere un riferimento [**all'interfaccia IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) della gestione sessione.
3.  Usando il [**puntatore IAudioSessionManager2,**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) ottenere un riferimento all'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) della gestione sessione.
4.  Eseguire una query [**per IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) [**dall'interfaccia IAudioSessionControl.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
5.  Chiamare [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) e passare **TRUE** o **FALSE** per specificare la preferenza di ducking. La preferenza specificata può essere modificata dinamicamente durante la sessione. Si noti che la modifica di rifiuto esplicito non ha effetto fino a quando il flusso non viene arrestato e avviato di nuovo.

Il codice seguente illustra come un'applicazione può specificare la preferenza di ducking. Il chiamante della funzione deve passare **TRUE** o **FALSE** nel parametro DuckingOptOutChecked. A seconda del valore passato, il ducking è abilitato o disabilitato tramite [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).


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

[Esperienza di paperino predefinita](stream-attenuation.md)
</dt> <dt>

[Fornire un comportamento di papera personalizzato](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considerazioni sull'implementazione per l'abbassamento delle notifiche](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Recupero di eventi di ducking](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



