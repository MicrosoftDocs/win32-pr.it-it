---
description: Il metodo OnRenderStart imposta le informazioni per il rendering.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Metodo CBaseVideoRenderer.OnRenderStart (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78c82b00b8b719b03d096ac0f83e43c8471ea98d56eab7bf67d28b0adae852f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157036"
---
# <a name="cbasevideorendereronrenderstart-method"></a>Metodo CBaseVideoRenderer.OnRenderStart

Il `OnRenderStart` metodo imposta le informazioni per il rendering.

## <a name="syntax"></a>Sintassi


```C++
void OnRenderStart(
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

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro recupera l'ora corrente del clock dal sistema e la archivia in una variabile membro da usare al termine del disegno. La funzione esegue anche la registrazione delle prestazioni. Questa funzione membro deve essere chiamata subito prima dell'avvio del disegno.

Questa funzione membro esegue l'override di [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




