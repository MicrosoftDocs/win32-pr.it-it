---
description: Il metodo OnReceiveFirstSample viene chiamato quando il filtro riceve un campione mentre è sospeso.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Metodo CBaseRenderer. OnReceiveFirstSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333351"
---
# <a name="cbaserendereronreceivefirstsample-method"></a>CBaseRenderer. OnReceiveFirstSample, metodo

Il `OnReceiveFirstSample` metodo viene chiamato quando il filtro riceve un campione mentre è sospeso.

## <a name="syntax"></a>Sintassi


```C++
virtual void OnReceiveFirstSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) chiama questo metodo. Non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override. Questo metodo è destinato principalmente ai renderer di video. Quando un renderer video viene sospeso, viene in genere visualizzato il primo campione come immagine ancora.

La ricerca del grafico mentre viene sospesa causa anche la chiamata del metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




