---
description: Il Metodo BeginFlush avvia un'operazione di svuotamento.
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Metodo CTransformFilter. BeginFlush (Transfrm. h)
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
ms.openlocfilehash: bd9a4bf1543f4899d4c879e9d1a9d9cf1035b765
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325735"
---
# <a name="ctransformfilterbeginflush-method"></a>CTransformFilter. BeginFlush, metodo

Il `BeginFlush` metodo inizia un'operazione di svuotamento.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT** .

## <a name="remarks"></a>Commenti

All'inizio di un'operazione di scaricamento, il metodo [**CTransformInputPin:: BeginFlush**](ctransforminputpin-beginflush.md) del PIN di input chiama questo metodo. Questo metodo passa la `BeginFlush` chiamata downstream.

Se la classe derivata utilizza un thread di lavoro per recapitare gli esempi, sarà necessario rimuovere tutti i dati in coda durante un'operazione di scaricamento. Questa operazione può essere eseguita nel `BeginFlush` metodo o nel metodo [**EndFlush**](ctransformfilter-endflush.md) . Si noti tuttavia che le chiamate a `BeginFlush` non vengono sincronizzate con il thread di streaming. Se il `BeginFlush` metodo elimina i dati in coda, il filtro deve prestare attenzione a non elaborare altri dati tra le `BeginFlush` chiamate a e **EndFlush** . Per ulteriori informazioni, vedere [flusso di dati per gli sviluppatori di filtri](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




