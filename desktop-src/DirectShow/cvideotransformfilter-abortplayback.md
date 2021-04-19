---
description: Il metodo AbortPlayback viene usato per segnalare un errore di streaming. Invia un \_ evento ERRORABORT EC al gestore del grafico dei filtri e invia una notifica di fine flusso a valle.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Metodo CVideoTransformFilter. AbortPlayback (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324180"
---
# <a name="cvideotransformfilterabortplayback-method"></a>CVideoTransformFilter. AbortPlayback, metodo

Il `AbortPlayback` metodo viene usato per segnalare un errore di streaming. Invia un evento [**\_ ERRORABORT EC**](ec-errorabort.md) al gestore del grafico dei filtri e invia una notifica di fine flusso a valle.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*h* 
</dt> <dd>

Valore **HRESULT** dell'operazione non riuscita. Questo valore viene utilizzato come primo parametro di evento per l' \_ evento ERRORABORT EC.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore del parametro *HR* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




