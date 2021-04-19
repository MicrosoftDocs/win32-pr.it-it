---
description: "Il metodo GetStopPosition recupera l'ora in cui si interrompe la riproduzione rispetto alla durata del flusso. Questo metodo implementa il metodo IMediaSeeking:: GetStopPosition."
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Metodo CSourceSeeking. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329501"
---
# <a name="csourceseekinggetstopposition-method"></a>CSourceSeeking. GetStopPosition, metodo

Il `GetStopPosition` metodo recupera l'ora in cui si interrompe la riproduzione rispetto alla durata del flusso. Questo metodo implementa il metodo [**IMediaSeeking:: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStop* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di arresto, in unità del formato dell'ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Operazione riuscita<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Valore del puntatore **null**<br/> |



 

## <a name="remarks"></a>Commenti

L'ora di arresto è specificata dalla variabile membro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




