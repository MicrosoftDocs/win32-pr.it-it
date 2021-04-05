---
description: Formati di dispositivo
ms.assetid: 591437e4-21ef-42f1-a752-7f50440cbd63
title: Formati di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcd1b611075191e522cf00d959f120abfb3baa9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125763"
---
# <a name="device-formats"></a>Formati di dispositivo

Per un'applicazione audio, un vantaggio derivante dall'uso di un'API audio di livello superiore, ad esempio DirectSound o le funzioni **waveOutXxx** multimediali di Windows, consiste nel fare in modo che l'API si converta automaticamente tra i formati di flusso usati dall'applicazione e i formati usati dal dispositivo audio. Al contrario, le API di base audio sono più restrittive perché richiedono che i flussi dell'applicazione usino formati identici a quelli di o sono strettamente correlati ai formati usati dal dispositivo. In questo modo, le applicazioni che usano le API di base per riprodurre o registrare flussi audio potrebbero essere necessarie per eseguire alcune o tutte le conversioni tra formati di flusso.

Un'applicazione che usa WASAPI per gestire i flussi in modalità condivisa può basarsi sul motore audio per eseguire solo conversioni di formato limitate. Il motore audio è in grado di eseguire la conversione tra le dimensioni campione PCM standard utilizzate dall'applicazione e gli esempi a virgola mobile utilizzati dal motore per l'elaborazione interna. Tuttavia, il formato per un flusso di applicazioni in genere deve avere lo stesso numero di canali e la stessa frequenza di campionamento del formato del flusso usato dal dispositivo.

Se un'applicazione usa un dispositivo in modalità esclusiva, l'applicazione deve usare un formato di flusso supportato in modo esplicito dall'hardware audio. In modalità esclusiva, l'applicazione e il dispositivo scambiano i dati audio direttamente, senza l'intervento del motore audio.

Molti dispositivi audio supportano sia il formato PCM che il formato di flusso non PCM. Tuttavia, il motore audio può combinare solo flussi PCM. In questo modo, solo i flussi in modalità esclusiva possono avere formati non PCM. Inoltre, solo i formati non PCM con frequenza dati fissa sono supportati in modalità esclusiva. Un esempio di formato non PCM a frequenza fissa è un flusso audio a 48 kHz Windows Media Audio Professional (WMA Pro) che passa attraverso un collegamento di interfaccia digitale (S/PDIF) Sony/Philips in formato digitale senza essere decodificato. Per ulteriori informazioni sull'utilizzo di flussi WMA Pro su S/PDIF, vedere la documentazione seguente:

