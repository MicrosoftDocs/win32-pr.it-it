---
description: Il metodo set segnala l'evento.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: Metodo CAMEvent. set (Wxutil. h)
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
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331335"
---
# <a name="cameventset-method"></a>Metodo CAMEvent. set

Il `Set` metodo segnala l'evento.

## <a name="syntax"></a>Sintassi


```C++
void Set();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il comportamento varia a seconda che l'oggetto sia un evento di reimpostazione automatica o un evento di reimpostazione manuale:

-   **Reimpostazione automatica**: se un thread è in attesa di questo evento, viene rilasciato un thread e l'evento viene reimpostato. Se nessun thread è in attesa di questo evento, l'evento rimane segnalato.
-   **Ripristino manuale**: tutti i thread in attesa di questo evento vengono rilasciati. L'evento rimane segnalato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




