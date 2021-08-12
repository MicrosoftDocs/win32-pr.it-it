---
description: Il metodo ReconnectPin interrompe una connessione pin esistente e la riconnette allo stesso pin, usando un tipo di supporto specificato.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Metodo CBaseFilter.ReconnectPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39cef0ac5a0a7c4f186b8eae90a96a8e26fbf886f819dc7562cb7d8df4e087e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659721"
---
# <a name="cbasefilterreconnectpin-method"></a>Metodo CBaseFilter.ReconnectPin

Il `ReconnectPin` metodo interrompe una connessione pin esistente e la riconnette allo stesso pin, usando un tipo di supporto specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin* 
</dt> <dd>

Puntatore all'interfaccia [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) segnaposto.

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntatore a [**una struttura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto oppure **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                                                               |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | [**m \_ pGraph member**](cbasefilter-m-pgraph.md) variable is **NULL**.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il [**metodo IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) nel gestore del grafico del filtro. Se [**l'interfaccia IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) non è disponibile, il metodo chiama [**IFilterGraph::Reconnect.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




