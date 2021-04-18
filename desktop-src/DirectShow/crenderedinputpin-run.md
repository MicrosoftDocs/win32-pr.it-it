---
description: "Il metodo Run notifica al pin che il filtro è ora in esecuzione. Questo metodo esegue l'override del Metodo CBasePin:: Run."
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: Metodo CRenderedInputPin. Run (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328826"
---
# <a name="crenderedinputpinrun-method"></a>Metodo CRenderedInputPin. Run

Il `Run` metodo notifica al pin che il filtro è ora in esecuzione. Questo metodo esegue l'override del metodo [**CBasePin:: Run**](cbasepin-run.md) .

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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amextra. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




