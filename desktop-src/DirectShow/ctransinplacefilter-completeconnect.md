---
description: 'Metodo CTransInPlaceFilter.CompleteConnect: il metodo CompleteConnect completa una connessione pin.'
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Metodo CTransInPlaceFilter.CompleteConnect (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9cc0bc839a4e35c4ce896acdf50da10f0c2bb0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084789"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a>Metodo CTransInPlaceFilter.CompleteConnect

Il `CompleteConnect` metodo completa una connessione pin.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*direction* 
</dt> <dd>

Membro del [**tipo enumerato PIN \_ DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) che specifica quale pin nel filtro sta effettuando la connessione.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin in questo tentativo di connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                             |
| <dl> <dt>**VFW \_ E NON IN \_ \_ \_ GRAPH**</dt> </dl> | Il filtro non è in un grafico filtri.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CTransformFilter::CompleteConnect.**](ctransformfilter-completeconnect.md)

Il comportamento del filtro dipende dall'ordine delle connessioni pin:

-   Se il pin di input è connesso per primo, la connessione usa un allocatore temporaneo. Quando il pin di output è connesso, il filtro riconnette il pin di input. Riconnettendo il pin di input, il filtro upstream rinegozia l'allocatore. A questo punto, il pin di input propone un allocatore dal filtro downstream. Per altre informazioni, vedere [**CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).
-   Se il pin di output è connesso per primo, il pin di output non seleziona un allocatore. Quando il pin di input è connesso, negozia un allocatore per entrambe le connessioni. Se i tipi di supporti di input e output non sono uguali, il filtro riconnette il pin di output usando il tipo di input.

Il filtro esegue tutte le riconnessioni dei pin chiamando il [**metodo CBaseFilter::ReconnectPin.**](cbasefilter-reconnectpin.md) Il **metodo ReconnectPin,** a sua volta, chiama il metodo [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) nel gestore del grafico dei filtri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




