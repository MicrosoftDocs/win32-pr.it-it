---
description: Definisce se la modalità a mosaico corrente è discreta o continua.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Enumerazione D3DPATCHEDGESTYLE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886293"
---
# <a name="d3dpatchedgestyle-enumeration"></a><span data-ttu-id="48049-103">Enumerazione D3DPATCHEDGESTYLE</span><span class="sxs-lookup"><span data-stu-id="48049-103">D3DPATCHEDGESTYLE enumeration</span></span>

<span data-ttu-id="48049-104">Definisce se la modalità a mosaico corrente è discreta o continua.</span><span class="sxs-lookup"><span data-stu-id="48049-104">Defines whether the current tessellation mode is discrete or continuous.</span></span>

## <a name="syntax"></a><span data-ttu-id="48049-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48049-105">Syntax</span></span>


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a><span data-ttu-id="48049-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="48049-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="48049-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ discreto**</span><span class="sxs-lookup"><span data-stu-id="48049-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="48049-108">Stile del bordo discreto.</span><span class="sxs-lookup"><span data-stu-id="48049-108">Discrete edge style.</span></span> <span data-ttu-id="48049-109">In modalità discreta, è possibile specificare lo schema a mosaico float, ma verrà troncato in numeri interi.</span><span class="sxs-lookup"><span data-stu-id="48049-109">In discrete mode, you can specify float tessellation but it will be truncated to integers.</span></span>

</dd> <dt>

<span data-ttu-id="48049-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ continuo**</span><span class="sxs-lookup"><span data-stu-id="48049-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE\_CONTINUOUS**</span></span>
</dt> <dd>

<span data-ttu-id="48049-111">Stile bordo continuo.</span><span class="sxs-lookup"><span data-stu-id="48049-111">Continuous edge style.</span></span> <span data-ttu-id="48049-112">In modalità continua, lo schema a mosaico viene specificato come valori float che possono essere facilmente variati per ridurre gli artefatti "pop".</span><span class="sxs-lookup"><span data-stu-id="48049-112">In continuous mode, tessellation is specified as float values that can be smoothly varied to reduce "popping" artifacts.</span></span>

</dd> <dt>

<span data-ttu-id="48049-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="48049-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="48049-114">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="48049-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="48049-115">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="48049-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="48049-116">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="48049-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48049-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="48049-117">Remarks</span></span>

<span data-ttu-id="48049-118">Si noti che lo schema a mosaico continuo produce uno schema a mosaico completamente diverso da quello discreto per gli stessi valori a mosaico (questo è più evidente in modalità wireframe).</span><span class="sxs-lookup"><span data-stu-id="48049-118">Note that continuous tessellation produces a completely different tessellation pattern from the discrete one for the same tessellation values (this is more apparent in wireframe mode).</span></span> <span data-ttu-id="48049-119">Pertanto, 4,0 Continuous non è uguale a 4 discreto.</span><span class="sxs-lookup"><span data-stu-id="48049-119">Thus, 4.0 continuous is not the same as 4 discrete.</span></span>

## <a name="requirements"></a><span data-ttu-id="48049-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48049-120">Requirements</span></span>



| <span data-ttu-id="48049-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="48049-121">Requirement</span></span> | <span data-ttu-id="48049-122">Valore</span><span class="sxs-lookup"><span data-stu-id="48049-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48049-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48049-123">Header</span></span><br/> | <dl> <span data-ttu-id="48049-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="48049-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48049-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48049-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48049-126">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="48049-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




