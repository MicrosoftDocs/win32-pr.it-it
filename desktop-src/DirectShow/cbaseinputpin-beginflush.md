---
description: Il metodo CBaseInputPin avvia un'operazione di scaricamento. Questo metodo implementa il metodo IPin::BeginFlush.
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Metodo CBaseInputPin.BeginFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b9e5e4e97a3a010523f61cc9efedf224d8dfc7fa373c9514b6d38dc0105d2d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103211"
---
# <a name="cbaseinputpinbeginflush-method"></a>Metodo CBaseInputPin.BeginFlush

Il `CBaseInputPin` metodo avvia un'operazione di scaricamento. Questo metodo implementa il [**metodo IPin::BeginFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo imposta il flag [**\_ BFlushing CBaseInputPin::m**](cbaseinputpin-m-bflushing.md) su **TRUE,** in modo che il metodo [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) rifiuti altri esempi.

La classe derivata deve eseguire l'override di questo metodo ed eseguire la procedura seguente:

1.  Chiamare il [**metodo IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sui pin di input downstream. Se il pin non ha ancora fornito campioni di supporti a valle, è possibile ignorare questo passaggio. Se i pin di output derivano dalla [**classe CBaseOutputPin,**](cbaseoutputpin.md) è possibile chiamare il metodo [**CBaseOutputPin::D eliverBeginFlush.**](cbaseoutputpin-deliverbeginflush.md)
2.  Chiamare il metodo della classe base.
3.  Iniziare a rimuovere i dati in coda.
4.  Restituisce da qualsiasi chiamata bloccata al **metodo Receive.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




