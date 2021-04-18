---
description: Il metodo EndOfStream viene chiamato dopo che l'oggetto recapita l'ultimo campione. La classe derivata deve implementare questo metodo.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Metodo CPullPin. EndOfStream (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331171"
---
# <a name="cpullpinendofstream-method"></a>CPullPin. EndOfStream, metodo

Il `EndOfStream` metodo viene chiamato dopo che l'oggetto recapita l'ultimo campione. La classe derivata deve implementare questo metodo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Utilizzare questo metodo per chiamare [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) in ogni pin di input downstream che riceve i dati da questo oggetto. Se i pin di output del filtro derivano da [**CBaseOutputPin**](cbaseoutputpin.md), chiamare il metodo [**CBaseOutputPin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




