---
description: Questa sezione elenca i tipi di supporti usati per i dati MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Tipi di supporti MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f6486b455fc2045ceb0256f6b6344f06a8923ef767c397068022acec052627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684931"
---
# <a name="mpeg-1-media-types"></a>Tipi di supporti MPEG-1

Questa sezione elenca i tipi di supporti usati per i dati MPEG-1.

## <a name="mpeg-1-system-stream"></a>Flusso di sistema MPEG-1



| Etichetta | Valore |
|-----------------------|-------------------------------------------------|
| Tipo principale            | Flusso \_ MEDIATYPE                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1System                       |
| Tipo di formato           | FORMAT \_ MPEGStreams                             |
| Struttura del formato      | [**AM \_ MPEGSYSTEMTYPE**](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| Contenuto dell'esempio multimediale | Flusso di byte; nessun allineamento                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a>Flusso di sistema MPEG-1 da Video CD



| Etichetta | Valore |
|-----------------------|----------------------------|
| Tipo principale            | Flusso \_ MEDIATYPE          |
| Subtype               | MEDIASUBTYPE \_ MPEG1VideoCD |
| Tipo di formato           | GUID \_ NULL                 |
| Struttura del formato      | Nessuno                       |
| Contenuto dell'esempio multimediale | Flusso di byte; nessun allineamento. |



 

## <a name="mpeg-1-audio-packet"></a>Pacchetto audio MPEG-1



| Etichetta | Valore |
|-----------------------|------------------------------------------------|
| Tipo principale            | MEDIATYPE \_ Audio                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Tipo di formato           | FORMAT \_ WaveFormatEx                           |
| Struttura del formato      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| Contenuto dell'esempio multimediale | Singolo pacchetto MPEG-1, inclusa l'intestazione del pacchetto. |



 

## <a name="mpeg-1-audio-payload"></a>MPEG-1 Audio Payload



| Etichetta | Valore |
|-----------------------|--------------------------------------------|
| Tipo principale            | MEDIATYPE \_ Audio                           |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload                 |
| Tipo di formato           | FORMAT \_ WaveFormatEx                       |
| Struttura del formato      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| Contenuto dell'esempio multimediale | Dati audio MPEG-1 allineati ai byte.            |



 

## <a name="mpeg-1-video-packet"></a>Pacchetto video MPEG-1



| Etichetta | Valore |
|-----------------------|------------------------------------------------|
| Tipo principale            | MEDIATYPE \_ Video                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Tipo di formato           | FORMAT \_ MPEGVideo                              |
| Struttura del formato      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| Contenuto dell'esempio multimediale | Singolo pacchetto MPEG-1, inclusa l'intestazione del pacchetto. |



 

## <a name="mpeg-1-video-payload"></a>Payload video MPEG-1



| Etichetta | Valore |
|-----------------------|------------------------------------------|
| Tipo principale            | MEDIATYPE \_ Video                         |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload               |
| Tipo di formato           | FORMAT \_ MPEGVideo                        |
| Struttura del formato      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| Contenuto dell'esempio multimediale | Dati video MPEG-1 allineati ai byte.          |



 

## <a name="mpeg-1-native-video-stream"></a>Flusso video nativo MPEG-1



| Etichetta | Valore |
|-----------------------|------------------------------------------------|
| Tipo principale            | Flusso \_ MEDIATYPE                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Video                      |
| Tipo di formato           | GUID \_ NULL                                     |
| Struttura del formato      | Nessuno                                           |
| Contenuto dell'esempio multimediale | Matrice di byte del flusso video (nessun livello di sistema). |



 

## <a name="mpeg-1-native-audio-stream"></a>Flusso audio nativo MPEG-1



| Etichetta | Valore |
|-----------------------|------------------------------------------------|
| Tipo principale            | Flusso \_ MEDIATYPE                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Audio                      |
| Tipo di formato           | GUID \_ NULL                                     |
| Struttura del formato      | Nessuno                                           |
| Contenuto dell'esempio multimediale | Matrice di byte del flusso audio (nessun livello di sistema). |



 

## <a name="remarks"></a>Commenti

I DirectShow mpeg-1 supportano questi tipi come indicato di seguito.



| Filtra               | Direzione | Tipi di supporti supportati                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| MPEG-1 Splitter      | Input     | Flusso di sistema MPEG-1 Stream di sistema MPEG-1 da Video CD<br/>                                                 |
| MPEG-1 Splitter      | Output    | Pacchetto audio MPEG-1 Payload audio MPEG-1<br/> Pacchetto video MPEG-1<br/> Payload video MPEG-1<br/> |
| Software Audio Codec | Input     | Pacchetto audio MPEG-1 Payload audio MPEG-1<br/>                                                                |
| Software Video Codec | Input     | Payload mpeg-1 video packetMPEG-1 Video<br/>                                                                |
| Software Audio Codec | Output    | Audio PCM                                                                                                         |
| Software Video Codec | Output    | Video non compresso (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)                                    |



 

I tipi di file multimediali di payload e pacchetto MPEG-1 Video contengono un'intestazione di sequenza completa in modo che i dati possano essere riprodotti dal centro di un file senza la necessità di un'intestazione di sequenza per inizializzare la riproduzione video.

L'intestazione della sequenza video viene aggiunta al tipo di dati video per il video MPEG in modo che la riproduzione possa iniziare dal centro di un flusso. La lunghezza di questo campo è fino a 140 byte. include il codice di inizio dell'intestazione di sequenza (0x000001B3) all'inizio, insieme a tutte le matrici di quantizzazione trovate nella prima intestazione di sequenza rilevata.

 

 




