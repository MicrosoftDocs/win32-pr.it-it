---
description: Il metodo StartUsingOutputPin Ottiene l'accesso al pin per un'operazione di flusso.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Metodo CDynamicOutputPin. StartUsingOutputPin (Amfilter. h)
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
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332340"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a>CDynamicOutputPin. StartUsingOutputPin, metodo

Il `StartUsingOutputPin` metodo ottiene l'accesso al pin per un'operazione di flusso.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                                               |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>          | Errore imprevisto.<br/>                                      |
| <dl> <dt>**stato di VFW \_ E \_ \_ modificato**</dt> </dl> | Il filtro è stato arrestato o è iniziato lo scaricamento del PIN.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo prima di chiamare i metodi che recapitano i dati al pin di input connesso o che modificano il tipo di supporto della connessione. Questa regola, ad esempio, si applica ai metodi seguenti:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Successivamente, chiamare il metodo [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) per rilasciare l'accesso al pin.

Se il PIN è bloccato, `StartUsingOutputPin` attende che il PIN venga sbloccato. Se il filtro si interrompe mentre il metodo è in attesa, il metodo restituisce \_ immediatamente \_ lo stato VFW E \_ modificato. Il pin mantiene un conteggio del numero di volte `StartUsingOutputPin` in cui è stato chiamato senza una chiamata corrispondente a **StopUsingOutputPin**. Se un altro thread tenta di bloccare il pin mentre questo conteggio è diverso da zero, il pin imposta lo stato di blocco su "Pending". Il PIN viene bloccato una volta completate tutte le operazioni di streaming, nella chiamata finale a **StopUsingOutputPin**.

Quando si chiama questo metodo, non è necessario mantenere la sezione [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical. In caso contrario, se il PIN è bloccato, non può mai essere sbloccato, causando un deadlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




