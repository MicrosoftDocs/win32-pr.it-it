---
description: 'Metodo CTransformInputPin.SetMediaType: il metodo SetMediaType imposta il tipo di supporto per la connessione.'
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Metodo CTransformInputPin.SetMediaType (Transfrm.h)
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
ms.openlocfilehash: 9343f464a7a5abe19c9310ffc7b36e504c02b23abf6b0f88d822815ae9952daf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767571"
---
# <a name="ctransforminputpinsetmediatype-method"></a>Metodo CTransformInputPin.SetMediaType

Il `SetMediaType` metodo imposta il tipo di supporto per la connessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Monte* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBasePin::SetMediaType.**](cbasepin-setmediatype.md) Chiama il metodo [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) del filtro per informare il filtro.

Il pin deve verificare che il tipo di supporto sia accettabile prima di chiamare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




