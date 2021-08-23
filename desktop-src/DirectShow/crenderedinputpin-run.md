---
description: Il metodo Run notifica al pin che il filtro è in esecuzione. Questo metodo esegue l'override del metodo CBasePin::Run.
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: Metodo CRenderedInputPin.Run (Amextra.h)
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
ms.openlocfilehash: c372101aee2817e08545080048c98a25af7efb152f4873e54366e73571763065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652021"
---
# <a name="crenderedinputpinrun-method"></a>Metodo CRenderedInputPin.Run

Il `Run` metodo notifica al pin che il filtro è in esecuzione. Questo metodo esegue l'override [**del metodo CBasePin::Run.**](cbasepin-run.md)

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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amextra.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




