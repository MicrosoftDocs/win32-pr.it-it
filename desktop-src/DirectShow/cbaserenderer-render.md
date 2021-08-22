---
description: Il metodo Render esegue il rendering di un esempio.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Metodo CBaseRenderer.Render (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 185baf6818d2022dbe7b64cfab888945e1a2405433eefa925d2de70dcca286e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016859"
---
# <a name="cbaserendererrender-method"></a>Metodo CBaseRenderer.Render

Il `Render` metodo esegue il rendering di un esempio.

## <a name="syntax"></a>Sintassi


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili sono quelli riportati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Il filtro viene arrestato o *pMediaSample* è **NULL.**<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                                              |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo virtuale [**puro CBaseRenderer::D oRenderSample**](cbaserenderer-dorendersample.md), che esegue il lavoro reale. La classe derivata deve implementare **DoRenderSample.**

Immediatamente prima di **chiamare DoRenderSample,** questo metodo chiama il [**metodo CBaseRenderer::OnRenderStart.**](cbaserenderer-onrenderstart.md) Subito dopo, chiama il [**metodo CBaseRenderer::OnRenderEnd.**](cbaserenderer-onrenderend.md) La classe derivata può eseguire l'override di questi due metodi in base alle esigenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




