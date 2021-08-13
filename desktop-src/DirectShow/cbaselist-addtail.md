---
description: Il metodo AddTail aggiunge un altro elenco alla fine di questo elenco.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Metodo CBaseList.AddTail (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5663a69d803def2b37f9a1ba677966a5b26a8bfc6f7b6eb1eb98eef85bcd961d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659154"
---
# <a name="cbaselistaddtail-method"></a>Metodo CBaseList.AddTail

Il `AddTail` metodo aggiunge un altro elenco alla fine di questo elenco.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Plist* 
</dt> <dd>

Puntatore all'elenco da accodare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Se il metodo ha esito negativo, è possibile che alcuni elementi siano stati aggiunti all'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




