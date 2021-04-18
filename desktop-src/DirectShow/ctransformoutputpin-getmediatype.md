---
description: Il metodo GetMediaType recupera un tipo di supporto preferito, in base al valore di indice.
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Metodo CTransformOutputPin. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e52a5bc3b6a2b931a8592372e2ef636863c50ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330843"
---
# <a name="ctransformoutputpingetmediatype-method"></a>CTransformOutputPin. GetMediaType, metodo

Il `GetMediaType` metodo recupera un tipo di supporto preferito, in base al valore di indice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iPosition* 
</dt> <dd>

Valore di indice in base zero.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Operazione riuscita<br/>            |
| <dl> <dt>**\_non ci \_ sono \_ altri \_ elementi di VFW**</dt> </dl> | Indice non compreso nell'intervallo<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) . Se il pin di input del filtro non è connesso, il metodo restituisce VFW \_ s \_ non \_ più \_ elementi. In caso contrario, chiama il metodo [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) del filtro per recuperare il tipo di supporto. Il metodo **CTransformFilter:: GetMediaType** è virtuale puro; la classe derivata del filtro deve eseguirne l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




