---
description: Il metodo SourceThreadCanWait contiene o rilascia il thread di streaming.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Metodo CBaseRenderer.SourceThreadCanWait (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba9f8e202d7c98bfea5d7068fa63a8d889d88fb10b4c6a7cb3516fadbca7ebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954770"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a>Metodo CBaseRenderer.SourceThreadCanWait

Il `SourceThreadCanWait` metodo contiene o rilascia il thread di streaming.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bCanWait* 
</dt> <dd>

Valore booleano che indica se contenere il thread di streaming. Se **TRUE,** il thread di streaming viene bloccato durante l'attesa del filtro per il rendering degli esempi successivi. Se **FALSE,** il thread di streaming viene rilasciato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

La chiamata al metodo con il valore FALSE forza la restituzione del filtro `SourceThreadCanWait` da una chiamata [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) bloccata.  Quando il filtro è in esecuzione, blocca le **chiamate Receive** fino all'ora di presentazione dell'esempio corrente. Quando il filtro viene sospeso, blocca le **chiamate Receive** per un periodo illimitato. Questo comportamento regola il flusso di dati nel flusso. Quando il filtro viene arrestato o scaricato, tuttavia, non deve bloccarsi.

Il blocco è controllato dal metodo [**CBaseRenderer::WaitForRenderTime,**](cbaserenderer-waitforrendertime.md) che attende due eventi: [**CBaseRenderer::m \_ RenderEvent**](cbaserenderer-m-renderevent.md) e [**CBaseRenderer::m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md). **\_ L'evento m RenderEvent** viene segnalato all'arrivo dell'ora di presentazione. **\_ L'evento m ThreadSignal** viene segnalato quando `SourceThreadCanWait` viene chiamato con il valore **FALSE.** Se `SourceThreadCanWait` si chiama con il valore **TRUE,** l'evento viene reimpostato.

I [**metodi CBaseRenderer::Stop**](cbaserenderer-stop.md) e [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) chiamano con il valore `SourceThreadCanWait` **FALSE** (rilascio del thread di streaming). I metodi [**CBaseRenderer::P ause**](cbaserenderer-pause.md), [**CBaseRenderer::Run**](cbaserenderer-run.md)e [**CBaseRenderer::EndFlush**](cbaserenderer-endflush.md) chiamano con il `SourceThreadCanWait` valore **TRUE**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




