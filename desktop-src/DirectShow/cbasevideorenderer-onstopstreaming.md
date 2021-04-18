---
description: Il metodo OnStopStreaming viene chiamato alla fine del flusso per correggere gli orari del report della pagina delle proprietà.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Metodo CBaseVideoRenderer. OnStopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325364"
---
# <a name="cbasevideorendereronstopstreaming-method"></a>CBaseVideoRenderer. OnStopStreaming, metodo

Il `OnStopStreaming` metodo viene chiamato alla fine del flusso per correggere gli orari del report della pagina delle proprietà.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro viene chiamata due volte, una volta in pausa e di nuovo quando il flusso viene effettivamente arrestato.

Questa funzione membro esegue l'override di [**CBaseRenderer:: OnStopStreaming**](cbaserenderer-onstopstreaming.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




