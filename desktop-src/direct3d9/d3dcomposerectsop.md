---
description: Specifica come combinare i dati del glifo dalle aree di origine e di destinazione in una chiamata a ComposeRects.
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: Enumerazione D3DCOMPOSERECTSOP (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cd47cb14ab129bf27a4b59ba07e0be12d144fb8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322366"
---
# <a name="d3dcomposerectsop-enumeration"></a><span data-ttu-id="03c95-103">Enumerazione D3DCOMPOSERECTSOP</span><span class="sxs-lookup"><span data-stu-id="03c95-103">D3DCOMPOSERECTSOP enumeration</span></span>

<span data-ttu-id="03c95-104">Specifica come combinare i dati del glifo dalle aree di origine e di destinazione in una chiamata a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span><span class="sxs-lookup"><span data-stu-id="03c95-104">Specifies how to combine the glyph data from the source and destination surfaces in a call to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span></span>

## <a name="syntax"></a><span data-ttu-id="03c95-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03c95-105">Syntax</span></span>


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a><span data-ttu-id="03c95-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="03c95-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="03c95-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**Copia di D3DCOMPOSERECTS \_**</span><span class="sxs-lookup"><span data-stu-id="03c95-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**D3DCOMPOSERECTS\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="03c95-108">Copiare l'origine nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="03c95-108">Copy the source to the destination.</span></span>

</dd> <dt>

<span data-ttu-id="03c95-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ o**</span><span class="sxs-lookup"><span data-stu-id="03c95-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS\_OR**</span></span>
</dt> <dd>

<span data-ttu-id="03c95-110">OR bit per bit l'origine e la destinazione.</span><span class="sxs-lookup"><span data-stu-id="03c95-110">Bitwise OR the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="03c95-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ e**</span><span class="sxs-lookup"><span data-stu-id="03c95-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS\_AND**</span></span>
</dt> <dd>

<span data-ttu-id="03c95-112">Bit per bit e l'origine e la destinazione.</span><span class="sxs-lookup"><span data-stu-id="03c95-112">Bitwise AND the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="03c95-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS \_ neg**</span><span class="sxs-lookup"><span data-stu-id="03c95-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS\_NEG**</span></span>
</dt> <dd>

<span data-ttu-id="03c95-114">Copiare l'origine negata nella destinazione (DST & ~ src).</span><span class="sxs-lookup"><span data-stu-id="03c95-114">Copy the negated source to the destination (Dst & ~Src).</span></span>

</dd> <dt>

<span data-ttu-id="03c95-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="03c95-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="03c95-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="03c95-116">Reserved.</span></span> <span data-ttu-id="03c95-117">Utilizzato per forzare l'enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="03c95-117">Used to force enumeration to 32-bits in size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03c95-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03c95-118">Requirements</span></span>



| <span data-ttu-id="03c95-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c95-119">Requirement</span></span> | <span data-ttu-id="03c95-120">Valore</span><span class="sxs-lookup"><span data-stu-id="03c95-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03c95-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03c95-121">Header</span></span><br/> | <dl> <span data-ttu-id="03c95-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="03c95-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03c95-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03c95-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c95-124">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="03c95-124">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




