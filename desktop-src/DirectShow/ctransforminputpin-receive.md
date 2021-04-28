---
description: "Metodo CTransformInputPin.Receive: il metodo Receive riceve l'esempio multimediale successivo nel flusso. Questo metodo implementa il metodo IMemInputPin::Receive."
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Metodo CTransformInputPin.Receive (Transfrm.h)
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
ms.openlocfilehash: 2a6a3c5dd4c9f11d45e1b719498d515a536e5ef8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084969"
---
# <a name="ctransforminputpinreceive-method"></a>Metodo CTransformInputPin.Receive

Il `Receive` metodo riceve l'esempio multimediale successivo nel flusso. Questo metodo implementa il [**metodo IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

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

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Il pin è attualmente in fase di scaricamento; L'esempio è stato rifiutato.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                                        |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) del pin, che controlla lo stato di streaming del pin e verifica le modifiche al formato nel tipo di supporto. Chiama quindi il metodo [**CTransformFilter::Receive**](ctransformfilter-receive.md) del filtro, che elabora l'esempio e lo recapita a valle.

Se il filtro deve accedere all'esempio dopo la fine del metodo, deve contenere un conteggio dei riferimenti chiamando il metodo **IUnknown::AddRef** sull'esempio. Ad esempio, alcuni filtri del decodificatore necessitano del campione corrente per decodificare il campione successivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




