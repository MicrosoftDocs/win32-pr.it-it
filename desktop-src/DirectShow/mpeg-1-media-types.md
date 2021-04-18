---
description: Questa sezione elenca i tipi di supporto usati per i dati MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Tipi di supporto MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d1ff7c121c52db39d574f9bbae3650b04312e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320568"
---
# <a name="mpeg-1-media-types"></a>Tipi di supporto MPEG-1

Questa sezione elenca i tipi di supporto usati per i dati MPEG-1.

## <a name="mpeg-1-system-stream"></a>Flusso di sistema MPEG-1



|                       |                                                 |
|-----------------------|-------------------------------------------------|
| Tipo principale            | \_Flusso MEDIATYPE                               |
| Subtype               | \_MPEG1SYSTEM MEDIASUBTYPE                       |
| Tipo di formato           | FORMATO \_ MPEGStreams                             |
| Struttura Format      | [**AM \_ MPEGSYSTEMTYPE**](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| Contenuto di esempio multimediale | Flusso di byte; Nessun allineamento                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a>Flusso di sistema MPEG-1 dal CD video



|                       |                            |
|-----------------------|----------------------------|
| Tipo principale            | \_Flusso MEDIATYPE          |
| Subtype               | \_MPEG1VIDEOCD MEDIASUBTYPE |
| Tipo di formato           | GUID \_ null                 |
| Struttura Format      | nessuno                       |
| Contenuto di esempio multimediale | Flusso di byte; Nessun allineamento. |



 

## <a name="mpeg-1-audio-packet"></a>Pacchetto audio MPEG-1



|                       |                                                |
|-----------------------|------------------------------------------------|
| Tipo principale            | \_Audio MEDIATYPE                               |
| Subtype               | \_MPEG1PACKET MEDIASUBTYPE                      |
| Tipo di formato           | FORMATO \_ WAVEFORMATEX                           |
| Struttura Format      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| Contenuto di esempio multimediale | Singolo pacchetto MPEG-1, inclusa l'intestazione del pacchetto. |



 

## <a name="mpeg-1-audio-payload"></a>Payload audio MPEG-1



|                       |                                            |
|-----------------------|--------------------------------------------|
| Tipo principale            | \_Audio MEDIATYPE                           |
| Subtype               | \_MPEG1PAYLOAD MEDIASUBTYPE                 |
| Tipo di formato           | FORMATO \_ WAVEFORMATEX                       |
| Struttura Format      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| Contenuto di esempio multimediale | Dati audio MPEG-1 allineati a byte.            |



 

## <a name="mpeg-1-video-packet"></a>Pacchetto video MPEG-1



|                       |                                                |
|-----------------------|------------------------------------------------|
| Tipo principale            | Video di MEDIATYPE \_                               |
| Subtype               | \_MPEG1PACKET MEDIASUBTYPE                      |
| Tipo di formato           | FORMATO \_ mpegvideo                              |
| Struttura Format      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| Contenuto di esempio multimediale | Singolo pacchetto MPEG-1, inclusa l'intestazione del pacchetto. |



 

## <a name="mpeg-1-video-payload"></a>Payload video MPEG-1



|                       |                                          |
|-----------------------|------------------------------------------|
| Tipo principale            | Video di MEDIATYPE \_                         |
| Subtype               | \_MPEG1PAYLOAD MEDIASUBTYPE               |
| Tipo di formato           | FORMATO \_ mpegvideo                        |
| Struttura Format      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| Contenuto di esempio multimediale | Dati video MPEG-1 allineati a byte.          |



 

## <a name="mpeg-1-native-video-stream"></a>Flusso video nativo MPEG-1



|                       |                                                |
|-----------------------|------------------------------------------------|
| Tipo principale            | \_Flusso MEDIATYPE                              |
| Subtype               | \_MPEG1VIDEO MEDIASUBTYPE                      |
| Tipo di formato           | GUID \_ null                                     |
| Struttura Format      | nessuno                                           |
| Contenuto di esempio multimediale | Matrice di byte del flusso video (nessun livello di sistema). |



 

## <a name="mpeg-1-native-audio-stream"></a>Flusso audio MPEG-1 nativo



|                       |                                                |
|-----------------------|------------------------------------------------|
| Tipo principale            | \_Flusso MEDIATYPE                              |
| Subtype               | \_MPEG1AUDIO MEDIASUBTYPE                      |
| Tipo di formato           | GUID \_ null                                     |
| Struttura Format      | nessuno                                           |
| Contenuto di esempio multimediale | Matrice di byte del flusso audio (nessun livello di sistema). |



 

## <a name="remarks"></a>Commenti

I filtri DirectShow MPEG-1 supportano questi tipi come indicato di seguito.



| Filtra               | Direzione | Tipi di supporto supportati                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| Barra di divisione MPEG-1      | Input     | Flusso di sistema MPEG-1 System streamMPEG-1 dal CD video<br/>                                                 |
| Barra di divisione MPEG-1      | Output    | Payload audio MPEG-1 audio packetMPEG-1<br/> Pacchetto video MPEG-1<br/> Payload video MPEG-1<br/> |
| Codec audio software | Input     | Payload audio MPEG-1 audio packetMPEG-1<br/>                                                                |
| Codec video software | Input     | Payload video MPEG-1 packetMPEG-1<br/>                                                                |
| Codec audio software | Output    | Audio PCM                                                                                                         |
| Codec video software | Output    | Video non compresso (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)                                    |



 

I tipi di supporto per pacchetti video e payload MPEG-1 contengono un'intestazione di sequenza completa, in modo che i dati possano essere riprodotti dal centro di un file senza che sia necessaria un'intestazione di sequenza per inizializzare la riproduzione video.

L'intestazione della sequenza video viene aggiunta al tipo di dati video per MPEG video in modo che la riproduzione possa iniziare dal centro di un flusso. La lunghezza di questo campo è fino a 140 byte. include il codice di avvio dell'intestazione della sequenza (0x000001B3) all'inizio, insieme alle matrici di quantizzazione trovate nella prima intestazione di sequenza rilevata.

 

 




