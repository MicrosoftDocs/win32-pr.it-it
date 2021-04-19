---
description: Il metodo CompleteConnect completa una connessione a un altro pin.
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Metodo CBasePin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9068bf63d3168a8c6d9e1bca2ef709f63e80a3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332652"
---
# <a name="cbasepincompleteconnect-method"></a>CBasePin. CompleteConnect, metodo

Il `CompleteConnect` metodo completa una connessione a un altro pin.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato su entrambi i pin alla fine del processo di connessione. Il pin di connessione lo chiama dall'interno del metodo [**CBasePin:: Connect**](cbasepin-connect.md) e il pin ricevente lo chiama dall'interno del metodo [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .

Nella classe di base, questo metodo restituisce semplicemente S \_ OK. Se una classe derivata presenta requisiti per il completamento di una connessione, deve eseguire l'override di questo metodo. Ad esempio, la classe [**CBaseOutputPin**](cbaseoutputpin.md) usa questo metodo per decidere l'allocatore di memoria.

Se questo metodo ha esito negativo, anche il tentativo di connessione complessiva ha esito negativo e il pin si disconnette dal pin di ricezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




