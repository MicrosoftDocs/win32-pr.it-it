---
description: Il metodo ScheduleSample esegue l'override della classe di base che esegue il lavoro principale per mantenere un conteggio dei campioni estratti ed eliminati (usati dall'implementazione di IQualProp).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Metodo CBaseVideoRenderer.ScheduleSample (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f68701fd4c4d682d6bcd89c3b82d6bf054188a9bbdcb47c9019b563fad4a877f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658235"
---
# <a name="cbasevideorendererschedulesample-method"></a>Metodo CBaseVideoRenderer.ScheduleSample

Il metodo esegue l'override della classe di base che esegue il lavoro principale per mantenere un conteggio dei campioni estratti ed eliminati `ScheduleSample` (usati [**dall'implementazione di IQualProp).**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop)

## <a name="syntax"></a>Sintassi


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'esempio multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'esempio è pianificato. In caso contrario, restituisce **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




