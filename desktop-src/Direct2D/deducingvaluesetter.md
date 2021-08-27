---
title: DeducingValueSetter (D2d1effecthelpers.h)
description: Deduce la classe e gli argomenti e quindi chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo valore.
ms.assetid: 4C3D64A8-0CC0-405A-A5B3-627C2DF25EA1
keywords:
- DeducingValueSetter Direct2D
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
ms.openlocfilehash: bfba4f6123b9e097d5c9c5fedb2e872974fc3d15a5c54464eca4ae6e27c3048c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108861"
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
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Direct2D::D educingValueGetter**](deducingvaluegetter.md)
</dt> </dl>

 

 





