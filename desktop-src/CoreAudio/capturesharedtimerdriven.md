---
description: Questa applicazione di esempio usa le API Audio core per acquisire dati audio da un dispositivo di input specificato dall'utente e scrive i dati in un file wav denominato in modo univoco nella directory corrente. In questo esempio viene illustrata la memorizzazione nel buffer basata su timer.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d9e8cbd686bdd71804ed067a5b3d9ff36ed8271c8b0edb04b8077ca162fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957380"
---
# <a name="capturesharedtimerdriven"></a>CaptureSharedTimerDriven

Questa applicazione di esempio usa le API Audio core per acquisire dati audio da un dispositivo di input specificato dall'utente e scrive i dati in un file wav denominato in modo univoco nella directory corrente. In questo esempio viene illustrata la memorizzazione nel buffer basata su timer.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

In questo esempio vengono illustrate le funzionalità seguenti.

-   [API MMDevice per](mmdevice-api.md) l'enumerazione e la selezione di dispositivi multimediali.
-   [WASAPI per](wasapi.md) le operazioni di gestione dei flussi.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Località    | Percorso/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK Windows \\ \\ v7.0 \\ Samples \\ Multimedia Audio \\ \\ CaptureSharedTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio CaptureSharedTimerDriven, seguire questa procedura:

1.  Aprire la shell CMD per Windows SDK e passare alla directory di esempio CaptureSharedTimerDriven.
2.  Eseguire il comando nella directory CaptureSharedTimerDriven per aprire il progetto `start WASAPICaptureSharedTimerDriven.sln` WASAPICaptureSharedTimerDriven nella Visual Studio predefinita.
3.  Nella finestra selezionare la configurazione della soluzione **Debug** o **Release,** selezionare il **menu** Compila dalla barra dei menu e selezionare l'opzione **Compila.** Se non si apre un Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposta in modo esplicito la variabile di ambiente MSSdk, usata nel file di progetto WASAPICaptureSharedTimerDriven.vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se l'applicazione demo viene compilata correttamente, viene generato WASAPICaptureSharedTimerDriven.exe file eseguibile. Per eseguirlo, digitare `WASAPICaptureSharedTimerDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi. Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata dell'acquisizione nel dispositivo multimediale predefinito.

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

Nella tabella seguente vengono illustrati gli argomenti.

| Argomento        | Descrizione                                                |
|-----------------|------------------------------------------------------------|
| -?              | Visualizza la Guida.                                                |
| -H              | Visualizza la Guida.                                                |
| -l              | Latenza di acquisizione audio in millisecondi.                     |
| -d              | Durata dell'acquisizione audio in secondi.                         |
| -M              | Disabilita l'utilizzo di MMCSS.                                 |
| -console        | Usare il dispositivo console predefinito.                            |
| -communications | Usare il dispositivo di comunicazione predefinito.                      |
| -multimedia     | Usare il dispositivo multimediale predefinito.                         |
| -endpoint       | Usare l'identificatore dell'endpoint specificato nel valore dell'opzione. |



 

Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e chiede all'utente di selezionare un dispositivo per la sessione di acquisizione. La console predefinita, le comunicazioni e i dispositivi multimediali sono elencati seguiti dai dispositivi e dagli identificatori dell'endpoint. Se non viene specificata alcuna durata, il flusso audio dal dispositivo specificato viene acquisito per 10 secondi. L'applicazione scrive i dati acquisiti in un file wav denominato in modo univoco.

CaptureSharedTimerDriven illustra il buffering basato su timer. In questa modalità, il client deve attendere un periodo di tempo (metà della latenza, specificata dal valore dell'opzione -d, in millisecondi). Quando il client si riattiva, a metà del periodo di elaborazione, esegue il pull del set successivo di campioni dal motore. Prima del passaggio di ogni elaborazione nel ciclo di buffering, il client deve individuare la quantità di dati di acquisizione disponibili in modo che i dati non superino il buffer di acquisizione. I dati audio acquisiti dal dispositivo specificato possono essere elaborati abilitando il buffering basato su eventi. Questa modalità è illustrata [nell'esempio CaptureSharedEventDriven.](capturesharedeventdriven.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio di base](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



