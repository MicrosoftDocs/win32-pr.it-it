---
description: Definisce le funzioni di confronto supportate.
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: Enumerazione D3DCMPFUNC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCMPFUNC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e49f0e058e795e00349020619f1e6d6310dfd94f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886273"
---
# <a name="d3dcmpfunc-enumeration"></a><span data-ttu-id="29948-103">Enumerazione D3DCMPFUNC</span><span class="sxs-lookup"><span data-stu-id="29948-103">D3DCMPFUNC enumeration</span></span>

<span data-ttu-id="29948-104">Definisce le funzioni di confronto supportate.</span><span class="sxs-lookup"><span data-stu-id="29948-104">Defines the supported compare functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="29948-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29948-105">Syntax</span></span>


```C++
typedef enum D3DCMPFUNC { 
  D3DCMP_NEVER         = 1,
  D3DCMP_LESS          = 2,
  D3DCMP_EQUAL         = 3,
  D3DCMP_LESSEQUAL     = 4,
  D3DCMP_GREATER       = 5,
  D3DCMP_NOTEQUAL      = 6,
  D3DCMP_GREATEREQUAL  = 7,
  D3DCMP_ALWAYS        = 8,
  D3DCMP_FORCE_DWORD   = 0x7fffffff
} D3DCMPFUNC, *LPD3DCMPFUNC;
```



## <a name="constants"></a><span data-ttu-id="29948-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="29948-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="29948-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ mai**</span><span class="sxs-lookup"><span data-stu-id="29948-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP\_NEVER**</span></span>
</dt> <dd>

<span data-ttu-id="29948-108">Interrompi sempre il test.</span><span class="sxs-lookup"><span data-stu-id="29948-108">Always fail the test.</span></span>

</dd> <dt>

<span data-ttu-id="29948-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ less**</span><span class="sxs-lookup"><span data-stu-id="29948-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP\_LESS**</span></span>
</dt> <dd>

<span data-ttu-id="29948-110">Accettare il nuovo pixel se il relativo valore è minore del valore del pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="29948-110">Accept the new pixel if its value is less than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="29948-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP \_ uguale a**</span><span class="sxs-lookup"><span data-stu-id="29948-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="29948-112">Accettare il nuovo pixel se il relativo valore è uguale al valore del pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="29948-112">Accept the new pixel if its value equals the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="29948-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**\_LESSEQUAL D3DCMP**</span><span class="sxs-lookup"><span data-stu-id="29948-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP\_LESSEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="29948-114">Accettare il nuovo pixel se il relativo valore è minore o uguale al valore del pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="29948-114">Accept the new pixel if its value is less than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="29948-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ maggiore**</span><span class="sxs-lookup"><span data-stu-id="29948-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP\_GREATER**</span></span>
</dt> <dd>

<span data-ttu-id="29948-116">Accettare il nuovo pixel se il relativo valore è maggiore del valore del pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="29948-116">Accept the new pixel if its value is greater than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="29948-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**\_NOTEQUAL D3DCMP**</span><span class="sxs-lookup"><span data-stu-id="29948-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP\_NOTEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="29948-118">Accettare il nuovo pixel se il valore non è uguale al valore del pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="29948-118">Accept the new pixel if its value does not equal the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="29948-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**\_GREATEREQUAL D3DCMP**</span><span class="sxs-lookup"><span data-stu-id="29948-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP\_GREATEREQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="29948-120">Accettare il nuovo pixel se il relativo valore è maggiore o uguale al valore del pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="29948-120">Accept the new pixel if its value is greater than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="29948-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP \_ sempre**</span><span class="sxs-lookup"><span data-stu-id="29948-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP\_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="29948-122">Superare sempre il test.</span><span class="sxs-lookup"><span data-stu-id="29948-122">Always pass the test.</span></span>

</dd> <dt>

<span data-ttu-id="29948-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="29948-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="29948-124">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="29948-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="29948-125">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="29948-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="29948-126">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="29948-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29948-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="29948-127">Remarks</span></span>

<span data-ttu-id="29948-128">I valori in questo tipo enumerato definiscono le funzioni di confronto supportate per gli \_ Stati di rendering D3DRS ZFUNC, D3DRS \_ ALPHAFUNC e D3DRS \_ STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="29948-128">The values in this enumerated type define the supported compare functions for the D3DRS\_ZFUNC, D3DRS\_ALPHAFUNC, and D3DRS\_STENCILFUNC render states.</span></span>

## <a name="requirements"></a><span data-ttu-id="29948-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29948-129">Requirements</span></span>



| <span data-ttu-id="29948-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="29948-130">Requirement</span></span> | <span data-ttu-id="29948-131">Valore</span><span class="sxs-lookup"><span data-stu-id="29948-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29948-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29948-132">Header</span></span><br/> | <dl> <span data-ttu-id="29948-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="29948-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29948-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29948-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29948-135">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="29948-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="29948-136">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="29948-136">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
