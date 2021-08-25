---
description: Per configurare il motore di acquisizione, è possibile utilizzare gli attributi seguenti.
ms.assetid: C153F0AD-4E8B-41DA-B7FB-8D10AC20D22E
title: Attributi del motore di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e79d0410407d12b46c0577615088f0f925b8558169d02140486b9fdc8fb303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959151"
---
# <a name="capture-engine-attributes"></a>Attributi del motore di acquisizione

Per configurare il motore di acquisizione, è possibile utilizzare gli attributi seguenti.

I seguenti attributi sono correlati ai dispositivi di acquisizione:



| Attributo                                                                                                                              | Descrizione                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [FLUSSO DELLA FOTOCAMERA DEL MOTORE DI ACQUISIZIONE MF \_ \_ \_ \_ \_ BLOCCATO](mf-capture-engine-camera-stream-blocked.md)                                            | Segnala che l'acquisizione video è bloccata dal driver.                                                         |
| [FLUSSO DELLA FOTOCAMERA DEL MOTORE DI ACQUISIZIONE MF \_ \_ \_ \_ \_ SBLOCCATO](mf-capture-engine-camera-stream-unblocked.md)                                        | Segnala che l'acquisizione video viene ripristinata dopo essere stata bloccata.                                                        |
| [MF \_ CAPTURE \_ ENGINE \_ D3D \_ MANAGER](mf-capture-engine-d3d-manager.md)                                                                 | Imposta un puntatore a Gestione dispositivi DXGI nel motore di acquisizione.                                                   |
| [MF \_ CAPTURE \_ ENGINE \_ DECODER \_ MFT \_ FIELDOFUSE \_ UNLOCK \_ ATTRIBUTE](mf-capture-engine-decoder-mft-fieldofuse-unlock-attribute.md)      | Consente al motore di acquisizione di usare un decodificatore con restrizioni sul campo di utilizzo.                                    |
| [DISABILITARE \_ \_ \_ DXVA NEL MOTORE \_ DI ACQUISIZIONE MF](mf-capture-engine-disable-dxva.md)                                                               | Specifica se il motore di acquisizione usa DirectX Video Acceleration (DXVA) per la decodifica video.                    |
| [DISABILITARE LE TRASFORMAZIONI HARDWARE DI MF \_ CAPTURE \_ \_ \_](mf-capture-engine-disable-hardware-transforms.md)                                        | Disabilita l'uso di trasformazioni di Media Foundation basate su hardware (MFT) nel motore di acquisizione.                       |
| [ABILITAZIONE DELLA NOTIFICA \_ \_ \_ \_ \_ STREAMSTATE \_ DELLA FOTOCAMERA DA PARTE DEL MOTORE DI ACQUISIZIONE MF](mf-capture-engine-enable-camera-streamstate-notification.md)         | Indica se le notifiche sullo stato del flusso devono essere abilitate.                                                    |
| [MF \_ CAPTURE \_ ENGINE \_ ENCODER \_ MFT \_ FIELDOFUSE \_ UNLOCK \_ ATTRIBUTE](mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute.md)      | Consente al motore di acquisizione di usare un codificatore con restrizioni sul campo di utilizzo.                                   |
| [GUID DEL GENERATORE \_ DI EVENTI DEL MOTORE DI \_ \_ \_ ACQUISIZIONE \_ MF](mf-capture-engine-event-generator-guid.md)                                              | Identifica il componente che ha generato un evento di acquisizione.                                                           |
| [INDICE DEL FLUSSO \_ DI EVENTI DEL MOTORE DI \_ \_ ACQUISIZIONE \_ \_ MF](mf-capture-engine-event-stream-index.md)                                                  | Identifica il flusso che ha generato un evento di acquisizione.                                                                 |
| [CONFIGURAZIONE \_ \_ MEDIASOURCE DEL MOTORE \_ DI ACQUISIZIONE \_ MF](mf-capture-engine-mediasource-config.md)                                                   | Contiene le proprietà di configurazione per l'origine di acquisizione.                                                          |
| [ESEMPI DI MAX \_ PROCESSED AUDIO SINK DEL MOTORE DI \_ \_ ACQUISIZIONE \_ \_ \_ \_ \_ MF](mf-capture-engine-record-sink-audio-max-processed-samples.md)     | Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso audio del sink di registrazione.                   |
| [MF \_ CAPTURE \_ ENGINE \_ RECORD \_ SINK \_ AUDIO \_ MAX \_ UNPROCESSED \_ SAMPLES](mf-capture-engine-record-sink-audio-max-unprocessed-samples.md) | Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso audio del sink di registrazione. |
| [MF \_ CAPTURE \_ ENGINE \_ RECORD \_ SINK \_ VIDEO \_ MAX \_ PROCESSED \_ SAMPLES](mf-capture-engine-record-sink-video-max-processed-samples.md)     | Imposta il numero massimo di campioni elaborati che possono essere memorizzati nel buffer nel percorso video del sink di registrazione.                   |
| [MF \_ CAPTURE \_ ENGINE \_ RECORD \_ SINK \_ VIDEO \_ MAX \_ UNPROCESSED \_ SAMPLES](mf-capture-engine-record-sink-video-max-unprocessed-samples.md) | Imposta il numero massimo di campioni non elaborati che possono essere memorizzati nel buffer per l'elaborazione nel percorso video del sink di record.  |
| [TIPO DI \_ SINK DEL MOTORE DI \_ ACQUISIZIONE \_ MF \_](/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type)                                                                     | Specifica un tipo di sink di acquisizione.                                                                                  |
| [IL MOTORE DI \_ ACQUISIZIONE \_ MF \_ USA SOLO \_ \_ DISPOSITIVI \_ AUDIO](mf-capture-engine-use-audio-device-only.md)                                           | Specifica se il motore di acquisizione acquisisce audio ma non video.                                                 |
| [IL MOTORE DI \_ ACQUISIZIONE \_ MF \_ USA SOLO \_ \_ DISPOSITIVI \_ VIDEO](mf-capture-engine-use-video-device-only.md)                                           | Specifica se il motore di acquisizione acquisisce video ma non audio.                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 



