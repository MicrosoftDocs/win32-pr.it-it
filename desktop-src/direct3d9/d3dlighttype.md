---
description: Definisce il tipo di luce.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: Enumerazione D3DLIGHTTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 83c94db3126443f757f01a69d7d773417f70683a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322932"
---
# <a name="d3dlighttype-enumeration"></a><span data-ttu-id="82bef-103">Enumerazione D3DLIGHTTYPE</span><span class="sxs-lookup"><span data-stu-id="82bef-103">D3DLIGHTTYPE enumeration</span></span>

<span data-ttu-id="82bef-104">Definisce il tipo di luce.</span><span class="sxs-lookup"><span data-stu-id="82bef-104">Defines the light type.</span></span>

## <a name="syntax"></a><span data-ttu-id="82bef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82bef-105">Syntax</span></span>


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a><span data-ttu-id="82bef-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="82bef-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="82bef-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**Punto di D3DLIGHT \_**</span><span class="sxs-lookup"><span data-stu-id="82bef-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="82bef-108">Light è un'origine punto.</span><span class="sxs-lookup"><span data-stu-id="82bef-108">Light is a point source.</span></span> <span data-ttu-id="82bef-109">La luce ha una posizione nello spazio e irradia la luce in tutte le direzioni.</span><span class="sxs-lookup"><span data-stu-id="82bef-109">The light has a position in space and radiates light in all directions.</span></span>

</dd> <dt>

<span data-ttu-id="82bef-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**Punto di D3DLIGHT \_**</span><span class="sxs-lookup"><span data-stu-id="82bef-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="82bef-111">Light è un'origine Spotlight.</span><span class="sxs-lookup"><span data-stu-id="82bef-111">Light is a spotlight source.</span></span> <span data-ttu-id="82bef-112">Questa luce è simile a un punto chiaro, ad eccezione del fatto che l'illuminazione è limitata a un cono.</span><span class="sxs-lookup"><span data-stu-id="82bef-112">This light is like a point light, except that the illumination is limited to a cone.</span></span> <span data-ttu-id="82bef-113">Questo tipo di luce ha una direzione e diversi altri parametri che determinano la forma del cono che produce.</span><span class="sxs-lookup"><span data-stu-id="82bef-113">This light type has a direction and several other parameters that determine the shape of the cone it produces.</span></span> <span data-ttu-id="82bef-114">Per informazioni su questi parametri, vedere la struttura [**D3DLIGHT9**](d3dlight9.md) .</span><span class="sxs-lookup"><span data-stu-id="82bef-114">For information about these parameters, see the [**D3DLIGHT9**](d3dlight9.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="82bef-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**\_Direzionale D3DLIGHT**</span><span class="sxs-lookup"><span data-stu-id="82bef-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT\_DIRECTIONAL**</span></span>
</dt> <dd>

<span data-ttu-id="82bef-116">Light è una fonte di luce direzionale.</span><span class="sxs-lookup"><span data-stu-id="82bef-116">Light is a directional light source.</span></span> <span data-ttu-id="82bef-117">Equivale all'uso di una sorgente di luce puntiforme a una distanza infinita.</span><span class="sxs-lookup"><span data-stu-id="82bef-117">This is equivalent to using a point light source at an infinite distance.</span></span>

</dd> <dt>

<span data-ttu-id="82bef-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="82bef-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="82bef-119">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="82bef-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="82bef-120">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="82bef-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="82bef-121">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="82bef-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82bef-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="82bef-122">Remarks</span></span>

<span data-ttu-id="82bef-123">Le luci direzionali sono leggermente più veloci delle fonti di luce del punto, ma le luci puntiformi hanno un aspetto leggermente migliore.</span><span class="sxs-lookup"><span data-stu-id="82bef-123">Directional lights are slightly faster than point light sources, but point lights look a little better.</span></span> <span data-ttu-id="82bef-124">I faretti offrono effetti visivi interessanti, ma sono molto dispendiosi in termini di tempo.</span><span class="sxs-lookup"><span data-stu-id="82bef-124">Spotlights offer interesting visual effects but are computationally time-consuming.</span></span>

## <a name="requirements"></a><span data-ttu-id="82bef-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82bef-125">Requirements</span></span>



| <span data-ttu-id="82bef-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="82bef-126">Requirement</span></span> | <span data-ttu-id="82bef-127">Valore</span><span class="sxs-lookup"><span data-stu-id="82bef-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82bef-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82bef-128">Header</span></span><br/> | <dl> <span data-ttu-id="82bef-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="82bef-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82bef-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82bef-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82bef-131">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="82bef-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="82bef-132">**D3DLIGHT9**</span><span class="sxs-lookup"><span data-stu-id="82bef-132">**D3DLIGHT9**</span></span>](d3dlight9.md)
</dt> </dl>

 

 




