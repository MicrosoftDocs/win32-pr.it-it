---
description: Il metodo Receive viene chiamato quando l'oggetto riceve un campione multimediale dal pin di output. La classe derivata deve implementare questo metodo.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: Metodo CPullPin. Receive (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a651822378b6a3c0754ecbd5ace4a5e464f014f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331160"
---
# <a name="cpullpinreceive-method"></a>Metodo CPullPin. Receive

Il `Receive` metodo viene chiamato quando l'oggetto riceve un campione multimediale dal pin di output. La classe derivata deve implementare questo metodo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Se si restituisce un valore diverso da S \_ OK, il thread di pull dei dati verrà interrotto.

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato ogni volta che un nuovo campione arriva dal pin di output. Scrivere questo metodo in modo analogo al metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

I timestamp dell'esempio specificano gli offset di byte rispetto alla posizione iniziale originale specificata nel metodo [**CPullPin:: Seek**](cpullpin-seek.md) .

La posizione iniziale viene arrotondata per difetto al limite di allineamento più vicino e la posizione di arresto viene arrotondata per eccesso al limite di allineamento più vicino. Inoltre, se la posizione di arresto supera la durata totale, viene invece utilizzata la durata.

Tutti i timestamp vengono specificati come offset di byte moltiplicato per 10 milioni, definito come unità di costante. Di conseguenza, un secondo è un byte. Per trovare gli offset di byte effettivi, chiamare [**IMediaSample:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) e dividere i risultati in base alle unità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




