---
description: Il metodo GetClassID recupera l'identificatore di classe. Questo metodo implementa il metodo IPersist::GetClassID.
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Metodo CBaseMediaFilter.GetClassID (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a733c3ef6e7098a556facb5258f567bdae0179ba4da133076b9bbc961cf0b26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502921"
---
# <a name="cbasemediafiltergetclassid-method"></a>Metodo CBaseMediaFilter.GetClassID

Il `GetClassID` metodo recupera l'identificatore di classe. Questo metodo implementa il **metodo IPersist::GetClassID.**

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

Puntatore a una variabile che riceve l'identificatore di classe.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o E \_ POINTER.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




