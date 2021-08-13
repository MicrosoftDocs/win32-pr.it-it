---
description: Questa applicazione di esempio, che illustra il buffering basato su eventi, usa le API Audio core per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c23213e1e60d0fdf77de67a91ea3bba3c928a51f9e562876dd1a4e018595dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119216551"
---
# <a name="renderexclusiveeventdriven"></a>RenderExclusiveEventDriven

Questa applicazione di esempio usa le API Core Audio per eseguire il rendering dei dati audio in un dispositivo di output specificato dall'utente. Questo esempio illustra il buffering basato su eventi per un client di rendering in modalità esclusiva. Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio.

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



| Località    | Percorso/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v7.0 \\ Samples \\ Multimedia Audio \\ \\ RenderExclusiveEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio RenderExclusiveEventDriven, seguire questa procedura:

1.  Aprire la shell CMD per Windows SDK e passare alla directory di esempio RenderExclusiveEventDriven.
2.  Eseguire il `start WASAPIRenderExclusiveEventDriven.sln` comando nella directory RenderExclusiveEventDriven per aprire il progetto WASAPIRenderExclusiveEventDriven nella finestra Visual Studio.
3.  Nella finestra selezionare la configurazione  della soluzione **Debug** o Versione, scegliere il **menu** Compila dalla barra dei menu e selezionare l'opzione **Compila.** Se non si apre Visual Studio shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposta in modo esplicito la variabile di ambiente MSSdk, usata nel file di progetto WASAPIRenderExclusiveEventDriven.vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se si compila correttamente l'applicazione demo, viene generato un file eseguibile, WASAPIRenderExclusiveEventDriven.exe, Per eseguirlo, digitare `WASAPIRenderExclusiveEventDriven` in una finestra di comando seguita da argomenti obbligatori o facoltativi. L'esempio seguente illustra come eseguire l'esempio specificando la durata della riproduzione nel dispositivo multimediale predefinito.

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

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

L'esempio RenderExclusiveEventDriven illustra il buffering basato su eventi. L'esempio illustra come:

-   Creare un'istanza di un client audio, configurarlo per l'esecuzione in modalità esclusiva e abilitare il buffer basato su eventi impostando il flag **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK** nella chiamata a [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Associare il client agli esempi pronti per il rendering fornendo un handle di evento al sistema chiamando il metodo [**IAudioClient::SetEventHandle.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
-   Creare un thread di rendering per elaborare gli esempi dal motore audio.
-   Allineare correttamente i buffer su un limite di 128 byte prima di inviarli al dispositivo. Questa operazione viene eseguita regolando la periodicità del motore.
-   Controllare il formato di combinazione dell'endpoint del dispositivo per determinare se è possibile eseguire il rendering degli esempi. Se il dispositivo non supporta il formato di combinazione, i dati vengono convertiti in PCM.
-   Gestire il cambio di flusso.

Dopo l'avvio della sessione di rendering e l'avvio del flusso, il motore audio segnala all'handle di evento fornito di inviare una notifica al client ogni volta che un buffer diventa pronto per l'elaborazione da parte del client. I dati audio possono essere elaborati anche in un ciclo basato su timer. Questa modalità è illustrata [nell'esempio RenderExclusiveTimerDriven.](renderexclusivetimerdriven.md)

Per altre informazioni sul rendering di un flusso, vedere [Rendering di un flusso](rendering-a-stream.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio di base](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



