---
title: DeducingStringGetter (D2d1effecthelpers.h)
description: Deduce la classe e gli argomenti e quindi chiama un callback del getter della proprietà della funzione membro per una proprietà di tipo stringa.
ms.assetid: 434E3360-D6C3-46CB-818E-15A185F4BB84
keywords:
- DeducingStringGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99e23a2f79f38527dfae76c74e5e2ad8b828dce1a0ff984f622bd95fd287c97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342961"
---
# <a name="deducingstringgetter"></a>DeducingStringGetter

Deduce la classe e gli argomenti e quindi chiama un callback del getter della proprietà della funzione membro per una proprietà di tipo stringa.

> [!Note]  
> DeducingStringGetter non deve essere chiamato direttamente.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringGetter(
    _In_ HRESULT (C::*callback)(PWSTR, UINT32, UINT32*) const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize 
    ) 
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Direct2D::D educingStringSetter**](deducingstringsetter.md)
</dt> </dl>

 

 





