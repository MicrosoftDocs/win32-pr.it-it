---
description: Codici FOURCC
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: Codici FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb789bc16a1643ee737c1c1a63bdbc5704567931
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123567"
---
# <a name="fourcc-codes"></a>Codici FOURCC

A molti formati multimediali digitali sono assegnati codici FOURCC. Un codice FOURCC è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII. Ad esempio, il codice FOURCC per YUY2 video è' YUY2'. Per i formati video compressi e i formati video non RGB (ad esempio YUV), il membro di **bicompressione** della struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) deve essere impostato sul codice FourCC.

Sono disponibili diverse macro C/C++ che semplificano la dichiarazione di valori FOURCC nel codice sorgente. La macro **MAKEFOURCC** , ad esempio, è dichiarata in mmsystem. h e la macro **FCC** è dichiarata in Aviriff. h. Utilizzarli come indicato di seguito:


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



È anche possibile dichiarare direttamente un codice FOURCC come valore letterale stringa semplicemente invertendo l'ordine dei caratteri. Ad esempio:


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



Invertire l'ordine è necessario perché il sistema operativo Microsoft Windows utilizza un'architettura little-endian. ' Y ' = 0x59,' U ' = 0x55 è 2' = 0x32, quindi ' 2YUY ' è 0x32595559.

### <a name="converting-fourcc-codes-to-subtype-guids"></a>Conversione di codici FOURCC in GUID di sottotipo

Un intervallo di 2 \* guid 32 è riservato per rappresentare FourCC. Questi GUID sono tutti il formato in `XXXXXXXX-0000-0010-8000-00AA00389B71` cui `XXXXXXXX` è il codice FourCC. Pertanto, il GUID del sottotipo per YUY2 è `32595559-0000-0010-8000-00AA00389B71` .

Molti di questi GUID sono già definiti nel file di intestazione UUIDs. h. Ad esempio, il sottotipo YUY2 è definito come MEDIASUBTYPE \_ YUY2. La libreria di classi base DirectShow fornisce anche una classe helper, [**FOURCCMap**](fourccmap.md), che può essere usata per convertire i codici FourCC in valori GUID. Il costruttore **FOURCCMap** accetta un codice FourCC come parametro di input. È quindi possibile eseguire il cast dell'oggetto **FOURCCMap** al GUID corrispondente:


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

 

 



