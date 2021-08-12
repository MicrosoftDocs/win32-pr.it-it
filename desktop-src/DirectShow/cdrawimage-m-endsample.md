---
description: La variabile \_ membro m EndSample specifica l'ora di arresto dell'esempio più recente.
ms.assetid: 694815b6-8da5-4174-b2c7-7d686a557c6c
title: Membro CDrawImage::m_EndSample (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_EndSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2877e709cb7d0d8a259dfa91e1ebe3b723771493e012bf29eef0fffe1c7eaeaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656984"
---
# <a name="cdrawimagem_endsample-member"></a>Membro CDrawImage::m \_ EndSample

La `m_EndSample` variabile membro specifica l'ora di arresto dell'esempio più recente.

## <a name="syntax"></a>Sintassi


```C++
CRefTime m_EndSample;
```



## <a name="remarks"></a>Osservazioni

Il valore è valido solo all'interno del metodo [**CDrawImage::D isplaySampleTimes.**](cdrawimage-displaysampletimes.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




