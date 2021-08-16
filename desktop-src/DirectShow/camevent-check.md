---
description: Il metodo Check controlla se l'evento è impostato, senza bloccarsi.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: Metodo CAMEvent.Check (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a961d7df45ddac7ade5e39f91c1aed56609ce2d2eeb8e7423799c9a4903884e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955540"
---
# <a name="cameventcheck-method"></a>Metodo CAMEvent.Check

Il `Check` metodo verifica se l'evento è impostato, senza bloccarsi.

## <a name="syntax"></a>Sintassi


```C++
BOOL Check();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

Restituisce **TRUE se** l'evento è impostato oppure FALSE in caso **contrario.** Questo metodo chiama il [**metodo CAMEvent::Wait**](camevent-wait.md) con un timeout pari a zero. Se l'oggetto è un evento di reimpostazione automatica, questo metodo reimposta l'evento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




