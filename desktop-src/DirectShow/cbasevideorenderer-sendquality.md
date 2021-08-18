---
description: Il metodo SendQuality invia un messaggio di qualità per indicare cosa deve fare il fornitore sulla qualità.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Metodo CBaseVideoRenderer.SendQuality (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acda4bd9b00434e33c24ac44625b3c1d45350d45b4ec0b242d2638333ad11ed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074765"
---
# <a name="cbasevideorenderersendquality-method"></a>Metodo CBaseVideoRenderer.SendQuality

Il metodo invia un messaggio di qualità per indicare cosa deve fare il `SendQuality` fornitore sulla qualità.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*trLate* 
</dt> <dd>

Intervallo di tempo entro il quale il frame è in ritardo.

</dd> <dt>

*trRealStream* 
</dt> <dd>

Ora corrente del flusso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro invia un messaggio di controllo qualità a monte per controllare la gestione della qualità. La natura del messaggio di qualità( ovvero se ridurre o aumentare il numero di campioni) è determinata nell'implementazione della gestione della qualità in questa classe derivata (vedere [**CBaseVideoRenderer::ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




