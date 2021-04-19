---
description: Il metodo SetSampleSize specifica una dimensione del campione fissa o specifica che i campioni hanno una dimensione variabile.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Metodo CMediaType. SetSampleSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0992afd0576c1039397e6ecaa2119a989283136e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328505"
---
# <a name="cmediatypesetsamplesize-method"></a>CMediaType. SetSampleSize, metodo

Il `SetSampleSize` metodo specifica una dimensione del campione fissa o specifica che i campioni hanno una dimensione variabile.

## <a name="syntax"></a>Sintassi


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SZ* 
</dt> <dd>

Dimensioni campione, in byte o zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il valore di *SZ* è zero, il tipo di supporto utilizza dimensioni campione variabili. In caso contrario, le dimensioni del campione vengono fissate a *SZ* bytes.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




