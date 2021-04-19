---
description: 'Il metodo Receive riceve il campione multimediale successivo nel flusso. Questo metodo implementa il metodo IMemInputPin:: Receive.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Metodo CTransformInputPin. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59b087c4b783305b831871a030d1006d576e7d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333311"
---
# <a name="ctransforminputpinreceive-method"></a>Metodo CTransformInputPin. Receive

Il `Receive` metodo riceve il campione multimediale successivo nel flusso. Questo metodo implementa il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Receive(
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

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Il PIN sta attualmente scaricando; esempio rifiutato.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                                        |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) del PIN, che controlla lo stato del flusso del PIN e controlla la presenza di modifiche al formato nel tipo di supporto. Chiama quindi il metodo [**CTransformFilter:: Receive**](ctransformfilter-receive.md) del filtro, che elabora l'esempio e lo recapita a valle.

Se il filtro deve accedere all'esempio dopo la restituzione di questo metodo, deve conservare un conteggio dei riferimenti chiamando il metodo **IUnknown:: AddRef** nell'esempio. Alcuni filtri decodificatori, ad esempio, richiedono l'esempio corrente per decodificare l'esempio successivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




