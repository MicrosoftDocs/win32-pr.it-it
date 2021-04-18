---
description: Il metodo di inattività determina se l'oggetto è in attesa di dati.
ms.assetid: be1b5633-f9e9-497e-8b6f-5634eae91273
title: Metodo COutputQueue. IsValid (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsIdle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bf8b42189e356659e74398eaa3eefeb5f771a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330667"
---
# <a name="coutputqueueisidle-method"></a>Metodo COutputQueue. IsValid

Il `IsIdle` metodo determina se l'oggetto è in attesa di dati.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsIdle();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il thread è in attesa e la matrice di esempio è vuota. In caso contrario, restituisce **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




