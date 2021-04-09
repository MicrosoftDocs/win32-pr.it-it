---
description: Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b94fa423cd4d4e7dc7121e927696529bfadf9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049210"
---
# <a name="renderexclusiveeventdriven"></a>RenderExclusiveEventDriven

Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente. In questo esempio viene illustrato il buffer basato sugli eventi per un client di rendering in modalità esclusiva. Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio.

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
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ RenderExclusiveEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio RenderExclusiveEventDriven, seguire questa procedura:

1.  Aprire la shell CMD per la Windows SDK e passare alla directory di esempio RenderExclusiveEventDriven.
2.  Eseguire il comando `start WASAPIRenderExclusiveEventDriven.sln` nella directory RenderExclusiveEventDriven per aprire il progetto WASAPIRenderExclusiveEventDriven nella finestra di Visual Studio.
3.  Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** . Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, WASAPIRenderExclusiveEventDriven. vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile WASAPIRenderExclusiveEventDriven.exe. Per eseguirlo, digitare `WASAPIRenderExclusiveEventDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi. Nell'esempio seguente viene illustrato come eseguire l'esempio specificando la durata della riproduzione sul dispositivo multimediale predefinito.

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

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

L'esempio RenderExclusiveEventDriven illustra il buffering basato sugli eventi. Nell'esempio viene illustrato come eseguire le operazioni seguenti:

-   Creare un'istanza di un client audio, configurarlo per l'esecuzione in modalità esclusiva e abilitare la memorizzazione nel buffer basata sugli eventi impostando il flag **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** nella chiamata a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Associare il client agli esempi pronti per il rendering fornendo un handle di evento al sistema chiamando il metodo [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .
-   Creare un thread di rendering per elaborare gli esempi dal motore audio.
-   Allineare i buffer in modo corretto in un limite di 128 byte prima di inviarli al dispositivo. Questa operazione viene eseguita regolando la periodicità del motore.
-   Controllare il formato di combinazione dell'endpoint del dispositivo per determinare se è possibile eseguire il rendering degli esempi. Se il dispositivo non supporta il formato di combinazione, i dati vengono convertiti nel PCM.
-   Gestire il cambio di flusso.

Dopo l'inizio della sessione di rendering e l'avvio del flusso, il motore audio segnala all'handle di evento fornito di notificare al client ogni volta che un buffer è pronto per l'elaborazione da parte del client. I dati audio possono anche essere elaborati in un ciclo basato su timer. Questa modalità è illustrata nell'esempio [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) .

Per altre informazioni sul rendering di un flusso, vedere [rendering di un flusso](rendering-a-stream.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio principali](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



