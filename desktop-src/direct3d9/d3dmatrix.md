---
description: Descrive una matrice.
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: D3DMATRIX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b4339d2e44e1add46103bae58ad3e02c8a6509b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322927"
---
# <a name="d3dmatrix"></a><span data-ttu-id="d7fbe-103">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="d7fbe-103">D3DMATRIX</span></span>

<span data-ttu-id="d7fbe-104">Descrive una matrice.</span><span class="sxs-lookup"><span data-stu-id="d7fbe-104">Describes a matrix.</span></span>

``` syntax
typedef struct _D3DMATRIX {
    union {
        struct {
            float        _11, _12, _13, _14;
            float        _21, _22, _23, _24;
            float        _31, _32, _33, _34;
            float        _41, _42, _43, _44;

        };
        float m[4][4];
    };
} D3DMATRIX;
```

<span data-ttu-id="d7fbe-105">Tipi derivati: \* LPD3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="d7fbe-105">Derived types: \*LPD3DMATRIX</span></span>

## <a name="members"></a><span data-ttu-id="d7fbe-106">Membri</span><span class="sxs-lookup"><span data-stu-id="d7fbe-106">Members</span></span>



| <span data-ttu-id="d7fbe-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d7fbe-107">Item</span></span>                                                        | <span data-ttu-id="d7fbe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7fbe-108">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fbe-109"><span id="_ij"></span><span id="_IJ"></span>\_IJ</span><span class="sxs-lookup"><span data-stu-id="d7fbe-109"><span id="_ij"></span><span id="_IJ"></span>\_ij</span></span><br/> | <span data-ttu-id="d7fbe-110">Matrice di float che rappresentano una matrice 4x4, dove i è il numero di riga e j è il numero di colonna.</span><span class="sxs-lookup"><span data-stu-id="d7fbe-110">An array of floats that represent a 4x4 matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="d7fbe-111">34, ad esempio, corrisponde \_ \[ a un ₄ ₃ \] , il componente nella terza riga e nella quarta colonna.</span><span class="sxs-lookup"><span data-stu-id="d7fbe-111">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7fbe-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7fbe-112">Remarks</span></span>

<span data-ttu-id="d7fbe-113">In Direct3D l' \_ elemento 34 di una matrice di proiezione non può essere un numero negativo.</span><span class="sxs-lookup"><span data-stu-id="d7fbe-113">In Direct3D, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="d7fbe-114">Se l'applicazione deve usare un valore negativo in questa posizione, deve ridimensionare l'intera matrice di proiezione di-1.</span><span class="sxs-lookup"><span data-stu-id="d7fbe-114">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7fbe-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7fbe-115">Requirements</span></span>



| <span data-ttu-id="d7fbe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7fbe-116">Requirement</span></span> | <span data-ttu-id="d7fbe-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d7fbe-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fbe-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7fbe-118">Header</span></span><br/> | <dl> <span data-ttu-id="d7fbe-119"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7fbe-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7fbe-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7fbe-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fbe-121">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="d7fbe-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d7fbe-122">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="d7fbe-122">**GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="d7fbe-123">**MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="d7fbe-123">**MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="d7fbe-124">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="d7fbe-124">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

<span data-ttu-id="d7fbe-125">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="d7fbe-125">**SetTransform**</span></span>
</dt> <dt>

[<span data-ttu-id="d7fbe-126">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="d7fbe-126">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> <dt>

[<span data-ttu-id="d7fbe-127">Trasformazioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d7fbe-127">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
