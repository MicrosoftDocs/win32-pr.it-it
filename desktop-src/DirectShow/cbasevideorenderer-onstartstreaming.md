---
description: Il metodo OnStartStreaming reimposta tutte le volte che controlla il flusso.
ms.assetid: a2bb07f2-6880-4030-96c5-d146982dfe66
title: Metodo CBaseVideoRenderer.OnStartStreaming (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2a55d509c900c7be68d3225826c208755d31ef66e0c24119bd1d044dad1aefc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157056"
---
# <a name="cbasevideorendereronstartstreaming-method"></a>Metodo CBaseVideoRenderer.OnStartStreaming

Il `OnStartStreaming` metodo reimposta tutte le volte che controlla il flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnStartStreaming();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro esegue l'override di [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




