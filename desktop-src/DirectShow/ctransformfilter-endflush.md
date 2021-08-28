---
description: "Metodo CTransformFilter.EndFlush: il metodo EndFlush termina un'operazione di scaricamento."
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Metodo CTransformFilter.EndFlush (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 593ce39dbba6ccf90838b4847bb0a548b67e4785bb21d3f299882e1eecdf8394
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083911"
---
# <a name="ctransformfilterendflush-method"></a>Metodo CTransformFilter.EndFlush

Il `EndFlush` metodo termina un'operazione di scaricamento.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT.**

## <a name="remarks"></a>Commenti

Al termine di un'operazione di scaricamento, il metodo [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) del pin di input chiama questo metodo. Questo metodo passa la `EndFlush` chiamata a valle.

Se la classe derivata usa un thread di lavoro per recapitare gli esempi, deve rimuovere tutti i dati in coda prima di inviare la `EndFlush` chiamata a valle. Per altre informazioni, vedere [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




