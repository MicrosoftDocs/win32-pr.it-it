---
description: Il metodo SetDiscontinuity specifica se questo esempio rappresenta un'interruzione nel flusso di dati. Questo metodo implementa il metodo IMediaSample::SetDiscontinuity.
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Metodo CMediaSample.SetDiscontinuity (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4189498c60a52692c057a867dba8bc48c43d2b1c32fbd6091738a3711102f4b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832181"
---
# <a name="cmediasamplesetdiscontinuity-method"></a>Metodo CMediaSample.SetDiscontinuity

Il `SetDiscontinuity` metodo specifica se questo esempio rappresenta un'interruzione nel flusso di dati. Questo metodo implementa il [**metodo IMediaSample::SetDiscontinuity.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bDiscont* 
</dt> <dd>

Valore booleano che specifica se questo esempio è una discontinuità. Se **TRUE,** l'esempio multimediale non è più disponibile con l'esempio precedente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo aggiorna la variabile membro [**CMediaSample::m \_ dwFlags,**](cmediasample-m-dwflags.md) che specifica la proprietà discontinuity.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




