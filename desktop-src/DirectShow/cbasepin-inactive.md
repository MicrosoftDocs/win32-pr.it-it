---
description: 'Metodo CBasePin.Inactive: il metodo Inactive notifica al pin che il filtro non è più attivo.'
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Metodo CBasePin.Inactive (Amfilter.h)
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
ms.openlocfilehash: 8307f3823758eee2f70368e41d3f2dc01333fd538fe2feed30d31b7db876f118
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052741"
---
# <a name="cbasepininactive-method"></a>Metodo CBasePin.Inactive

Il `Inactive` metodo notifica al segnaposto che il filtro non è più attivo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Quando il filtro si arresta, la [**classe CBaseFilter**](cbasefilter.md) chiama questo metodo su tutti i pin connessi del filtro.

Questo metodo non esegue alcuna operazione nella classe di base. Le classi derivate devono eseguire l'override di questo metodo per liberare tutte le risorse ottenute dal [**metodo CBasePin::Active;**](cbasepin-active.md) ad esempio per decommettere gli allocatori del pin.

Lo stato interno del gestore del grafo del filtro non viene aggiornato fino al termine di questo metodo, quindi non testare lo stato da questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




