---
description: "Metodo CBaseOutputPin.DeliverEndFlush: il metodo DeliverEndFlush richiede al pin di input connesso di terminare un'operazione di scaricamento."
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Metodo CBaseOutputPin.DeliverEndFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f3fd5c1bc686ee5c0b4ff0cd1285a5114b93049
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096179"
---
# <a name="cbaseoutputpindeliverendflush-method"></a>Metodo CBaseOutputPin.DeliverEndFlush

Il `DeliverEndFlush` metodo richiede al pin di input connesso di terminare un'operazione di scaricamento.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>              |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il pin non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il [**metodo IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




