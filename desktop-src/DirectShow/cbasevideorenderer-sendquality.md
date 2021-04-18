---
description: Il metodo SendQuality Invia un messaggio di qualità per indicare cosa deve fare il fornitore per la qualità.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Metodo CBaseVideoRenderer. SendQuality (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a6ae7228be0f3012c49d652d11bf2c1c3bfc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325349"
---
# <a name="cbasevideorenderersendquality-method"></a>CBaseVideoRenderer. SendQuality, metodo

Il `SendQuality` metodo invia un messaggio di qualità per indicare cosa deve fare il fornitore per la qualità.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*trLate* 
</dt> <dd>

Quantità di tempo in cui il frame è in ritardo.

</dd> <dt>

*trRealStream* 
</dt> <dd>

Currentstream tempo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro invia un messaggio di controllo di qualità upstream per controllare la gestione della qualità. La natura del messaggio di qualità, ovvero se ridurre o aumentare il numero di campioni, viene determinata nell'implementazione della gestione della qualità in questa classe derivata (vedere [**CBaseVideoRenderer:: ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




