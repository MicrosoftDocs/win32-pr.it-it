---
description: Il metodo MoveToTail suddivide l'elenco e aggiunge la parte Head alla parte finale di un altro elenco.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Metodo CBaseList. MoveToTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c28e1051c08884e70e56b25b0fb2707ccd55ed1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328649"
---
# <a name="cbaselistmovetotail-method"></a>CBaseList. MoveToTail, metodo

Il `MoveToTail` metodo suddivide l'elenco e aggiunge la parte Head alla parte finale di un altro elenco.

## <a name="syntax"></a>Sintassi


```C++
BOOL MoveToTail(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Indicatore di posizione che contrassegna la suddivisione nell'elenco.

</dd> <dt>

*pList* 
</dt> <dd>

Puntatore a un altro elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo suddivide l'elenco dopo la posizione specificata dal parametro *pos* . La parte finale rimane nell'elenco. La parte Head viene aggiunta alla parte finale dell'altro elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