-   Descrizione del Tag Format WAVE \_ \_ WMA \_ SPDIF Wave Format nella documentazione di Windows DDK.
-   Il white paper denominato "supporto driver audio per il formato WMA Pro-Over-S/PDIF" nel sito Web delle [tecnologie per dispositivi audio per Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

WASAPI usa una struttura **WAVEFORMATEX** o **WAVEFORMATEXTENSIBLE** per specificare un formato di flusso. Una struttura **WAVEFORMATEXTENSIBLE** è effettivamente una struttura **WAVEFORMATEX** che è stata estesa per descrivere un intervallo di formati più ampio. Qualsiasi formato che può essere descritto da una struttura **WAVEFORMATEX** autonoma può anche essere descritto da una struttura **WAVEFORMATEXTENSIBLE** .

Il primo membro della struttura **WAVEFORMATEXTENSIBLE** è una struttura **WAVEFORMATEX** . Il contenuto di una struttura **WAVEFORMATEX** indica se si tratta di una struttura **WAVEFORMATEX** autonoma o di una parte di una struttura **WAVEFORMATEXTENSIBLE** .

Una struttura **WAVEFORMATEX** autonoma può descrivere in modo adeguato un formato con uno o due canali e una dimensione di esempio costituita da un multiplo di 8 bit. Una struttura **WAVEFORMATEX** non è in grado di specificare il mapping dei canali alle posizioni degli altoparlanti. Inoltre, anche se **WAVEFORMATEX** specifica le dimensioni del contenitore per ogni esempio audio, non può specificare il numero di bit di precisione in un campione, ad esempio 20 bit di precisione in un contenitore a 24 bit. Al contrario, la struttura **WAVEFORMATEXTENSIBLE** può specificare sia il mapping dei canali agli altoparlanti sia il numero di bit di precisione in ogni campione.

Per ulteriori informazioni su **WAVEFORMATEX** e **WAVEFORMATEXTENSIBLE**, vedere la documentazione di Windows DDK.

A partire da Windows 7, **WAVEFORMATEXTENSIBLE** è stato esteso per rappresentare i formati di dispositivo per la trasmissione di audio codificato tramite un'interfaccia compatibile con IEC 61937. Per informazioni sulla nuova struttura, vedere [rappresentazione di formati per trasmissioni IEC 61937](representing-formats-for-iec-61937-transmissions.md).

### <a name="specifying-the-device-format"></a>Specifica del formato del dispositivo

I metodi WASAPI seguenti usano le strutture **WAVEFORMATEX** e **WAVEFORMATEXTENSIBLE** per descrivere i formati di flusso:

-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)
-   [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

Il metodo **GetMixFormat** Recupera il formato di flusso utilizzato dal motore audio per l'elaborazione interna dei flussi in modalità condivisa. Il metodo usa sempre una struttura **WAVEFORMATEXTENSIBLE** , anziché una struttura **WAVEFORMATEX** autonoma, per specificare il formato.

Il metodo **IsFormatSupported** indica se un dispositivo endpoint audio supporta un formato di flusso specifico. Il chiamante deve specificare se il formato del flusso deve essere utilizzato in modalità condivisa o in modalità esclusiva. Per i formati in modalità condivisa, il metodo esegue una query sul motore audio per determinare se supporta il formato specificato. Per i formati in modalità esclusiva, il metodo esegue una query sul driver di dispositivo. Alcuni driver di dispositivo segnaleranno che supportano un formato PCM a 1 canale o a 2 canali se il formato è specificato da una struttura **WAVEFORMATEX** autonoma, ma rifiuterà lo stesso formato se è specificato da una struttura **WAVEFORMATEXTENSIBLE** . Per ottenere risultati affidabili da questi driver, le applicazioni in modalità esclusiva devono chiamare **IsFormatSupported** due volte per ogni formato PCM a 1 canale o a 2 canali: una chiamata deve usare una struttura **WAVEFORMATEX** autonoma per specificare il formato e l'altra chiamata deve usare una struttura **WAVEFORMATEXTENSIBLE** per specificare lo stesso formato.

Dopo che un'applicazione ha usato **GetMixFormat** o **IsFormatSupported** per trovare un formato appropriato per un flusso in modalità condivisa o esclusiva, l'applicazione può chiamare il metodo **Initialize** per inizializzare un flusso con tale formato. Un'applicazione che tenta di inizializzare un flusso in modalità condivisa con un formato non identico al formato di combinazione ottenuto dal metodo **GetMixFormat** , ma con lo stesso numero di canali e la stessa frequenza di campionamento del formato di combinazione, è probabile che abbia esito positivo. Prima di chiamare **Initialize**, l'applicazione può chiamare **IsFormatSupported** per verificare che **Initialize** accetterà il formato.

Il formato di combinazione utilizzato dal motore audio per l'elaborazione interna dei flussi in modalità condivisa è strettamente correlato a, ma non è necessariamente identico a, il formato di flusso utilizzato dal dispositivo dell'endpoint audio in modalità condivisa. Tramite il pannello di controllo multimediale di Windows, Mmsys.cpl, l'utente può selezionare il formato di flusso che verrà usato da un dispositivo dell'endpoint audio quando opera in modalità condivisa. Attenersi alla procedura seguente:

1.  Per eseguire Mmsys.cpl, aprire una finestra del prompt dei comandi e immettere il comando seguente:

    **mmsys.cpldi controllo**

    In alternativa, è possibile eseguire Mmsys.cpl facendo clic con il pulsante destro del mouse sull'icona dell'altoparlante nell'area di notifica che si trova sul lato destro della barra delle applicazioni e selezionando **dispositivi di riproduzione** o dispositivi di **registrazione**.

2.  Una volta aperta la finestra di Mmsys.cpl, selezionare un dispositivo nell'elenco dei dispositivi di riproduzione o nell'elenco dei dispositivi di registrazione e fare clic su **Proprietà**.
3.  Quando viene visualizzata la finestra Proprietà, fare clic su **Avanzate** e selezionare un formato nell'elenco dei formati disponibili nella casella **formato predefinito**.

Si supponga, ad esempio, che l'utente selezioni il formato predefinito seguente nell'elenco dei formati disponibili per un dispositivo di riproduzione:

**2 canali, 16 bit, 44100 Hz (qualità CD)**

Si tratta del formato che verrà usato successivamente dal dispositivo in modalità condivisa. In Windows Vista, il motore audio userà una versione leggermente modificata del formato per l'elaborazione interna dei flussi in modalità condivisa. Il motore audio userà un formato con lo stesso numero di canali (due) e la stessa frequenza di campionamento (44100 Hz), ma convertirà i campioni in numeri a virgola mobile prima di elaborarli. Il motore audio converte gli esempi a virgola mobile nella combinazione di output in interi a 16 bit prima di riprodurli tramite il dispositivo.

Un'applicazione può eseguire una query sulla proprietà [**pkey \_ Audioengine \_ DeviceFormat**](pkey-audioengine-deviceformat.md) del dispositivo di un endpoint audio per ottenere il formato in modalità condivisa selezionato dall'utente per il dispositivo. Per informazioni sull'esecuzione di query sulle proprietà di un dispositivo, vedere [proprietà del dispositivo](device-properties.md).

Alcune applicazioni potrebbero trovare il formato specificato dalla proprietà **pkey \_ Audioengine \_ DeviceFormat** del dispositivo come formato appropriato per l'apertura di un flusso in modalità esclusiva sul dispositivo. Altre applicazioni che gestiscono flussi in modalità esclusiva potrebbero avere requisiti aggiuntivi che richiedono una negoziazione del formato complesso con il dispositivo. In genere, una di queste applicazioni costruisce un elenco di formati appropriati, con i formati preferiti all'inizio dell'elenco. L'applicazione chiama quindi in modo iterativo **IsFormatSupported** con ogni formato successivo nell'elenco, iniziando dall'inizio dell'elenco, fino a quando non viene trovato un formato supportato dal dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



