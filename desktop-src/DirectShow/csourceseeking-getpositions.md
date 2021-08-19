---
description: Il metodo GetPositions recupera la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo IMediaSeeking::GetPositions.
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Metodo CSourceSeeking.GetPositions (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b6f52d8d8b30a28d942d4395a465b9c7c49d0a23020ad212c81eb170d20ca0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073337"
---
# <a name="csourceseekinggetpositions-method"></a>Metodo CSourceSeeking.GetPositions

Il `GetPositions` metodo recupera la posizione corrente e la posizione di arresto. Questo metodo implementa il [**metodo IMediaSeeking::GetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntatore a una variabile che riceve la posizione iniziale.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntatore a una variabile che riceve la posizione di arresto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Per il *parametro pCurrent,* questo metodo restituisce il valore della variabile membro [**CSourceSeeking::m \_ rtStart,**](csourceseeking-m-rtstart.md) che rappresenta l'ora di ricerca più recente, non la posizione di streaming corrente. Tuttavia, quando un'applicazione chiama **IMediaSeeking::GetPositions** tramite il gestore del grafico filtri, i valori provengono in genere da un filtro renderer, non da un filtro di origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




