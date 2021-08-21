---
description: Il metodo PreparePerformanceData imposta i valori m \_ trLate e m \_ trFrame del frame corrente.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Metodo CBaseVideoRenderer.PreparePerformanceData (Renbase.h)
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
ms.openlocfilehash: e8cb276b37e64b6bb34751ed2d034666f7ceeddd90d8e52e47b2a1fca499ff9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658335"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a>Metodo CBaseVideoRenderer.PreparePerformanceData

Il `PreparePerformanceData` metodo imposta i valori m **\_ trLate** e **m \_ trFrame** del frame corrente.

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

Valore che indica la ritardo dell'esempio oltre il tempo di scadenza, in unità di tempo di riferimento.

</dd> <dt>

*trFrame* 
</dt> <dd>

Tempo interframe, in unità di tempo di riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro imposta **m \_ trLate** sul valore di *trLate* e **m \_ trFrame** sul valore *di trFrame*.

Quando la funzione membro [**CBaseVideoRenderer::RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) viene chiamata da [**CBaseVideoRenderer::OnRenderStart**](cbasevideorenderer-onrenderstart.md) o [**CBaseVideoRenderer::OnDirectRender,**](cbasevideorenderer-ondirectrender.md)passa i valori di **m \_ trLate** e **m \_ trFrame** per aggiornare le statistiche. `PreparePerformanceData` viene chiamato da [**CBaseVideoRenderer::OnWaitEnd**](cbasevideorenderer-onwaitend.md) per impostare questi valori dei membri dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




