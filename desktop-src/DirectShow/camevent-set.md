---
description: Il metodo Set segnala l'evento .
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: Metodo CAMEvent.Set (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 84059a66a77744b7ea570473474f6b773beae8005b7c4a68e73e59c76829f13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794281"
---
# <a name="cameventset-method"></a>Metodo CAMEvent.Set

Il `Set` metodo segnala l'evento .

## <a name="syntax"></a>Sintassi


```C++
void Set();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il comportamento dipende dal fatto che l'oggetto sia un evento di reimpostazione automatica o un evento di reimpostazione manuale:

-   **Reimpostazione automatica:** se un thread è in attesa di questo evento, viene rilasciato un thread e l'evento viene reimpostato. Se nessun thread è in attesa di questo evento, l'evento rimane segnalato.
-   **Reimpostazione manuale:** vengono rilasciati tutti i thread in attesa di questo evento. L'evento rimane segnalato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




