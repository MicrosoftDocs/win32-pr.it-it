---
description: Registrazione loopback
ms.assetid: 71c567f7-fffa-4b75-897a-63ed30c4c9b0
title: Registrazione loopback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa5ffe48bf11ad57b02085ab00dfd1ca09be0f72a56935cbd8d1bb40543033f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005274"
---
# <a name="loopback-recording"></a>Registrazione loopback

In modalità loopback, un client di WASAPI può acquisire il flusso audio riprodotto da un dispositivo endpoint di rendering. Per aprire un flusso in modalità loopback, il client deve:

-   Ottenere [**un'interfaccia IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) per il dispositivo endpoint di rendering.
-   Inizializzare un flusso di acquisizione in modalità loopback nel dispositivo endpoint di rendering.

Dopo aver seguito questi passaggi, il client può chiamare il metodo [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) per ottenere [**un'interfaccia IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) nel dispositivo endpoint di rendering.

WASAPI offre la modalità loopback principalmente per supportare l'annullamento dell'eco acustica (AEC). Tuttavia, altri tipi di applicazioni audio potrebbero trovare la modalità loopback utile per acquisire la combinazione di sistema riprodotta dal motore audio.

Nell'esempio di codice in [Acquisizione](capturing-a-stream.md)di un flusso è possibile modificare facilmente la funzione RecordAudioStream per configurare un flusso di acquisizione in modalità loopback. Le modifiche necessarie sono:

-   Nella chiamata al metodo [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) modificare il primo parametro (*dataFlow*) da eCapture a eRender.
-   Nella chiamata al metodo [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) modificare il valore del secondo parametro (*StreamFlags*) da 0 a AUDCLNT \_ STREAMFLAGS \_ LOOPBACK.

Nelle versioni di Windows precedenti Windows 10 1703, il client di acquisizione in modalità pull non riceve alcun evento quando un flusso viene inizializzato con il buffering basato su eventi ed è abilitato per il loopback. Per risolvere questo problema, inizializzare un flusso di rendering in modalità guidata da eventi. Ogni volta che il client riceve un evento per il flusso di rendering, deve segnalare al client di acquisizione di eseguire il thread di acquisizione che legge il set successivo di esempi dal buffer dell'endpoint di acquisizione. Nelle Windows 10 1703 e successive sono supportati i client di loopback guidati da eventi e non è più necessaria la soluzione alternativa che interessa il flusso di rendering.  

Un client può abilitare la modalità loopback solo per un flusso in modalità condivisa (AUDCLNT \_ SHAREMODE \_ SHARED). I flussi in modalità esclusiva non possono operare in modalità loopback.

L'implementazione del loopback da parte di WASAPI dipende dalle funzionalità dell'hardware. Se l'hardware supporta un pin di loopback nell'endpoint di rendering, WASAPI usa l'audio fornito su questo pin per il flusso di loopback. Quando l'hardware non supporta un pin di loopback, WASAPI copia il flusso di output dal motore audio nel buffer di acquisizione dell'applicazione loopback, oltre a copiare i dati audio nel pin di rendering dell'hardware.

Alcuni fornitori di hardware implementano dispositivi loopback (anziché aggiungere istanze nei dispositivi di rendering) nelle schede audio. Anche se i dispositivi di loopback hardware sono simili al funzionamento della modalità loopback WASAPI, possono essere più difficili da usare.

I dispositivi loopback hardware hanno gli svantaggi seguenti per le applicazioni audio:

-   Non tutte le schede audio hanno dispositivi di loopback. Di conseguenza, le applicazioni che dipendono da esse non funzionano in tutti i sistemi.
-   Prima che un'applicazione possa registrare da un dispositivo loopback, l'utente deve identificare il dispositivo loopback e abilitarlo per l'uso.

Fornitori diversi assegnano nomi diversi ai dispositivi di loopback hardware. I nomi seguenti sono esempi:

-   Stereo Mix
-   Waveout Mix
-   Output misto
-   What You Hear

La mancanza di nomi standardizzati potrebbe causare agli utenti difficoltà a identificare un dispositivo loopback in un elenco di nomi di dispositivi.

Un dispositivo di loopback hardware è un dispositivo di acquisizione. Pertanto, se un adattatore supporta un dispositivo loopback, un'applicazione audio può registrare dal dispositivo nello stesso modo in cui registra da qualsiasi altro dispositivo di acquisizione.

Ad esempio, se si seleziona un dispositivo di loopback hardware come dispositivo di acquisizione predefinito, è possibile usare la funzione RecordAudioStream (senza modifiche) nell'esempio di codice [in](capturing-a-stream.md) Acquisizione di un flusso per acquisire il flusso dal dispositivo. È anche possibile usare un'API audio legacy, ad esempio le funzioni **waveInXxx** multimediali Windows, per acquisire il flusso dal dispositivo.

Se la scheda audio contiene un dispositivo di loopback hardware, è possibile usare il pannello di controllo multimediale di Windows, Mmsys.cpl, per designare il dispositivo come dispositivo di acquisizione predefinito. Attenersi alla procedura seguente:

1.  Per eseguire Mmsys.cpl, aprire una finestra del prompt dei comandi e immettere il comando seguente:

    ```C++
    control mmsys.cpl,,1
    ```

    

    In alternativa, è possibile eseguire Mmsys.cpl facendo clic con il pulsante destro del mouse sull'icona del parlante nell'area di notifica, che si trova sul lato destro della barra delle applicazioni, e selezionando Registrazione **dispositivi**.

2.  Dopo l'Mmsys.cpl visualizzata, fare clic con il pulsante destro del mouse in un punto qualsiasi dell'elenco dei dispositivi di registrazione e verificare che l'opzione **Mostra dispositivi** disabilitati sia selezionata. In caso contrario, se il dispositivo loopback è disabilitato, non verrà visualizzato nell'elenco.
3.  Esplorare l'elenco dei dispositivi di registrazione per individuare il dispositivo loopback( se esistente). Se il dispositivo loopback è disabilitato, abilitarlo facendo clic con il pulsante destro del mouse sul dispositivo e scegliendo **Abilita**.
4.  Infine, per selezionare il dispositivo loopback come dispositivo di acquisizione predefinito, fare clic con il pulsante destro del mouse sul dispositivo e scegliere **Imposta come dispositivo predefinito.**

WASAPI supporta la registrazione loopback indipendentemente dal fatto che l'hardware audio contenga un dispositivo loopback o che l'utente abbia abilitato il dispositivo.

Windows Vista offre DRM (Digital Rights Management). I provider di contenuti si basano su DRM per proteggere la musica proprietaria o altro contenuto da copie non autorizzate e altri usi non autorizzati. Analogamente, un driver audio attendibile non consente a un dispositivo loopback di acquisire flussi digitali che contengono contenuto protetto. Windows Vista consente solo ai driver attendibili di riprodurre contenuto protetto. Per altre informazioni sui driver attendibili e su DRM, vedere la documentazione Windows DDK.

Il loopback WASAPI contiene la combinazione di tutto l'audio riprodotto, indipendentemente dalla sessione di Servizi terminal da cui ha avuto origine l'audio. Ad esempio, è possibile eseguire un client di loopback in un servizio in esecuzione nella sessione 0 e acquisire l'audio da tutte le sessioni utente, nonché l'audio riprodotto dalla sessione 0.

Desktop remoto consente il reindirizzamento dell'audio al client. Questa operazione viene implementata creando nuovi dispositivi audio che vengono visualizzati solo per la sessione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> </dl>

 

 



