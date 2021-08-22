---
description: 'Membro CTransformOutputPin::m_pPosition : oggetto helper per passare i comandi di ricerca a monte.'
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: Membro CTransformOutputPin::m_pPosition (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bfa565d38fa982ea457da13ee9cf08a1d0f2fe8d5ba52ef3c5b86379fc02b509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538161"
---
# <a name="ctransformoutputpinm_pposition-member"></a>Membro CTransformOutputPin::m \_ pPosition

Oggetto helper per passare i comandi seek upstream.

## <a name="syntax"></a>Sintassi


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Osservazioni

Quando viene eseguita la prima query sul segnaposto per [**l'interfaccia IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) o [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) viene creato e aggregato un oggetto helper [**CPosPassThru.**](cpospassthru.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




