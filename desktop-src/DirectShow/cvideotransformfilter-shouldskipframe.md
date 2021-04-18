---
description: Il metodo ShouldSkipFrame determina se il filtro deve eliminare un campione specificato.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Metodo CVideoTransformFilter. ShouldSkipFrame (Vtrans. h)
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
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325501"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a>CVideoTransformFilter. ShouldSkipFrame, metodo

Il `ShouldSkipFrame` metodo determina se il filtro deve eliminare un campione specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIn* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il filtro deve eliminare questo esempio oppure **false** se il filtro deve elaborare l'esempio.

## <a name="remarks"></a>Commenti

Questo metodo restituisce **true** se vengono soddisfatte le condizioni seguenti:

-   Nell'esempio sono presenti timestamp.
-   Il tempo di decodifica medio è almeno il 25% della durata del fotogramma.
-   Il renderer è attualmente almeno un frame tardivo, come segnalato tramite messaggi di qualità.
-   Se si ignora il fotogramma chiave successivo, il frame arriverà prima di più di un frame.

Ai fini di questo calcolo, il filtro registra le seguenti informazioni durante l'elaborazione dei dati:

-   Tempo di decodifica medio negli ultimi 20 frame (**m \_ itrAvgDecode**)
-   Il numero di frame dall'ultimo fotogramma chiave (**m \_ nFramesSinceKeyFrame**)
-   Stima del numero di frame tra i fotogrammi chiave (**m \_ nKeyFramePeriod**)

Quando il filtro rilascia un frame, continua a rilasciare i frame fino a raggiungere il fotogramma chiave successivo. Se questo metodo restituisce **true**, invia anche un evento [**di \_ \_ modifica della qualità EC**](ec-quality-change.md) a Filter Graph Manager.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




