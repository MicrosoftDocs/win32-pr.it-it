---
description: Il metodo IsEndOfStream esegue una query se è stata ricevuta la notifica di fine del flusso.
ms.assetid: 44f9b740-ff7d-4387-9c2c-a5b6b90f3295
title: Metodo CBaseRenderer. IsEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e07afb4dfb10e38d90184ba5747f200d1bc716d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326940"
---
# <a name="cbaserendererisendofstream-method"></a>CBaseRenderer. IsEndOfStream, metodo

Il `IsEndOfStream` metodo esegue una query se è stata ricevuta la notifica di fine del flusso.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsEndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il flag [**\_ bEOS CBaseRenderer:: m**](cbaserenderer-m-beos.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




