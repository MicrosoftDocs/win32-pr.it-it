---
description: "Il metodo GetSyncSource recupera l'orologio di riferimento utilizzato dal filtro. Questo metodo implementa il metodo IMediaFilter:: GetSyncSource."
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: Metodo CBaseFilter. GetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64f2d46ded16384e53e5281632bc0a064021f673
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331544"
---
# <a name="cbasefiltergetsyncsource-method"></a>CBaseFilter. GetSyncSource, metodo

Il `GetSyncSource` metodo recupera l'orologio di riferimento utilizzato dal filtro. Questo metodo implementa il metodo [**IMediaFilter:: GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pClock* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del clock.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un \_ puntatore S OK o e \_ .

## <a name="remarks"></a>Commenti

Se il filtro non usa un clock di riferimento, *\* pClock* è impostato su **null**. Quando il metodo restituisce un risultato, se *\* pClock* è diverso da **null**, l'interfaccia **IReferenceClock** include un conteggio dei riferimenti in attesa. Assicurarsi di rilasciarlo al termine dell'operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




