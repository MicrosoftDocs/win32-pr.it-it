---
description: Il metodo RecordFrameLateness registra il momento in cui si è verificato il rendering e raccoglie le statistiche per la pagina delle proprietà.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Metodo CBaseVideoRenderer. RecordFrameLateness (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325360"
---
# <a name="cbasevideorendererrecordframelateness-method"></a>CBaseVideoRenderer. RecordFrameLateness, metodo

Il `RecordFrameLateness` metodo registra il momento in cui si è verificato il rendering e raccoglie le statistiche per la pagina delle proprietà.

## <a name="syntax"></a>Sintassi


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*trLate* 
</dt> <dd>

Valore che indica la latenza dell'esempio oltre il tempo di scadenza, in unità di tempo di riferimento.

</dd> <dt>

*trFrame* 
</dt> <dd>

Tempo di interframe, in unità di tempo di riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




