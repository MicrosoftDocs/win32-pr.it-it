---
description: Il metodo DrawImage Disegna un frame video nella finestra del video.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Metodo CDrawImage. DrawImage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327212"
---
# <a name="cdrawimagedrawimage-method"></a>Metodo CDrawImage. DrawImage

Il `DrawImage` metodo disegna un frame video nella finestra del video.

## <a name="syntax"></a>Sintassi


```C++
BOOL DrawImage(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio che contiene l'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo delega a [**CDrawImage:: FastRender**](cdrawimage-fastrender.md) o [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md), a seconda che il filtro appartenga all'allocatore che ha fornito l'esempio. Se il filtro è proprietario dell'allocatore, l'esempio è sicuramente un oggetto [**CImageSample**](cimagesample.md) . In tal caso, nell'esempio viene utilizzata la memoria condivisa allocata da GDI e l'immagine può essere disegnata utilizzando **BitBlt** o **StretchBlt**. In caso contrario, le immagini devono essere disegnate usando le funzioni **SetDIBitsToDevice** o **StretchDIBits** più lente.

Nelle compilazioni di debug questo metodo chiama **DisplaySampleTimes** per creare i timestamp dell'esempio sull'immagine video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




