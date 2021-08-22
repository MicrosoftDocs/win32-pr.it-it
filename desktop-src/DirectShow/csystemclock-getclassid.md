---
description: Il metodo GetClassID recupera l'identificatore di classe (CLSID) dell'oggetto. Questo metodo implementa il metodo IPersist::GetClassID.
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Metodo CSystemClock.GetClassID (Sysclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2afb141c3a79255504eb13dadb39cc0fb5094c19e0979db04c251f1e2fe75133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317191"
---
# <a name="csystemclockgetclassid-method"></a>Metodo CSystemClock.GetClassID

Il `GetClassID` metodo recupera l'identificatore di classe (CLSID) dell'oggetto . Questo metodo implementa il **metodo IPersist::GetClassID.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pClsID* 
</dt> <dd>

Puntatore a una variabile che riceve il valore CLSID \_ SystemClock.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o E \_ POINTER.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Classe CSystemClock<br/>                                                                                                                                                              |
| Intestazione<br/>  | <dl> <dt>Sysclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




