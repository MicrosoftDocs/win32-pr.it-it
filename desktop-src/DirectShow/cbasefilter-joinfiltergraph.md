---
description: 'Il metodo JoinFilterGraph notifica al filtro che è stato aggiunto o lasciato un grafico di filtro. Questo metodo implementa il metodo IBaseFilter:: JoinFilterGraph.'
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: Metodo CBaseFilter. JoinFilterGraph (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45453c6423b8fa9f68e5d8dff86d13b130d65f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331538"
---
# <a name="cbasefilterjoinfiltergraph-method"></a>CBaseFilter. JoinFilterGraph, metodo

Il `JoinFilterGraph` metodo notifica al filtro che è stato aggiunto o ha lasciato un grafico di filtro. Questo metodo implementa il metodo [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGraph* 
</dt> <dd>

Puntatore all'interfaccia [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) dell'oggetto Filter Graph Manager oppure **null** se il filtro sta uscendo dal grafico.

</dd> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode contenente un nome per il filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo imposta la variabile membro [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md) uguale al parametro *pGraph* . Viene inoltre eseguita una query per un puntatore all'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) e viene archiviato nella variabile membro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) . Tuttavia, il filtro non mantiene un conteggio dei riferimenti in nessuna di queste interfacce. In questo modo si creerebbe un conteggio dei riferimenti circolari, perché il gestore del grafico del filtro mantiene un conteggio dei riferimenti sul filtro.

Il metodo copia la stringa specificata da *pname* nella variabile membro [**CBaseFilter:: m \_ pname**](cbasefilter-m-pname.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




