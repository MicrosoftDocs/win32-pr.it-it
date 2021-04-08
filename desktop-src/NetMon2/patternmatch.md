---
description: La struttura PATTERNMATCH definisce gli elementi del criterio utilizzati per valutare un frame.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: Struttura PATTERNMATCH (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967774"
---
# <a name="patternmatch-structure"></a><span data-ttu-id="15e48-103">Struttura PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="15e48-103">PATTERNMATCH structure</span></span>

<span data-ttu-id="15e48-104">La struttura **PATTERNMATCH** definisce gli elementi del criterio utilizzati per valutare un frame.</span><span class="sxs-lookup"><span data-stu-id="15e48-104">The **PATTERNMATCH** structure defines pattern elements used to evaluate a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e48-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15e48-105">Syntax</span></span>


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a><span data-ttu-id="15e48-106">Members</span><span class="sxs-lookup"><span data-stu-id="15e48-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="15e48-107">**Flag**</span><span class="sxs-lookup"><span data-stu-id="15e48-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="15e48-108">Flag di corrispondenza criterio:</span><span class="sxs-lookup"><span data-stu-id="15e48-108">Pattern match flags:</span></span>



| <span data-ttu-id="15e48-109">Valore</span><span class="sxs-lookup"><span data-stu-id="15e48-109">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="15e48-110">Significato</span><span class="sxs-lookup"><span data-stu-id="15e48-110">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <span data-ttu-id="15e48-111"><dt>**Modello \_ Flag di corrispondenza \_ \_ non**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="15e48-111"><dt>**PATTERN\_MATCH\_FLAGS\_NOT**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="15e48-112">Se impostato, questo flag mantiene i frame che non dispongono del modello specificato nella posizione corretta.</span><span class="sxs-lookup"><span data-stu-id="15e48-112">When set, this flag retains frames that lack the specified pattern in the proper spot.</span></span><br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <span data-ttu-id="15e48-113"><dt>**Modello \_ \_Porta flag di corrispondenza \_ \_ specificata**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="15e48-113"><dt>**PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="15e48-114">Cerca un valore del numero di porta.</span><span class="sxs-lookup"><span data-stu-id="15e48-114">Seeks a port number value.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="15e48-115">**OffsetBasis**</span><span class="sxs-lookup"><span data-stu-id="15e48-115">**OffsetBasis**</span></span>
</dt> <dd>

<span data-ttu-id="15e48-116">Tipi di offset, che possono essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="15e48-116">Types of offset, which can be one of the following:</span></span>



| <span data-ttu-id="15e48-117">Valore</span><span class="sxs-lookup"><span data-stu-id="15e48-117">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="15e48-118">Significato</span><span class="sxs-lookup"><span data-stu-id="15e48-118">Meaning</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <span data-ttu-id="15e48-119"><dt>**OFFSET \_ \_ di base rispetto \_ al \_ frame**</dt></span><span class="sxs-lookup"><span data-stu-id="15e48-119"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_FRAME**</dt></span></span> </dl>                                         | <span data-ttu-id="15e48-120">Imposta un offset, in byte, relativo all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="15e48-120">Sets an offset, in bytes, relative to start of the frame.</span></span><br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <span data-ttu-id="15e48-121"><dt>**OFFSET \_ \_ di base \_ rispetto \_ al \_ protocollo effettivo**</dt></span><span class="sxs-lookup"><span data-stu-id="15e48-121"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="15e48-122">Imposta un offset, in byte, relativo all'inizio del protocollo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="15e48-122">Sets an offset, in bytes, relative to the start of the referenced protocol.</span></span><br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <span data-ttu-id="15e48-123"><dt>**OFFSET \_ \_ di base rispetto \_ a \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="15e48-123"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IPX**</dt></span></span> </dl>                                               | <span data-ttu-id="15e48-124">Imposta un offset, in byte, solo rispetto a IPX.</span><span class="sxs-lookup"><span data-stu-id="15e48-124">Sets an offset, in bytes, only relative to IPX.</span></span><br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <span data-ttu-id="15e48-125"><dt>**OFFSET \_ \_ di base rispetto \_ all' \_ IP**</dt></span><span class="sxs-lookup"><span data-stu-id="15e48-125"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IP**</dt></span></span> </dl>                                                  | <span data-ttu-id="15e48-126">Imposta un offset, in byte, solo rispetto a IP.</span><span class="sxs-lookup"><span data-stu-id="15e48-126">Sets an offset, in bytes, only relative to IP.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="15e48-127">**Porta**</span><span class="sxs-lookup"><span data-stu-id="15e48-127">**Port**</span></span>
</dt> <dd>

<span data-ttu-id="15e48-128">Valore della porta, se specificato.</span><span class="sxs-lookup"><span data-stu-id="15e48-128">Port value, if specified.</span></span>

</dd> <dt>

<span data-ttu-id="15e48-129">**Offset**</span><span class="sxs-lookup"><span data-stu-id="15e48-129">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="15e48-130">Offset, in byte, relativo a **OffsetBasis**.</span><span class="sxs-lookup"><span data-stu-id="15e48-130">The offset, in bytes, relative to the **OffsetBasis**.</span></span>

</dd> <dt>

<span data-ttu-id="15e48-131">**Length**</span><span class="sxs-lookup"><span data-stu-id="15e48-131">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="15e48-132">Lunghezza del criterio corrispondente.</span><span class="sxs-lookup"><span data-stu-id="15e48-132">Length of the matched pattern.</span></span>

</dd> <dt>

<span data-ttu-id="15e48-133">**PatternToMatch**</span><span class="sxs-lookup"><span data-stu-id="15e48-133">**PatternToMatch**</span></span>
</dt> <dd>

<span data-ttu-id="15e48-134">Criterio di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="15e48-134">Pattern to match.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15e48-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="15e48-135">Remarks</span></span>

<span data-ttu-id="15e48-136">Questa struttura viene utilizzata per costruire un filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="15e48-136">This structure is used to construct a capture filter.</span></span> <span data-ttu-id="15e48-137">Per ulteriori informazioni sull'implementazione di questa struttura, vedere [Capture filters](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="15e48-137">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

<span data-ttu-id="15e48-138">Un filtro di acquisizione può contenere fino a quattro strutture **PATTERNMATCH** .</span><span class="sxs-lookup"><span data-stu-id="15e48-138">A capture filter can contain up to four **PATTERNMATCH** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="15e48-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15e48-139">Requirements</span></span>



| <span data-ttu-id="15e48-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="15e48-140">Requirement</span></span> | <span data-ttu-id="15e48-141">Valore</span><span class="sxs-lookup"><span data-stu-id="15e48-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="15e48-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15e48-142">Minimum supported client</span></span><br/> | <span data-ttu-id="15e48-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="15e48-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="15e48-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15e48-144">Minimum supported server</span></span><br/> | <span data-ttu-id="15e48-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="15e48-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="15e48-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15e48-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="15e48-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="15e48-147"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15e48-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15e48-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e48-149">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="15e48-149">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




