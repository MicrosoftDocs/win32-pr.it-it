---
description: Il metodo OnReceiveFirstSample viene chiamato quando il filtro riceve un campione durante la sospensione.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Metodo CBaseRenderer.OnReceiveFirstSample (Renbase.h)
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
ms.openlocfilehash: 882a356f47aa146ec8ba1b06d7af43235c8213334c0d82d0a241c590654bf2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157701"
---
# <a name="cbaserendereronreceivefirstsample-method"></a>Metodo CBaseRenderer.OnReceiveFirstSample

Il `OnReceiveFirstSample` metodo viene chiamato quando il filtro riceve un campione durante la sospensione.

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

Il [**metodo CBaseRenderer::Receive**](cbaserenderer-receive.md) chiama questo metodo. Non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override. Questo metodo è destinato principalmente ai renderer video. Quando un renderer video viene sospeso, in genere visualizza il primo esempio come immagine non ancorata.

La ricerca del grafo in pausa comporta anche la chiamata di questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




