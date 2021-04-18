---
description: Il metodo FindPinNumber Recupera il numero di un PIN specificato sul filtro.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: Metodo CSource. FindPinNumber (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324650"
---
# <a name="csourcefindpinnumber-method"></a>CSource. FindPinNumber, metodo

Il `FindPinNumber` metodo recupera il numero di un PIN specificato sul filtro.

## <a name="syntax"></a>Sintassi


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iPin* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero del PIN oppure 1 se il PIN non viene trovato in questo filtro. Il primo pin è numerato zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




