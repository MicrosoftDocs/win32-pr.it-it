---
description: Il metodo di flusso esegue una query per determinare se il filtro sta effettuando il flusso di dati.
ms.assetid: af1529e1-f79d-469e-b234-7742916a3431
title: Metodo CBaseRenderer. IsValid (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cc47e2897338e2ac8a8eeee74424630ce57ccda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333487"
---
# <a name="cbaserendererisstreaming-method"></a>CBaseRenderer. il metodo di trasmissione

Il `IsStreaming` metodo esegue una query per determinare se il filtro sta inviando dati in streaming.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsStreaming();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il flag [**CBaseRenderer:: m \_ bStreaming**](cbaserenderer-m-bstreaming.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




