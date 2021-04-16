---
description: Definisce le costanti che descrivono le modalità di ombreggiatura supportate.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Enumerazione D3DSHADEMODE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354539"
---
# <a name="d3dshademode-enumeration"></a><span data-ttu-id="f6750-103">Enumerazione D3DSHADEMODE</span><span class="sxs-lookup"><span data-stu-id="f6750-103">D3DSHADEMODE enumeration</span></span>

<span data-ttu-id="f6750-104">Definisce le costanti che descrivono le modalità di ombreggiatura supportate.</span><span class="sxs-lookup"><span data-stu-id="f6750-104">Defines constants that describe the supported shading modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6750-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6750-105">Syntax</span></span>


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a><span data-ttu-id="f6750-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="f6750-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f6750-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ Flat**</span><span class="sxs-lookup"><span data-stu-id="f6750-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE\_FLAT**</span></span>
</dt> <dd>

<span data-ttu-id="f6750-108">Modalità ombreggiatura piatta.</span><span class="sxs-lookup"><span data-stu-id="f6750-108">Flat shading mode.</span></span> <span data-ttu-id="f6750-109">Il colore e il componente speculare del primo vertice nel triangolo vengono utilizzati per determinare il colore e il componente speculare della faccia.</span><span class="sxs-lookup"><span data-stu-id="f6750-109">The color and specular component of the first vertex in the triangle are used to determine the color and specular component of the face.</span></span> <span data-ttu-id="f6750-110">Questi colori rimangono costanti nel triangolo; ovvero non vengono interpolate.</span><span class="sxs-lookup"><span data-stu-id="f6750-110">These colors remain constant across the triangle; that is, they are not interpolated.</span></span> <span data-ttu-id="f6750-111">Il Alpha speculare è interpolato.</span><span class="sxs-lookup"><span data-stu-id="f6750-111">The specular alpha is interpolated.</span></span> <span data-ttu-id="f6750-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f6750-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f6750-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**\_Gouraud D3DSHADE**</span><span class="sxs-lookup"><span data-stu-id="f6750-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE\_GOURAUD**</span></span>
</dt> <dd>

<span data-ttu-id="f6750-114">Modalità di ombreggiatura Gouraud.</span><span class="sxs-lookup"><span data-stu-id="f6750-114">Gouraud shading mode.</span></span> <span data-ttu-id="f6750-115">Il colore e i componenti speculari della faccia sono determinati da un'interpolazione lineare tra tutti e tre i vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="f6750-115">The color and specular components of the face are determined by a linear interpolation between all three of the triangle's vertices.</span></span>

</dd> <dt>

<span data-ttu-id="f6750-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ Phong**</span><span class="sxs-lookup"><span data-stu-id="f6750-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE\_PHONG**</span></span>
</dt> <dd>

<span data-ttu-id="f6750-117">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="f6750-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f6750-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f6750-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f6750-119">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f6750-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f6750-120">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f6750-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f6750-121">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f6750-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6750-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6750-122">Remarks</span></span>

<span data-ttu-id="f6750-123">Il primo vertice di un triangolo per la modalità ombreggiatura piatta viene definito nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="f6750-123">The first vertex of a triangle for flat shading mode is defined in the following manner.</span></span>

-   <span data-ttu-id="f6750-124">Per un elenco di triangolo, il primo vertice del triangolo i è \* 3.</span><span class="sxs-lookup"><span data-stu-id="f6750-124">For a triangle list, the first vertex of the triangle i is i \* 3.</span></span>
-   <span data-ttu-id="f6750-125">Per una striscia di triangolo, il primo vertice del triangolo i è Vertex i.</span><span class="sxs-lookup"><span data-stu-id="f6750-125">For a triangle strip, the first vertex of the triangle i is vertex i.</span></span>
-   <span data-ttu-id="f6750-126">Per una ventola del triangolo, il primo vertice del triangolo i è vertice i + 1.</span><span class="sxs-lookup"><span data-stu-id="f6750-126">For a triangle fan, the first vertex of the triangle i is vertex i + 1.</span></span>

<span data-ttu-id="f6750-127">I membri di questo tipo enumerato definiscono i vale per lo stato di \_ rendering MODOOMBRA di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="f6750-127">The members of this enumerated type define the vales for the D3DRS\_SHADEMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6750-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6750-128">Requirements</span></span>



| <span data-ttu-id="f6750-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6750-129">Requirement</span></span> | <span data-ttu-id="f6750-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f6750-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6750-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6750-131">Header</span></span><br/> | <dl> <span data-ttu-id="f6750-132"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6750-132"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6750-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6750-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6750-134">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="f6750-134">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="f6750-135">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="f6750-135">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
