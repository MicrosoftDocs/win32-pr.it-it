---
description: Flag che indica se la qualità è stata modificata.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: Membro CTransformFilter::m_bQualityChanged (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 454d8bad4ced2291b061b09992ad450d9e483f269e3fd72b192adbbacb077d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953610"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>Membro CTransformFilter::m \_ bQualityChanged

Flag che indica se la qualità è stata modificata. La prima volta che il filtro elimina un campione, invia un evento [**EC \_ QUALITY \_ CHANGE**](ec-quality-change.md) al gestore del grafico del filtro e imposta questo flag su **TRUE.** Questo evento non viene inviato di nuovo fino a quando il filtro non si arresta e si riavvia, anche se nel frattempo continua a eliminare i campioni.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




