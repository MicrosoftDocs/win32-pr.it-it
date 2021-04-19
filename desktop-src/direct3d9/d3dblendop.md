---
description: Definisce le operazioni di Blend supportate. Per le definizioni dei termini, vedere la sezione Osservazioni.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: Enumerazione D3DBLENDOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322377"
---
# <a name="d3dblendop-enumeration"></a><span data-ttu-id="abfc1-104">Enumerazione D3DBLENDOP</span><span class="sxs-lookup"><span data-stu-id="abfc1-104">D3DBLENDOP enumeration</span></span>

<span data-ttu-id="abfc1-105">Definisce le operazioni di Blend supportate.</span><span class="sxs-lookup"><span data-stu-id="abfc1-105">Defines the supported blend operations.</span></span> <span data-ttu-id="abfc1-106">Per le definizioni dei termini, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="abfc1-106">See Remarks for definitions of terms.</span></span>

## <a name="syntax"></a><span data-ttu-id="abfc1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abfc1-107">Syntax</span></span>


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a><span data-ttu-id="abfc1-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="abfc1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="abfc1-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ aggiungere**</span><span class="sxs-lookup"><span data-stu-id="abfc1-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="abfc1-110">Il risultato è la destinazione aggiunta all'origine.</span><span class="sxs-lookup"><span data-stu-id="abfc1-110">The result is the destination added to the source.</span></span> <span data-ttu-id="abfc1-111">Risultato = origine + destinazione</span><span class="sxs-lookup"><span data-stu-id="abfc1-111">Result = Source + Destination</span></span>

</dd> <dt>

<span data-ttu-id="abfc1-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**\_Sottrazione D3DBLENDOP**</span><span class="sxs-lookup"><span data-stu-id="abfc1-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="abfc1-113">Il risultato è la destinazione sottratta da all'origine.</span><span class="sxs-lookup"><span data-stu-id="abfc1-113">The result is the destination subtracted from to the source.</span></span> <span data-ttu-id="abfc1-114">Risultato = origine-destinazione</span><span class="sxs-lookup"><span data-stu-id="abfc1-114">Result = Source - Destination</span></span>

</dd> <dt>

<span data-ttu-id="abfc1-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**\_REVSUBTRACT D3DBLENDOP**</span><span class="sxs-lookup"><span data-stu-id="abfc1-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP\_REVSUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="abfc1-116">Il risultato è l'origine sottratta dalla destinazione.</span><span class="sxs-lookup"><span data-stu-id="abfc1-116">The result is the source subtracted from the destination.</span></span> <span data-ttu-id="abfc1-117">Risultato = destinazione-origine</span><span class="sxs-lookup"><span data-stu-id="abfc1-117">Result = Destination - Source</span></span>

</dd> <dt>

<span data-ttu-id="abfc1-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ min**</span><span class="sxs-lookup"><span data-stu-id="abfc1-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="abfc1-119">Il risultato è il valore minimo dell'origine e della destinazione.</span><span class="sxs-lookup"><span data-stu-id="abfc1-119">The result is the minimum of the source and destination.</span></span> <span data-ttu-id="abfc1-120">Risultato = MIN (origine, destinazione)</span><span class="sxs-lookup"><span data-stu-id="abfc1-120">Result = MIN(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="abfc1-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ Max**</span><span class="sxs-lookup"><span data-stu-id="abfc1-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="abfc1-122">Il risultato è il valore massimo dell'origine e della destinazione.</span><span class="sxs-lookup"><span data-stu-id="abfc1-122">The result is the maximum of the source and destination.</span></span> <span data-ttu-id="abfc1-123">Risultato = MAX (origine, destinazione)</span><span class="sxs-lookup"><span data-stu-id="abfc1-123">Result = MAX(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="abfc1-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="abfc1-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="abfc1-125">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="abfc1-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="abfc1-126">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="abfc1-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="abfc1-127">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="abfc1-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abfc1-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="abfc1-128">Remarks</span></span>

<span data-ttu-id="abfc1-129">L'origine, la destinazione e il risultato sono definiti come segue:</span><span class="sxs-lookup"><span data-stu-id="abfc1-129">Source, Destination, and Result are defined as:</span></span>



| <span data-ttu-id="abfc1-130">Termine</span><span class="sxs-lookup"><span data-stu-id="abfc1-130">Term</span></span>        | <span data-ttu-id="abfc1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="abfc1-131">Type</span></span>   | <span data-ttu-id="abfc1-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abfc1-132">Description</span></span>                                                            |
|-------------|--------|------------------------------------------------------------------------|
| <span data-ttu-id="abfc1-133">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="abfc1-133">Source</span></span>      | <span data-ttu-id="abfc1-134">Input</span><span class="sxs-lookup"><span data-stu-id="abfc1-134">Input</span></span>  | <span data-ttu-id="abfc1-135">Colore del pixel di origine prima dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="abfc1-135">Color of the source pixel before the operation.</span></span>                        |
| <span data-ttu-id="abfc1-136">Destination</span><span class="sxs-lookup"><span data-stu-id="abfc1-136">Destination</span></span> | <span data-ttu-id="abfc1-137">Input</span><span class="sxs-lookup"><span data-stu-id="abfc1-137">Input</span></span>  | <span data-ttu-id="abfc1-138">Colore del pixel nel buffer di destinazione prima dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="abfc1-138">Color of the pixel in the destination buffer before the operation.</span></span>     |
| <span data-ttu-id="abfc1-139">Risultato</span><span class="sxs-lookup"><span data-stu-id="abfc1-139">Result</span></span>      | <span data-ttu-id="abfc1-140">Output</span><span class="sxs-lookup"><span data-stu-id="abfc1-140">Output</span></span> | <span data-ttu-id="abfc1-141">Valore restituito che rappresenta il colore sfumato risultante dall'operazione.</span><span class="sxs-lookup"><span data-stu-id="abfc1-141">Returned value that is the blended color resulting from the operation.</span></span> |



 

<span data-ttu-id="abfc1-142">Questo tipo enumerato definisce i valori utilizzati dagli Stati di rendering seguenti:</span><span class="sxs-lookup"><span data-stu-id="abfc1-142">This enumerated type defines values used by the following render states:</span></span>

-   <span data-ttu-id="abfc1-143">\_BLENDOP D3DRS</span><span class="sxs-lookup"><span data-stu-id="abfc1-143">D3DRS\_BLENDOP</span></span>
-   <span data-ttu-id="abfc1-144">\_BLENDOPALPHA D3DRS</span><span class="sxs-lookup"><span data-stu-id="abfc1-144">D3DRS\_BLENDOPALPHA</span></span>

## <a name="requirements"></a><span data-ttu-id="abfc1-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abfc1-145">Requirements</span></span>



| <span data-ttu-id="abfc1-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="abfc1-146">Requirement</span></span> | <span data-ttu-id="abfc1-147">Valore</span><span class="sxs-lookup"><span data-stu-id="abfc1-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abfc1-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abfc1-148">Header</span></span><br/> | <dl> <span data-ttu-id="abfc1-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="abfc1-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abfc1-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abfc1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abfc1-151">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="abfc1-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="abfc1-152">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="abfc1-152">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="abfc1-153">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="abfc1-153">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
