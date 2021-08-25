---
title: DeducingBlobGetter (D2d1effecthelpers.h)
description: Deduce la classe e gli argomenti e quindi chiama un callback del metodo get della proprietà della funzione membro per una proprietà di tipo BLOB.
ms.assetid: 1B8800CB-2AD0-4684-99D7-986F6C53A6F1
keywords:
- DeducingBlobGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045f781ae22aa4550a298ba7becfe2bc4a939528657f663ec021870bf3afa78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918281"
---
# <a name="deducingblobgetter"></a>DeducingBlobGetter

Deduce la classe e gli argomenti e quindi chiama un callback del metodo get della proprietà della funzione membro per una proprietà di tipo BLOB.

> [!Note]  
> DeducingBlobGetter non deve essere chiamato direttamente.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobGetter(  
    _In_ HRESULT (C::*callback)(BYTE *, UINT32, UINT32*) const,  
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

[**Direct2D::D educingBlobSetter**](deducingblobsetter.md)
</dt> </dl>

 

 





