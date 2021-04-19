---
description: Il metodo Run notifica al pin che il filtro è ora in esecuzione.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: Metodo CBasePin. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328256"
---
# <a name="cbasepinrun-method"></a>Metodo CBasePin. Run

Il `Run` metodo notifica al pin che il filtro è ora in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tStart* 
</dt> <dd>

Ora di inizio passata al metodo [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) del filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Quando il filtro passa da sospeso a in esecuzione, la classe [**CBaseFilter**](cbasefilter.md) chiama questo metodo su tutti i pin del filtro.

Questo metodo non esegue alcuna operazione nella classe di base. Classi derivate possono eseguire l'override di questo metodo. Ad esempio, un PIN potrebbe avviare un thread di lavoro che fornisce esempi.

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

 

 




