---
description: Formati dei dispositivi
ms.assetid: 591437e4-21ef-42f1-a752-7f50440cbd63
title: Formati dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332f3ecd4b30213328552077bdef040a63e31992deaf217b77838dd0cd0797f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957340"
---
# <a name="device-formats"></a>Formati dei dispositivi

Per un'applicazione audio, un vantaggio dell'uso di un'API audio di livello superiore, ad esempio DirectSound o le funzioni **waveOutXxx** multimediali di Windows, è che l'API esegue automaticamente la conversione tra i formati di flusso usati dall'applicazione e i formati usati dal dispositivo audio. Al contrario, le API audio di base sono più restrittive perché richiedono che i flussi dell'applicazione usino formati uguali o strettamente correlati ai formati usati dal dispositivo. Di conseguenza, le applicazioni che usano le API audio di base per riprodurre o registrare flussi audio potrebbero essere necessarie per eseguire alcune o tutte le conversioni tra formati di flusso.

Un'applicazione che usa WASAPI per gestire i flussi in modalità condivisa può basarsi sul motore audio per eseguire solo conversioni di formato limitate. Il motore audio può eseguire la conversione tra le dimensioni del campione PCM standard usate dall'applicazione e i campioni a virgola mobile usati dal motore per l'elaborazione interna. Tuttavia, il formato per un flusso dell'applicazione deve in genere avere lo stesso numero di canali e la stessa frequenza di campionamento del formato di flusso usato dal dispositivo.

Se un'applicazione usa un dispositivo in modalità esclusiva, l'applicazione deve usare un formato di flusso supportato in modo esplicito dall'hardware audio. In modalità esclusiva, l'applicazione e il dispositivo scambiano i dati audio direttamente, senza intervento del motore audio.

Molti dispositivi audio supportano sia formati di flusso PCM che non PCM. Tuttavia, il motore audio può combinare solo flussi PCM. Di conseguenza, solo i flussi in modalità esclusiva possono avere formati non PCM. Inoltre, solo i formati non PCM con velocità dati fisse sono supportati in modalità esclusiva. Un esempio di formato non PCM a velocità fissa è un flusso audio Windows Media Audio Professional (WMA Pro) a 48 kHz che passa attraverso un collegamento S/PDIF (Digital Interface) di Sony/Philips senza essere decodificato. Per altre informazioni sull'uso di flussi Pro WMA su S/PDIF, vedere la documentazione seguente:

