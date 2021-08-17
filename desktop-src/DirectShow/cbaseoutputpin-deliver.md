---
description: Il metodo Deliver recapita un campione di supporti al pin di input connesso.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: Metodo CBaseOutputPin.Deliver (Amfilter.h)
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
ms.openlocfilehash: f6786e9e763af26619b2dc4f6abc25aa2fd9527d7278e7da02f6042908e56bdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341381"
---
# <a name="cbaseoutputpindeliver-method"></a>Metodo CBaseOutputPin.Deliver

Il `Deliver` metodo recapita un campione di supporti al pin di input connesso.

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

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>              |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il pin non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il [**metodo IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input. **Receive** può bloccarsi se [**il metodo IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) restituisce S \_ OK.

Rilasciare l'esempio dopo aver chiamato questo metodo. Il pin di input potrebbe contenere un conteggio dei riferimenti nell'esempio, quindi non riutilizzare l'esempio. Chiamare sempre il [**metodo CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) per ottenere un nuovo esempio.

Mantenere la sezione critica del filtro prima di chiamare questo metodo. In caso contrario, il pin potrebbe essere disconnesso durante la chiamata al metodo. Se il filtro usa un thread di lavoro per distribuire gli esempi, mantenere la sezione critica quando il filtro è pronto per la consegna di un campione. In caso contrario, è possibile mantenere la sezione critica nel metodo [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del filtro, in cui il filtro elabora gli esempi.

I thread di lavoro possono creare un potenziale deadlock. Quando il thread contiene la sezione critica, potrebbe attendere una modifica dello stato nel filtro. Allo stesso tempo, la modifica dello stato potrebbe essere in attesa del completamento del thread. Per evitare questo problema, il codice di modifica dello stato deve segnalare un evento che termina il thread e quindi attendere che il thread segnali il completamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




