---
description: Il metodo Render esegue il rendering di un campione.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Metodo CBaseRenderer. Render (Renbase. h)
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
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333332"
---
# <a name="cbaserendererrender-method"></a>Metodo CBaseRenderer. Render

Il `Render` metodo esegue il rendering di un campione.

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

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Il filtro è stato interrotto oppure *pMediaSample* è **null**.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                                              |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo virtuale pure [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md), che esegue le operazioni effettive. La classe derivata deve implementare **DoRenderSample**.

Immediatamente prima di chiamare **DoRenderSample**, questo metodo chiama il metodo [**CBaseRenderer:: OnRenderStart**](cbaserenderer-onrenderstart.md) . Immediatamente dopo, viene chiamato il metodo [**CBaseRenderer:: OnRenderEnd**](cbaserenderer-onrenderend.md) . La classe derivata può eseguire l'override di questi due metodi in base alle esigenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




