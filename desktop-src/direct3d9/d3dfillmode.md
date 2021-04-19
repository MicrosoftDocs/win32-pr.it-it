---
description: Definisce le costanti che descrivono la modalità di riempimento.
ms.assetid: be835432-e8d5-4afb-a810-2dac25bdc9dc
title: Enumerazione D3DFILLMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFILLMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 33cf03258933055aa18aecb42fffe4d8f33b1e51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323759"
---
# <a name="d3dfillmode-enumeration"></a><span data-ttu-id="f5549-103">Enumerazione D3DFILLMODE</span><span class="sxs-lookup"><span data-stu-id="f5549-103">D3DFILLMODE enumeration</span></span>

<span data-ttu-id="f5549-104">Definisce le costanti che descrivono la modalità di riempimento.</span><span class="sxs-lookup"><span data-stu-id="f5549-104">Defines constants describing the fill mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5549-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5549-105">Syntax</span></span>


```C++
typedef enum D3DFILLMODE { 
  D3DFILL_POINT        = 1,
  D3DFILL_WIREFRAME    = 2,
  D3DFILL_SOLID        = 3,
  D3DFILL_FORCE_DWORD  = 0x7fffffff
} D3DFILLMODE, *LPD3DFILLMODE;
```



## <a name="constants"></a><span data-ttu-id="f5549-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="f5549-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f5549-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**Punto di D3DFILL \_**</span><span class="sxs-lookup"><span data-stu-id="f5549-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**D3DFILL\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="f5549-108">Punti di riempimento.</span><span class="sxs-lookup"><span data-stu-id="f5549-108">Fill points.</span></span>

</dd> <dt>

<span data-ttu-id="f5549-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**\_Wireframe D3DFILL**</span><span class="sxs-lookup"><span data-stu-id="f5549-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL\_WIREFRAME**</span></span>
</dt> <dd>

<span data-ttu-id="f5549-110">Inserire i wireframe.</span><span class="sxs-lookup"><span data-stu-id="f5549-110">Fill wireframes.</span></span>

</dd> <dt>

<span data-ttu-id="f5549-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL \_ Solid**</span><span class="sxs-lookup"><span data-stu-id="f5549-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL\_SOLID**</span></span>
</dt> <dd>

<span data-ttu-id="f5549-112">Riempire i solidi.</span><span class="sxs-lookup"><span data-stu-id="f5549-112">Fill solids.</span></span>

</dd> <dt>

<span data-ttu-id="f5549-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f5549-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f5549-114">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f5549-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f5549-115">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f5549-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f5549-116">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f5549-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5549-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5549-117">Remarks</span></span>

<span data-ttu-id="f5549-118">I valori in questo tipo enumerato vengono usati dallo stato di \_ rendering FillMode di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="f5549-118">The values in this enumerated type are used by the D3DRS\_FILLMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5549-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5549-119">Requirements</span></span>



| <span data-ttu-id="f5549-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5549-120">Requirement</span></span> | <span data-ttu-id="f5549-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f5549-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5549-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5549-122">Header</span></span><br/> | <dl> <span data-ttu-id="f5549-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5549-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5549-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5549-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5549-125">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="f5549-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="f5549-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="f5549-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
