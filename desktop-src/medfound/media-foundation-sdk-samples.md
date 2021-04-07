---
description: Questa sezione descrive le applicazioni di esempio che illustrano come usare Media Foundation. Encoding SamplesPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated o argomenti obsoleti SamplesRelated
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Esempi di Media Foundation SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f335b5ba744b098efdb7570aa861ad36fc9216cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761417"
---
# <a name="media-foundation-sdk-samples"></a>Esempi di Media Foundation SDK

In questa sezione vengono descritte le applicazioni di esempio che illustrano come utilizzare Media Foundation.

-   [Esempi di codifica](#encoding-samples)
-   [Esempi di riproduzione](#playback-samples)
-   [Plug-in](#plug-ins)
-   [Esempi di Reader di origine](#source-reader-samples)
-   [Acquisizione video](#video-capture)
-   [Esempi vari](#miscellaneous-samples)
-   [Esempi deprecati o obsoleti](#deprecated-or-obsolete-samples)
-   [Argomenti correlati](#related-topics)

## <a name="encoding-samples"></a>Esempi di codifica



| Esempio                            | Descrizione                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [Transcodifica](transcode-sample.md) | Viene illustrato come ricodificare un file multimediale in un formato Windows Media. |



 

## <a name="playback-samples"></a>Esempi di riproduzione



| Esempio                                            | Descrizione                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BasicPlayback](/previous-versions//bb970475(v=vs.85))          | Riproduce file audio e video usando la [sessione multimediale](media-session.md). In questo esempio viene illustrato come creare topologie di riproduzione, controllare la sessione multimediale e ricevere eventi della sessione durante la riproduzione. |
| [MFPlayer](/previous-versions//bb970516(v=vs.85))                    | Illustra alcune funzioni di riproduzione che non sono incluse nell'esempio [BasicPlayback](/previous-versions//bb970475(v=vs.85)) .                                                                                              |
| [ProtectedPlayback](protectedplayback-sample.md) | Riproduce file audio e video protetti. Questo esempio illustra come usare la sessione del percorso multimediale protetto (PMP) e come usare gli oggetti di attivazione del contenuto.                                                              |



 

## <a name="plug-ins"></a>Plug-Ins



| Esempio                                       | Sub-Area                         | Descrizione                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [Decodificatore](decoder-sample.md)                | Trasformazione Media Foundation (MFT) | Decodificatore video.                                                                                         |
| [EVRPresenter](evrpresenter-sample.md)      | Varie                    | Presenter personalizzato per il [renderer video avanzato](enhanced-video-renderer.md) (EVR).                 |
| [\_AUDIODELAY MFT](mft-audiodelay-sample.md) | MFT                              | Trasformazione effetto audio. Viene illustrato come scrivere un MFT di base per l'elaborazione audio.                           |
| [\_Scala di grigi MFT](mft-grayscale-sample.md)   | MFT                              | Effetto video in scala di grigi. Viene illustrato come scrivere un MFT di base per l'elaborazione video.                           |
| [MPEG1Source](mpeg1source-sample.md)        | Origine supporto                     | Analizza i flussi a livello di sistema MPEG-1. Viene illustrato come scrivere un'origine multimediale personalizzata e un gestore del flusso di byte. |
| [WavSink](wavsink-sample.md)                | Sink multimediale                       | Sink di archivio che scrive i file WAV. Viene illustrato come scrivere un sink multimediale personalizzato.                        |
| [WavSource](wavsource-sample.md)            | Origine supporto                     | Analizza i file WAV. Viene illustrato come scrivere un'origine multimediale personalizzata e un gestore del flusso di byte.                   |



 

## <a name="source-reader-samples"></a>Esempi di Reader di origine



| Esempio                                      | Descrizione                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [Clip audio](audio-clip-sample.md)         | Usa il [lettore di origine](source-reader.md) per decodificare l'audio da un file multimediale.      |
| [VideoThumbnail](videothumbnail-sample.md) | Usa il [lettore di origine](source-reader.md) per ottenere singoli frame da un file video. |



 

## <a name="video-capture"></a>Acquisizione video



| Esempio                                        | Descrizione                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [MFCaptureD3D](mfcaptured3d-sample.md)       | Mostra come visualizzare in anteprima i video da un dispositivo di acquisizione video, usando Direct3D per eseguire il rendering del video. |
| [MFCaptureToFile](mfcapturetofile-sample.md) | Mostra come acquisire video da una videocamera a un file.                                   |



 

## <a name="miscellaneous-samples"></a>Esempi vari



| Esempio                                         | Descrizione                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ASFParser](asfparser-sample.md)              | Viene illustrato come analizzare i dati da un file Advanced Systems Format (ASF).                                                                                   |
| [DXVA-HD](dxva-hd-sample.md)                  | Mostra come usare Microsoft DirectX Video Acceleration High Definition (DXVA-HD).                                                                      |
| [\_VIDEOPROC DXVA2](dxva2-videoproc-sample.md) | Usa l'accelerazione video DirectX (DXVA) 2,0 per creare un flusso di video YUV 4:2:2. Questo esempio illustra come usare le funzionalità di elaborazione video di DXVA. |



 

## <a name="deprecated-or-obsolete-samples"></a>Esempi deprecati o obsoleti



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Esempio</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfplayer2-sample.md">MFPlayer2</a></td>
<td>Illustra alcune funzionalità di riproduzione avanzate dell'API <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> .</td>
</tr>
<tr class="even">
<td><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></td>
<td>Applica un effetto scala di grigi al video. Viene illustrato come inserire MFTs in una topologia di riproduzione.<br/>
<blockquote>
[!Note]<br />
Questo esempio non è più incluso nell'SDK.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="playlist-sample.md">Playlist</a></td>
<td>Riproduce una sequenza di file audio usando l'origine del sequencer.<br/>
<blockquote>
[!Note]<br />
Questo esempio non è più incluso nell'SDK.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="simplecapture-sample.md">SimpleCapture</a></td>
<td>Mostra come visualizzare in anteprima i video da un dispositivo di acquisizione video, usando l'API MFPlay.</td>
</tr>
<tr class="odd">
<td><a href="simpleplay-sample.md">SimplePlay</a></td>
<td>Viene illustrato come riprodurre un file multimediale tramite l'API MFPlay.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
