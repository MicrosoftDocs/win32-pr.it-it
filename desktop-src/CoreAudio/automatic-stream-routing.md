---
description: Questo articolo descrive come aggiornare un'implementazione di WASAPI per sfruttare i vantaggi del routing automatico dei flussi.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Routing automatico del flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a9848c5fd764ee49e485fc112c35c347a0f84d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966339"
---
# <a name="automatic-stream-routing"></a>Routing automatico del flusso

Questo articolo descrive come aggiornare un'implementazione di WASAPI per sfruttare i vantaggi del routing automatico dei flussi.

A partire da Windows 7, ogni volta che viene modificato il dispositivo audio predefinito, il flusso di riproduzione audio di un'app viene trasferito senza interruzioni dal dispositivo audio predefinito precedente al nuovo dispositivo audio predefinito. Questo trasferimento viene eseguito automaticamente senza codice dell'applicazione aggiuntivo. Tuttavia, prima di Windows 10, versione 1607, le app che usavano l'API di sessione audio di Windows di basso livello (WASAPI) non potevano partecipare a questa funzionalità di routing automatico dei flussi. Le app che usano WASAPI sono necessarie per implementare il proprio modulo di routing del flusso aggiungendo codice aggiuntivo per rilevare l'arrivo e la rimozione di dispositivi audio e passare il flusso a tali dispositivi in base alle esigenze. Le applicazioni che usano WASAPI che non implementano il proprio meccanismo di routing del flusso all'arrivo o alla rimozione del dispositivo rischiano di offrire un'esperienza utente inferiore a quella ideale.

A partire da Windows 10, versione 1607, le app che usano WASAPI possono sfruttare il routing automatico dei flussi. Se l'applicazione usa WASAPI, è consigliabile aggiornare l'applicazione per sfruttare questa nuova funzionalità attenendosi alla procedura seguente:

1.  Windows 10, versione 1607, definisce due nuovi GUID che possono essere usati per attivare un'interfaccia di rendering o acquisizione audio con routing automatico dei flussi [, \_ \_ rendering audio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids) e [ \_ \_ acquisizione audio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids). Ottenere una rappresentazione di stringa di questi GUID chiamando [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid). Nell'esempio seguente viene illustrata questa chiamata per il GUID di rendering audio.

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  Attivare l'endpoint audio passando la stringa dell'identificatore alla funzione WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) . Nell'esempio seguente l'identificatore di rendering audio ottenuto nel passaggio 1 viene passato:

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

    

Dopo aver modificato l'app per attivare l'interfaccia audio nel modo descritto in precedenza, parteciperà alla funzionalità di routing automatico dei flussi.

Per illustrare il routing automatico dei flussi, usare un portatile o un tablet dotato di altoparlanti interni per riprodurre l'audio. È necessario ascoltare la riproduzione audio degli altoparlanti interni del dispositivo. Durante la riproduzione dell'audio, connettere una coppia di cuffie. A questo punto si dovrebbe ascoltare la riproduzione audio attraverso le cuffie. Quindi, scollegare le cuffie e audio deve essere indirizzato automaticamente ai relatori interni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Routing del flusso](stream-routing.md)
</dt> <dt>

[**MediaDevice.GetDefaultAudioRenderId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[**MediaDevice.GetDefaultAudioCaptureId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
