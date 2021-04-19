---
description: Definisce le modalità di eliminazione supportate.
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: Enumerazione D3DCULL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e88aa1baf86b2b03177cc686bf83299311065283
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322365"
---
# <a name="d3dcull-enumeration"></a><span data-ttu-id="42c52-103">Enumerazione D3DCULL</span><span class="sxs-lookup"><span data-stu-id="42c52-103">D3DCULL enumeration</span></span>

<span data-ttu-id="42c52-104">Definisce le modalità di eliminazione supportate.</span><span class="sxs-lookup"><span data-stu-id="42c52-104">Defines the supported culling modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c52-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42c52-105">Syntax</span></span>


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a><span data-ttu-id="42c52-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="42c52-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="42c52-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ None**</span><span class="sxs-lookup"><span data-stu-id="42c52-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="42c52-108">Non eliminare i visi indietro.</span><span class="sxs-lookup"><span data-stu-id="42c52-108">Do not cull back faces.</span></span>

</dd> <dt>

<span data-ttu-id="42c52-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL \_ CW**</span><span class="sxs-lookup"><span data-stu-id="42c52-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="42c52-110">Riattivazione dei visi con vertici in senso orario.</span><span class="sxs-lookup"><span data-stu-id="42c52-110">Cull back faces with clockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="42c52-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL \_ CCW**</span><span class="sxs-lookup"><span data-stu-id="42c52-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL\_CCW**</span></span>
</dt> <dd>

<span data-ttu-id="42c52-112">Eliminare i volti indietro con vertici in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="42c52-112">Cull back faces with counterclockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="42c52-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="42c52-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="42c52-114">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="42c52-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="42c52-115">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="42c52-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="42c52-116">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="42c52-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42c52-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="42c52-117">Remarks</span></span>

<span data-ttu-id="42c52-118">I valori in questo tipo enumerato vengono usati dallo stato di \_ rendering CULLMODE di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="42c52-118">The values in this enumerated type are used by the D3DRS\_CULLMODE render state.</span></span> <span data-ttu-id="42c52-119">Le modalità di eliminazione definiscono la modalità di eliminazione delle facce posteriori durante il rendering di una geometria.</span><span class="sxs-lookup"><span data-stu-id="42c52-119">The culling modes define how back faces are culled when rendering a geometry.</span></span>

## <a name="requirements"></a><span data-ttu-id="42c52-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42c52-120">Requirements</span></span>



| <span data-ttu-id="42c52-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="42c52-121">Requirement</span></span> | <span data-ttu-id="42c52-122">Valore</span><span class="sxs-lookup"><span data-stu-id="42c52-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42c52-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42c52-123">Header</span></span><br/> | <dl> <span data-ttu-id="42c52-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="42c52-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42c52-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42c52-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c52-126">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="42c52-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="42c52-127">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="42c52-127">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="42c52-128">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="42c52-128">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
