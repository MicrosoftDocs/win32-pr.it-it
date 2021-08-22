---
description: Il metodo EOS aggiorna i timestamp memorizzati nella cache dopo una notifica di fine flusso.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: Metodo CRendererPosPassThru.EOS (Ctlutil.h)
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
ms.openlocfilehash: 10f87fbb66f8ad1d89ff31c6653780b3fde23ecbaf55d72b6f3de2f59546b49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073415"
---
# <a name="crendererpospassthrueos-method"></a>Metodo CRendererPosPassThru.EOS

Il `EOS` metodo aggiorna i timestamp memorizzati nella cache dopo una notifica di fine flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EOS();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                            | Descrizione                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Esito negativo. È possibile che il filtro non sia in streaming.<br/> |



 

## <a name="remarks"></a>Commenti

Il filtro deve chiamare questo metodo quando riceve una notifica di fine flusso ([**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)). Il metodo imposta entrambi i timestamp memorizzati nella cache come posizione di arresto, assicurando che il metodo [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) restituisca i valori corretti alla fine del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




