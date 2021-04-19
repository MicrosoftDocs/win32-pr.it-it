---
description: Il metodo AttemptConnection si connette a un altro PIN usando un tipo di supporto specificato.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Metodo CBasePin. AttemptConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f80d81b5f105f528292a23f8b58257066b425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332772"
---
# <a name="cbasepinattemptconnection-method"></a>CBasePin. AttemptConnection, metodo

Il `AttemptConnection` metodo si connette a un altro PIN utilizzando un tipo di supporto specificato.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di ricezione.

</dd> <dt>

*PMT* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Esito positivo.<br/>                          |
| <dl> <dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt> </dl> | Il tipo di supporto non è accettabile.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo tenta di connettere i due pin con un tipo di supporto specifico. Se il tipo non è accettabile, il metodo ha esito negativo senza provare altri tipi di supporto.

Se il tipo di supporto è accettabile, questo metodo chiama il metodo [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del PIN di ricezione. Chiama quindi il metodo [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) per completare la connessione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




