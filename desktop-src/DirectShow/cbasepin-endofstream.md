---
description: 'Il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il metodo IPin:: EndOfStream. Chiamare questo metodo solo sui pin di input.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Metodo CBasePin. EndOfStream (Amfilter. h)
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
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332768"
---
# <a name="cbasepinendofstream-method"></a>CBasePin. EndOfStream, metodo

Il `EndOfStream` metodo notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) . Chiamare questo metodo solo sui pin di input.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Il filtro deve passare le notifiche di fine flusso downstream ai pin di input dei filtri connessi. Se il filtro è un renderer, deve inviare una notifica di evento [**EC \_ completo**](ec-complete.md) al gestore del grafico dei filtri. Per altre informazioni, vedere [flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md).

Nella classe di base, questo metodo non esegue alcuna operazione. Le classi derivate devono eseguire l'override del metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




