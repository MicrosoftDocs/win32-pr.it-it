---
description: Il metodo CheckTime determina se è scaduta un'ora specificata.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Metodo CCmdQueue.CheckTime (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 826b59d12c135e9c86ce923f37e1558dca4f13efafb4880aecab1384829a484a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910431"
---
# <a name="ccmdqueuechecktime-method"></a>Metodo CCmdQueue.CheckTime

Il `CheckTime` metodo determina se è scaduta un'ora specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*time* 
</dt> <dd>

Ora di controllo.

</dd> <dt>

*bStream* 
</dt> <dd>

**TRUE** se il *parametro time* è un valore di tempo di flusso; **FALSE** se *l'ora* è un valore dell'ora di presentazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se l'ora specificata non è ancora passata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




