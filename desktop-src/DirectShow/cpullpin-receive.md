---
description: Il metodo Receive viene chiamato quando l'oggetto riceve un campione multimediale dal pin di output. La classe derivata deve implementare questo metodo.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: Metodo CPullPin.Receive (Pullpin.h)
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
ms.openlocfilehash: fdf38c9c873dd8d95ae60341fc2f7dba02abff1f8b34fd89d0d1f720dc59b55f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831541"
---
# <a name="cpullpinreceive-method"></a>Metodo CPullPin.Receive

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

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** La restituzione di un valore diverso da S \_ OK arresterà il thread di pull dei dati.

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato ogni volta che arriva un nuovo campione dal pin di output. Scrivere questo metodo nello stesso modo del [**metodo IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

I timestamp nell'esempio specificano gli offset dei byte rispetto alla posizione iniziale originale specificata nel [**metodo CPullPin::Seek.**](cpullpin-seek.md)

La posizione iniziale viene arrotondata al limite di allineamento più vicino e la posizione di arresto viene arrotondata per eserciti al limite di allineamento più vicino. Inoltre, se la posizione di arresto supera la durata totale, viene usata la durata.

Tutti i timestamp vengono specificati come offset di byte moltiplicato per 10.000.000, definito come unità costanti. Pertanto, nozioni di secondo è un byte. Per trovare gli offset di byte effettivi, chiamare [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) e dividere i risultati per UNITÀ.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




