---
description: Il metodo OnStopStreaming viene chiamato alla fine del flusso per correggere gli orari per il report della pagina delle proprietà.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Metodo CBaseVideoRenderer.OnStopStreaming (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38e1e3fef83bab4d598cfd36294c5c405c1eca938372b43f12a6401c4be3c46b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586041"
---
# <a name="cbasevideorendereronstopstreaming-method"></a>Metodo CBaseVideoRenderer.OnStopStreaming

Il metodo viene chiamato alla fine del flusso per correggere gli orari per `OnStopStreaming` il report della pagina delle proprietà.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro viene chiamata due volte, una volta durante la sospensione e di nuovo quando il flusso viene effettivamente arrestato.

Questa funzione membro esegue l'override di [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




