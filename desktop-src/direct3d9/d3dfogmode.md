---
description: Definisce le costanti che descrivono la modalità di nebbia.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Enumerazione D3DFOGMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355239"
---
# <a name="d3dfogmode-enumeration"></a><span data-ttu-id="c33c5-103">Enumerazione D3DFOGMODE</span><span class="sxs-lookup"><span data-stu-id="c33c5-103">D3DFOGMODE enumeration</span></span>

<span data-ttu-id="c33c5-104">Definisce le costanti che descrivono la modalità di nebbia.</span><span class="sxs-lookup"><span data-stu-id="c33c5-104">Defines constants that describe the fog mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c33c5-105">Syntax</span></span>


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a><span data-ttu-id="c33c5-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="c33c5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c33c5-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ None**</span><span class="sxs-lookup"><span data-stu-id="c33c5-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="c33c5-108">Nessun effetto di nebbia.</span><span class="sxs-lookup"><span data-stu-id="c33c5-108">No fog effect.</span></span>

</dd> <dt>

<span data-ttu-id="c33c5-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ Exp**</span><span class="sxs-lookup"><span data-stu-id="c33c5-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG\_EXP**</span></span>
</dt> <dd>

<span data-ttu-id="c33c5-110">L'effetto nebbia si intensifica in modo esponenziale in base alla formula seguente.</span><span class="sxs-lookup"><span data-stu-id="c33c5-110">Fog effect intensifies exponentially, according to the following formula.</span></span>

![formula dell'intensità dell'effetto nebbia](images/fogexp.png)

</dd> <dt>

<span data-ttu-id="c33c5-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**\_Exp2 D3DFOG**</span><span class="sxs-lookup"><span data-stu-id="c33c5-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG\_EXP2**</span></span>
</dt> <dd>

<span data-ttu-id="c33c5-113">L'effetto nebbia si intensifica in modo esponenziale con il quadrato della distanza in base alla formula seguente.</span><span class="sxs-lookup"><span data-stu-id="c33c5-113">Fog effect intensifies exponentially with the square of the distance, according to the following formula.</span></span>

![formula dell'intensità dell'effetto nebbia basata sul quadrato della distanza](images/fogexp2.png)

</dd> <dt>

<span data-ttu-id="c33c5-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ lineare**</span><span class="sxs-lookup"><span data-stu-id="c33c5-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="c33c5-116">L'effetto nebbia si intensifica in modo lineare tra i punti di inizio e di fine, in base alla formula seguente.</span><span class="sxs-lookup"><span data-stu-id="c33c5-116">Fog effect intensifies linearly between the start and end points, according to the following formula.</span></span>

![formula dell'intensità dell'effetto nebbia in base ai punti iniziale e finale](images/fogliner.png)

<span data-ttu-id="c33c5-118">Questa è l'unica modalità di nebbia attualmente supportata.</span><span class="sxs-lookup"><span data-stu-id="c33c5-118">This is the only fog mode currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="c33c5-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c33c5-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c33c5-120">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c33c5-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c33c5-121">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c33c5-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c33c5-122">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c33c5-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c33c5-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c33c5-123">Remarks</span></span>

<span data-ttu-id="c33c5-124">I valori in questo tipo enumerato vengono usati dagli Stati di \_ rendering D3DRS FOGTABLEMODE e D3DRS \_ FOGVERTEXMODE.</span><span class="sxs-lookup"><span data-stu-id="c33c5-124">The values in this enumerated type are used by the D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states.</span></span>

<span data-ttu-id="c33c5-125">La nebbia può essere considerata una misura di visibilità: più basso è il valore di nebbia prodotto da un'equazione di nebbia, minore è la visibilità di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c33c5-125">Fog can be considered a measure of visibility: the lower the fog value produced by a fog equation, the less visible an object is.</span></span>

## <a name="requirements"></a><span data-ttu-id="c33c5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c33c5-126">Requirements</span></span>



| <span data-ttu-id="c33c5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c33c5-127">Requirement</span></span> | <span data-ttu-id="c33c5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c33c5-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c33c5-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c33c5-129">Header</span></span><br/> | <dl> <span data-ttu-id="c33c5-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c33c5-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c33c5-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c33c5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33c5-132">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="c33c5-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="c33c5-133">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="c33c5-133">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
