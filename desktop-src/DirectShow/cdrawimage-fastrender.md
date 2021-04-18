---
description: Il metodo FastRender disegna l'immagine video usando le funzioni BitBlt o StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Metodo CDrawImage. FastRender (Winutil. h)
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
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327210"
---
# <a name="cdrawimagefastrender-method"></a>CDrawImage. FastRender, metodo

Il `FastRender` metodo disegna l'immagine video usando le funzioni **BitBlt** o **StretchBlt** .

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

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio che contiene l'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo [**CDrawImage::D rawImage**](cdrawimage-drawimage.md) chiama questo metodo, ma solo se l'allocatore per la connessione è un oggetto [**CImageAllocator**](cimageallocator.md) . In tal caso, l'esempio multimediale è sicuramente un oggetto [**CImageSample**](cimagesample.md) . L'oggetto **CImageSample** usa la funzione **CreateDIBSection** per allocare la memoria condivisa per la bitmap, che consente di creare l'immagine usando **BitBlt** o **StretchBlt**.

Questo metodo chiama **BitBlt** se i rettangoli di origine e destinazione corrispondono esattamente o **StretchBlt** in caso contrario.

Se il filtro non è il proprietario dell'allocatore, il metodo **DrawImage** USA [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md) per creare l'immagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




