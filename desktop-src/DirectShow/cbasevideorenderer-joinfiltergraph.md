---
description: Il metodo JoinFilterGraph Invia \_ \_ una notifica di evento distrutta dalla finestra EC quando un filtro viene rimosso dal grafico dei filtri.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Metodo CBaseVideoRenderer. JoinFilterGraph (Renbase. h)
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
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330232"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a>CBaseVideoRenderer. JoinFilterGraph, metodo

Il `JoinFilterGraph` metodo invia una notifica di evento [**\_ \_ distrutta dalla finestra EC**](ec-window-destroyed.md) quando un filtro viene rimosso dal grafico dei filtri.

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

Puntatore al grafico di filtro da unire.

</dd> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore al nome del filtro da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questa funzione membro esegue l'override della funzione membro [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) . Se il filtro sta lasciando il grafico del filtro (*pGraph* è **null**), invia una notifica di evento [**\_ \_ distrutta dalla finestra EC**](ec-window-destroyed.md) , in modo che il gestore di risorse non mantenga il renderer come oggetto attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




