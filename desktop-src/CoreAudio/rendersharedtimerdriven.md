---
description: Questa applicazione di esempio, che illustra il buffering basato su timer, usa le API Audio core per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89d2814f359668f8724d3deb65a7c2a9eeff5b06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410094"
---
# <a name="rendersharedtimerdriven"></a>RenderSharedTimerDriven

Questa applicazione di esempio usa le API Core Audio per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente. Questo esempio illustra il buffering basato su timer per un client di rendering in modalità condivisa. Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio.

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
-   WASAPI per le operazioni di gestione dei flussi.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Percorso    | Percorso/URL                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ RenderSharedTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio RenderSharedTimerDriven, seguire questa procedura:

1.  Aprire la shell CMD per il Windows SDK e passare alla directory di esempio RenderSharedTimerDriven.
2.  Eseguire il `start WASAPIRenderSharedTimerDriven.sln` comando nella directory RenderSharedTimerDriven per aprire il progetto WASAPIRenderSharedTimerDriven nella finestra Visual Studio.
3.  Nella finestra selezionare la configurazione  della soluzione **Debug** o Versione, scegliere il **menu** Compila dalla barra dei menu e selezionare l'opzione **Compila.** Se non si apre Visual Studio shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposta in modo esplicito la variabile di ambiente MSSdk, usata nel file di progetto WASAPIRenderSharedTimerDriven.vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se si compila correttamente l'applicazione demo, viene generato un file eseguibile, WASAPIRenderSharedTimerDriven.exe, Per eseguirlo, digitare `WASAPIRenderSharedTimerDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi. Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata della riproduzione nel dispositivo multimediale predefinito.

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

Nella tabella seguente vengono illustrati gli argomenti .

| Argomento        | Descrizione                                                |
|-----------------|------------------------------------------------------------|
| -?              | Visualizza la Guida.                                                |
| -H              | Visualizza la Guida.                                                |
| -f              | Frequenza delle onde sinsino in Hz.                                 |
| -l              | Latenza di rendering audio in millisecondi.                      |
| -d              | Durata dell'ondata seno in secondi.                             |
| -M              | Disabilita l'uso di MMCSS.                                 |
| -console        | Usare il dispositivo console predefinito.                            |
| -communications | Usare il dispositivo di comunicazione predefinito.                      |
| -multimedia     | Usare il dispositivo multimediale predefinito.                         |
| -endpoint       | Usare l'identificatore dell'endpoint specificato nel valore dell'opzione. |



 

Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e richiede all'utente di selezionare un dispositivo per la sessione di rendering. Dopo che l'utente ha specificato un dispositivo, l'applicazione esegue il rendering di un'onda seno a 440 Hz per 10 secondi. Questi valori possono essere modificati specificando i valori delle opzioni -f e -d.

RenderSharedTimerDriven illustra il buffer basato su timer. In questa modalità, il client deve attendere un periodo di tempo (metà della latenza, specificata dal valore dell'opzione -d, in millisecondi). Quando il client si riattiva, a metà del periodo di elaborazione, estrae il set successivo di campioni dal motore. Prima che ogni elaborazione passi nel ciclo di memorizzazione nel buffer, il client deve individuare la quantità di dati di cui eseguire il rendering in modo che i dati non esercitino il buffer.

I dati audio da riprodurre nel dispositivo specificato possono essere elaborati abilitando il buffer basato su eventi. Questa modalità è illustrata [nell'esempio RenderSharedEventDriven.](rendersharedeventdriven.md)

Per altre informazioni sul rendering di un flusso, vedere [Rendering di un flusso](rendering-a-stream.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio di base](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



