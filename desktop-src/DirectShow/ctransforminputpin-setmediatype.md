---
description: Il metodo SetMediaType imposta il tipo di supporto per la connessione.
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Metodo CTransformInputPin. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b42531a003fbad1a2a08864390a512296c440e64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333310"
---
# <a name="ctransforminputpinsetmediatype-method"></a>CTransformInputPin. SetMediaType, metodo

Il `SetMediaType` metodo imposta il tipo di supporto per la connessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Mt* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBasePin:: SetMediaType**](cbasepin-setmediatype.md) . Chiama il metodo [**CTransformFilter:: SetMediaType**](ctransformfilter-setmediatype.md) del filtro per informare il filtro.

Il PIN deve verificare che il tipo di supporto sia accettabile prima di chiamare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




