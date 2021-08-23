---
description: Il metodo SetAbortSignal imposta un flag che indica se arrestare il rendering e rifiutare altri esempi.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Metodo CBaseRenderer.SetAbortSignal (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 819f279d20192ff82d9021e03780713f714682abf47aaf854b4568312572e8d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526535"
---
# <a name="cbaserenderersetabortsignal-method"></a>Metodo CBaseRenderer.SetAbortSignal

Il `SetAbortSignal` metodo imposta un flag che indica se arrestare il rendering e rifiutare altri esempi.

## <a name="syntax"></a>Sintassi


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bAbort* 
</dt> <dd>

Valore booleano che indica se arrestare il rendering. Se **TRUE,** il filtro non eseguirà il rendering di altri esempi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo imposta il flag [**\_ BAbort CBaseRenderer::m.**](cbaserenderer-m-babort.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




