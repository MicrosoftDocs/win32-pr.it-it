---
description: Il metodo ShouldSkipFrame determina se il filtro deve eliminare un campione specificato.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Metodo CVideoTransformFilter.ShouldSkipFrame (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26a0c35be9914641abfa053cd1ee00f46bb09222aecbebc55d45900331a2ee81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075941"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a>Metodo CVideoTransformFilter.ShouldSkipFrame

Il `ShouldSkipFrame` metodo determina se il filtro deve eliminare un campione specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*spilla* 
</dt> <dd>

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se il filtro deve eliminare questo esempio oppure **FALSE** se il filtro deve elaborare questo esempio.

## <a name="remarks"></a>Commenti

Questo metodo restituisce **TRUE** se vengono soddisfatte le condizioni seguenti:

-   L'esempio include timestamp.
-   Il tempo medio di decodifica è almeno il 25% della durata del fotogramma.
-   Il renderer è attualmente con almeno un frame in ritardo, come segnalato tramite messaggi di qualità.
-   Se si ignora il fotogramma chiave successivo, il fotogramma non arriva più di un fotogramma in anticipo.

Ai fini di questo calcolo, il filtro registra le informazioni seguenti durante l'elaborazione dei dati:

-   Tempo medio di decodifica negli ultimi 20 fotogrammi (**m \_ itrAvgDecode**)
-   Numero di fotogrammi dall'ultimo fotogramma chiave (**m \_ nFramesSinceKeyFrame**)
-   Stima del numero di fotogrammi tra fotogrammi chiave (**m \_ nKeyFramePeriod**)

Quando il filtro rilascia un frame, continua a rilasciare i fotogrammi fino a raggiungere il fotogramma chiave successivo. Se questo metodo restituisce **TRUE,** invia anche un evento [**EC QUALITY \_ \_ CHANGE**](ec-quality-change.md) a Filter Graph Manager.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




