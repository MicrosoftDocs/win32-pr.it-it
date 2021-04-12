---
description: Video FourCC
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: Video FourCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344851"
---
# <a name="video-fourccs"></a>Video FourCC

A molti formati video sono assegnati codici FOURCC. Un codice FOURCC è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII. Ad esempio, il codice FOURCC per YUY2 video è' YUY2'.

Diverse macro C/C++ sono definite per la dichiarazione di valori FOURCC nel codice sorgente. La macro **MAKEFOURCC** è definita in mmsystem. h e la macro **FCC** è definita in Aviriff. h e in diversi altri file di intestazione. È anche possibile dichiarare direttamente un codice FOURCC come valore letterale stringa semplicemente invertendo l'ordine dei caratteri. Pertanto, le istruzioni seguenti sono equivalenti:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

Nell'ultimo esempio è necessario invertire l'ordine dei byte perché Windows utilizza un'architettura little-endian. ' Y ' = 0x59,' U ' = 0x55 è 2' = 0x32, quindi ' 2YUY ' è 0x32595559.

Alcune delle API [DirectX Video Acceleration 2,0](directx-video-acceleration-2-0.md) usano un valore **D3DFORMAT** per descrivere un formato video. Un codice FOURCC può essere usato anche in questo contesto:

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a>Costanti FOURCC

Nella tabella seguente sono elencati alcuni codici FOURCC comuni.



| Valore FOURCC | Descrizione                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| H264       | Video H. 264.                                                                                                          |
| I420       | Video YUV archiviato in formato Planar 4:2:0.                                                                              |
| 'IYUV'       | Video YUV archiviato in formato Planar 4:2:0.                                                                              |
| ' 4S2'       | Video MPEG-4 Part 2.                                                                                                  |
| Mp4s       | Microsoft MPEG 4 codec versione 3. Questo codec non è più supportato.                                                  |
| MP4V       | Video MPEG-4 Part 2.                                                                                                  |
| MPG1       | Video MPEG-1.                                                                                                         |
| 'MSS1'       | Contenuto codificato con il codec Windows Media Video 7 dello schermo.                                                          |
| 'MSS2'       | Contenuto codificato con il codec della schermata Windows Media Video 9.                                                          |
| UYVY       | Video YUV archiviato in formato 4:2:2 compresso. Simile a YUY2 ma con un ordine di dati diverso.                         |
| WMV1       | Contenuto codificato con il codec Windows Media Video 7.                                                                 |
| WMV2       | Contenuto codificato con il codec Windows Media Video 8.                                                                 |
| WMV3       | Contenuto codificato con il codec Windows Media Video 9.                                                                 |
| 'WMVA'       | Contenuto codificato con la versione precedente e obsoleta del codec del profilo avanzato Windows Media Video 9.                 |
| 'WMVP'       | Contenuto codificato con il codec di immagine Windows Media Video 9,1.                                                         |
| WVC1       | SMPTE 421M ("VC-1"). Contenuto codificato con Windows Media Video 9 profilo avanzato.                                     |
| 'WVP2'       | Contenuto codificato con il codec Windows Media Video 9,1 image V2.                                                      |
| YUY2       | Video YUV archiviato in formato 4:2:2 compresso.                                                                              |
| YV12       | Video YUV archiviato in formato Planar 4:2:0 o 4:1:1. Identico a I420/IYUV, tranne per il fatto che i piani utente e V sono stati scambiati. |
| YVU9       | Video YUV archiviato in formato Planar 16:1:1.                                                                             |
| YVYU       | Video YUV archiviato in formato 4:2:2 compresso. Simile a YUY2 ma con un ordine di dati diverso.                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[GUID del sottotipo video](video-subtype-guids.md)
</dt> </dl>

 

 



