---
description: 'Metodo CBasePin.CheckMediaType: il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.'
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Metodo CBasePin.CheckMediaType (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe39f3a7aac155f3cc87fa6d58f402043861d1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099398"
---
# <a name="cbasepincheckmediatype-method"></a>Metodo CBasePin.CheckMediaType

Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il tipo di supporto proposto è accettabile. In caso contrario, restituisce S \_ FALSE o un codice di errore.

## <a name="remarks"></a>Commenti

La classe derivata deve eseguire l'override di questo metodo virtuale puro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




