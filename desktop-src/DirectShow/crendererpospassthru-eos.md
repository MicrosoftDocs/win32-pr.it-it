---
description: Il metodo EOS aggiorna i timestamp memorizzati nella cache dopo una notifica di fine del flusso.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: Metodo CRendererPosPassThru. EOS (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9e6990d946f32b441f0a33ceba8c0a59fdae488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333173"
---
# <a name="crendererpospassthrueos-method"></a>Metodo CRendererPosPassThru. EOS

Il `EOS` metodo aggiorna i timestamp memorizzati nella cache dopo una notifica di fine del flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EOS();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                            | Descrizione                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Esito negativo. Probabilmente il filtro non è in streaming.<br/> |



 

## <a name="remarks"></a>Commenti

Il filtro deve chiamare questo metodo quando riceve una notifica di fine flusso ([**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)). Il metodo imposta entrambi i timestamp memorizzati nella cache uguale alla posizione di arresto, assicurando che il metodo [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) restituisca i valori corretti alla fine del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




