---
description: Definisce il tipo di base di una superficie della patch di ordine superiore.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: Enumerazione D3DBASISTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132306"
---
# <a name="d3dbasistype-enumeration"></a><span data-ttu-id="fd6e9-103">Enumerazione D3DBASISTYPE</span><span class="sxs-lookup"><span data-stu-id="fd6e9-103">D3DBASISTYPE enumeration</span></span>

<span data-ttu-id="fd6e9-104">Definisce il tipo di base di una superficie della patch di ordine superiore.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-104">Defines the basis type of a high-order patch surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6e9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd6e9-105">Syntax</span></span>


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a><span data-ttu-id="fd6e9-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="fd6e9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd6e9-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ Bezier**</span><span class="sxs-lookup"><span data-stu-id="fd6e9-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS\_BEZIER**</span></span>
</dt> <dd>

<span data-ttu-id="fd6e9-108">I vertici di input vengono considerati come una serie di patch di Bézier.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-108">Input vertices are treated as a series of Bézier patches.</span></span> <span data-ttu-id="fd6e9-109">Il numero di vertici specificati deve essere divisibile per 4.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-109">The number of vertices specified must be divisible by 4.</span></span> <span data-ttu-id="fd6e9-110">Non verrà eseguito il rendering di parti della mesh oltre questo criterio.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-110">Portions of the mesh beyond this criterion will not be rendered.</span></span> <span data-ttu-id="fd6e9-111">Si presuppone la continuità completa tra le sottopatch all'interno dell'area sottoposta a rendering da ogni chiamata.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-111">Full continuity is assumed between sub-patches in the interior of the surface rendered by each call.</span></span> <span data-ttu-id="fd6e9-112">Solo i vertici negli angoli di ogni sottopatch si trovano nella superficie risultante.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-112">Only the vertices at the corners of each sub-patch are guaranteed to lie on the resulting surface.</span></span>

</dd> <dt>

<span data-ttu-id="fd6e9-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**\_Perequazione BSpline D3DBASIS**</span><span class="sxs-lookup"><span data-stu-id="fd6e9-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS\_BSPLINE**</span></span>
</dt> <dd>

<span data-ttu-id="fd6e9-114">I vertici di input vengono trattati come punti di controllo di una superficie B-spline.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-114">Input vertices are treated as control points of a B-spline surface.</span></span> <span data-ttu-id="fd6e9-115">Il numero di aperture di cui è stato eseguito il rendering è due meno del numero di aperture in tale direzione.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-115">The number of apertures rendered is two fewer than the number of apertures in that direction.</span></span> <span data-ttu-id="fd6e9-116">In generale, la superficie generata non contiene i vertici di controllo specificati.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-116">In general, the generated surface does not contain the control vertices specified.</span></span>

</dd> <dt>

<span data-ttu-id="fd6e9-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ CATMULL \_ ROM**</span><span class="sxs-lookup"><span data-stu-id="fd6e9-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS\_CATMULL\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="fd6e9-118">Una base di interpolazione definisce la superficie in modo che la superficie attraversi tutti i vertici di input specificati.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-118">An interpolating basis defines the surface so that the surface goes through all the input vertices specified.</span></span> <span data-ttu-id="fd6e9-119">In DirectX 8, era D3DBASIS \_ interpolazione.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-119">In DirectX 8, this was D3DBASIS\_INTERPOLATE.</span></span>

</dd> <dt>

<span data-ttu-id="fd6e9-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fd6e9-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="fd6e9-121">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-121">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="fd6e9-122">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-122">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="fd6e9-123">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-123">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd6e9-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd6e9-124">Remarks</span></span>

<span data-ttu-id="fd6e9-125">I membri di **D3DBASISTYPE** specificano la formulazione da utilizzare per la valutazione della primitiva della superficie della patch di ordine superiore durante la suddivisione a mosaico.</span><span class="sxs-lookup"><span data-stu-id="fd6e9-125">The members of **D3DBASISTYPE** specify the formulation to be used in evaluating the high-order patch surface primitive during tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd6e9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd6e9-126">Requirements</span></span>



| <span data-ttu-id="fd6e9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd6e9-127">Requirement</span></span> | <span data-ttu-id="fd6e9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="fd6e9-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6e9-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd6e9-129">Header</span></span><br/> | <dl> <span data-ttu-id="fd6e9-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd6e9-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd6e9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd6e9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6e9-132">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="fd6e9-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="fd6e9-133">**\_Informazioni D3DRECTPATCH**</span><span class="sxs-lookup"><span data-stu-id="fd6e9-133">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="fd6e9-134">**\_Informazioni D3DTRIPATCH**</span><span class="sxs-lookup"><span data-stu-id="fd6e9-134">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> </dl>

 

 




