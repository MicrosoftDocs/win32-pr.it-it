---
description: Il metodo Run notifica al pin che il filtro è in esecuzione.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: Metodo CBasePin.Run (Amfilter.h)
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
ms.openlocfilehash: 4f145a827546a9258ee2968d0348ab7725147bb47132f5df5acbd2865a45b78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429811"
---
# <a name="cbasepinrun-method"></a>Metodo CBasePin.Run

Il `Run` metodo notifica al pin che il filtro è in esecuzione.

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

Ora di inizio passata al metodo [**IMediaFilter::Run del**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Quando il filtro passa dalla sospensione all'esecuzione, la [**classe CBaseFilter**](cbasefilter.md) chiama questo metodo su tutti i pin del filtro.

Questo metodo non esegue alcuna operazione nella classe di base. Le classi derivate possono eseguire l'override di questo metodo. Ad esempio, un pin potrebbe avviare un thread di lavoro che fornisce esempi.

Lo stato interno del gestore del grafico filtri non viene aggiornato fino a quando non viene restituita questa funzione membro, quindi non testare lo stato da questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




