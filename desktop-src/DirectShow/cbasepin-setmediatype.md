---
description: 'Metodo CBasePin.SetMediaType: il metodo SetMediaType imposta il tipo di supporto per la connessione.'
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Metodo CBasePin.SetMediaType (Amfilter.h)
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
ms.openlocfilehash: e71047b5063a5975266e5e24db936a0baf9e7b65e81ce29b402ccce4638267a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108641"
---
# <a name="cbasepinsetmediatype-method"></a>Metodo CBasePin.SetMediaType

Il `SetMediaType` metodo imposta il tipo di supporto per la connessione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo stabilisce il formato per una connessione pin. Prima di chiamare questo metodo, il pin chiama il [**metodo CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) per determinare se il tipo di supporto è accettabile. Si presuppone quindi *che il parametro pmt* sia un tipo di supporto accettabile.

Nella classe di base questo metodo imposta la variabile membro [**CBasePin::m \_ mt**](cbasepin-m-mt.md) e restituisce S \_ OK. Una classe derivata può eseguire l'override di questo metodo se richiede una notifica quando viene impostato il tipo di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




