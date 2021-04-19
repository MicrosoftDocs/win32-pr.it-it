---
description: Il metodo Deliver recapita un campione multimediale al pin di input connesso.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: Metodo CBaseOutputPin. Deliver (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332069"
---
# <a name="cbaseoutputpindeliver-method"></a>Metodo CBaseOutputPin. Deliver

Il `Deliver` Metodo recapita un campione multimediale al pin di input connesso.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>              |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il PIN non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input. **Receive** può bloccare se il metodo [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) restituisce S \_ OK.

Rilasciare l'esempio dopo aver chiamato questo metodo. Il pin di input potrebbe mantenere un conteggio dei riferimenti nell'esempio, quindi non riutilizzare l'esempio. Chiamare sempre il metodo [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) per ottenere un nuovo campione.

Mantenere la sezione critica del filtro prima di chiamare questo metodo. In caso contrario, il PIN potrebbe essere disconnesso durante la chiamata al metodo. Se il filtro utilizza un thread di lavoro per recapitare gli esempi, mantenere la sezione critica quando il filtro è pronto per fornire un campione. In caso contrario, è possibile mantenere la sezione critica nel metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del filtro, in cui il filtro elabora gli esempi.

I thread di lavoro possono creare un potenziale deadlock. Quando il thread include la sezione critica, potrebbe attendere una modifica dello stato nel filtro. Allo stesso tempo, la modifica dello stato potrebbe essere in attesa del completamento del thread. Per evitare questo problema, il codice di modifica dello stato dovrebbe segnalare un evento che termina il thread, quindi attendere il completamento del segnale del thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




