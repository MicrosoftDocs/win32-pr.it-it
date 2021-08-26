---
description: 'Metodo CBasePin.CheckConnect: il metodo CheckConnect determina se una connessione pin è adatta.'
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Metodo CBasePin.CheckConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0a91e936f13c76ed4d99d7c5048820777afa47c9a52c260bb7f34acb702cb777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916851"
---
# <a name="cbasepincheckconnect-method"></a>Metodo CBasePin.CheckConnect

Il `CheckConnect` metodo determina se una connessione pin è adatta.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin* 
</dt> <dd>

Puntatore all'interfaccia [**IPin dell'altro**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                               | Descrizione                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Operazione completata.<br/>                           |
| <dl> <dt>**DIREZIONE VFW \_ E \_ NON \_ VALIDA**</dt> </dl> | Le direzioni del pin non sono compatibili.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato su entrambi i pin all'inizio del processo di connessione. Il pin di connessione lo chiama dall'interno del metodo [**CBasePin::Connessione e**](cbasepin-connect.md) il pin ricevente lo chiama dall'interno del metodo [**CBasePin::ReceiveConnection.**](cbasepin-receiveconnection.md)

Usare questo metodo per determinare se il pin specificato dal *parametro pPin* è adatto per una connessione. La classe base restituisce un errore se entrambi i pin hanno la stessa direzione (input o entrambi gli output). Le classi derivate possono eseguire l'override di questo metodo per verificare altre funzionalità nel pin. Ad esempio, la [**classe CBaseOutputPin**](cbaseoutputpin.md) esegue una query sul pin di input per l'interfaccia [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)

Se questo metodo ha esito negativo, la connessione ha esito negativo e il pin chiama il metodo [**CBasePin::BreakConnect.**](cbasepin-breakconnect.md) Usare **BreakConnect** per liberare tutte le risorse ottenute in `CheckConnect` . Ad esempio, se `CheckConnect` chiama il **metodo QueryInterface,** **BreakConnect** deve rilasciare l'interfaccia .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




