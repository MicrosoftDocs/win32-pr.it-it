---
description: Il metodo ChangeMediaType modifica dinamicamente il tipo di supporto per la connessione.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Metodo CDynamicOutputPin. ChangeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333453"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a>CDynamicOutputPin. ChangeMediaType, metodo

Il `ChangeMediaType` metodo modifica dinamicamente il tipo di supporto per la connessione. La modifica può verificarsi durante l'esecuzione del grafico dei filtri. Una volta chiamato questo metodo, non è possibile recapitare gli esempi con il vecchio tipo di supporto. Il chiamante deve assicurarsi che non siano presenti esempi obsoleti in sospeso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                                                                                                                      |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                | Esito negativo. Probabilmente il filtro proprietario non ha chiamato [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).<br/> |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il PIN non è connesso.<br/>                                                                                                     |



 

## <a name="remarks"></a>Commenti

Chiamare il metodo [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) prima di chiamare questo metodo.

Questo metodo controlla prima di tutto se il pin di input downstream può accettare il nuovo formato senza riconnettersi. Viene eseguita una query sul pin di input per l'interfaccia [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) . Se il pin di input supporta **IPinConnection**, il metodo chiama il metodo [**IPinConnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) con il tipo di supporto proposto. Se il pin di input accetta il nuovo tipo di supporto, il metodo chiama il metodo [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) e rinegozia i requisiti dell'allocatore.

D'altra parte, se il pin downstream non supporta **IPinConnection** o se rifiuta il nuovo tipo di supporto, il metodo chiama il metodo [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) per eseguire una riconnessione dinamica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




