---
description: Il metodo SetType specifica il tipo principale.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Metodo CMediaType.SetType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37d035202d4674da11016620dc3c3d1ba3ab99f6ca514b9581f7dd2e4d9592d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954390"
---
# <a name="cmediatypesettype-method"></a>Metodo CMediaType.SetType

Il `SetType` metodo specifica il tipo principale.

## <a name="syntax"></a>Sintassi


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ptype* 
</dt> <dd>

Puntatore a **un GUID** che specifica il tipo principale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




