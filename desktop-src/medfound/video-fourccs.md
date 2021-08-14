---
description: Video FOURCC
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: Video FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21de7470fe512116336a7ea296d4e8f3e776d60290efc449a29899dafe2bf392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688509"
---
# <a name="video-fourccs"></a>Video FOURCC

A molti formati video sono assegnati codici FOURCC. Un codice FOURCC è un intero senza segno a 32 bit creato concatenando quattro caratteri ASCII. Ad esempio, il codice FOURCC per il video YUY2 è "YUY2".

Sono definite diverse macro C/C++ per la dichiarazione di valori FOURCC nel codice sorgente. La macro **MAKEFOURCC** è definita in Mmsystem.h e la macro **FCC** è definita in Aviriff.h e in vari altri file di intestazione. È anche possibile dichiarare un codice FOURCC direttamente come valore letterale stringa semplicemente invertindo l'ordine dei caratteri. Di conseguenza, le istruzioni seguenti sono equivalenti:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

Nell'ultimo esempio, l'invertimento dell'ordine dei byte è necessario perché Windows usa un'architettura little-endian. 'Y' = 0x59, 'U' = 0x55 e '2' = 0x32, quindi '2YUY' è 0x32595559.

Alcune API [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md) usano un **valore D3DFORMAT** per descrivere un formato video. Un codice FOURCC può essere usato anche in questo contesto:

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a>Costanti FOURCC

Nella tabella seguente sono elencati alcuni codici FOURCC comuni.



| Valore FOURCC | Descrizione                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| 'H264'       | Video H.264.                                                                                                          |
| 'I420'       | Video YUV archiviato in formato planare 4:2:0.                                                                              |
| 'IYUV'       | Video YUV archiviato in formato planare 4:2:0.                                                                              |
| 'M4S2'       | Video mpeg-4 parte 2.                                                                                                  |
| 'MP4S'       | Codec Microsoft MPEG 4 versione 3. Questo codec non è più supportato.                                                  |
| 'MP4V'       | Video mpeg-4 parte 2.                                                                                                  |
| 'MPG1'       | Video MPEG-1.                                                                                                         |
| 'MSS1'       | Contenuto codificato con il codec Windows video multimediale 7.                                                          |
| 'MSS2'       | Contenuto codificato con il codec dello schermo Windows Media Video 9.                                                          |
| 'UYVY'       | Video YUV archiviato in formato 4:2:2. Simile a YUY2 ma con un ordinamento diverso dei dati.                         |
| 'WMV1'       | Contenuto codificato con il codec Windows Media Video 7.                                                                 |
| 'WMV2'       | Contenuto codificato con il codec Windows Media Video 8.                                                                 |
| 'WMV3'       | Contenuto codificato con il codec Windows Media Video 9.                                                                 |
| 'WMVA'       | Contenuto codificato con la versione obsoleta precedente del codec Windows Media Video 9 Advanced Profile.                 |
| 'WMVP'       | Contenuto codificato con il codec Windows Media Video 9.1.                                                         |
| 'WVC1'       | SMPTE 421M ("VC-1"). Contenuto codificato con Windows profilo avanzato di Media Video 9.                                     |
| 'WVP2'       | Contenuto codificato con il codec Windows Media Video 9.1 Image v2.                                                      |
| 'YUY2'       | Video YUV archiviato in formato 4:2:2.                                                                              |
| 'YV12'       | Video YUV archiviato in formato planare 4:2:0 o 4:1:1. Identico a I420/IYUV, ad eccezione del fatto che i piani you e V vengono commutati. |
| 'YVU9'       | Video YUV archiviato in formato planare 16:1:1.                                                                             |
| 'YVYU'       | Video YUV archiviato in formato 4:2:2. Simile a YUY2 ma con un ordinamento diverso dei dati.                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di file multimediali video](video-media-types.md)
</dt> <dt>

[GUID sottotipo video](video-subtype-guids.md)
</dt> </dl>

 

 



