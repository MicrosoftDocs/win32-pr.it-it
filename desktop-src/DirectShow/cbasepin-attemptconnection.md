---
description: Il metodo AttemptConnection si connette a un altro pin usando un tipo di supporto specificato.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Metodo CBasePin.AttemptConnection (Amfilter.h)
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
ms.openlocfilehash: e70683d5307b81db14d23fec2c163b085cccaf64b7926eb41efdb5dfe9ac7611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872397"
---
# <a name="cbasepinattemptconnection-method"></a>Metodo CBasePin.AttemptConnection

Il `AttemptConnection` metodo si connette a un altro pin usando un tipo di supporto specificato.

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

Puntatore all'interfaccia [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di ricezione.

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili sono quelli riportati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Operazione completata.<br/>                          |
| <dl> <dt>**TIPO VFW \_ E \_ NON \_ \_ ACCETTATO**</dt> </dl> | Il tipo di supporto non è accettabile.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo tenta di connettere i due pin a un tipo di supporto specifico. Se il tipo non è accettabile, il metodo ha esito negativo senza provare altri tipi di supporti.

Se il tipo di supporto è accettabile, questo metodo chiama il metodo [**IPin::ReceiveConnection del**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) pin ricevente. Chiama quindi il [**metodo CBasePin::CompleteConnect**](cbasepin-completeconnect.md) per completare la connessione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




