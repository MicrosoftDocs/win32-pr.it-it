---
description: Il metodo SetSampleSize specifica una dimensione fissa del campione o specifica che i campioni hanno una dimensione variabile.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Metodo CMediaType.SetSampleSize (Mtype.h)
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
ms.openlocfilehash: 5a29393ed4c9251d1e12895ad57a61f96bdc80bb05757ce72fc9485bb42a1047
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954410"
---
# <a name="cmediatypesetsamplesize-method"></a>Metodo CMediaType.SetSampleSize

Il `SetSampleSize` metodo specifica una dimensione fissa del campione o specifica che i campioni hanno una dimensione variabile.

## <a name="syntax"></a>Sintassi


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Sz* 
</dt> <dd>

Dimensioni del campione, in byte o zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il valore di *sz* è zero, il tipo di supporto usa dimensioni di esempio variabili. In caso contrario, le dimensioni del campione sono fisse *in sz* byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




