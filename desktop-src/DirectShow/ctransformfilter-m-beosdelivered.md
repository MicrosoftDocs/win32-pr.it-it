---
description: Flag che indica se il filtro ha inviato una notifica di fine flusso.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: Membro CTransformFilter::m_bEOSDelivered (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38d27fabb9dd3ed2a37ed5d836bfdfb1036f4255e6af48580ab6e0678abad74b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655105"
---
# <a name="ctransformfilterm_beosdelivered-member"></a>Membro CTransformFilter::m \_ bEOSDelivered

Flag che indica se il filtro ha inviato una notifica di fine flusso.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a>Osservazioni

Se il filtro viene sospeso quando non ha una connessione di input, invia una notifica di fine flusso a valle e imposta questo flag su **TRUE.** La notifica di fine flusso garantisce che il filtro downstream non attenda i campioni. Si noti che il metodo [**EndOfStream**](ctransformfilter-endofstream.md) del filtro non imposta questo flag.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




