---
description: Questa applicazione di esempio illustra l'apertura e la chiusura di flussi di comunicazione e la generazione di eventi ducking che un'applicazione può ottenere per implementare l'attenuazione del flusso.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878334"
---
# <a name="duckingcapturesample"></a>DuckingCaptureSample

Questa applicazione di esempio illustra l'apertura e la chiusura di flussi di comunicazione e la generazione di eventi ducking che un'applicazione può ottenere per implementare l'attenuazione del flusso. Questa applicazione implementa un client di chat che usa le API audio principali per leggere i dati audio da un dispositivo di comunicazione e riprodurli sul dispositivo di output.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

In questo esempio vengono illustrate le funzionalità seguenti.

-   [API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.
-   [WASAPI](wasapi.md) per l'accesso al dispositivo di acquisizione e rendering delle comunicazioni, alle operazioni di gestione del flusso e alla gestione degli eventi ducking.
-   [API Wave](/previous-versions//ms713499(v=vs.85)) per accedere al dispositivo di comunicazione e acquisire l'input audio.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio 2008                                             |           |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Location    | Percorso/URL                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ DuckingCaptureSample \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio DuckingCaptureSample, seguire questa procedura:

1.  Aprire DuckingCaptureSample. sln in Visual Studio 2008.
2.  Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** . Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, DuckingCaptureSample. vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se l'applicazione viene compilata correttamente, viene generato un file eseguibile, DuckingCaptureSample.exe. Per eseguirlo, selezionare **Avvia debug** o **Avvia senza eseguire debug** dal menu **debug** oppure digitare `DuckingCaptureSample` una finestra di comando.

DuckingCaptureSample fornisce all'utente due implementazioni per acquisire l'audio dal dispositivo console predefinito: WASAPI e le API Wave. Per avviare una sessione di acquisizione, selezionare una modalità e fare clic su **Avvia** nell'interfaccia utente dell'applicazione. Per terminare la sessione, fare clic su **Arresta**. A seconda del dispositivo specificato dall'utente (input o output), l'applicazione usa l'API MMDevice per ottenere un riferimento al dispositivo di comunicazione predefinito di rendering o acquisizione. Dopo l'avvio di una sessione di chat da parte dell'utente, l'applicazione esegue le attività seguenti:

-   Crea e Inizializza un client audio in modalità guidata dagli eventi.
-   Associa il client all'handle di evento che segnala che gli esempi sono pronti per l'acquisizione o il rendering.
-   Imposta un client di acquisizione e un client di rendering per il trasporto.
-   Crea il thread di chat e avvia il motore audio.

Per l'acquisizione di dati audio, a ogni passaggio di elaborazione, l'esempio usa il client di acquisizione per ottenere la quantità totale di dati acquisiti disponibili nel buffer, leggere i dati dal dispositivo di input predefinito e rilasciare il pacchetto e rendere disponibile il buffer per la lettura del set successivo di dati acquisiti.

Per il rendering, l'applicazione determina la quantità di dati accodati per la riproduzione nel buffer dell'endpoint di acquisizione. Scrive di conseguenza nel buffer e rilascia il buffer in preparazione al successivo passaggio di elaborazione fino a quando tutti i dati non sono stati scritti. Per il rendering, i frame invisibili vengono preregistrati per impedire che il motore audio si inconvenienti all'avvio. DuckingCaptureSample Mostra anche come nascondere il flusso di rendering dal mixer del volume.

Per altre informazioni sulla funzionalità di attenuazione dei flussi, vedere [uso di un dispositivo di comunicazione](using-the-communication-device.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio principali](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
