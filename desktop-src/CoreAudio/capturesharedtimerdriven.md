---
description: Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input specificato dall'utente e lo scrive in un file con estensione wav denominato in modo univoco nella directory corrente. Questo esempio illustra il buffering basato sul timer.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049200"
---
# <a name="capturesharedtimerdriven"></a>CaptureSharedTimerDriven

Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input specificato dall'utente e lo scrive in un file con estensione wav denominato in modo univoco nella directory corrente. Questo esempio illustra il buffering basato sul timer.

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
-   [WASAPI](wasapi.md) per le operazioni di gestione del flusso.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Location    | Percorso/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ CaptureSharedTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio CaptureSharedTimerDriven, seguire questa procedura:

1.  Aprire la shell CMD per la Windows SDK e passare alla directory di esempio CaptureSharedTimerDriven.
2.  Eseguire il comando `start WASAPICaptureSharedTimerDriven.sln` nella directory CaptureSharedTimerDriven per aprire il progetto WASAPICaptureSharedTimerDriven nella finestra di Visual Studio.
3.  Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** . Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, WASAPICaptureSharedTimerDriven. vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile WASAPICaptureSharedTimerDriven.exe. Per eseguirlo, digitare `WASAPICaptureSharedTimerDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi. Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata di acquisizione nel dispositivo multimediale predefinito.

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

La tabella seguente illustra gli argomenti.

| Argomento        | Descrizione                                                |
|-----------------|------------------------------------------------------------|
| -?              | Visualizza la guida.                                                |
| -H              | Visualizza la guida.                                                |
| -l              | Latenza di acquisizione audio in millisecondi.                     |
| -d              | Durata acquisizione audio in secondi.                         |
| -M              | Disabilita l'uso di MMCSS.                                 |
| -Console        | Usare il dispositivo console predefinito.                            |
| -comunicazioni | Usare il dispositivo di comunicazione predefinito.                      |
| -Multimedia     | Usare il dispositivo multimediale predefinito.                         |
| -endpoint       | Usare l'identificatore dell'endpoint specificato nel valore dell'opzione. |



 

Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e chiede all'utente di selezionare un dispositivo per la sessione di acquisizione. La console, la comunicazione e i dispositivi multimediali predefiniti sono elencati seguiti dai dispositivi e dagli identificatori dell'endpoint. Se non viene specificata alcuna durata, il flusso audio dal dispositivo specificato viene acquisito per 10 secondi. L'applicazione scrive i dati acquisiti in un file con estensione wav denominato in modo univoco.

CaptureSharedTimerDriven illustra il buffering basato sul timer. In questa modalità il client deve attendere un periodo di tempo (metà della latenza, specificata dal valore del parametro-d, in millisecondi). Quando il client viene riattivato, a metà del periodo di elaborazione, estrae il set successivo di campioni dal motore. Prima che ogni elaborazione venga superata nel ciclo di buffering, il client deve rilevare la quantità di dati di acquisizione disponibili, in modo che i dati non sovraccarichino il buffer di acquisizione. I dati audio acquisiti dal dispositivo specificato possono essere elaborati abilitando il buffering basato sugli eventi. Questa modalità è illustrata nell'esempio [CaptureSharedEventDriven](capturesharedeventdriven.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio principali](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



