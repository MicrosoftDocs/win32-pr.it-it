---
description: Questa applicazione di esempio usa le API Core Audio per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente. Questo esempio illustra il buffering basato su timer per un client di rendering in modalità esclusiva.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6876c448aa7737683aff4e495416020af7def54cb01109c3d6ad2d1c26d20780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077445"
---
# <a name="renderexclusivetimerdriven"></a>RenderExclusiveTimerDriven

Questa applicazione di esempio usa le API Core Audio per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente. Questo esempio illustra il buffering basato su timer per un client di rendering in modalità esclusiva. Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Visualizzare i file di esempio](#view-the-sample-files)
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



| Località    | Percorso/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v7.0 \\ Samples \\ Multimedia Audio \\ \\ RenderExclusiveTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio RenderExclusiveTimerDriven, seguire questa procedura:

1.  Aprire la shell CMD per Windows SDK e passare alla directory di esempio RenderExclusiveTimerDriven.
2.  Eseguire il comando nella `start WASAPIRenderExclusiveTimerDriven.sln` directory RenderExclusiveTimerDriven per aprire il progetto WASAPIRenderExclusiveTimerDriven nella finestra Visual Studio.
3.  Nella finestra selezionare la configurazione  della soluzione **Debug** o Versione, scegliere il **menu** Compila dalla barra dei menu e selezionare l'opzione **Compila.** Se non si apre Visual Studio shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposta in modo esplicito la variabile di ambiente MSSdk, usata nel file di progetto WASAPIRenderExclusiveTimerDriven.vcproj.

## <a name="view-the-sample-files"></a>Visualizzare i file di esempio

Se si compila correttamente l'applicazione demo, viene generato un file eseguibile, WASAPIRenderExclusiveTimerDriven.exe file. Per eseguirlo, digitare `WASAPIRenderExclusiveTimerDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi. Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata di riproduzione nel dispositivo console predefinito.

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

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

RenderExclusiveTimerDriven illustra il buffering basato su timer. In questa modalità, il client deve attendere un periodo di tempo (metà della latenza, specificata dal valore dell'opzione -d, in millisecondi). Quando il client si riattiva, a metà del periodo di elaborazione, estrae il set successivo di campioni dal motore. Prima che ogni elaborazione passi nel ciclo di memorizzazione nel buffer, il client deve individuare la quantità di dati di cui eseguire il rendering in modo che i dati non esercitino il buffer.

I dati audio da riprodurre nel dispositivo specificato possono essere elaborati abilitando il buffer basato su eventi. Questa modalità è illustrata nell'esempio RenderExclusiveTimerDriven.

Per altre informazioni sul rendering di un flusso, vedere [Rendering di un flusso](rendering-a-stream.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio di base](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



