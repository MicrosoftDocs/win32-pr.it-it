---
description: Microsoft Media Foundation è stato introdotto in Windows Vista come sostituzione per DirectShow. Naturalmente, la DirectShow è ancora supportata in Windows 7, ma gli sviluppatori sono invitati a usare Media Foundation nelle nuove applicazioni multimediali digitali.
ms.assetid: c345c0d9-5325-4f73-b9ec-1673ad10e3e4
title: Novità di Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd2cd2b70ce23968ba9a302e4ab4e825914931ebffff651b534ee0974d75cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012061"
---
# <a name="whats-new-for-media-foundation"></a>Novità di Media Foundation

Microsoft Media Foundation è stato introdotto in Windows Vista come sostituzione per DirectShow. Naturalmente, la DirectShow è ancora supportata in Windows 7, ma gli sviluppatori sono invitati a usare Media Foundation nelle nuove applicazioni multimediali digitali.

I miglioramenti apportati Media Foundation possono essere riepilogati come segue:

-   Migliore supporto del formato, incluso MPEG-4
-   Supporto per i dispositivi di acquisizione e i codec hardware
-   Modello di programmazione semplificato
-   Miglioramenti alla piattaforma

## <a name="better-format-support"></a>Supporto del formato migliore

La pipeline audio/video di Media Foundation è stata implementata in Windows Vista, ma supportava un set limitato di formati e contenitori di file, il che significava che alcune applicazioni dovevano eseguire il fall back su tecnologie meno recenti, ad esempio DirectShow. In Windows 7, Media Foundation include i nuovi codec, le origini multimediali e i sink multimediali seguenti:

-   Decodificatore AAC
-   Codificatore AAC
-   Origine file AVI/WAVE
-   Decodificatore video DV
-   Decodificatore video H.264
-   Codificatore video H.264
-   Decodificatore MJPEG
-   Sink di file MP3\*
-   Origine file MP4/3GP
-   Sink di file MP4/3GP

> [!Note]  
> Il sink di file MP3 non include un codificatore audio MP3.

 

Per altre informazioni, vedere [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).

## <a name="hardware-device-support"></a>Supporto dei dispositivi hardware

Media Foundation supporta ora i tipi di dispositivi hardware seguenti nella pipeline audio/video:

-   Dispositivi di acquisizione video UVC 1.1, ad esempio webcam
-   Dispositivi di acquisizione audio
-   Codificatori e decodificatori hardware
-   Processori video hardware, ad esempio convertitori di spazi colori

I codec hardware possono eseguire una transcoddtura video molto veloce. Ad esempio, un'applicazione potrebbe trasferire file Windows Media Video (WMV) in un telefono cellulare che supporta solo file 3GP. Usando un codificatore hardware, l'applicazione può transcodificare il file nel backgound, appena prima di trasferirlo al dispositivo.

I dispositivi hardware sono rappresentati in Media Foundation da un oggetto proxy e vengono usati nella pipeline esattamente come i componenti basati su software.

## <a name="simplified-programming-model"></a>Modello di programmazione semplificato

In Windows Vista, Media Foundation ha esposto un set di API di livello relativamente basso. Queste API sono flessibili, ma troppo complesse per attività semplici. Windows 7 aggiunge nuove API di alto livello che semplificano la scrittura di applicazioni multimediali in C++. Queste nuove API di alto livello includono quanto segue.



| API                                | Descrizione                                                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Lettore di origine](source-reader.md) | Il lettore di origine estrae dati non elaborati o decodificati da un file multimediale. Ad esempio, è possibile usare il lettore di origine per ottenere bitmap di anteprima da un file video o per analizzare i dati della forma d'onda in un file audio. È anche possibile usare il lettore di origine per ottenere dati live da un dispositivo di acquisizione audio o video. <br/> |
| [Sink Writer](sink-writer.md)     | Il writer sink consente di creare file multimediali passando dati non compressi o codificati. Ad esempio, è possibile usarlo per ricodificare un file video o per acquisire video live da una webcam a un file.                                                                                                         |
| [API transcodifica](transcode-api.md) | Questa funzionalità supporta gli scenari di codifica audio/video più comuni.<br/>                                                                                                                                                                                                                               |



 

È comunque possibile usare le API di basso livello in Media Foundation. È possibile farlo se è necessario un maggiore controllo sulla pipeline audio/video.

## <a name="platform-improvements"></a>Miglioramenti della piattaforma

