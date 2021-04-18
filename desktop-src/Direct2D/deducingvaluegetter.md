---
title: DeducingValueGetter (D2d1effecthelpers. h)
description: Deduce la classe e gli argomenti e quindi chiama un callback del Getter della proprietà membro-funzione per una proprietà di tipo valore.
ms.assetid: E2E5CCC3-B112-4D3C-8840-121A55C4F1A2
keywords:
- Direct2D DeducingValueGetter
topic_type:
- apiref
api_name:
- DeducingValueGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd6eac823457882513f97557939db884efcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325797"
---
# <a name="deducingvaluegetter"></a>DeducingValueGetter

Deduce la classe e gli argomenti e quindi chiama un callback del Getter della proprietà membro-funzione per una proprietà di tipo valore.

> [!Note]  
> DeducingValueGetter non deve essere chiamato direttamente.

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueGetter(
    _In_ P (C::*callback)() const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Direct2D::D educingValueSetter**](deducingvaluesetter.md)
</dt> </dl>

 

 





