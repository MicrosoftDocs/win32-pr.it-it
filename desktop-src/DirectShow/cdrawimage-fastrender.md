---
description: Il metodo FastRender disegna l'immagine video usando le funzioni BitBlt o StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Metodo CDrawImage.FastRender (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146c3736f7aaa89fc9a724d9dd7e4bfb58160e21e2de57f40a8e855c8a3c1446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043606"
---
# <a name="cdrawimagefastrender-method"></a>Metodo CDrawImage.FastRender

Il `FastRender` metodo disegna l'immagine video usando le **funzioni BitBlt** **o StretchBlt.**

## <a name="syntax"></a>Sintassi


```C++
void FastRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio che contiene l'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il [**metodo CDrawImage::D rawImage**](cdrawimage-drawimage.md) chiama questo metodo, ma solo se l'allocatore per la connessione è un [**oggetto CImageAllocator.**](cimageallocator.md) In tal caso, l'esempio multimediale è garantito come [**oggetto CImageSample.**](cimagesample.md) **L'oggetto CImageSample** usa la funzione **CreateDIBSection** per allocare memoria condivisa per la bitmap, che consente di disegnare l'immagine usando **BitBlt** **o StretchBlt.**

Questo metodo chiama **BitBlt** se i rettangoli di origine e targer corrispondono esattamente oppure **StretchBlt** in caso contrario.

Se il filtro non è proprietario dell'allocatore, il **metodo DrawImage** usa [**CDrawImage::SlowRender**](cdrawimage-slowrender.md) per disegnare l'immagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




