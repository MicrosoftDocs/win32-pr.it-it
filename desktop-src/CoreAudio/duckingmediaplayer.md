---
description: In questa applicazione di esempio viene illustrata l'attenuazione dei flussi implementando un lettore multimediale che mostra il comportamento di attenuazione predefinito fornito dal sistema, rifiuta gli eventi ducking e implementa la gestione personalizzata quando vengono ricevuti gli eventi ducking.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: DuckingMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320517"
---
# <a name="duckingmediaplayer"></a>DuckingMediaPlayer

In questa applicazione di esempio viene illustrata l'attenuazione dei flussi implementando un lettore multimediale che mostra il comportamento di attenuazione predefinito fornito dal sistema, rifiuta gli eventi ducking e implementa la gestione personalizzata quando vengono ricevuti gli eventi ducking. Questo esempio deve essere usato in ID insieme ad con [DuckingCaptureSample](duckingcapturesample.md). Per altre informazioni sull'attenuazione dei flussi o sull'abbassamento di livello, vedere [esperienza ducking predefinita](stream-attenuation.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

In questo esempio vengono illustrate le funzionalità seguenti.

-   DirectShow per riprodurre un file multimediale.
-   [WASAPI](wasapi.md) per la gestione del flusso e la gestione degli eventi ducking.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Location    | Percorso/URL                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ DuckingMediaPlayer \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio DuckingMediaPlayer, seguire questa procedura:

1.  Aprire DuckingMediaPlayer. sln in Visual Studio 2008.
2.  Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** . Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, DuckingMediaPlayer. vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se l'applicazione viene compilata correttamente, viene generato un file eseguibile, DuckingMediaPlayer.exe. Per eseguirlo, selezionare **Avvia debug** o **Avvia senza eseguire debug** dal menu **debug** oppure digitare `DuckingMediaPlayer` una finestra di comando.

Per visualizzare una dimostrazione di ducking, è necessario eseguire contemporaneamente DuckingMediaPlayer e DuckingCaptureSample. DuckingCaptureSample apre un flusso di comunicazione e segnala al sistema di generare un evento ducking. Il DuckingMediaPlayer riceve una notifica al sistema quando si verifica un evento ducking e il lettore multimediale esegue l'azione richiesta dall'utente.

Per disabilitare il comportamento di ducking:

1.  Nella finestra DuckingCaptureSample selezionare **USA dispositivo di input predefinito** e fare clic su **Avvia** per avviare una sessione di acquisizione dal dispositivo di comunicazione.
2.  In DuckingMediaPlayer selezionare un file multimediale da riprodurre e specificare l'opzione ducking come **rifiuto esplicito**.

Si noti che il file multimediale viene riprodotto senza interruzioni. Gli eventi generati dal sistema quando il flusso di comunicazione aperto vengono ignorati.

Per illustrare il comportamento predefinito di ducking fornito dal sistema, eseguire le operazioni seguenti:

1.  Selezionare l'opzione **suoni** dal pannello di controllo. Nella scheda **comunicazioni** selezionare **Riduci il volume di altri suoni del 80%**.
2.  Nella finestra DuckingCaptureSample selezionare **USA dispositivo di input predefinito** e fare clic su **Avvia** per avviare una sessione di acquisizione dal dispositivo di comunicazione.
3.  In DuckingMediaPlayer selezionare un file multimediale da riprodurre senza scegliere le opzioni di ducking.
4.  Nella finestra DuckingCaptureSample fare clic su **Interrompi** per arrestare il flusso di comunicazione.

Si noti che quando DuckingCaptureSample apre il flusso di comunicazione, il file multimediale riprodotto da DuckingMediaPlayer viene riprodotto senza interruzioni, ma il livello del volume è ridotto. Quando la sessione di comunicazione viene arrestata, il volume viene reimpostato sull'impostazione originale. Questo comportamento di attenuazione del flusso è il comportamento predefinito di ducking implementato dal sistema.

Per visualizzare un comportamento di ducking personalizzato implementato da Media Player:

1.  Nella finestra DuckingCaptureSample selezionare **USA dispositivo di input predefinito** e fare clic su **Avvia** per avviare una sessione di acquisizione dal dispositivo di comunicazione.
2.  In DuckingMediaPlayer selezionare un file multimediale da riprodurre e specificare l'opzione ducking come **pausa in Duck**.
3.  Nella finestra DuckingCaptureSample fare clic su **Interrompi** per arrestare il flusso di comunicazione.

Si noti che quando DuckingCaptureSample apre il flusso di comunicazione, il file multimediale riprodotto da DuckingMediaPlayer viene sospeso. La riproduzione riprende quando la sessione di comunicazione viene arrestata. Questo comportamento di attenuazione del flusso è il comportamento di ducking implementato da Media Player.

DuckingMediaPlayer illustra anche come integrare il controllo del volume per ogni applicazione con il mixer del volume.

Per ulteriori informazioni sulla funzionalità di attenuazione dei flussi, vedere l' [esperienza di ducking predefinita](stream-attenuation.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio principali](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



