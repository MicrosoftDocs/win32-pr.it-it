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
ms.openlocfilehash: 1c35bcaabcb4a088a5ea1871efe57aefa63175c15588973bc046f51353137994
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916831"
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
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




