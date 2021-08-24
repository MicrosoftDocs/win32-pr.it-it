---
description: 'Costruttore CAMEvent.CAMEvent : metodo costruttore.'
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Costruttore CAMEvent.CAMEvent (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0fd5895ada4bbbd1bf4ad24710f7782fdfb9c932f2d9446ff0d992335437da9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540556"
---
# <a name="cameventcamevent-constructor"></a>Costruttore CAMEvent.CAMEvent

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fManualReset* 
</dt> <dd>

Valore booleano che specifica se l'oggetto è un evento di reimpostazione manuale o un evento di reimpostazione automatica. Se **TRUE,** l'oggetto è un evento di reimpostazione manuale. In caso contrario, si tratta di un evento di reimpostazione automatica.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.** Se il costruttore ha esito negativo, questo parametro riceve un codice di errore. In questo caso, l'oggetto non è in uno stato valido.

Per compatibilità con le versioni precedenti di strmbase.lib, il valore predefinito di questo parametro è **NULL.** È tuttavia preferibile passare un valore non **NULL,** in modo che il chiamante possa controllare lo stato dell'oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'evento inizia in uno stato non firmato.

Con un evento di reimpostazione automatica, il [**metodo CAMEvent::Wait**](camevent-wait.md) reimposta l'evento su nonsignaled quando il metodo viene restituito. Con un evento di reimpostazione manuale, l'evento rimane segnalato fino a quando non si chiama il [**metodo CAMEvent::Reset.**](camevent-reset.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




