---
description: Questa applicazione di esempio illustra l'apertura e la chiusura dei flussi di comunicazione e la causa di eventi di chiusura che un'applicazione può ottenere per implementare l'attenuazione del flusso.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76515f9d20e31bf4583b715e09da38c29bfdac34f6c975087f64bf2617696542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018459"
---
# <a name="duckingcapturesample"></a>DuckingCaptureSample

Questa applicazione di esempio illustra l'apertura e la chiusura dei flussi di comunicazione e la causa di eventi di chiusura che un'applicazione può ottenere per implementare l'attenuazione del flusso. Questa applicazione implementa un client di chat che usa le API Audio core per leggere i dati audio da un dispositivo di comunicazione e riprodurlo nel dispositivo di output.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

Questo esempio illustra le funzionalità seguenti.

-   [API MMDevice per](mmdevice-api.md) l'enumerazione e la selezione di dispositivi multimediali.
-   [WASAPI per l'accesso](wasapi.md) al dispositivo di acquisizione e rendering delle comunicazioni, le operazioni di gestione dei flussi e la gestione degli eventi di acquisizione delle comunicazioni.
-   [API WAVE per l'accesso](/previous-versions//ms713499(v=vs.85)) al dispositivo di comunicazione e l'acquisizione dell'input audio.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio 2008                                             |           |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Località    | Percorso/URL                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK Windows \\ \\ v7.0 \\ Samples \\ Multimedia Audio \\ \\ DuckingCaptureSample \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio DuckingCaptureSample, seguire questa procedura:

1.  Aprire Il file DuckingCaptureSample.sln in Visual Studio 2008.
2.  Nella finestra selezionare la configurazione  della soluzione **Debug** o Versione, scegliere il **menu** Compila dalla barra dei menu e selezionare l'opzione **Compila.** Se non si apre Visual Studio shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposta in modo esplicito la variabile di ambiente MSSdk, usata nel file di progetto, DuckingCaptureSample.vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se l'applicazione viene compilata correttamente, viene generato un file eseguibile DuckingCaptureSample.exe file. Per eseguirlo, scegliere **Avvia debug** o Avvia senza **eseguire debug** dal menu **Debug** o digitare in una finestra `DuckingCaptureSample` di comando.

DuckingCaptureSample fornisce all'utente due implementazioni per acquisire l'audio dal dispositivo console predefinito: LE API WASAPI e Wave. Per avviare una sessione di acquisizione, selezionare una modalità e fare clic **su Avvia** nell'interfaccia utente dell'applicazione. Per terminare la sessione, fare clic su **Arresta**. A seconda del dispositivo specificato dall'utente (input o output), l'applicazione usa l'API MMDevice per ottenere un riferimento al dispositivo di comunicazione di rendering o acquisizione predefinito. Dopo che l'utente ha avviato una sessione di chat, l'applicazione esegue le attività seguenti:

-   Crea e inizializza un client audio in modalità basata su eventi.
-   Associa il client all'handle dell'evento che segnala che gli esempi sono pronti per l'acquisizione o il rendering.
-   Configura un client di acquisizione e un client di rendering per il trasporto.
-   Crea il thread di chat e avvia il motore audio.

Per l'acquisizione di dati audio, con ogni passaggio di elaborazione, l'esempio usa il client di acquisizione per ottenere la quantità totale di dati acquisiti disponibili nel buffer, leggere i dati dal dispositivo di input predefinito e rilasciare il pacchetto e rendere disponibile il buffer per la lettura del set successivo di dati acquisiti.

Per il rendering, l'applicazione determina la quantità di dati accodati per la riproduzione nel buffer dell'endpoint di acquisizione. Scrive di conseguenza nel buffer e rilascia il buffer in preparazione del successivo passaggio di elaborazione fino a quando non vengono scritti tutti i dati. Per il rendering, i fotogrammi invisibile all'utente vengono pre-acquisiti per impedire al motore audio di avere problemi all'avvio. DuckingCaptureSample mostra anche come nascondere il flusso di rendering dal mixer di volumi.

Per altre informazioni sulla funzionalità di attenuazione del flusso, vedere [Uso di un dispositivo di comunicazione](using-the-communication-device.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio di base](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
