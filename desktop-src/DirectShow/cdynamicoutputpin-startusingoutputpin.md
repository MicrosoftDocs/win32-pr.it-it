---
description: Il metodo StartUsingOutputPin ottiene l'accesso al pin per un'operazione di streaming.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Metodo CDynamicOutputPin.StartUsingOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4438c6670b0535711c453e64496ffd4b21263acab728e090024f9e1e01427969
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749451"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a>Metodo CDynamicOutputPin.StartUsingOutputPin

Il `StartUsingOutputPin` metodo ottiene l'accesso al pin per un'operazione di streaming.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                                               |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl>          | Errore imprevisto.<br/>                                      |
| <dl> <dt>**STATO VFW \_ E \_ \_ MODIFICATO**</dt> </dl> | Il filtro è stato arrestato o il pin ha iniziato lo scaricamento.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo prima di chiamare qualsiasi metodo che recapita dati al pin di input connesso o che modifica il tipo di supporto della connessione. Ad esempio, questa regola si applica ai metodi seguenti:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Chiamare quindi il [**metodo CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) per rilasciare l'accesso al pin.

Se il pin è bloccato, attende che il `StartUsingOutputPin` pin diventi sbloccato. Se il filtro si arresta mentre il metodo è in attesa, il metodo restituisce immediatamente VFW \_ E \_ STATE \_ CHANGED. Il pin mantiene un conteggio di quante volte è stato chiamato senza `StartUsingOutputPin` una chiamata corrispondente a **StopUsingOutputPin**. Se un altro thread tenta di bloccare il pin mentre il conteggio è diverso da zero, il pin imposta lo stato di blocco su "pending". Il pin viene bloccato al termine di tutte le operazioni di streaming, nella chiamata finale **a StopUsingOutputPin**.

Non contenere la [**sezione critica CDynamicOutputPin::m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) quando si chiama questo metodo. In caso contrario, se il pin è bloccato, non può mai essere sbloccato, causando un deadlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




