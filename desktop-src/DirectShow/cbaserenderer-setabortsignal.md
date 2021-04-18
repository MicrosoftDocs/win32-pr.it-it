---
description: Il metodo SetAbortSignal imposta un flag che indica se arrestare il rendering e rifiutare ulteriori esempi.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Metodo CBaseRenderer. SetAbortSignal (Renbase. h)
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
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329533"
---
# <a name="cbaserenderersetabortsignal-method"></a>CBaseRenderer. SetAbortSignal, metodo

Il `SetAbortSignal` metodo imposta un flag che indica se arrestare il rendering e rifiutare ulteriori esempi.

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

Valore booleano che indica se arrestare il rendering. Se **true**, il filtro non eseguirà il rendering di altri esempi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo imposta il flag [**CBaseRenderer:: m \_ bAbort**](cbaserenderer-m-babort.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




