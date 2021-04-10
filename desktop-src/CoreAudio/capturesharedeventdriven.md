---
description: Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input specificato dall'utente e lo scrive in un file con estensione wav denominato in modo univoco nella directory corrente. In questo esempio viene illustrata la memorizzazione nel buffer basata sugli eventi.
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: CaptureSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126906"
---
# <a name="capturesharedeventdriven"></a>CaptureSharedEventDriven

Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input specificato dall'utente e lo scrive in un file con estensione wav denominato in modo univoco nella directory corrente. In questo esempio viene illustrata la memorizzazione nel buffer basata sugli eventi.

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
-   [WASAPI](wasapi.md) per le operazioni di gestione del flusso, ad esempio l'avvio e l'arresto del flusso e il cambio di flusso.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Location    | Percorso/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ CaptureSharedEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio CaptureSharedEventDriven, seguire questa procedura:

1.  Aprire la shell CMD per la Windows SDK e passare alla directory di esempio CaptureSharedEventDriven.
2.  Eseguire il comando `start WASAPICaptureSharedEventDriven.sln` nella directory CaptureSharedEventDriven per aprire il progetto WASAPICaptureSharedEventDriven nella finestra di Visual Studio.
3.  Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** . Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, WASAPICaptureSharedEventDriven. vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile WASAPICaptureSharedEventDriven.exe. Per eseguirlo, digitare `WASAPICaptureSharedEventDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi. Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata di acquisizione nel dispositivo multimediale predefinito.

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

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

CaptureSharedEventDriven illustra la memorizzazione nel buffer basata sugli eventi. Il client audio di cui è stata creata un'istanza per questo esempio è configurato per l'esecuzione in modalità condivisa e l'elaborazione del client del buffer audio viene eseguita mediante l'impostazione del flag **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** nella chiamata a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize). Nell'esempio viene illustrato come il client deve fornire un handle di evento al sistema chiamando il metodo [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) . Dopo l'inizio della sessione di acquisizione e l'avvio del flusso, il motore audio segnala all'handle di evento fornito di notificare al client ogni volta che un buffer è pronto per l'elaborazione da parte del client. I dati audio possono anche essere elaborati in un ciclo basato su timer. Questa modalità è dimostrato nell'esempio [CaptureSharedTimerDriven](capturesharedtimerdriven.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio principali](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



