---
description: Il metodo OnError viene chiamato se si verifica un errore durante lo streaming. La classe derivata deve implementare questo metodo.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: Metodo CPullPin.OnError (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0d9873e2d327c424b2cd1ffda7112676f53399a63d2a9ca92dca1f50a02f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908881"
---
# <a name="cpullpinonerror-method"></a>Metodo CPullPin.OnError

Il `OnError` metodo viene chiamato se si verifica un errore durante lo streaming. La classe derivata deve implementare questo metodo.

## <a name="syntax"></a>Sintassi


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*h* 
</dt> <dd>

Specifica il valore **HRESULT** restituito dal metodo che ha avuto esito negativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

L'oggetto chiama questo metodo ogni volta che si verifica un errore che interrompe il thread di pull dei dati. Il filtro può usare questo metodo per eseguire il ripristino dagli errori di streaming normalmente. Nella maggior parte dei casi, l'errore viene restituito dal filtro upstream, quindi il filtro upstream è responsabile della segnalazione a Filter Graph Manager. Se l'errore si verifica all'interno del [**metodo CPullPin::Receive,**](cpullpin-receive.md) il filtro deve inviare un [**evento EC \_ ERRORABORT.**](ec-errorabort.md) Vedere [**IMediaEventSink::Notify.**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




