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
# <a name="deducingvaluesetter"></a><span data-ttu-id="f7fef-104">DeducingValueSetter</span><span class="sxs-lookup"><span data-stu-id="f7fef-104">DeducingValueSetter</span></span>

<span data-ttu-id="f7fef-105">Deduce la classe e gli argomenti e quindi chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo valore.</span><span class="sxs-lookup"><span data-stu-id="f7fef-105">Deduces the class and arguments and then calls a member-function property setter callback for a value-type property.</span></span>

> [!Note]  
> <span data-ttu-id="f7fef-106">DeducingValueSetter non deve essere chiamato direttamente.</span><span class="sxs-lookup"><span data-stu-id="f7fef-106">DeducingValueSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueSetter(
    _In_ HRESULT (C::*callback)(P),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="f7fef-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7fef-107">Requirements</span></span>



| <span data-ttu-id="f7fef-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7fef-108">Requirement</span></span> | <span data-ttu-id="f7fef-109">Valore</span><span class="sxs-lookup"><span data-stu-id="f7fef-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7fef-110">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7fef-110">Header</span></span><br/> | <dl> <span data-ttu-id="f7fef-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7fef-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7fef-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7fef-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7fef-113">**Direct2D::D educingValueGetter**</span><span class="sxs-lookup"><span data-stu-id="f7fef-113">**Direct2D::DeducingValueGetter**</span></span>](deducingvaluegetter.md)
</dt> </dl>

 

 





