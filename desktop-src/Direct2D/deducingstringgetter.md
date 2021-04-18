---
title: DeducingStringGetter (D2d1effecthelpers. h)
description: Deduce la classe e gli argomenti e quindi chiama un callback del Getter della proprietà membro-funzione per una proprietà di tipo stringa.
ms.assetid: 434E3360-D6C3-46CB-818E-15A185F4BB84
keywords:
- Direct2D DeducingStringGetter
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
ms.openlocfilehash: ac65b9e5d7e37e2db83f06f80172e90f9f27f80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328853"
---
# <a name="deducingstringgetter"></a>DeducingStringGetter

Deduce la classe e gli argomenti e quindi chiama un callback del Getter della proprietà membro-funzione per una proprietà di tipo stringa.

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
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Direct2D::D educingStringSetter**](deducingstringsetter.md)
</dt> </dl>

 

 





