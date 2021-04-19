---
description: Il metodo CompleteConnect completa una connessione pin.
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Metodo CTransInPlaceFilter. CompleteConnect (Transip. h)
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
ms.openlocfilehash: 4fdc9d1d5567cda2e4b0fd4a351136405493ef61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332979"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a>CTransInPlaceFilter. CompleteConnect, metodo

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

Membro del tipo enumerato di [**\_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) , che specifica quale pin del filtro sta effettuando la connessione.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin in questo tentativo di connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT**. I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                             |
| <dl> <dt>**VFW \_ E \_ non \_ in \_ Graph**</dt> </dl> | Il filtro non è in un grafico dei filtri.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) .

Il comportamento del filtro dipende dall'ordine delle connessioni pin:

-   Se il pin di input è connesso per primo, la connessione usa un allocatore temporaneo. Quando il pin di output è connesso, il filtro riconnette il pin di input. Riconnettendo il pin di input, il filtro upstream rinegozierà l'allocatore. A questo punto, il pin di input propone un allocatore dal filtro downstream. Per ulteriori informazioni, vedere [**CTransInPlaceInputPin:: Getallocator**](ctransinplaceinputpin-getallocator.md).
-   Se il pin di output è connesso per primo, il pin di output non seleziona un allocatore. Quando il pin di input è connesso, negozia un allocatore per entrambe le connessioni. Se i tipi di supporto di input e di output non sono uguali, il filtro riconnette il pin di output usando il tipo di input.

Il filtro esegue tutte le riconnessioni pin chiamando il metodo [**CBaseFilter:: ReconnectPin**](cbasefilter-reconnectpin.md) . Il metodo **ReconnectPin** , a sua volta, chiama il metodo [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) in gestione grafico dei filtri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




