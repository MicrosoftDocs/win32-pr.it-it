---
description: Definisce le operazioni del buffer di stencil.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: Enumerazione D3DSTENCILOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTENCILOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 34784a57d3afd3862d380554040f3909ec905898
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322439"
---
# <a name="d3dstencilop-enumeration"></a><span data-ttu-id="5c92f-103">Enumerazione D3DSTENCILOP</span><span class="sxs-lookup"><span data-stu-id="5c92f-103">D3DSTENCILOP enumeration</span></span>

<span data-ttu-id="5c92f-104">Definisce le operazioni del buffer di stencil.</span><span class="sxs-lookup"><span data-stu-id="5c92f-104">Defines stencil-buffer operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c92f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c92f-105">Syntax</span></span>


```C++
typedef enum D3DSTENCILOP { 
  D3DSTENCILOP_KEEP         = 1,
  D3DSTENCILOP_ZERO         = 2,
  D3DSTENCILOP_REPLACE      = 3,
  D3DSTENCILOP_INCRSAT      = 4,
  D3DSTENCILOP_DECRSAT      = 5,
  D3DSTENCILOP_INVERT       = 6,
  D3DSTENCILOP_INCR         = 7,
  D3DSTENCILOP_DECR         = 8,
  D3DSTENCILOP_FORCE_DWORD  = 0x7fffffff
} D3DSTENCILOP, *LPD3DSTENCILOP;
```



## <a name="constants"></a><span data-ttu-id="5c92f-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="5c92f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5c92f-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ Keep**</span><span class="sxs-lookup"><span data-stu-id="5c92f-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP\_KEEP**</span></span>
</dt> <dd>

<span data-ttu-id="5c92f-108">Non aggiornare la voce nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="5c92f-108">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="5c92f-109">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5c92f-109">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="5c92f-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ zero**</span><span class="sxs-lookup"><span data-stu-id="5c92f-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="5c92f-111">Impostare la voce stencil-buffer su 0.</span><span class="sxs-lookup"><span data-stu-id="5c92f-111">Set the stencil-buffer entry to 0.</span></span>

</dd> <dt>

<span data-ttu-id="5c92f-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ Sostituisci**</span><span class="sxs-lookup"><span data-stu-id="5c92f-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP\_REPLACE**</span></span>
</dt> <dd>

<span data-ttu-id="5c92f-113">Sostituire la voce dello stencil buffer con un valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="5c92f-113">Replace the stencil-buffer entry with a reference value.</span></span>

</dd> <dt>

<span data-ttu-id="5c92f-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**\_INCRSAT D3DSTENCILOP**</span><span class="sxs-lookup"><span data-stu-id="5c92f-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP\_INCRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="5c92f-115">Incrementa la voce dello stencil buffer, bloccando il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="5c92f-115">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="5c92f-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**\_DECRSAT D3DSTENCILOP**</span><span class="sxs-lookup"><span data-stu-id="5c92f-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP\_DECRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="5c92f-117">Decrementa la voce del buffer di stencil, che viene fissata a zero.</span><span class="sxs-lookup"><span data-stu-id="5c92f-117">Decrement the stencil-buffer entry, clamping to zero.</span></span>

</dd> <dt>

<span data-ttu-id="5c92f-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP \_ invertito**</span><span class="sxs-lookup"><span data-stu-id="5c92f-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP\_INVERT**</span></span>
</dt> <dd>

<span data-ttu-id="5c92f-119">Inverti i bit nella voce dello stencil buffer.</span><span class="sxs-lookup"><span data-stu-id="5c92f-119">Invert the bits in the stencil-buffer entry.</span></span>

</dd> <dt>

<span data-ttu-id="5c92f-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**\_Incr D3DSTENCILOP**</span><span class="sxs-lookup"><span data-stu-id="5c92f-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP\_INCR**</span></span>
</dt> <dd>

<span data-ttu-id="5c92f-121">Incrementa la voce dello stencil buffer, eseguendo il wrapping su zero se il nuovo valore supera il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="5c92f-121">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="5c92f-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**\_Decr D3DSTENCILOP**</span><span class="sxs-lookup"><span data-stu-id="5c92f-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP\_DECR**</span></span>
</dt> <dd>

<span data-ttu-id="5c92f-123">Decrementa la voce dello stencil buffer, eseguendo il wrapping fino al valore massimo se il nuovo valore è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="5c92f-123">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span>

</dd> <dt>

<span data-ttu-id="5c92f-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5c92f-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="5c92f-125">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="5c92f-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="5c92f-126">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="5c92f-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="5c92f-127">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="5c92f-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c92f-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c92f-128">Remarks</span></span>

<span data-ttu-id="5c92f-129">Gli stencil: le voci del buffer sono valori integer compresi tra 0 e 2 Grigioni-1, dove n è la profondità di bit del buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="5c92f-129">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c92f-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c92f-130">Requirements</span></span>



| <span data-ttu-id="5c92f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c92f-131">Requirement</span></span> | <span data-ttu-id="5c92f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="5c92f-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c92f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c92f-133">Header</span></span><br/> | <dl> <span data-ttu-id="5c92f-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c92f-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c92f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c92f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c92f-136">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="5c92f-136">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




