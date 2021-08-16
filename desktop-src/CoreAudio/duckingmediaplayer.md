---
description: Questa applicazione di esempio illustra l'attenuazione del flusso implementando un lettore multimediale che mostra il comportamento di attenuazione predefinito fornito dal sistema, rifiuta esplicitamente l'attenuazione degli eventi e implementa la gestione personalizzata quando vengono ricevuti eventi di attenuazione.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: Insodd dimediaplayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab5a469ec2a7fb1551980d0a08a758e8e8e8f522831dc2148b2d8fb222ecdfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828282"
---
# <a name="duckingmediaplayer"></a>Insodd dimediaplayer

Questa applicazione di esempio illustra l'attenuazione del flusso implementando un lettore multimediale che mostra il comportamento di attenuazione predefinito fornito dal sistema, rifiuta esplicitamente l'attenuazione degli eventi e implementa la gestione personalizzata quando vengono ricevuti eventi di attenuazione. Questo esempio deve essere usato in coniugazione con [l'esempio DiaframmateCaptureSample.](duckingcapturesample.md) Per altre informazioni sull'attenuazione del flusso o l'accodamento del flusso, vedere [Default Ducking Experience](stream-attenuation.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

In questo esempio vengono illustrate le funzionalità seguenti.

-   DirectShow riprodurre un file multimediale.
-   [WASAPI per](wasapi.md) la gestione dei flussi e la gestione degli eventi di gestione.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Località    | Percorso/URL                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ DuckingMediaPlayer \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio DisaccodatoMediaPlayer, seguire questa procedura:

1.  Aprire il file SoloMediaPlayer.sln in Visual Studio 2008.
2.  Nella finestra selezionare la configurazione della soluzione **Debug** o **Release,** selezionare il **menu** Compila dalla barra dei menu e selezionare l'opzione **Compila.** Se non si apre un Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK. In tal caso, l'esempio non verrà compilato a meno che non si sia impostata in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, DuckingMediaPlayer.vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se l'applicazione viene compilata correttamente, viene generato DuckingMediaPlayer.exe file eseguibile. Per eseguirlo, scegliere **Avvia debug** o **Avvia** senza eseguire debug dal menu **Debug** oppure digitare in una finestra `DuckingMediaPlayer` di comando.

Per visualizzare una dimostrazione dell'atrofia, è necessario eseguire Contemporaneamente GlispingMediaPlayer e IlcaptureSample. L'esempio DiassingCaptureSample apre un flusso di comunicazione e segnala al sistema di generare un evento di allarme. Il lettore multimediale viene avvisato dal sistema quando si verifica un evento di eserzione e il lettore multimediale esegue l'azione richiesta dall'utente.

Per disabilitare il comportamento di inasamento:

1.  Nella finestra DuckingCaptureSample selezionare **Use default input device**(Usa dispositivo di input predefinito) e fare clic su **Start** (Avvia) per avviare una sessione di acquisizione dal dispositivo di comunicazione.
2.  In DuckingMediaPlayer selezionare un file multimediale da riprodurre e specificare l'opzione che consente di rifiutare esplicitamente **.**

Si noti che il file multimediale viene riprodotto senza interruzioni. Gli eventi generati dal sistema all'apertura del flusso di comunicazione vengono ignorati.

Per illustrare il comportamento predefinito di inaserzione fornito dal sistema, eseguire le operazioni seguenti:

1.  Selezionare **l'opzione** Suoni nel pannello di controllo. Nella scheda **Comunicazioni** selezionare Riduci il volume di altri suoni **dell'80%.**
2.  Nella finestra DuckingCaptureSample selezionare **Use default input device**(Usa dispositivo di input predefinito) e fare clic su **Start** (Avvia) per avviare una sessione di acquisizione dal dispositivo di comunicazione.
3.  In DuckingMediaPlayer selezionare un file multimediale da riprodurre, senza scegliere alcuna delle opzioni per la riproduzione.
4.  Nella finestra DuckingCaptureSample fare clic su **Arresta** per arrestare il flusso di comunicazione.

Si noti che quando il file di comunicazione viene aperto da LoweringCaptureSample, il file multimediale riprodotto da CopyrightingMediaPlayer viene riprodotto senza interruzioni, ma il livello del volume viene abbassato. Quando la sessione di comunicazione viene arrestata, il volume viene reimpostato sull'impostazione originale. Questo comportamento di attenuazione del flusso è il comportamento predefinito di attenuazione implementato dal sistema.

Per visualizzare un comportamento di "papera" personalizzato implementato dal lettore multimediale:

1.  Nella finestra DuckingCaptureSample selezionare **Use default input device**(Usa dispositivo di input predefinito) e fare clic su **Start** (Avvia) per avviare una sessione di acquisizione dal dispositivo di comunicazione.
2.  In DuckingMediaPlayer selezionare un file multimediale da riprodurre e specificare l'opzione di accodamento **come Pause on Paper**.
3.  Nella finestra DuckingCaptureSample fare clic su **Arresta** per arrestare il flusso di comunicazione.

Si noti che quando il flusso di comunicazione viene aperto da DuckingCaptureSample, il file multimediale riprodotto da CopyrightingMediaPlayer viene sospeso. La riproduzione riprende quando la sessione di comunicazione viene arrestata. Questo comportamento di attenuazione del flusso è il comportamento di attenuazione implementato dal lettore multimediale.

L'esempio seguente illustra anche come integrare il controllo del volume per ogni applicazione con il mixer di volumi.

Per altre informazioni sulla funzionalità di attenuazione del flusso, vedere [Esperienza di attenuazione predefinita.](stream-attenuation.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio di base](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



