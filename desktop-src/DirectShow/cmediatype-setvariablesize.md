---
description: Il metodo SetVariableSize specifica che gli esempi non hanno dimensioni fisse.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Metodo CMediaType.SetVariableSize (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 118167d0068c058c925e5b63e2e951ff860917c40a5c3533daf9f02e6927649a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073965"
---
# <a name="cmediatypesetvariablesize-method"></a>Metodo CMediaType.SetVariableSize

Il `SetVariableSize` metodo specifica che gli esempi non hanno dimensioni fisse.

## <a name="syntax"></a>Sintassi


```C++
void SetVariableSize();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo imposta il **membro bFixedSizeSamples** su **FALSE.** Le chiamate successive al [**metodo CMediaType::GetSampleSize**](cmediatype-getsamplesize.md) restituiscono zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




