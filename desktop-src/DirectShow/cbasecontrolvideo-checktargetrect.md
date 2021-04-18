---
description: Il metodo CheckTargetRect determina se un rettangolo di destinazione è valido.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Metodo CBaseControlVideo. CheckTargetRect (Ctlutil. h)
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
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327582"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a>CBaseControlVideo. CheckTargetRect, metodo

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

Questa funzione membro determina se il rettangolo di destinazione richiesto è valido. Poiché il rettangolo di destinazione specifica una posizione nel client logico della finestra, le coordinate possono essere negative, anche se la larghezza e l'altezza complessive non possono essere pari a zero o a un valore negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




