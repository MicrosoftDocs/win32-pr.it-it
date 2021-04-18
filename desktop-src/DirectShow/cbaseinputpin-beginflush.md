---
description: "Il metodo CBaseInputPin avvia un'operazione di svuotamento. Questo metodo implementa il metodo IPin:: BeginFlush."
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Metodo CBaseInputPin. BeginFlush (Amfilter. h)
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
ms.openlocfilehash: 93c0f687daf65e91443f4f59896d641b9b0cfd43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327959"
---
# <a name="cbaseinputpinbeginflush-method"></a>CBaseInputPin. BeginFlush, metodo

Il `CBaseInputPin` metodo inizia un'operazione di svuotamento. Questo metodo implementa il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo imposta il flag [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) su **true**, che fa in modo che il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) rifiuti altri esempi.

La classe derivata deve eseguire l'override di questo metodo ed eseguire i passaggi seguenti:

1.  Chiamare il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sui pin di input downstream. Se il PIN non ha ancora recapitato alcun campione multimediale a valle, è possibile ignorare questo passaggio. Se i pin di output derivano dalla classe [**CBaseOutputPin**](cbaseoutputpin.md) , è possibile chiamare il metodo [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .
2.  Chiamare il metodo della classe base.
3.  Inizia l'eliminazione dei dati in coda.
4.  Restituisce da qualsiasi chiamata bloccata al metodo **Receive** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




