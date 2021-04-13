---
description: Microsoft Media Foundation è stato introdotto in Windows Vista come sostituzione di DirectShow. Naturalmente, DirectShow è ancora supportato in Windows 7, ma gli sviluppatori sono invitati a usare Media Foundation nelle nuove applicazioni multimediali digitali.
ms.assetid: c345c0d9-5325-4f73-b9ec-1673ad10e3e4
title: Novità per Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0270c28e5aca2a1f0fdad893743a1e8fb630fa5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351366"
---
# <a name="whats-new-for-media-foundation"></a>Novità di Media Foundation

Microsoft Media Foundation è stato introdotto in Windows Vista come sostituzione di DirectShow. Naturalmente, DirectShow è ancora supportato in Windows 7, ma gli sviluppatori sono invitati a usare Media Foundation nelle nuove applicazioni multimediali digitali.

I miglioramenti apportati a Media Foundation possono essere riepilogati come segue:

-   Migliore supporto per il formato, incluso MPEG-4
-   Supporto per i dispositivi di acquisizione e i codec hardware
-   Un modello di programmazione semplificato
-   Miglioramenti alla piattaforma

## <a name="better-format-support"></a>Supporto per formati migliori

La pipeline Media Foundation audio/video è stata implementata in Windows Vista, ma supporta un set limitato di formati e di contenitori di file, il che significa che alcune applicazioni devono eseguire il fallback su tecnologie precedenti, ad esempio DirectShow. In Windows 7, Media Foundation include i nuovi codec, le origini supporti e i sink multimediali seguenti:

-   Decoder AAC
-   Codificatore AAC
-   Origine file AVI/WAVE
-   Decoder video DV
-   Decoder video H. 264
-   Codificatore video H. 264
-   Decodificatore MJPEG
-   Sink di file MP3\*
-   Origine file MP4/3GP
-   Sink di file MP4/3GP

> [!Note]  
> Il sink di file MP3 non include un codificatore audio MP3.

 

Per ulteriori informazioni, vedere [formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md).

## <a name="hardware-device-support"></a>Supporto dei dispositivi hardware

Media Foundation supporta ora i seguenti tipi di dispositivi hardware nella pipeline audio/video:

-   Dispositivi di acquisizione video UVC 1,1, ad esempio webcam
-   Dispositivi di acquisizione audio
-   Codificatori e decodificatori hardware
-   Processori video hardware, ad esempio convertitori di spazio colore

I codec hardware possono eseguire una transcodifica video molto rapida. Ad esempio, un'applicazione può trasferire file Windows Media Video (WMV) a un telefono cellulare che supporta solo file 3GP. Usando un codificatore hardware, l'applicazione può transcodificare il file in backgound, appena prima di trasferirlo al dispositivo.

I dispositivi hardware sono rappresentati in Media Foundation da un oggetto proxy e vengono usati nella pipeline esattamente come i componenti basati su software.

## <a name="simplified-programming-model"></a>Modello di programmazione semplificato

In Windows Vista Media Foundation esposto un set di API relativamente di basso livello. Queste API sono flessibili, ma troppo complesse per le attività semplici. Windows 7 aggiunge nuove API di alto livello che semplificano la scrittura di applicazioni multimediali in C++. Di seguito sono riportate le nuove API di alto livello.



| API                                | Descrizione                                                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Lettore di origine](source-reader.md) | Il lettore di origine estrae i dati non elaborati o decodificati da un file multimediale. Ad esempio, è possibile usare il lettore di origine per ottenere le bitmap di anteprima da un file video o per analizzare i dati della forma d'onda in un file audio. È anche possibile usare il lettore di origine per ottenere i dati dinamici da un dispositivo di acquisizione audio o video. <br/> |
| [Writer sink](sink-writer.md)     | Il writer di sink consente di creare file multimediali passando dati non compressi o codificati. Ad esempio, è possibile usarlo per codificare di nuovo un file video o per acquisire video live da una webcam a un file.                                                                                                         |
| [API transcodifica](transcode-api.md) | Questa funzionalità supporta gli scenari più comuni di codifica audio/video.<br/>                                                                                                                                                                                                                               |



 

È comunque possibile usare le API di basso livello in Media Foundation. Questa operazione può essere eseguita se è necessario un maggiore controllo sulla pipeline audio/video.

