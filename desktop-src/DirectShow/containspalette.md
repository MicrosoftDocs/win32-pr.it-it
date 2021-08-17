---
description: La funzione ContainsPalette determina se una struttura VIDEOINFOHEADER specificata contiene una tavolozza.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: Funzione ContainsPalette (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c9e5ab793dfaadb868cc09cfbe25e59c02dc338b470992b81ab1990581e5c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954170"
---
# <a name="containspalette-function"></a>Funzione ContainsPalette

La **funzione ContainsPalette** determina se una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) specificata contiene una tavolozza.

## <a name="syntax"></a>Sintassi


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Puntatore a una [**struttura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se bitdepth è minore o uguale a 8 (**bmiHeader.biBitCount**) o se il numero di indici di colore è maggiore di zero (**bmiHeader.biClrUsed**). In **caso contrario, restituisce FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per video e immagini](video-and-image-functions.md)
</dt> </dl>

 

 




