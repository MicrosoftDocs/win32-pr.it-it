---
description: "Il metodo GetClassID recupera l'identificatore di classe (CLSID) dell'oggetto. Questo metodo implementa il metodo IPersist:: GetClassID."
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Metodo CSystemClock. GetClassID (Sysclock. h)
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
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333711"
---
# <a name="csystemclockgetclassid-method"></a>CSystemClock. GetClassID, metodo

Il `GetClassID` metodo recupera l'identificatore di classe (CLSID) dell'oggetto. Questo metodo implementa il metodo **IPersist:: GetClassID** .

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

Restituisce un \_ puntatore S OK o e \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Classe CSystemClock<br/>                                                                                                                                                              |
| Intestazione<br/>  | <dl> <dt>Sysclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




