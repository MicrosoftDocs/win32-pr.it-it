---
description: Definisce i token di monitoraggio di debug.
ms.assetid: c0df4c9f-a232-45cf-b543-e95ee84a4a8d
title: Enumerazione D3DDEBUGMONITORTOKENS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEBUGMONITORTOKENS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 82c3ecfa7d197e1ab912dbafe0d26fcb2281e605
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969318"
---
# <a name="d3ddebugmonitortokens-enumeration"></a><span data-ttu-id="14e11-103">Enumerazione D3DDEBUGMONITORTOKENS</span><span class="sxs-lookup"><span data-stu-id="14e11-103">D3DDEBUGMONITORTOKENS enumeration</span></span>

<span data-ttu-id="14e11-104">Definisce i token di monitoraggio di debug.</span><span class="sxs-lookup"><span data-stu-id="14e11-104">Defines the debug monitor tokens.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e11-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14e11-105">Syntax</span></span>


```C++
typedef enum D3DDEBUGMONITORTOKENS { 
  D3DDMT_ENABLE       = 0,
  D3DDMT_DISABLE      = 1,
  D3DDMT_FORCE_DWORD  = 0x7fffffff
} D3DDEBUGMONITORTOKENS, *LPD3DDEBUGMONITORTOKENS;
```



## <a name="constants"></a><span data-ttu-id="14e11-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="14e11-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="14e11-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**\_Abilitazione di D3DDMT**</span><span class="sxs-lookup"><span data-stu-id="14e11-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="14e11-108">Abilitare il monitoraggio del debug.</span><span class="sxs-lookup"><span data-stu-id="14e11-108">Enable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="14e11-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**\_Disabilitazione D3DDMT**</span><span class="sxs-lookup"><span data-stu-id="14e11-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="14e11-110">Disabilitare il monitoraggio di debug.</span><span class="sxs-lookup"><span data-stu-id="14e11-110">Disable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="14e11-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="14e11-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="14e11-112">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="14e11-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="14e11-113">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="14e11-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="14e11-114">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="14e11-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14e11-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="14e11-115">Remarks</span></span>

<span data-ttu-id="14e11-116">I valori in questo tipo enumerato vengono usati dallo stato di \_ rendering DEBUGMONITORTOKEN di D3DRS e sono rilevanti solo per le compilazioni di debug.</span><span class="sxs-lookup"><span data-stu-id="14e11-116">The values in this enumerated type are used by the D3DRS\_DEBUGMONITORTOKEN render state and are only relevant for debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="14e11-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14e11-117">Requirements</span></span>



| <span data-ttu-id="14e11-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="14e11-118">Requirement</span></span> | <span data-ttu-id="14e11-119">Valore</span><span class="sxs-lookup"><span data-stu-id="14e11-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14e11-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14e11-120">Header</span></span><br/> | <dl> <span data-ttu-id="14e11-121"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="14e11-121"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14e11-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14e11-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e11-123">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="14e11-123">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="14e11-124">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="14e11-124">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
