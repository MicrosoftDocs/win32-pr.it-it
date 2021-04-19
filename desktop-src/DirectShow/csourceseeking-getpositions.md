---
description: 'Il metodo GetPositions recupera la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo IMediaSeeking:: GetPositions.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Metodo CSourceSeeking. GetPositions (Ctlutil. h)
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
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329505"
---
# <a name="csourceseekinggetpositions-method"></a>Metodo CSourceSeeking. GetPositions

Il `GetPositions` metodo recupera la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .

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

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Per il parametro *pCurrent* , questo metodo restituisce il valore della variabile membro [**\_ rtStart di CSourceSeeking:: m**](csourceseeking-m-rtstart.md) , che rappresenta il tempo di ricerca più recente, non la posizione corrente del flusso. Tuttavia, quando un'applicazione chiama **IMediaSeeking:: GetPositions** tramite Filter Graph Manager, i valori provengono in genere da un filtro renderer, non da un filtro di origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




