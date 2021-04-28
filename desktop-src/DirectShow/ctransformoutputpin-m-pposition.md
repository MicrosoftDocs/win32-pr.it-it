---
description: 'CTransformOutputPin::m_pPosition: oggetto helper per passare i comandi di ricerca a monte.'
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
ms.openlocfilehash: b9c5a1b5d5ced7a9f3985ceebdd2bdcb8e491d2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084859"
---
# <a name="ctransformoutputpinm_pposition-member"></a>Membro CTransformOutputPin::m \_ pPosition

Oggetto helper per passare i comandi di ricerca a monte.

## <a name="syntax"></a>Sintassi


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Osservazioni

Quando il pin viene sottoposto a query per la prima volta per [**l'interfaccia IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) o [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) crea e aggrega un oggetto helper [**CPosPassThru.**](cpospassthru.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




