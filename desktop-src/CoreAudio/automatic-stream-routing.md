---
description: Questo articolo descrive come aggiornare un'implementazione WASAPI per sfruttare i vantaggi del routing automatico dei flussi.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Routing automatico dei flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd152db35c580d93cf76ccfaffd66b37225f2be7fae11f217a6895b289a58e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957390"
---
# <a name="automatic-stream-routing"></a>Routing automatico dei flussi

Questo articolo descrive come aggiornare un'implementazione WASAPI per sfruttare i vantaggi del routing automatico dei flussi.

A partire da Windows 7, ogni volta che viene modificato il dispositivo audio predefinito, il flusso di riproduzione audio di un'app viene trasferito senza problemi dal dispositivo audio predefinito precedente al nuovo dispositivo audio predefinito. Questo trasferimento viene eseguito automaticamente senza codice aggiuntivo dell'applicazione. Tuttavia, prima di Windows 10 versione 1607, le app che usavano l'API di sessione audio di basso livello Windows (WASAPI) non potevano partecipare a questa funzionalità di routing dei flussi automatizzato. Le app che usano WASAPI dovevano implementare la propria forma di routing del flusso aggiungendo codice aggiuntivo per rilevare l'arrivo e la rimozione di dispositivi audio e passare il flusso a tali dispositivi in base alle esigenze. Le applicazioni che usano WASAPI che non implementavano il proprio meccanismo di routing dei flussi all'arrivo o alla rimozione del dispositivo rischiavano di offrire un'esperienza utente inferiore a quella ideale.

A partire dal Windows 10 versione 1607, le app che usano WASAPI possono sfruttare il routing automatico dei flussi. Se l'applicazione usa WASAPI, è consigliabile aggiornare l'applicazione per sfruttare questa nuova funzionalità seguendo questa procedura:

1.  Windows 10 versione 1607 definisce due nuovi GUID che possono essere usati per attivare un rendering audio o un'interfaccia di acquisizione con routing automatico dei flussi, [DEVINTERFACE \_ AUDIO \_ RENDER](/windows/desktop/CoreAudio/devinterface-xxx-guids) e [DEVINTERFACE \_ AUDIO \_ CAPTURE.](/windows/desktop/CoreAudio/devinterface-xxx-guids) Ottenere una rappresentazione di stringa di questi GUID chiamando [**StringFromIID.**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid) L'esempio seguente mostra questa chiamata per il GUID di rendering audio.

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  Attivare l'endpoint audio passando la stringa dell'identificatore alla funzione [**WASAPI ActivateAudioInterfaceAsync.**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) L'esempio seguente passa l'identificatore di rendering audio ottenuto nel passaggio 1:

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  Liberare la memoria allocata per contenere l'identificatore dell'endpoint:

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

Dopo aver modificato l'app per attivare l'interfaccia audio nel modo descritto in precedenza, questa farà parte della funzionalità di routing automatico dei flussi.

Per illustrare il routing automatico dei flussi, usare un portatile o un tablet dotato di altoparlanti interni per riprodurre l'audio. Si dovrebbe ascoltare l'audio riprodotto attraverso gli altoparlanti interni del dispositivo. Durante la riproduzione dell'audio, collegare un paio di cuffi. Si dovrebbe ora ascoltare l'audio riprodotto tramite le cuffi. Scollegare quindi le cuffi e l'audio per tornare automaticamente agli altoparlanti interni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Routing di flusso](stream-routing.md)
</dt> <dt>

[**MediaDevice.GetDefaultAudioRenderId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[**MediaDevice.GetDefaultAudioCaptureId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
