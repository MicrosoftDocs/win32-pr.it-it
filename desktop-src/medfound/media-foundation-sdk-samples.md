---
description: Questa sezione descrive le applicazioni di esempio che illustrano come usare gli esempi Media Foundation.EncodingPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated or Obsolete SamplesRelated topics (Esempi pre-individuati o obsoleti)Esempi correlati
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Esempi di Media Foundation SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5482fabe5e4bfdfe5d451fd8ccb9c0ba0504a5ff
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482717"
---
# <a name="media-foundation-sdk-samples"></a>Esempi di Media Foundation SDK

In questa sezione vengono descritte applicazioni di esempio che illustrano come usare Media Foundation.

-   [Esempi di codifica](#encoding-samples)
-   [Esempi di riproduzione](#playback-samples)
-   [Plug-in](#plug-ins)
-   [Esempi di lettore di origine](#source-reader-samples)
-   [Acquisizione video](#video-capture)
-   [Esempi vari](#miscellaneous-samples)
-   [Esempi deprecati o obsoleti](#deprecated-or-obsolete-samples)
-   [Argomenti correlati](#related-topics)

## <a name="encoding-samples"></a>Esempi di codifica



| Esempio                            | Descrizione                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [Transcode](transcode-sample.md) | Illustra come ricodificare un file multimediale in Windows formato multimediale. |



 

## <a name="playback-samples"></a>Esempi di riproduzione



| Esempio                                            | Descrizione                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BasicPlayback](/previous-versions//bb970475(v=vs.85))          | Riproduce file audio e video usando la [sessione multimediale](media-session.md). Questo esempio illustra come creare topologie di riproduzione, controllare la sessione multimediale e ricevere eventi di sessione durante la riproduzione. |
| [MFPlayer](/previous-versions//bb970516(v=vs.85))                    | Illustra alcune funzioni di riproduzione non incluse [nell'esempio BasicPlayback.](/previous-versions//bb970475(v=vs.85))                                                                                              |
| [ProtectedPlayback](protectedplayback-sample.md) | Riproduce file audio e video protetti. Questo esempio illustra come usare la sessione PMP (Protected Media Path) e come usare gli oggetti di abilitazione del contenuto.                                                              |



 

## <a name="plug-ins"></a>Plug-Ins



| Esempio                                       | Sub-Area                         | Descrizione                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [Decoder](decoder-sample.md)                | Media Foundation trasformazione (MFT) | Decodificatore video.                                                                                         |
| [EVRPresenter](evrpresenter-sample.md)      | Varie                    | Presentatore personalizzato per [il renderer video](enhanced-video-renderer.md) avanzato (EVR).                 |
| [MFT \_ AudioDelay](mft-audiodelay-sample.md) | MFT                              | Trasformazione dell'effetto audio. Illustra come scrivere un MFT di base per l'elaborazione audio.                           |
| [Gradazioni di grigio MFT \_](mft-grayscale-sample.md)   | MFT                              | Effetto video in scala di grigi. Illustra come scrivere un MFT di base per l'elaborazione video.                           |
| [MPEG1Source](mpeg1source-sample.md)        | Origine multimediale                     | Analizza i flussi a livello di sistema MPEG-1. Illustra come scrivere un'origine multimediale personalizzata e un gestore del flusso di byte. |
| [WavSink](wavsink-sample.md)                | Sink multimediale                       | Sink di archivio che scrive file wav. Illustra come scrivere un sink multimediale personalizzato.                        |
| [WavSource](wavsource-sample.md)            | Origine multimediale                     | Analizza i file wav. Illustra come scrivere un'origine multimediale personalizzata e un gestore del flusso di byte.                   |



 

## <a name="source-reader-samples"></a>Esempi di lettore di origine



| Esempio                                      | Descrizione                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [Audio Clip](audio-clip-sample.md)         | Usa il [lettore di origine](source-reader.md) per decodificare l'audio da un file multimediale.      |
| [VideoThumbnail](videothumbnail-sample.md) | Usa il [lettore di](source-reader.md) origine per ottenere singoli fotogrammi da un file video. |



 

## <a name="video-capture"></a>Acquisizione video



| Esempio                                        | Descrizione                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [MFCaptureD3D](mfcaptured3d-sample.md)       | Illustra come visualizzare in anteprima un video da un dispositivo di acquisizione video, usando Direct3D per eseguire il rendering del video. |
| [MFCaptureToFile](mfcapturetofile-sample.md) | Illustra come acquisire video da una videocamera a un file.                                   |



 

## <a name="miscellaneous-samples"></a>Esempi vari



| Esempio                                         | Descrizione                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ASFParser](asfparser-sample.md)              | Illustra come analizzare i dati da un file ASF (Advanced Systems Format).                                                                                   |
| [DXVA-HD](dxva-hd-sample.md)                  | Illustra come usare Microsoft DirectX Video Acceleration High Definition (DXVA-HD).                                                                      |
| [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) | Usa DirectX Video Acceleration (DXVA) 2.0 per creare un flusso di video YUV 4:2:2. Questo esempio illustra come usare le funzionalità di elaborazione video di DXVA. |



 

## <a name="deprecated-or-obsolete-samples"></a>Esempi deprecati o obsoleti




| Esempio | Descrizione | 
|--------|-------------|
| <a href="mfplayer2-sample.md">MFPlayer2</a> | Illustra alcune funzionalità di riproduzione avanzate dell'API <a href="using-mfplay-for-audio-video-playback.md">MFPlay.</a> | 
| <a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a> | Applica un effetto in scala di grigi al video. Illustra come inserire MFT in una topologia di riproduzione.<br /><blockquote>[!Note]<br />Questo esempio non è più incluso nell'SDK.</blockquote><br /> | 
| <a href="playlist-sample.md">Playlist</a> | Riproduce una sequenza di file audio usando l'origine sequencer.<br /><blockquote>[!Note]<br />Questo esempio non è più incluso nell'SDK.</blockquote><br /> | 
| <a href="simplecapture-sample.md">SimpleCapture</a> | Illustra come visualizzare in anteprima un video da un dispositivo di acquisizione video usando l'API MFPlay. | 
| <a href="simpleplay-sample.md">SimplePlay</a> | Illustra come riprodurre un file multimediale usando l'API MFPlay. | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
