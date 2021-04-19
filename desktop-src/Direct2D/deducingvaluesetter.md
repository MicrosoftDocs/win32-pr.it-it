---
title: DeducingValueSetter (D2d1effecthelpers. h)
description: Deduce la classe e gli argomenti e quindi chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo valore.
ms.assetid: 4C3D64A8-0CC0-405A-A5B3-627C2DF25EA1
keywords:
- Direct2D DeducingValueSetter
topic_type:
- apiref
api_name:
- DeducingValueSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e002c5a36c8ac0b196dfc5fb25e11f7f9d63806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330092"
---
# <a name="deducingvaluesetter"></a>DeducingValueSetter

Deduce la classe e gli argomenti e quindi chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo valore.

> [!Note]  
> DeducingValueSetter non deve essere chiamato direttamente.

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueSetter(
    _In_ HRESULT (C::*callback)(P),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Direct2D::D educingValueGetter**](deducingvaluegetter.md)
</dt> </dl>

 

 





