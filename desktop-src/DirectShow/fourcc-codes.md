---
description: Codici FOURCC
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: Codici FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25820d21fb8e8386fb11816c373debf427fa783b8a2f2d4723a46e689e6aea0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043321"
---
# <a name="fourcc-codes"></a>Codici FOURCC

A molti formati multimediali digitali sono assegnati codici FOURCC. Un codice FOURCC è un intero senza segno a 32 bit creato concatenando quattro caratteri ASCII. Ad esempio, il codice FOURCC per il video YUY2 è "YUY2". Per i formati video compressi e non RGB (ad esempio YUV), il membro **biCompression** della struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) deve essere impostato sul codice FOURCC.

Sono disponibili diverse macro C/C++ che semplificano la dichiarazione di valori FOURCC nel codice sorgente. Ad esempio, la macro **MAKEFOURCC** viene dichiarata in Mmsystem.h e la macro **FCC** viene dichiarata in Aviriff.h. Usarli come indicato di seguito:


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



È anche possibile dichiarare un codice FOURCC direttamente come valore letterale stringa semplicemente invertindo l'ordine dei caratteri. Esempio:


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



L'invertimento dell'ordine è necessario perché microsoft Windows sistema operativo usa un'architettura little-endian. 'Y' = 0x59, 'U' = 0x55 e '2' = 0x32, quindi '2YUY' è 0x32595559.

### <a name="converting-fourcc-codes-to-subtype-guids"></a>Conversione di codici FOURCC in GUID di sottotipo

Un intervallo di 2 \* 32 GUID è riservato per rappresentare i QUATTROC. Questi GUID sono tutti nel formato `XXXXXXXX-0000-0010-8000-00AA00389B71` in cui è il codice `XXXXXXXX` FOURCC. Di conseguenza, il GUID del sottotipo per YUY2 è `32595559-0000-0010-8000-00AA00389B71` .

Molti di questi GUID sono già definiti nel file di intestazione Uuids.h. Ad esempio, il sottotipo YUY2 è definito come MEDIASUBTYPE \_ YUY2. La DirectShow di classi base fornisce anche una classe helper, [**FOURCCMap,**](fourccmap.md)che può essere usata per convertire i codici FOURCC in valori GUID. Il **costruttore FOURCCMap** accetta un codice FOURCC come parametro di input. È quindi possibile eseguire il cast **dell'oggetto FOURCCMap** al GUID corrispondente:


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Sottotipi audio**](audio-subtypes.md)
</dt> <dt>

[Sottotipi video](video-subtypes.md)
</dt> <dt>

[Uso dei codec](working-with-codecs.md)
</dt> </dl>

 

 



