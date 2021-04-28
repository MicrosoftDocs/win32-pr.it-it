---
description: 'Metodo CBasePin.CompleteConnect: il metodo CompleteConnect completa una connessione a un altro pin.'
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Metodo CBasePin.CompleteConnect (Amfilter.h)
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
ms.openlocfilehash: fee207d7a17f12cc81036fbd4f82ec49a99f4a31
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096039"
---
# <a name="cbasepincompleteconnect-method"></a>Metodo CBasePin.CompleteConnect

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

Puntatore all'interfaccia [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato su entrambi i pin alla fine del processo di connessione. Il pin di connessione lo chiama dall'interno del metodo [**CBasePin::Connect**](cbasepin-connect.md) e il pin ricevente lo chiama dall'interno del metodo [**CBasePin::ReceiveConnection.**](cbasepin-receiveconnection.md)

Nella classe di base questo metodo restituisce semplicemente S \_ OK. Se una classe derivata ha requisiti per il completamento di una connessione, deve eseguire l'override di questo metodo. Ad esempio, la [**classe CBaseOutputPin**](cbaseoutputpin.md) usa questo metodo per decidere l'allocatore di memoria.

Se questo metodo ha esito negativo, anche il tentativo di connessione complessivo ha esito negativo e il pin si disconnette dal pin ricevente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




