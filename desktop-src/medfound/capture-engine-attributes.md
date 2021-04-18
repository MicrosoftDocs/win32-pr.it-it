---
description: Per configurare il motore di acquisizione, è possibile usare gli attributi seguenti.
ms.assetid: C153F0AD-4E8B-41DA-B7FB-8D10AC20D22E
title: Attributi del motore di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1340fa69f80d456a29331d303f313d41c31ee41
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "106320831"
---
# <a name="capture-engine-attributes"></a>Attributi del motore di acquisizione

Per configurare il motore di acquisizione, è possibile usare gli attributi seguenti.

Gli attributi seguenti sono correlati ai dispositivi di acquisizione:



| Attributo                                                                                                                              | Descrizione                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [\_ \_ flusso della fotocamera del motore di acquisizione MF \_ \_ \_ bloccato](mf-capture-engine-camera-stream-blocked.md)                                            | Segnala che l'acquisizione video è bloccata dal driver.                                                         |
| [\_ \_ flusso della fotocamera del motore di acquisizione MF \_ \_ \_ sbloccato](mf-capture-engine-camera-stream-unblocked.md)                                        | Segnala che l'acquisizione video viene ripristinata dopo essere stata bloccata.                                                        |
| [\_ \_ Gestione D3D del motore di acquisizione MF \_ \_](mf-capture-engine-d3d-manager.md)                                                                 | Imposta un puntatore al Gestione dispositivi DXGI nel motore di acquisizione.                                                   |
| [\_attributo di \_ \_ sblocco del decodificatore \_ \_ FIELDOFUSE \_ \_ di MF Capture Engine MFT](mf-capture-engine-decoder-mft-fieldofuse-unlock-attribute.md)      | Consente al motore di acquisizione di utilizzare un decodificatore con restrizioni per il campo di utilizzo.                                    |
| [\_motore di acquisizione MF \_ \_ disabilitare \_ DXVA](mf-capture-engine-disable-dxva.md)                                                               | Specifica se il motore di acquisizione usa l'accelerazione video DirectX (DXVA) per la decodifica dei video.                    |
| [MF \_ Capture \_ Disabilita \_ le \_ trasformazioni hardware](mf-capture-engine-disable-hardware-transforms.md)                                        | Disabilita l'uso di trasformazioni di Media Foundation basate su hardware (MFTs) nel motore di acquisizione.                       |
| [\_Abilitazione del motore di acquisizione MF \_ \_ \_ STREAMSTATE della fotocamera \_ \_](mf-capture-engine-enable-camera-streamstate-notification.md)         | Indica se le notifiche dello stato del flusso devono essere abilitate.                                                    |
| [\_ \_ \_ attributo Unlock del codificatore \_ MFT \_ FIELDOFUSE \_ \_ per MF Capture Engine](mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute.md)      | Consente al motore di acquisizione di usare un codificatore con restrizioni di campo per l'utilizzo.                                   |
| [\_ \_ \_ \_ GUID generatore eventi motore di acquisizione MF \_](mf-capture-engine-event-generator-guid.md)                                              | Identifica il componente che ha generato un evento di acquisizione.                                                           |
| [\_indice del \_ flusso di eventi del motore di acquisizione MF \_ \_ \_](mf-capture-engine-event-stream-index.md)                                                  | Identifica il flusso che ha generato un evento di acquisizione.                                                                 |
| [\_configurazione del \_ motore di acquisizione \_ MF \_](mf-capture-engine-mediasource-config.md)                                                   | Contiene le proprietà di configurazione per l'origine di acquisizione.                                                          |
| [\_esempi di \_ \_ \_ \_ \_ \_ elaborazione massima \_ del sink di record del motore di acquisizione MF](mf-capture-engine-record-sink-audio-max-processed-samples.md)     | Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso audio del sink di record.                   |
| [\_esempi non \_ \_ \_ \_ \_ \_ elaborati \_ di record del motore di acquisizione MF max](mf-capture-engine-record-sink-audio-max-unprocessed-samples.md) | Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso audio del sink di record. |
| [\_esempi di \_ \_ \_ \_ \_ elaborazione massima dei \_ record sink \_ del motore di acquisizione MF](mf-capture-engine-record-sink-video-max-processed-samples.md)     | Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso video del sink di record.                   |
| [\_ \_ \_ \_ \_ \_ numero massimo di \_ campioni non elaborati \_ di record del motore di acquisizione MF video sink](mf-capture-engine-record-sink-video-max-unprocessed-samples.md) | Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso video del sink di record.  |
| [\_tipo di \_ sink del motore di acquisizione MF \_ \_](/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type)                                                                     | Specifica un tipo di sink di acquisizione.                                                                                  |
| [\_motore di acquisizione MF \_ \_ Usa \_ \_ solo dispositivo audio \_](mf-capture-engine-use-audio-device-only.md)                                           | Specifica se il motore di acquisizione acquisisce audio ma non video.                                                 |
| [\_motore di acquisizione MF \_ \_ usare solo il \_ \_ dispositivo video \_](mf-capture-engine-use-video-device-only.md)                                           | Specifica se il motore di acquisizione acquisisce video ma non audio.                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 



