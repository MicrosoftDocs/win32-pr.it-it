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
ms.openlocfilehash: 3bd7735726d7e7d21bc16e8a811947b954ffaac4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085159"
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

Se la classe derivata usa un thread di lavoro per recapitare i campioni, deve rimuovere tutti i dati in coda durante un'operazione di scaricamento. Questa operazione può essere eseguita nel `BeginFlush` metodo o nel metodo [**EndFlush.**](ctransformfilter-endflush.md) Si noti tuttavia che le chiamate a `BeginFlush` non sono sincronizzate con il thread di streaming. Se il metodo elimina i dati in coda, il filtro deve prestare attenzione a non elaborare altri dati tra le `BeginFlush` `BeginFlush` chiamate **endFlush** e . Per altre informazioni, vedere Flusso di dati [per sviluppatori di filtri.](data-flow-for-filter-developers.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




