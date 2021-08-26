---
description: "Metodo CTransformFilter.BeginFlush: il metodo BeginFlush avvia un'operazione di scaricamento."
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Metodo CTransformFilter.BeginFlush (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be20231cf62148e3487aef405735f764bf5c02b7cbaadba3c140728b66bd5391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053861"
---
# <a name="ctransformfilterbeginflush-method"></a>Metodo CTransformFilter.BeginFlush

Il `BeginFlush` metodo avvia un'operazione di scaricamento.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT.**

## <a name="remarks"></a>Commenti

All'inizio di un'operazione di scaricamento, il metodo [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) del pin di input chiama questo metodo. Questo metodo passa la `BeginFlush` chiamata a valle.

Se la classe derivata usa un thread di lavoro per recapitare gli esempi, deve eliminare tutti i dati in coda durante un'operazione di scaricamento. Questa operazione può essere eseguita nel `BeginFlush` metodo o nel metodo [**EndFlush.**](ctransformfilter-endflush.md) Si noti tuttavia che le chiamate `BeginFlush` a non sono sincronizzate con il thread di streaming. Se il metodo rimuove i dati in coda, il filtro deve prestare attenzione a non elaborare altri dati tra le chiamate `BeginFlush` `BeginFlush` **endFlush e** . Per altre informazioni, vedere [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




