---
description: 'Il metodo ReceiveCanBlock determina se le chiamate al metodo IMemInputPin:: Receive potrebbero bloccarsi. Questo metodo implementa il metodo IMemInputPin:: ReceiveCanBlock.'
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Metodo CBaseInputPin. ReceiveCanBlock (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c80d6c8f834b45381b89e80d2e0acc392bf25a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333214"
---
# <a name="cbaseinputpinreceivecanblock-method"></a>CBaseInputPin. ReceiveCanBlock, metodo

Il `ReceiveCanBlock` metodo determina se le chiamate al metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) potrebbero bloccarsi. Questo metodo implementa il metodo [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Il valore possibile include quelli elencati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Il PIN non si bloccherà in una chiamata a **Receive**.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Il PIN potrebbe bloccarsi in una chiamata a **Receive**.<br/>    |



 

## <a name="remarks"></a>Commenti

Restituisce \_ false se è garantita la mancata blocco delle chiamate al metodo **Receive** . In caso contrario, restituire S \_ OK o un codice di errore. Se il metodo **Receive** chiama **Receive** su un pin downstream, il pin downstream potrebbe bloccarsi; `ReceiveCanBlock` è necessario tenere conto di questo fattore.

Un filtro upstream può utilizzare questo metodo per determinare la strategia di Threading. Se il metodo **Receive** potrebbe bloccarsi, il filtro upstream potrebbe decidere di usare un thread di lavoro che memorizza nel buffer i dati. Per un'implementazione di questa strategia, vedere la classe [**COutputQueue**](coutputqueue.md) .

Nella classe di base, questo metodo restituisce S \_ OK quando si verifica una delle condizioni seguenti:

-   Il filtro non ha pin di output.
-   Un pin di input connesso a questo filtro segnala che potrebbe bloccarsi.
-   Un pin di input connesso a questo filtro non supporta l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