-   Descrizione del tag wave WAVE FORMAT WMA SPDIF nella documentazione Windows \_ \_ \_ DDK.
-   Il white paper intitolato "Supporto dei driver audio per il formato WMA Pro-over-S/PDIF" nel sito [Web di Audio Device Technologies for Windows.](https://www.microsoft.com/whdc/device/audio/default.mspx)

WASAPI usa una **struttura WAVEFORMATEX** o **WAVEFORMATEXTENSIBLE** per specificare un formato di flusso. Una **struttura WAVEFORMATEXTENSIBLE** è in effetti una **struttura WAVEFORMATEX** estesa per descrivere una maggiore gamma di formati. Qualsiasi formato che può essere descritto da una struttura **WAVEFORMATEX** autonoma può essere descritto anche da una **struttura WAVEFORMATEXTENSIBLE.**

Il primo membro della **struttura WAVEFORMATEXTENSIBLE** è una **struttura WAVEFORMATEX.** Il contenuto di **una struttura WAVEFORMATEX** indica se è una struttura **WAVEFORMATEX** autonoma o parte di **una struttura WAVEFORMATEXTENSIBLE.**

Una struttura **WAVEFORMATEX** autonoma può descrivere in modo adeguato un formato con uno o due canali e una dimensione del campione che è un multiplo di 8 bit. Di per sé, una **struttura WAVEFORMATEX** non può specificare il mapping dei canali alle posizioni del parlante. Inoltre, anche se **WAVEFORMATEX** specifica le dimensioni del contenitore per ogni campione audio, non può specificare il numero di bit di precisione in un campione (ad esempio, 20 bit di precisione in un contenitore a 24 bit). Al contrario, la **struttura WAVEFORMATEXTENSIBLE** può specificare sia il mapping dei canali agli altoparlanti che il numero di bit di precisione in ogni campione.

Per altre informazioni su **WAVEFORMATEX** e **WAVEFORMATEXTENSIBLE,** vedere la documentazione Windows DDK.

A partire da Windows 7, **WAVEFORMATEXTENSIBLE** è stato esteso per rappresentare i formati di dispositivo per la trasmissione di audio codificato su un'interfaccia compatibile con IEC 61937. Per informazioni sulla nuova struttura, vedere Rappresentazione dei formati per le trasmissioni [IEC 61937](representing-formats-for-iec-61937-transmissions.md).

### <a name="specifying-the-device-format"></a>Specifica del formato del dispositivo

I metodi WASAPI seguenti usano le **strutture WAVEFORMATEX** e **WAVEFORMATEXTENSIBLE** per descrivere i formati di flusso:

-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)
-   [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

Il **metodo GetMixFormat** recupera il formato di flusso utilizzato dal motore audio per l'elaborazione interna dei flussi in modalità condivisa. Il metodo usa sempre una **struttura WAVEFORMATEXTENSIBLE,** anziché una struttura **WAVEFORMATEX** autonoma, per specificare il formato.

Il **metodo IsFormatSupported** indica se un dispositivo endpoint audio supporta un formato di flusso specifico. Il chiamante deve specificare se il formato del flusso deve essere utilizzato in modalità condivisa o in modalità esclusiva. Per i formati in modalità condivisa, il metodo esegue una query sul motore audio per determinare se supporta il formato specificato. Per i formati in modalità esclusiva, il metodo esegue una query sul driver di dispositivo. Alcuni driver di dispositivo segnalano che supportano un formato PCM a 1 canale o a 2 canali se il formato è specificato da una struttura **WAVEFORMATEX** autonoma, ma rifiuterà lo stesso formato se specificato da una **struttura WAVEFORMATEXTENSIBLE.** Per ottenere risultati affidabili da questi driver, le applicazioni in modalità esclusiva devono chiamare **IsFormatSupported** due volte per ogni formato PCM a 1 canale o a 2 canali. Una chiamata deve usare una struttura **WAVEFORMATEX** autonoma per specificare il formato e l'altra chiamata deve usare una struttura **WAVEFORMATEXTENSIBLE** per specificare lo stesso formato.

Dopo che un'applicazione ha usato **GetMixFormat** o **IsFormatSupported** per trovare un formato appropriato per un flusso in modalità condivisa o esclusiva, l'applicazione può chiamare il **metodo Initialize** per inizializzare un flusso con tale formato. Un'applicazione che tenta di inizializzare un flusso in modalità condivisa con un formato non identico al formato di combinazione ottenuto dal metodo **GetMixFormat,** ma con lo stesso numero di canali e la stessa frequenza di campionamento del formato di combinazione, avrà probabilmente esito positivo. Prima di **chiamare Initialize**, l'applicazione può chiamare **IsFormatSupported** per verificare che **Initialize** accetti il formato.

Il formato di combinazione utilizzato dal motore audio per l'elaborazione interna dei flussi in modalità condivisa è strettamente correlato, ma non è necessariamente identico al formato di flusso utilizzato dal dispositivo endpoint audio in modalità condivisa. Tramite il Windows di controllo multimediale, Mmsys.cpl, l'utente può selezionare il formato di flusso che verrà utilizzato da un dispositivo endpoint audio quando funziona in modalità condivisa. Attenersi alla procedura seguente:

1.  Per eseguire Mmsys.cpl, aprire una finestra del prompt dei comandi e immettere il comando seguente:

    **controllo mmsys.cpl**

    In alternativa, è possibile eseguire Mmsys.cpl facendo clic con il pulsante destro del mouse sull'icona del parlante nell'area di notifica, che si trova sul lato destro della barra delle applicazioni, e selezionando Dispositivi di riproduzione o Dispositivi di **registrazione**. 

2.  Dopo aver aperto Mmsys.cpl, selezionare un dispositivo dall'elenco dei dispositivi di riproduzione o dall'elenco dei dispositivi di registrazione e fare clic su **Proprietà**.
3.  Quando si apre la finestra delle proprietà, fare clic su Avanzate **e** selezionare un formato nell'elenco dei formati disponibili nella casella **Formato predefinito**.

Si supponga, ad esempio, che l'utente seleziona il formato predefinito seguente dall'elenco dei formati disponibili per un dispositivo di riproduzione:

**2 canali, 16 bit, 44100 Hz (qualità CD)**

Questo è il formato che il dispositivo userà successivamente quando opera in modalità condivisa. In Windows Vista, il motore audio userà una versione leggermente modificata di questo formato per l'elaborazione interna dei flussi in modalità condivisa. Il motore audio userà un formato con lo stesso numero di canali (due) e la stessa frequenza di campionamento (44100 Hz), ma convertirà gli esempi in numeri a virgola mobile prima di elaborarli. Il motore audio convertirà gli esempi a virgola mobile nella combinazione di output in numeri interi a 16 bit prima di riproducerli tramite il dispositivo.

Un'applicazione può eseguire una query sulla proprietà [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md) di un dispositivo endpoint audio per ottenere il formato in modalità condivisa selezionato dall'utente per il dispositivo. Per informazioni sull'esecuzione di query sulle proprietà di un dispositivo, vedere [Proprietà del dispositivo](device-properties.md).

Alcune applicazioni potrebbero trovare che il formato specificato dalla proprietà **PKEY \_ AudioEngine \_ DeviceFormat** di un dispositivo sia un formato adatto per l'apertura di un flusso in modalità esclusiva nel dispositivo. Altre applicazioni che gestiscono flussi in modalità esclusiva potrebbero avere requisiti aggiuntivi che imponeno una negoziazione del formato complessa con il dispositivo. In genere, una di queste applicazioni costruisce un elenco di formati adatti, con i formati preferiti all'inizio dell'elenco. L'applicazione chiama quindi in modo iterativo **IsFormatSupported** con ogni formato successivo nell'elenco, a partire dall'inizio dell'elenco, finché non trova un formato supportato dal dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



