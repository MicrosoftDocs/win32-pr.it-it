---
description: Il metodo NotifyMediaType invia una notifica all'oggetto CDrawImage del tipo di supporto corrente.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Metodo CDrawImage.NotifyMediaType (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3df1f904bb5c2acfc328e8779da6135f901de9601cea6735de21b2e76aeea9c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656792"
---
# <a name="cdrawimagenotifymediatype-method"></a>Metodo CDrawImage.NotifyMediaType

Il `NotifyMediaType` metodo invia una notifica **all'oggetto CDrawImage** del tipo di supporto corrente.

## <a name="syntax"></a>Sintassi


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaType* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) o **NULL per** cancellare il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il filtro proprietario deve chiamare questo metodo ogni volta che cambia il tipo di supporto. In genere ciò si verifica quando il pin si connette per la prima volta e dopo una modifica del formato dinamico.

**L'oggetto CDrawImage** archivia il *puntatore pMediaType* nella **variabile membro m \_ pMediaType.** Pertanto, se il chiamante deve rilasciare l'oggetto **CMediaType,** deve aggiornare l'oggetto **CDrawImage** chiamando nuovamente questo metodo, con un nuovo puntatore o con un **valore NULL.** In caso contrario, può verificarsi un errore quando **l'oggetto CDrawImage** tenta di fare riferimento al puntatore precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




