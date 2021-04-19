---
description: Il metodo CheckConnect determina se una connessione pin è adatta.
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Metodo CBasePin. CheckConnect (Amfilter. h)
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
ms.openlocfilehash: 24d5c221da417fd1fc2b3f9f140536f825b2f9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332769"
---
# <a name="cbasepincheckconnect-method"></a>CBasePin. CheckConnect, metodo

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

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                               | Descrizione                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                      | Esito positivo.<br/>                           |
| <dl> <dt>**\_direzione VFW E \_ non valida \_**</dt> </dl> | Le direzioni del PIN non sono compatibili.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato su entrambi i pin all'avvio del processo di connessione. Il pin di connessione lo chiama dall'interno del metodo [**CBasePin:: Connect**](cbasepin-connect.md) e il pin ricevente lo chiama dall'interno del metodo [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .

Utilizzare questo metodo per determinare se il PIN specificato dal parametro *pPin* è adatto a una connessione. La classe base restituisce un errore se entrambi i pin hanno la stessa direzione (sia di input sia di output). Le classi derivate possono eseguire l'override di questo metodo per verificare altre funzionalità nel pin. Ad esempio, la classe [**CBaseOutputPin**](cbaseoutputpin.md) esegue una query sul pin di input per la relativa interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

Se questo metodo ha esito negativo, la connessione ha esito negativo e il pin chiama il metodo [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) . Usare **BreakConnect** per liberare le risorse ottenute in `CheckConnect` . Se, ad esempio, `CheckConnect` chiama il metodo **QueryInterface** , **BreakConnect** deve rilasciare l'interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




