---
description: Il metodo SetMediaType imposta il tipo di supporto per la connessione.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Metodo CBasePin. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 07ac736558cea12a16c695cf109c3d6283ce4a13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330312"
---
# <a name="cbasepinsetmediatype-method"></a>CBasePin. SetMediaType, metodo

Il `SetMediaType` metodo imposta il tipo di supporto per la connessione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo stabilisce il formato per una connessione pin. Prima di chiamare questo metodo, il pin chiama il metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) per determinare se il tipo di supporto è accettabile. Pertanto, si presuppone che il parametro *PMT* sia un tipo di supporto accettabile.

Nella classe di base, questo metodo imposta la variabile membro [**CBasePin:: m \_ mt**](cbasepin-m-mt.md) e restituisce \_ OK. Una classe derivata può eseguire l'override di questo metodo se è necessaria una notifica quando è impostato il tipo di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




