---
description: Il metodo inattivo notifica al pin che il filtro non è più attivo.
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Metodo CBasePin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 431b243107c365b5d9fda729fff2de80d9193c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329538"
---
# <a name="cbasepininactive-method"></a>Metodo CBasePin. Inactive

Il `Inactive` metodo notifica al pin che il filtro non è più attivo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Quando il filtro viene arrestato, la classe [**CBaseFilter**](cbasefilter.md) chiama questo metodo su tutti i pin connessi del filtro.

Questo metodo non esegue alcuna operazione nella classe di base. Le classi derivate devono eseguire l'override di questo metodo per liberare tutte le risorse ottenute dal metodo [**CBasePin:: Active**](cbasepin-active.md) ; ad esempio, per decommitre gli allocatori del PIN.

Lo stato interno del gestore del grafico del filtro non viene aggiornato finché il metodo non viene restituito, pertanto non è necessario eseguire il test dello stato da questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