Windows 7 include numerosi miglioramenti alle API Media Foundation della piattaforma sottostante. Le applicazioni avanzate possono usare direttamente queste API. altre applicazioni otterrà i vantaggi indirettamente. I miglioramenti includono:

-   Modifiche nella pipeline video per ridurre il consumo di energia e l'utilizzo della memoria video.
-   [DXVA-HD:](dxva-hd.md)Microsoft DirectX Video Acceleration High Definition (DXVA-HD) è una nuova API per l'elaborazione video con accelerazione hardware. DXVA-HD offre un modello di composizione più flessibile rispetto all'API di elaborazione video DXVA precedente ed è più adatta per i formati video ad alta definizione.
-   Nuovo meccanismo per l'enumerazione delle origini e dei decodificatori, che include i valori dei vantaggi e un elenco preferito/bloccato. Questa funzionalità migliora l'affidabilità complessiva del sistema. Per altre informazioni, vedere i seguenti argomenti:
    -   [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
    -   [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)
    -   [Codec Merit](codec-merit.md)

## <a name="sdk-changes"></a>Modifiche dell'SDK

-   Nuove intestazioni e file di libreria: [Media Foundation intestazioni e librerie](media-foundation-headers-and-libraries.md)
-   Modifiche dll e lib: [modifiche alla libreria in Windows 7](media-foundation-headers-and-libraries.md)
-   Nuovi esempi di SDK:
    -   [Esempio di clip audio](audio-clip-sample.md)
    -   [Esempio DXVA-HD](dxva-hd-sample.md)
    -   [Esempio di MFCaptureD3D](mfcaptured3d-sample.md)
    -   [Esempio di MFCaptureToFile](mfcapturetofile-sample.md)
    -   [Transcodifica di esempio](transcode-sample.md)
    -   [Esempio di VideoThumbnail](videothumbnail-sample.md)
-   Miglioramenti a [TopoEdit:](topoedit.md)
    -   Supporto per la transcoding. Vedere Building a [Transcode Topology with TopoEdit (Creazione di una topologia transcodifica con TopoEdit).](building-a-transcode-topology-with-topoedit.md)
    -   Supporto per l'acquisizione di audio e video. Vedere [Topology Menu](topology-menu.md).

## <a name="new-in-windows-8"></a>Novità di Windows 8

Alcuni dei nuovi aggiornamenti per Media Foundation con Windows 8 sono:

-   [**IMFCaptureEngine controlla**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) uno o più dispositivi di acquisizione. Per un [elenco di attributi, vedere](capture-engine-attributes.md) Attributi del motore di acquisizione. Altre nuove interfacce correlate all'acquisizione di contenuti multimediali [**sono IMFCapturePhotoSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink), [**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink), [**IMFCaptureRecordSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink), [**IMFCaptureSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink)e [**IMFCaptureSource**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource).
-   Le estensioni Media Foundation seguenti sono nuove per Windows 8:
    -   [**IMFMediaEngineEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex)
    -   [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
    -   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
    -   [**IMFSinkWriterEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex)
    -   [**IMFSourceReaderEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex)
    -   [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex)
    -   [**IMFWorkQueueServicesEx**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
-   [L'API Video Direct3D 11](direct3d-11-video-apis.md) è una novità per Windows 8. Windows 8 Le app desktop possono comunque usare [l'API Video Direct3D 9,](direct3d-video-apis.md)ma Windows Store devono usare la nuova API Video Direct3D 11. Per altre informazioni su Microsoft Direct3D 11 Video, vedi Supporto della decodifica video [Direct3D 11 in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).
-   Sono stati apportati aggiornamenti e miglioramenti alle Media Foundation di lavoro. Per [altre informazioni, vedere Work Queue and Threading Improvements (Miglioramenti](media-foundation-work-queue-and-threading-improvements.md) della coda di lavoro e del threading).
-   [Codificatori di fotocamera H.264 UVC 1.5](camera-encoder-h264-uvc-1-5.md).
-   Per un elenco dell'API Media Foundation che può essere usata con le app di Windows Store, vedere Win32 e COM per le app di [Windows Store (multimediali).](media-foundation-headers-and-libraries.md)
-   Media Foundation non è incluso nelle edizioni N e WINDOWS 8. Per altre informazioni, vedere [Microsoft Windows Media Feature Pack for N and EDITION Versions of all Windows 8 Editions](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 




