---
description: Il metodo CheckTargetRect determina se un rettangolo di destinazione è valido.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Metodo CBaseControlVideo.CheckTargetRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8444764af729f9536471a6a9df221cc118edb7d043112eb0b5351f45982d87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057321"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a>Metodo CBaseControlVideo.CheckTargetRect

Il `CheckTargetRect` metodo determina se un rettangolo di destinazione è valido.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Puntatore al rettangolo di destinazione da controllare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ INVALIDARG se non è valido; in caso contrario, restituisce NOERROR (S \_ OK).

## <a name="remarks"></a>Commenti

Questa funzione membro determina se il rettangolo di destinazione richiesto è valido. Poiché il rettangolo di destinazione specifica una posizione nel client logico della finestra, le coordinate possono essere negative, anche se la larghezza e l'altezza complessive non possono essere zero o un valore negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




