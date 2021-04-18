---
description: Il metodo Duration recupera la durata del flusso.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: Metodo CPullPin. Duration (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecd05478f67934368aa6d1de84ae32a209ddcad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331173"
---
# <a name="cpullpinduration-method"></a>Metodo CPullPin. Duration

Il `Duration` metodo recupera la durata del flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ptDuration* 
</dt> <dd>

Puntatore a una variabile che riceve la durata, in byte, moltiplicata per 10 milioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

La durata è indeterminata fino a quando non viene chiamato il metodo [**CPullPin:: Connect**](cpullpin-connect.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




