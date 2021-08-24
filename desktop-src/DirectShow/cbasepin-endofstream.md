---
description: Il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il metodo IPin::EndOfStream. Chiamare questo metodo solo sui pin di input.
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Metodo CBasePin.EndOfStream (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9e1549000be728da0118323303a60a23a5930ad68d3c7d2d2b6c9c92d54c3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916431"
---
# <a name="cbasepinendofstream-method"></a>Metodo CBasePin.EndOfStream

Il `EndOfStream` metodo notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il [**metodo IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) Chiamare questo metodo solo sui pin di input.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il filtro deve passare le notifiche di fine flusso a valle ai pin di input dei filtri connessi. Se il filtro è un renderer, deve inviare una notifica [**\_ dell'evento EC COMPLETE**](ec-complete.md) al gestore del grafico del filtro. Per altre informazioni, vedere [Data Flow in Filter Graph](data-flow-in-the-filter-graph.md).

Nella classe di base questo metodo non esegue alcuna operazione. Le classi derivate devono eseguire l'override di questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




