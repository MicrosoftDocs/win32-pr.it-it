---
description: La funzione IsEqualObject controlla se due interfacce si trova nello stesso oggetto.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Funzione IsEqualObject (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e385cf887dceddcdc470b908d46f59405f573ab47837b26f8453ce6154eb0d72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817453"
---
# <a name="isequalobject-function"></a>Funzione IsEqualObject

La `IsEqualObject` funzione verifica se due interfacce sono nello stesso oggetto.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFirst* 
</dt> <dd>

Puntatore a un'interfaccia.

</dd> <dt>

*pSecond* 
</dt> <dd>

Puntatore all'altra interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se le interfacce sono entrambe nello stesso oggetto oppure **FALSE in caso contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper varie](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