## <a name="platform-improvements"></a>Miglioramenti della piattaforma

Windows 7 include numerosi miglioramenti alle API della piattaforma Media Foundation sottostante. Le applicazioni avanzate possono usare direttamente queste API; altre applicazioni otterranno i vantaggi indirettamente. I miglioramenti includono:

-   Modifiche della pipeline video per ridurre il consumo di energia e l'utilizzo della memoria del video.
-   [DXVA-HD](dxva-hd.md): Microsoft DirectX Video Acceleration High Definition (DXVA-HD) è una nuova API per l'elaborazione video con accelerazione hardware. DXVA-HD offre un modello di composizione più flessibile rispetto alla precedente API di elaborazione video DXVA ed è più adatto per i formati video ad alta definizione.
-   Un nuovo meccanismo per l'enumerazione di origini e decodificatori, che include valori di Merit e un elenco preferito/bloccato. Questa funzionalità migliora l'affidabilità complessiva del sistema. Per altre informazioni, vedere i seguenti argomenti:
    -   [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
    -   [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)
    -   [Meriti codec](codec-merit.md)

## <a name="sdk-changes"></a>Modifiche dell'SDK

-   Nuove intestazioni e file di libreria: [Media Foundation intestazioni e librerie](media-foundation-headers-and-libraries.md)
-   Modifiche a DLL e lib: [modifiche della libreria in Windows 7](media-foundation-headers-and-libraries.md)
-   Nuovi esempi di SDK:
    -   [Esempio di clip audio](audio-clip-sample.md)
    -   [Esempio di DXVA-HD](dxva-hd-sample.md)
    -   [Esempio MFCaptureD3D](mfcaptured3d-sample.md)
    -   [Esempio MFCaptureToFile](mfcapturetofile-sample.md)
    -   [Esempio di transcodifica](transcode-sample.md)
    -   [Esempio VideoThumbnail](videothumbnail-sample.md)
-   Miglioramenti di [TopoEdit](topoedit.md):
    -   Supporto per la transcodifica. Vedere compilazione di una [topologia transcodifica con TopoEdit](building-a-transcode-topology-with-topoedit.md).
    -   Supporto per l'acquisizione audio e video. Vedere [menu topologia](topology-menu.md).

## <a name="new-in-windows-8"></a>Novità di Windows 8

Alcuni dei nuovi aggiornamenti per Media Foundation con Windows 8 sono:

-   [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) controlla uno o più dispositivi di acquisizione. Vedere gli [attributi del motore di acquisizione](capture-engine-attributes.md) per un elenco di attributi. Altre nuove interfacce di acquisizione multimediale correlate sono [**IMFCapturePhotoSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink), [**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink), [**IMFCaptureRecordSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink), [**IMFCaptureSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink)e [**IMFCaptureSource**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource).
-   Di seguito sono riportate le nuove estensioni di classe di Media Foundation per Windows 8:
    -   [**IMFMediaEngineEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex)
    -   [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
    -   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
    -   [**IMFSinkWriterEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex)
    -   [**IMFSourceReaderEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex)
    -   [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex)
    -   [**IMFWorkQueueServicesEx**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
-   Le [API video Direct3D 11](direct3d-11-video-apis.md) sono nuove per Windows 8. Le app desktop di Windows 8 possono comunque usare l' [API video Direct3D 9](direct3d-video-apis.md), ma le app di Windows Store devono usare la nuova API video Direct3D 11. Per ulteriori informazioni sul video Microsoft Direct3D 11, vedere [supporto della decodifica video Direct3D 11 in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).
-   Sono stati apportati aggiornamenti e miglioramenti per Media Foundation le code di lavoro. Per altre informazioni, vedere [miglioramenti della coda di lavoro e del threading](media-foundation-work-queue-and-threading-improvements.md) .
-   [Codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).
-   Per un elenco di Media Foundation API che è possibile usare con le app di Windows Store, vedere [Win32 e com per app di Windows Store (Multimedia)](media-foundation-headers-and-libraries.md).
-   Media Foundation non è incluso nelle edizioni N e KN di Windows 8. Per ulteriori informazioni, vedere [Microsoft Windows Media Feature Pack per le versioni N e KN di tutte le edizioni di Windows 8](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 




