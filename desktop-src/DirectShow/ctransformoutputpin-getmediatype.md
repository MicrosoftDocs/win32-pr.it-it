---
description: 'Metodo CTransformOutputPin.GetMediaType: il metodo GetMediaType recupera un tipo di supporto preferito, in base al valore di indice.'
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Metodo CTransformOutputPin.GetMediaType (Transfrm.h)
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
ms.openlocfilehash: ddd064934eea6ef2c88a4304466b15811910e8e352041e7242c75650dd54b2a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812781"
---
# <a name="ctransformoutputpingetmediatype-method"></a>Metodo CTransformOutputPin.GetMediaType

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

Puntatore a [**un oggetto CMediaType**](cmediatype.md) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione riuscita<br/>            |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Indice non compreso nell'intervallo<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBasePin::GetMediaType.**](cbasepin-getmediatype.md) Se il pin di input del filtro non è connesso, il metodo restituisce VFW \_ S \_ NO MORE \_ \_ ITEMS. In caso contrario, chiama il metodo [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) del filtro per recuperare il tipo di supporto. Il **metodo CTransformFilter::GetMediaType** è virtuale puro; La classe derivata del filtro deve eseguirne l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




