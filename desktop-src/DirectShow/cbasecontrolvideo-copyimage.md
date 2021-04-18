---
description: Crea una copia di memoria di un'immagine.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Metodo CBaseControlVideo. CopyImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327580"
---
# <a name="cbasecontrolvideocopyimage-method"></a>CBaseControlVideo. CopyImage, metodo

Crea una copia di memoria di un'immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'esempio che contiene l'immagine del video.

</dd> <dt>

*pVideoInfo* 
</dt> <dd>

Puntatore al formato che rappresenta l'immagine del video.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Puntatore alla dimensione del buffer di output.

</dd> <dt>

*pVideoImage* 
</dt> <dd>

Puntatore al buffer di output.

</dd> <dt>

*pSourceRect* 
</dt> <dd>

Puntatore al rettangolo del video di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il parametro *pVideoImage* è **null**, il parametro *pBufferSize* viene compilato con il numero di byte che il buffer di output richiede per archiviare l'immagine. Se il buffer passato è troppo piccolo o la funzione membro non riesce ad allocare memoria sufficiente, la funzione membro restituisce E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

La funzione membro recupera l'immagine dall'esempio e la copia nel buffer di output. La sezione del video copiato nel buffer di output riflette il rettangolo di origine impostato tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) (anche se non riflette il rettangolo di destinazione).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




