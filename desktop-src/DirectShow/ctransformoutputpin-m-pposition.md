---
description: Oggetto helper per passare i comandi Seek upstream.
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Membro CTransformOutputPin:: m_pPosition (Transfrm. h)'
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
ms.openlocfilehash: dc98e439d7f6a2d6c6392ffb665b04e502047eb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330842"
---
# <a name="ctransformoutputpinm_pposition-member"></a>Membro pPosition di CTransformOutputPin:: m \_

Oggetto helper per passare i comandi Seek upstream.

## <a name="syntax"></a>Sintassi


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Osservazioni

Quando il PIN viene prima sottoposto a query per l'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) o [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , crea e aggrega un oggetto helper [**CPosPassThru**](cpospassthru.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




