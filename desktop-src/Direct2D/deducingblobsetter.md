---
title: DeducingBlobSetter (D2d1effecthelpers. h)
description: Deduce la classe e gli argomenti e quindi chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo BLOB.
ms.assetid: 4B8B871D-FE5E-4EF3-AEED-A3D92C10E8C6
keywords:
- Direct2D DeducingBlobSetter
topic_type:
- apiref
api_name:
- DeducingBlobSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d3bbfcc0a48d722bd98456821d7f7df5e8780a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330340"
---
# <a name="deducingblobsetter"></a>DeducingBlobSetter

Deduce la classe e gli argomenti e quindi chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo BLOB.

> [!Note]  
> DeducingBlobSetter non deve essere chiamato direttamente.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobSetter(  
    _In_ HRESULT (C::*callback)(const BYTE *, UINT32),  
    _In_ I *effect,  
    _In_reads_(dataSize) const BYTE *data,  
    UINT32 dataSize,  
    ) 
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Direct2D::D educingBlobGetter**](deducingblobgetter.md)
</dt> </dl>

 

 





