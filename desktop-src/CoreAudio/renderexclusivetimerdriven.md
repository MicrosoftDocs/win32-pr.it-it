---
description: Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente. Questo esempio illustra il buffering basato sul timer per un client di rendering in modalità esclusiva.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483484"
---
# <a name="renderexclusivetimerdriven"></a>RenderExclusiveTimerDriven

Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente. Questo esempio illustra il buffering basato sul timer per un client di rendering in modalità esclusiva. Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Visualizzare i file di esempio](#view-the-sample-files)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

In questo esempio vengono illustrate le funzionalità seguenti.

-   [API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.
-   WASAPI per le operazioni di gestione del flusso.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Location    | Percorso/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ RenderExclusiveTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio RenderExclusiveTimerDriven, seguire questa procedura:

1.  Aprire la shell CMD per la Windows SDK e passare alla directory di esempio RenderExclusiveTimerDriven.
2.  Eseguire il comando `start WASAPIRenderExclusiveTimerDriven.sln` nella directory RenderExclusiveTimerDriven per aprire il progetto WASAPIRenderExclusiveTimerDriven nella finestra di Visual Studio.
3.  Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** . Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, WASAPIRenderExclusiveTimerDriven. vcproj.

## <a name="view-the-sample-files"></a>Visualizzare i file di esempio

Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile WASAPIRenderExclusiveTimerDriven.exe. Per eseguirlo, digitare `WASAPIRenderExclusiveTimerDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi. Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata della riproduzione sul dispositivo console predefinito.

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

La tabella seguente illustra gli argomenti.

| Argomento        | Descrizione                                                |
|-----------------|------------------------------------------------------------|
| -?              | Visualizza la guida.                                                |
| -H              | Visualizza la guida.                                                |
| -f              | Frequenza di onda sinusoidale in Hz.                                 |
| -l              | Latenza di rendering audio in millisecondi.                      |
| -d              | Durata in secondi dell'onda sinusoidale.                             |
| -M              | Disabilita l'uso di MMCSS.                                 |
| -Console        | Usare il dispositivo console predefinito.                            |
| -comunicazioni | Usare il dispositivo di comunicazione predefinito.                      |
| -Multimedia     | Usare il dispositivo multimediale predefinito.                         |
| -endpoint       | Usare l'identificatore dell'endpoint specificato nel valore dell'opzione. |



 

Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e chiede all'utente di selezionare un dispositivo per la sessione di rendering. Dopo che l'utente ha specificato un dispositivo, l'applicazione esegue il rendering di un'onda sinusoidale a 440 Hz per 10 secondi. Questi valori possono essere modificati specificando i valori di opzione-f e-d.

RenderExclusiveTimerDriven illustra il buffering basato sul timer. In questa modalità il client deve attendere un periodo di tempo (metà della latenza, specificata dal valore del parametro-d, in millisecondi). Quando il client viene riattivato, a metà del periodo di elaborazione, estrae il set successivo di campioni dal motore. Prima che ogni elaborazione venga superata nel ciclo di buffering, il client deve rilevare la quantità di dati di cui eseguire il rendering in modo che i dati non sovraccarichino il buffer.

I dati audio da riprodurre sul dispositivo specificato possono essere elaborati abilitando il buffering basato sugli eventi. Questa modalità è illustrata nell'esempio RenderExclusiveTimerDriven.

Per altre informazioni sul rendering di un flusso, vedere [rendering di un flusso](rendering-a-stream.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio principali](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



