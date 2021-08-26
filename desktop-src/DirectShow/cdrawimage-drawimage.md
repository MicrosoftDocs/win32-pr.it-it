---
description: Il metodo DrawImage disegna un fotogramma video nella finestra video.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Metodo CDrawImage.DrawImage (Winutil.h)
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
ms.openlocfilehash: c2791d20b906f2a2adce31ce99b9e7498854c8fca00ade4507db0207e04b2cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043607"
---
# <a name="cdrawimagedrawimage-method"></a>Metodo CDrawImage.DrawImage

Il `DrawImage` metodo disegna un fotogramma video nella finestra video.

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

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio che contiene l'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo delega [**a CDrawImage::FastRender**](cdrawimage-fastrender.md) o [**CDrawImage::SlowRender**](cdrawimage-slowrender.md), a seconda che il filtro sia proprietario dell'allocatore che ha fornito l'esempio. Se il filtro è proprietario dell'allocatore, è garantito che l'esempio sia un [**oggetto CImageSample.**](cimagesample.md) In tal caso, l'esempio usa la memoria condivisa allocata da GDI e l'immagine può essere disegnata usando **BitBlt** **o StretchBlt**. In caso contrario, le immagini devono essere disegnate usando le funzioni **SetDIBitsToDevice** o **StretchDIBits più** lente.

Nelle build di debug, questo metodo chiama **DisplaySampleTimes** per disegnare i timestamp dell'esempio sull'immagine video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




