---
description: Il metodo Wait si blocca fino a quando non viene segnalato l'evento o fino a quando non si verifica un timeout.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Metodo CAMEvent.Wait (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3875647cb93619e8326066bc9af7a6f99f79a0b0a2df58f668b1e365fd39102b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662512"
---
# <a name="cameventwait-method"></a>Metodo CAMEvent.Wait

Il `Wait` metodo si blocca fino a quando l'evento non viene segnalato o fino a quando non si verifica un timeout.

## <a name="syntax"></a>Sintassi


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwTimeout* 
</dt> <dd>

Valore di timeout facoltativo, rappresentato in millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se l'evento viene segnalato. In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

Per gli eventi di reimpostazione automatica, l'evento viene reimpostato su uno stato nonsignaled quando questo metodo viene restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




