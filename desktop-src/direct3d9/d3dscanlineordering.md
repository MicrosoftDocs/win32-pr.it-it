---
description: Flag che indicano il metodo utilizzato dal rasterizzatore per creare un'immagine in una superficie.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: Enumerazione D3DSCANLINEORDERING (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2eaed36577f881266c12b0a927cfcdc2494f0d57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323649"
---
# <a name="d3dscanlineordering-enumeration"></a><span data-ttu-id="bc729-103">Enumerazione D3DSCANLINEORDERING</span><span class="sxs-lookup"><span data-stu-id="bc729-103">D3DSCANLINEORDERING enumeration</span></span>

<span data-ttu-id="bc729-104">Flag che indicano il metodo utilizzato dal rasterizzatore per creare un'immagine in una superficie.</span><span class="sxs-lookup"><span data-stu-id="bc729-104">Flags indicating the method the rasterizer uses to create an image on a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc729-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc729-105">Syntax</span></span>


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a><span data-ttu-id="bc729-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="bc729-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bc729-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ progressive**</span><span class="sxs-lookup"><span data-stu-id="bc729-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="bc729-108">L'immagine viene creata dalla prima scanline all'ultima senza alcuna omissione.</span><span class="sxs-lookup"><span data-stu-id="bc729-108">The image is created from the first scanline to the last without skipping any.</span></span>

</dd> <dt>

<span data-ttu-id="bc729-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING \_ INTERlacciato**</span><span class="sxs-lookup"><span data-stu-id="bc729-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING\_INTERLACED**</span></span>
</dt> <dd>

<span data-ttu-id="bc729-110">L'immagine viene creata usando il metodo interlacciato, in cui le linee dispari vengono disegnate su passi con numerazione dispari e anche le linee vengono disegnate su passaggi con numero pari.</span><span class="sxs-lookup"><span data-stu-id="bc729-110">The image is created using the interlaced method in which odd-numbered lines are drawn on odd-numbered passes and even lines are drawn on even-numbered passes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc729-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc729-111">Remarks</span></span>

<span data-ttu-id="bc729-112">Questa enumerazione viene utilizzata come membro in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) e [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).</span><span class="sxs-lookup"><span data-stu-id="bc729-112">This enumeration is used as a member in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) and [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc729-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc729-113">Requirements</span></span>



| <span data-ttu-id="bc729-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc729-114">Requirement</span></span> | <span data-ttu-id="bc729-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bc729-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc729-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc729-116">Header</span></span><br/> | <dl> <span data-ttu-id="bc729-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc729-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc729-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc729-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc729-119">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="bc729-119">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




