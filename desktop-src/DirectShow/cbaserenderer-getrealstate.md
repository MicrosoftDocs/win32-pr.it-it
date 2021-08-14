---
description: Il metodo GetRealState recupera lo stato del filtro.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Metodo CBaseRenderer.GetRealState (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c65ac4310abddc619296776981040cc5e1e6c5ad48ce37ea24210bc5a85d94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403420"
---
# <a name="cbaserenderergetrealstate-method"></a>Metodo CBaseRenderer.GetRealState

Il `GetRealState` metodo recupera lo stato del filtro.

## <a name="syntax"></a>Sintassi


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore di [**CBaseFilter::m \_ State**](cbasefilter-m-state.md). Il valore è un membro del [**tipo enumerato FILTER \_ STATE.**](/windows/win32/api/strmif/ne-strmif-filter_state)

## <a name="remarks"></a>Commenti

Questo metodo offre un'alternativa più semplice al [**metodo CBaseRenderer::GetState,**](cbaserenderer-getstate.md) per uso interno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




