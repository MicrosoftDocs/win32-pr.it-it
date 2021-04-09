---
description: Registrazione loopback
ms.assetid: 71c567f7-fffa-4b75-897a-63ed30c4c9b0
title: Registrazione loopback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374da7497096118905f5e4c79bbacda832a42a7b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966256"
---
# <a name="loopback-recording"></a>Registrazione loopback

In modalità loopback un client di WASAPI è in grado di acquisire il flusso audio che viene riprodotto da un dispositivo endpoint di rendering. Per aprire un flusso in modalità loopback, il client deve:

-   Ottenere un'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) per il dispositivo dell'endpoint di rendering.
-   Inizializzare un flusso di acquisizione in modalità loopback sul dispositivo dell'endpoint di rendering.

Dopo aver seguito questi passaggi, il client può chiamare il metodo [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) per ottenere un'interfaccia [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) sul dispositivo dell'endpoint di rendering.

WASAPI fornisce la modalità loopback principalmente per supportare l'annullamento dell'eco acustico (AEC). Tuttavia, altri tipi di applicazioni audio potrebbero trovare la modalità loopback utile per acquisire la combinazione di sistema riprodotta dal motore audio.

Nell'esempio di codice in [acquisizione di un flusso](capturing-a-stream.md), è possibile modificare facilmente la funzione RecordAudioStream per configurare un flusso di acquisizione in modalità loopback. Di seguito sono riportate le modifiche necessarie:

-   Nella chiamata al metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) modificare il primo parametro (*flusso di flussi*) da eCapture a eRender.
-   Nella chiamata al metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , modificare il valore del secondo parametro (*StreamFlags*) da 0 a AUDCLNT \_ StreamFlags \_ loopback.

Nelle versioni di Windows precedenti a Windows 10 1703, il client di acquisizione in modalità pull non riceve alcun evento quando un flusso viene inizializzato con il buffer guidato dagli eventi ed è abilitato per loopback. Per ovviare a questo problema, inizializzare un flusso di rendering in modalità guidata dagli eventi. Ogni volta che il client riceve un evento per il flusso di rendering, deve segnalare al client di acquisizione di eseguire il thread di acquisizione che legge il set successivo di esempi dal buffer dell'endpoint di acquisizione. Nelle versioni 1703 e successive di Windows 10, i client loopback basati su eventi sono supportati e non necessitano più della soluzione alternativa che interessano il flusso di rendering.  

Un client può abilitare la modalità loopback solo per un flusso in modalità condivisa (AUDCLNT \_ SHAREMODE \_ Shared). I flussi in modalità esclusiva non possono funzionare in modalità loopback.

L'implementazione di loopback da WASAPI dipende dalle capacità dell'hardware. Se l'hardware supporta un pin di loopback sull'endpoint di rendering, WASAPI usa l'audio fornito su questo pin per il flusso di loopback. Quando l'hardware non supporta un pin di loopback, WASAPI copia il flusso di output dal motore audio nel buffer di acquisizione dell'applicazione loopback, oltre a copiare i dati audio nel pin di rendering dell'hardware.

Alcuni fornitori di hardware implementano dispositivi loopback, anziché aggiungere istanze nei dispositivi di rendering, nelle schede audio. Sebbene i dispositivi loopback hardware siano simili in funzione alla modalità loopback WASAPI, possono essere più difficili da utilizzare.

I dispositivi loopback hardware presentano gli svantaggi seguenti per le applicazioni audio:

-   Non tutte le schede audio dispongono di dispositivi loopback. Pertanto, le applicazioni che dipendono da tali applicazioni non funzioneranno su tutti i sistemi.
-   Prima che un'applicazione possa registrare da un dispositivo loopback, l'utente deve identificare il dispositivo loopback e abilitarlo per l'utilizzo.

Fornitori diversi assegnano nomi diversi ai dispositivi loopback hardware. Di seguito sono riportati alcuni esempi:

-   Combinazione stereo
-   Combinazione di onda
-   Output misto
-   Cosa si sente

La mancanza di nomi standardizzati potrebbe impedire agli utenti di identificare un dispositivo loopback in un elenco di nomi di dispositivo.

Un dispositivo loopback hardware è un dispositivo di acquisizione. Pertanto, se un adapter supporta un dispositivo loopback, un'applicazione audio può registrare dal dispositivo nello stesso modo in cui registra da qualsiasi altro dispositivo di acquisizione.

Ad esempio, se si seleziona un dispositivo loopback hardware come dispositivo di acquisizione predefinito, è possibile usare la funzione RecordAudioStream (senza modifiche) nell'esempio di codice in [acquisizione di un flusso](capturing-a-stream.md) per acquisire il flusso dal dispositivo. È anche possibile usare un'API audio legacy, ad esempio le funzioni **waveInXxx** multimediali di Windows, per acquisire il flusso dal dispositivo.

Se la scheda audio contiene un dispositivo loopback hardware, è possibile usare il pannello di controllo multimediale di Windows, Mmsys.cpl, per designare il dispositivo come dispositivo di acquisizione predefinito. Attenersi alla procedura seguente:

1.  Per eseguire Mmsys.cpl, aprire una finestra del prompt dei comandi e immettere il comando seguente:

    ```C++
    control mmsys.cpl,,1
    ```

    

    In alternativa, è possibile eseguire Mmsys.cpl facendo clic con il pulsante destro del mouse sull'icona dell'altoparlante nell'area di notifica che si trova sul lato destro della barra delle applicazioni e selezionando **registrazione dispositivi**.

2.  Una volta aperta la finestra di Mmsys.cpl, fare clic con il pulsante destro del mouse in un punto qualsiasi dell'elenco dei dispositivi di registrazione e verificare che l'opzione **Mostra dispositivi disabilitati** sia selezionata. In caso contrario, se il dispositivo loopback è disabilitato, non verrà visualizzato nell'elenco.
3.  Sfogliare l'elenco dei dispositivi di registrazione per individuare il dispositivo loopback (se esistente). Se il dispositivo loopback è disabilitato, abilitarlo facendo clic con il pulsante destro del mouse sul dispositivo e scegliendo **Abilita**.
4.  Infine, per selezionare il dispositivo loopback come dispositivo di acquisizione predefinito, fare clic con il pulsante destro del mouse sul dispositivo e scegliere **Imposta come dispositivo predefinito**.

WASAPI supporta la registrazione loopback indipendentemente dal fatto che l'hardware audio contenga un dispositivo loopback o se l'utente ha abilitato il dispositivo.

Windows Vista fornisce Digital Rights Management (DRM). I provider di contenuti si basano sul DRM per proteggere la musica di proprietà o altro contenuto da copia non autorizzata e altri usi non validi. Analogamente, un driver audio attendibile non consente a un dispositivo loopback di acquisire flussi digitali contenenti contenuto protetto. Windows Vista consente solo ai driver attendibili di riprodurre contenuti protetti. Per ulteriori informazioni su driver attendibili e DRM, vedere la documentazione di Windows DDK.

Il loopback WASAPI contiene la combinazione di tutti i file audio riprodotti, indipendentemente dalla sessione di Servizi terminal da cui ha origine l'audio. Ad esempio, è possibile eseguire un client di loopback in un servizio in esecuzione nella sessione 0 e acquisire l'audio da tutte le sessioni utente, oltre che l'audio riprodotto dalla sessione 0.

Desktop remoto consente il reindirizzamento dell'audio al client. Questa operazione viene implementata creando nuovi dispositivi audio che vengono visualizzati solo per tale sessione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> </dl>

 

 



