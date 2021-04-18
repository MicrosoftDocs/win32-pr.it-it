---
description: "Il metodo StartStreaming viene chiamato quando il filtro passa allo stato sospeso. Questo metodo esegue l'override del metodo CTransformFilter:: StartStreaming."
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: Metodo CVideoTransformFilter. StartStreaming (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ae8d49401389830f9d5dbf0ec91e7f390c51ca6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325500"
---
# <a name="cvideotransformfilterstartstreaming-method"></a>CVideoTransformFilter. StartStreaming, metodo

Il `StartStreaming` metodo viene chiamato quando il filtro passa allo stato sospeso. Questo metodo esegue l'override del metodo [**CTransformFilter:: StartStreaming**](ctransformfilter-startstreaming.md) .

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo reimposta tutte le statistiche sulle prestazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




