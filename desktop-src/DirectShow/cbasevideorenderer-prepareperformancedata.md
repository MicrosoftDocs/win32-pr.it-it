---
description: Il metodo PreparePerformanceData imposta i \_ valori m trLate e m \_ trFrame del frame corrente.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Metodo CBaseVideoRenderer. PreparePerformanceData (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325361"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a>CBaseVideoRenderer. PreparePerformanceData, metodo

Il `PreparePerformanceData` metodo imposta i valori **m \_ trLate** e **m \_ trFrame** del frame corrente.

## <a name="syntax"></a>Sintassi


```C++
void PreparePerformanceData(
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

## <a name="remarks"></a>Commenti

Questa funzione membro imposta **m \_ trLate** sul valore di *trLate* e **m \_ trFrame** sul valore di *trFrame*.

Quando la funzione membro [**CBaseVideoRenderer:: RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) viene chiamata da [**CBaseVideoRenderer:: OnRenderStart**](cbasevideorenderer-onrenderstart.md) o [**CBaseVideoRenderer:: OnDirectRender**](cbasevideorenderer-ondirectrender.md), passa i valori di **m \_ trLate** e **m \_ trFrame** per l'aggiornamento delle statistiche. `PreparePerformanceData` viene chiamato da [**CBaseVideoRenderer:: OnWaitEnd**](cbasevideorenderer-onwaitend.md) per impostare questi valori del membro dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




