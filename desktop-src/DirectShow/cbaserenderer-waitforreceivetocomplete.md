---
description: Il metodo WaitForReceiveToComplete attende il completamento del metodo CBaseRenderer::Receive.
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Metodo CBaseRenderer.WaitForReceiveToComplete (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1f63efa53cc8e8829aba825e831f95595b16faf97bdf29777918c599aadade1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016789"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a>Metodo CBaseRenderer.WaitForReceiveToComplete

Il metodo attende il completamento del metodo `WaitForReceiveToComplete` [**CBaseRenderer::Receive.**](cbaserenderer-receive.md)

## <a name="syntax"></a>Sintassi


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

I [**metodi CBaseRenderer::Stop**](cbaserenderer-stop.md) e [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) chiamano questo metodo per sincronizzare la modifica dello stato con **il metodo Receive.**

In particolare, questo metodo invia messaggi mentre attende che il flag [**CBaseRenderer::m \_ bInReceive**](cbaserenderer-m-binreceive.md) diventi **FALSE.** Il flag diventa **TRUE** nel metodo [**CBaseRenderer::P repareReceive**](cbaserenderer-preparereceive.md) e torna a **FALSE** dopo che il metodo **Receive** ha chiamato il metodo [**CBaseRenderer::P repareRender.**](cbaserenderer-preparerender.md) La classe derivata può usare **PrepareRender** per impostare il riquadro. In attesa **del completamento di PrepareRender,** i messaggi di modifica del riquadro vengono inviati prima che si verifichi la modifica dello stato. In questo modo si evita un potenziale deadlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




