---
description: Definisce il grado delle variabili nell'equazione che descrive una curva.
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: Enumerazione D3DDEGREETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 773ef3a8dd8fc5f4657119c2021c5723e54a3bd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322407"
---
# <a name="d3ddegreetype-enumeration"></a><span data-ttu-id="e5711-103">Enumerazione D3DDEGREETYPE</span><span class="sxs-lookup"><span data-stu-id="e5711-103">D3DDEGREETYPE enumeration</span></span>

<span data-ttu-id="e5711-104">Definisce il grado delle variabili nell'equazione che descrive una curva.</span><span class="sxs-lookup"><span data-stu-id="e5711-104">Defines the degree of the variables in the equation that describes a curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5711-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5711-105">Syntax</span></span>


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a><span data-ttu-id="e5711-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="e5711-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e5711-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE \_ lineare**</span><span class="sxs-lookup"><span data-stu-id="e5711-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="e5711-108">La curva è descritta dalle variabili del primo ordine.</span><span class="sxs-lookup"><span data-stu-id="e5711-108">Curve is described by variables of first order.</span></span>

</dd> <dt>

<span data-ttu-id="e5711-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE \_ quadratico**</span><span class="sxs-lookup"><span data-stu-id="e5711-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE\_QUADRATIC**</span></span>
</dt> <dd>

<span data-ttu-id="e5711-110">La curva è descritta dalle variabili del secondo ordine.</span><span class="sxs-lookup"><span data-stu-id="e5711-110">Curve is described by variables of second order.</span></span>

</dd> <dt>

<span data-ttu-id="e5711-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**\_Cubi D3DDEGREE**</span><span class="sxs-lookup"><span data-stu-id="e5711-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE\_CUBIC**</span></span>
</dt> <dd>

<span data-ttu-id="e5711-112">La curva è descritta dalle variabili del terzo ordine.</span><span class="sxs-lookup"><span data-stu-id="e5711-112">Curve is described by variables of third order.</span></span>

</dd> <dt>

<span data-ttu-id="e5711-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE \_ quinte**</span><span class="sxs-lookup"><span data-stu-id="e5711-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE\_QUINTIC**</span></span>
</dt> <dd>

<span data-ttu-id="e5711-114">La curva è descritta dalle variabili del quarto ordine.</span><span class="sxs-lookup"><span data-stu-id="e5711-114">Curve is described by variables of fourth order.</span></span>

</dd> <dt>

<span data-ttu-id="e5711-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e5711-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e5711-116">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="e5711-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e5711-117">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="e5711-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e5711-118">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e5711-118">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5711-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5711-119">Remarks</span></span>

<span data-ttu-id="e5711-120">I valori di questa enumerazione vengono utilizzati per descrivere le curve utilizzate dalle patch rettangolari e di triangolo.</span><span class="sxs-lookup"><span data-stu-id="e5711-120">The values in this enumeration are used to describe the curves used by rectangle and triangle patches.</span></span> <span data-ttu-id="e5711-121">Per ulteriori informazioni, vedere D3DRS \_ CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="e5711-121">For more information, see D3DRS\_CULLMODE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5711-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5711-122">Requirements</span></span>



| <span data-ttu-id="e5711-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5711-123">Requirement</span></span> | <span data-ttu-id="e5711-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e5711-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5711-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5711-125">Header</span></span><br/> | <dl> <span data-ttu-id="e5711-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5711-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5711-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5711-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5711-128">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="e5711-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="e5711-129">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="e5711-129">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="e5711-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="e5711-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
