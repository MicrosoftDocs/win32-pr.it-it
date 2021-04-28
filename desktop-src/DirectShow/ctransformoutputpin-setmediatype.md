---
description: 'Metodo CTransformOutputPin.SetMediaType: il metodo SetMediaType imposta il tipo di supporto per la connessione.'
ms.assetid: 1d6569c1-e27b-4e96-af5a-64a78b762afd
title: Metodo CTransformOutputPin.SetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5aa8dcfbf573f6ca5b047c9f84567a84985732c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084799"
---
# <a name="ctransformoutputpinsetmediatype-method"></a>Metodo CTransformOutputPin.SetMediaType

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
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




