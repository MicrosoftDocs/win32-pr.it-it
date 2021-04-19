---
description: Il metodo SourceThreadCanWait include o rilascia il thread di streaming.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Metodo CBaseRenderer. SourceThreadCanWait (Renbase. h)
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
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332996"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a>CBaseRenderer. SourceThreadCanWait, metodo

Il `SourceThreadCanWait` metodo include o rilascia il thread di streaming.

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

Valore booleano che indica se mantenere il thread di streaming. Se **true**, il thread di streaming viene bloccato mentre il filtro attende il rendering degli esempi successivi. Se **false**, il thread di streaming viene rilasciato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

La chiamata al `SourceThreadCanWait` metodo con il valore **false** impone il ritorno del filtro da una chiamata [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) bloccata. Quando il filtro è in esecuzione, blocca le chiamate di **ricezione** fino al momento della presentazione del campione corrente. Quando il filtro è sospeso, blocca la **ricezione** delle chiamate a tempo indefinito. Questo comportamento regola il flusso di dati nel flusso. Quando il filtro viene arrestato o scaricato, tuttavia, non deve essere bloccato.

Il blocco è controllato dal metodo [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) , che attende due eventi: [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) e [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md). L' **evento \_ RenderEvent m** viene segnalato all'arrivo dell'ora di presentazione. L' **evento \_ ThreadSignal m** viene segnalato quando `SourceThreadCanWait` viene chiamato con il valore **false**. Se viene chiamato `SourceThreadCanWait` con il valore **true** , viene reimpostato l'evento.

I metodi [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chiamano `SourceThreadCanWait` con il valore **false** (che rilascia il thread di streaming). I metodi [**CBaseRenderer::P ause**](cbaserenderer-pause.md), [**CBaseRenderer:: Run**](cbaserenderer-run.md)e [**CBaseRenderer:: EndFlush**](cbaserenderer-endflush.md) chiamano `SourceThreadCanWait` con il valore **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




