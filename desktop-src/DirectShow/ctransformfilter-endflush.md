---
description: Il metodo EndFlush termina un'operazione di svuotamento.
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Metodo CTransformFilter. EndFlush (Transfrm. h)
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
ms.openlocfilehash: 348675f1369ec9b0deb5415ad14a864a8befef73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328340"
---
# <a name="ctransformfilterendflush-method"></a>CTransformFilter. EndFlush, metodo

Il `EndFlush` metodo termina un'operazione di svuotamento.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT** .

## <a name="remarks"></a>Commenti

Al termine di un'operazione di scaricamento, il metodo [**CTransformInputPin:: EndFlush**](ctransforminputpin-endflush.md) del PIN di input chiama questo metodo. Questo metodo passa la `EndFlush` chiamata downstream.

Se la classe derivata utilizza un thread di lavoro per recapitare gli esempi, è necessario rimuovere tutti i dati in coda prima di inviare la `EndFlush` chiamata downstream. Per ulteriori informazioni, vedere [flusso di dati per gli sviluppatori di filtri](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




