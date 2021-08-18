---
description: Il metodo MoveToHead suddivide l'elenco e inserisce la parte finale all'inizio di un altro elenco.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Metodo CBaseList.MoveToHead (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 18133107a3c8038780662bc39c8bd621c8b2c445a6e1e930f8fbfc015807e9fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928681"
---
# <a name="cbaselistmovetohead-method"></a>Metodo CBaseList.MoveToHead

Il `MoveToHead` metodo suddivide l'elenco e inserisce la parte finale all'inizio di un altro elenco.

## <a name="syntax"></a>Sintassi


```C++
BOOL MoveToHead(
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

Questo metodo suddivide l'elenco prima della posizione specificata dal *parametro pos.* La parte head rimane nell'elenco. La parte finale viene inserita nella parte superiore dell'altro elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




