---
description: Il metodo attivo notifica al pin che il filtro è ora attivo.
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Metodo CBasePin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a89c0c75671e6eb29b6ddb260c5f5ec0c385399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330938"
---
# <a name="cbasepinactive-method"></a>Metodo CBasePin. Active

Il `Active` metodo notifica al pin che il filtro è ora attivo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Quando il filtro passa da interrotto a sospeso, la classe [**CBaseFilter**](cbasefilter.md) chiama questo metodo su tutti i pin connessi del filtro.

Questo metodo non esegue alcuna operazione nella classe di base. Classi derivate possono eseguire l'override di questo metodo. ad esempio, un PIN potrebbe confermare gli allocatori o ottenere le risorse hardware.

Lo stato interno del gestore del grafico del filtro non viene aggiornato finché la funzione membro non viene restituita, pertanto non è necessario eseguire il test dello stato da questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




