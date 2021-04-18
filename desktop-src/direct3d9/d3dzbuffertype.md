---
description: Definisce le costanti che descrivono i formati del buffer di profondità.
ms.assetid: 5e5ce48b-8859-43e0-a9b4-5972cf6bf781
title: Enumerazione D3DZBUFFERTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DZBUFFERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 271a278f48c10a89fa6f552c3e1a7b4a83f274f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322851"
---
# <a name="d3dzbuffertype-enumeration"></a><span data-ttu-id="7b9e8-103">Enumerazione D3DZBUFFERTYPE</span><span class="sxs-lookup"><span data-stu-id="7b9e8-103">D3DZBUFFERTYPE enumeration</span></span>

<span data-ttu-id="7b9e8-104">Definisce le costanti che descrivono i formati del buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="7b9e8-104">Defines constants that describe depth-buffer formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b9e8-105">Syntax</span></span>


```C++
typedef enum D3DZBUFFERTYPE { 
  D3DZB_FALSE        = 0,
  D3DZB_TRUE         = 1,
  D3DZB_USEW         = 2,
  D3DZB_FORCE_DWORD  = 0x7fffffff
} D3DZBUFFERTYPE, *LPD3DZBUFFERTYPE;
```



## <a name="constants"></a><span data-ttu-id="7b9e8-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="7b9e8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7b9e8-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB \_ false**</span><span class="sxs-lookup"><span data-stu-id="7b9e8-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="7b9e8-108">Disabilitare il buffering di profondità.</span><span class="sxs-lookup"><span data-stu-id="7b9e8-108">Disable depth buffering.</span></span>

</dd> <dt>

<span data-ttu-id="7b9e8-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB \_ true**</span><span class="sxs-lookup"><span data-stu-id="7b9e8-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB\_TRUE**</span></span>
</dt> <dd>

<span data-ttu-id="7b9e8-110">Abilitare la memorizzazione nel buffer z.</span><span class="sxs-lookup"><span data-stu-id="7b9e8-110">Enable z-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="7b9e8-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**\_USEW D3DZB**</span><span class="sxs-lookup"><span data-stu-id="7b9e8-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB\_USEW**</span></span>
</dt> <dd>

<span data-ttu-id="7b9e8-112">Abilitare la memorizzazione nel buffer.</span><span class="sxs-lookup"><span data-stu-id="7b9e8-112">Enable w-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="7b9e8-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7b9e8-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="7b9e8-114">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="7b9e8-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="7b9e8-115">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="7b9e8-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="7b9e8-116">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7b9e8-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b9e8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b9e8-117">Remarks</span></span>

<span data-ttu-id="7b9e8-118">I membri di questo tipo enumerato vengono utilizzati con lo \_ stato di rendering ZENABLE di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="7b9e8-118">Members of this enumerated type are used with the D3DRS\_ZENABLE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b9e8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b9e8-119">Requirements</span></span>



| <span data-ttu-id="7b9e8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b9e8-120">Requirement</span></span> | <span data-ttu-id="7b9e8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7b9e8-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b9e8-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b9e8-122">Header</span></span><br/> | <dl> <span data-ttu-id="7b9e8-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b9e8-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b9e8-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b9e8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9e8-125">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="7b9e8-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="7b9e8-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="7b9e8-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
