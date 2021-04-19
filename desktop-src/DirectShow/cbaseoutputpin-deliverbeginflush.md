---
description: Il metodo DeliverBeginFlush richiede al pin di input connesso di iniziare un'operazione di svuotamento.
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Metodo CBaseOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dad764ceaa6cc57c8c5b7ee288859926b6c63f02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332258"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a>CBaseOutputPin. DeliverBeginFlush, metodo

Il `DeliverBeginFlush` metodo richiede al pin di input connesso di iniziare un'operazione di svuotamento.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>              |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il PIN non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




