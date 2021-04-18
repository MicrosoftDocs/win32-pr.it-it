---
description: Definisce la posizione in cui è necessario accedere a un componente color o color per i calcoli di illuminazione.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: Enumerazione D3DMATERIALCOLORSOURCE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8877eece8e33c6508768b22c989e992cf8178823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322928"
---
# <a name="d3dmaterialcolorsource-enumeration"></a><span data-ttu-id="52446-103">Enumerazione D3DMATERIALCOLORSOURCE</span><span class="sxs-lookup"><span data-stu-id="52446-103">D3DMATERIALCOLORSOURCE enumeration</span></span>

<span data-ttu-id="52446-104">Definisce la posizione in cui è necessario accedere a un componente color o color per i calcoli di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="52446-104">Defines the location at which a color or color component must be accessed for lighting calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="52446-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52446-105">Syntax</span></span>


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a><span data-ttu-id="52446-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="52446-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="52446-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**\_Materiale D3DMCS**</span><span class="sxs-lookup"><span data-stu-id="52446-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS\_MATERIAL**</span></span>
</dt> <dd>

<span data-ttu-id="52446-108">Usare il colore dal materiale corrente.</span><span class="sxs-lookup"><span data-stu-id="52446-108">Use the color from the current material.</span></span>

</dd> <dt>

<span data-ttu-id="52446-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**\_COLOR1 D3DMCS**</span><span class="sxs-lookup"><span data-stu-id="52446-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS\_COLOR1**</span></span>
</dt> <dd>

<span data-ttu-id="52446-110">Usare il colore del vertice diffuso.</span><span class="sxs-lookup"><span data-stu-id="52446-110">Use the diffuse vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="52446-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**\_Color2 D3DMCS**</span><span class="sxs-lookup"><span data-stu-id="52446-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS\_COLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="52446-112">Usare il colore del vertice speculare.</span><span class="sxs-lookup"><span data-stu-id="52446-112">Use the specular vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="52446-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="52446-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="52446-114">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="52446-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="52446-115">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="52446-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="52446-116">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="52446-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52446-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="52446-117">Remarks</span></span>

<span data-ttu-id="52446-118">Questi flag vengono utilizzati per impostare il valore degli Stati di rendering seguenti nel tipo enumerato [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="52446-118">These flags are used to set the value of the following render states in the [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type.</span></span>

-   <span data-ttu-id="52446-119">\_AMBIENTMATERIALSOURCE D3DRS</span><span class="sxs-lookup"><span data-stu-id="52446-119">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="52446-120">\_DIFFUSEMATERIALSOURCE D3DRS</span><span class="sxs-lookup"><span data-stu-id="52446-120">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="52446-121">\_EMISSIVEMATERIALSOURCE D3DRS</span><span class="sxs-lookup"><span data-stu-id="52446-121">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>
-   <span data-ttu-id="52446-122">\_SPECULARMATERIALSOURCE D3DRS</span><span class="sxs-lookup"><span data-stu-id="52446-122">D3DRS\_SPECULARMATERIALSOURCE</span></span>

## <a name="requirements"></a><span data-ttu-id="52446-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52446-123">Requirements</span></span>



| <span data-ttu-id="52446-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="52446-124">Requirement</span></span> | <span data-ttu-id="52446-125">Valore</span><span class="sxs-lookup"><span data-stu-id="52446-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52446-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52446-126">Header</span></span><br/> | <dl> <span data-ttu-id="52446-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="52446-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52446-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52446-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52446-129">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="52446-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="52446-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="52446-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
