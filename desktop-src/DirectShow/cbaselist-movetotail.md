---
description: Il metodo MoveToTail suddivide l'elenco e aggiunge la parte head alla fine di un altro elenco.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Metodo CBaseList.MoveToTail (Wxlist.h)
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
ms.openlocfilehash: 8ae7ab918c8c4ef707b2754f8b1ba1f8f3e76265a6b8ac0b252e765de2aff1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016919"
---
# <a name="cbaselistmovetotail-method"></a>Metodo CBaseList.MoveToTail

Il `MoveToTail` metodo suddivide l'elenco e aggiunge la parte head alla parte finale di un altro elenco.

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

Indicatore di posizione che contrassegna la divisione nell'elenco.

</dd> <dt>

*Plist* 
</dt> <dd>

Puntatore a un altro elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo suddivide l'elenco dopo la posizione specificata dal *parametro pos.* La parte finale rimane nell'elenco. La parte head viene aggiunta alla parte finale dell'altro elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




