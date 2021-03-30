---
title: def (direttiva pragma)
description: Direttiva pragma che alloca manualmente un registro shader a virgola mobile.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- Direttiva pragma def HLSL
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992912"
---
# <a name="def-pragma-directive"></a><span data-ttu-id="07fa4-104">def (direttiva pragma)</span><span class="sxs-lookup"><span data-stu-id="07fa4-104">def pragma Directive</span></span>

<span data-ttu-id="07fa4-105">Direttiva pragma che alloca manualmente un registro shader a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="07fa4-105">Pragma directive that manually allocates a floating-point shader register.</span></span>



| <span data-ttu-id="07fa4-106">\#pragma def ( *target*, *Register*, *val1*, *val2*,*Val3*, *Val4* )</span><span class="sxs-lookup"><span data-stu-id="07fa4-106">\#pragma def( *target*, *register*, *val1*, *val2*,*val3*, *val4* )</span></span> |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="07fa4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="07fa4-107">Parameters</span></span>



| <span data-ttu-id="07fa4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="07fa4-108">Item</span></span>                                                                        | <span data-ttu-id="07fa4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07fa4-109">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="07fa4-110"><span id="target"></span><span id="TARGET"></span>*destinazione*</span><span class="sxs-lookup"><span data-stu-id="07fa4-110"><span id="target"></span><span id="TARGET"></span>*target*</span></span><br/>       | <span data-ttu-id="07fa4-111">Destinazione contenente il registro da allocare.</span><span class="sxs-lookup"><span data-stu-id="07fa4-111">Target that contains the register to allocate.</span></span> <br/>                  |
| <span data-ttu-id="07fa4-112"><span id="register"></span><span id="REGISTER"></span>*Registro*</span><span class="sxs-lookup"><span data-stu-id="07fa4-112"><span id="register"></span><span id="REGISTER"></span>*register*</span></span><br/> | <span data-ttu-id="07fa4-113">Registro shader a virgola mobile da allocare.</span><span class="sxs-lookup"><span data-stu-id="07fa4-113">Floating-point shader register to allocate.</span></span> <br/>                     |
| <span data-ttu-id="07fa4-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span><span class="sxs-lookup"><span data-stu-id="07fa4-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span></span><br/>             | <span data-ttu-id="07fa4-115">Primo byte del valore da allocare al registro specificato.</span><span class="sxs-lookup"><span data-stu-id="07fa4-115">First byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="07fa4-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span><span class="sxs-lookup"><span data-stu-id="07fa4-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span></span><br/>             | <span data-ttu-id="07fa4-117">Secondo byte del valore da allocare al registro specificato.</span><span class="sxs-lookup"><span data-stu-id="07fa4-117">Second byte of the value to allocate to the specified register.</span></span> <br/> |
| <span data-ttu-id="07fa4-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span><span class="sxs-lookup"><span data-stu-id="07fa4-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span></span><br/>             | <span data-ttu-id="07fa4-119">Terzo byte del valore da allocare al registro specificato.</span><span class="sxs-lookup"><span data-stu-id="07fa4-119">Third byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="07fa4-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span><span class="sxs-lookup"><span data-stu-id="07fa4-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span></span><br/>             | <span data-ttu-id="07fa4-121">Quarto byte del valore da allocare al registro specificato.</span><span class="sxs-lookup"><span data-stu-id="07fa4-121">Fourth byte of the value to allocate to the specified register.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="07fa4-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="07fa4-122">Remarks</span></span>

<span data-ttu-id="07fa4-123">Il pragma def consente a uno sviluppatore di precompilare un registro shader a virgola mobile con il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="07fa4-123">The def pragma allows a developer to prefill a floating-point shader register with the specified value.</span></span> <span data-ttu-id="07fa4-124">Questo pragma viene usato raramente.</span><span class="sxs-lookup"><span data-stu-id="07fa4-124">This pragma is infrequently used.</span></span>

## <a name="see-also"></a><span data-ttu-id="07fa4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07fa4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07fa4-126">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07fa4-126">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="07fa4-127">\#pragma (direttiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07fa4-127">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





