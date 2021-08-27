---
description: Il metodo JoinFilterGraph invia la notifica \_ dell'evento EC WINDOW \_ DESTROYED quando un filtro viene rimosso dal grafico dei filtri.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Metodo CBaseVideoRenderer.JoinFilterGraph (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3aed2c887bc7a452cda978e96cd369a71cad4fab60a72e0c914ebe9d9790a41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052211"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a>Metodo CBaseVideoRenderer.JoinFilterGraph

Il `JoinFilterGraph` metodo invia la notifica [**\_ dell'evento EC WINDOW \_ DESTROYED**](ec-window-destroyed.md) quando un filtro viene rimosso dal grafico dei filtri.

## <a name="syntax"></a>Sintassi


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGraph* 
</dt> <dd>

Puntatore al grafico dei filtri da unire.

</dd> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore al nome del filtro aggiunto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questa funzione membro esegue l'override della funzione membro [**CBaseFilter::JoinFilterGraph.**](cbasefilter-joinfiltergraph.md) Se il filtro lascia il grafico dei filtri *(pGraph* è **NULL),** invia una notifica dell'evento [**EC WINDOW \_ \_ DESTROYED**](ec-window-destroyed.md) in modo che il gestore delle risorse non si aggiri sul renderer come oggetto attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




