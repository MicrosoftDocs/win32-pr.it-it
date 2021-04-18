---
description: La struttura CAPTUREFILTER contiene i dati del filtro di acquisizione.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Struttura CAPTUREFILTER (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314185"
---
# <a name="capturefilter-structure"></a><span data-ttu-id="d1af9-103">Struttura CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="d1af9-103">CAPTUREFILTER structure</span></span>

<span data-ttu-id="d1af9-104">La struttura **capturefilter** contiene i dati del filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d1af9-104">The **CAPTUREFILTER** structure contains capture filter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1af9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1af9-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a><span data-ttu-id="d1af9-106">Members</span><span class="sxs-lookup"><span data-stu-id="d1af9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d1af9-107">**FilterFlags**</span><span class="sxs-lookup"><span data-stu-id="d1af9-107">**FilterFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d1af9-108">Flag che descrivono il contenuto del filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d1af9-108">Flags that describe the contents of the capture filter.</span></span>



| <span data-ttu-id="d1af9-109">Valore</span><span class="sxs-lookup"><span data-stu-id="d1af9-109">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="d1af9-110">Significato</span><span class="sxs-lookup"><span data-stu-id="d1af9-110">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <span data-ttu-id="d1af9-111"><dt>**Capturefilter \_ \_I flag includono \_ tutti i \_ succhi**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="d1af9-111"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS**</dt> <dt>0x0001</dt></span></span> </dl>       | <span data-ttu-id="d1af9-112">Include tutti i succhi come frame accettabili.</span><span class="sxs-lookup"><span data-stu-id="d1af9-112">Includes all SAPs as acceptable frames.</span></span><br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <span data-ttu-id="d1af9-113"><dt>**Capturefilter \_ \_I flag includono \_ tutti \_ etype del**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="d1af9-113"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="d1af9-114">Includere tutti i ETYPE del come frame accettabili.</span><span class="sxs-lookup"><span data-stu-id="d1af9-114">Include all Etypes as acceptable frames.</span></span><br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <span data-ttu-id="d1af9-115"><dt>**Capturefilter \_ CONTRASSEGNA \_ \_ solo**</dt> <dt>0x0008</dt> locali</span><span class="sxs-lookup"><span data-stu-id="d1af9-115"><dt>**CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY**</dt> <dt>0x0008</dt></span></span> </dl>                          | <span data-ttu-id="d1af9-116">Nessuna modalità P</span><span class="sxs-lookup"><span data-stu-id="d1af9-116">No P-mode</span></span><br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <span data-ttu-id="d1af9-117"><dt>**Capturefilter \_ FLAG \_ Keep \_**</dt> <dt>0x0020</dt> RAW</span><span class="sxs-lookup"><span data-stu-id="d1af9-117"><dt>**CAPTUREFILTER\_FLAGS\_KEEP\_RAW**</dt> <dt>0x0020</dt></span></span> </dl>                                | <span data-ttu-id="d1af9-118">Mantieni i frame MAC SMT e token ring.</span><span class="sxs-lookup"><span data-stu-id="d1af9-118">Keep SMT and token ring MAC frames.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="d1af9-119">**lpSapTable**</span><span class="sxs-lookup"><span data-stu-id="d1af9-119">**lpSapTable**</span></span>
</dt> <dd>

<span data-ttu-id="d1af9-120">Puntatore a una matrice di valori SAP.</span><span class="sxs-lookup"><span data-stu-id="d1af9-120">Pointer to an array of SAP values.</span></span> <span data-ttu-id="d1af9-121">Questo membro indica i valori SAP validi da passare al driver.</span><span class="sxs-lookup"><span data-stu-id="d1af9-121">This member indicates the SAP values that are valid to pass to the driver.</span></span> <span data-ttu-id="d1af9-122">Se \_ i flag capturefilter \_ includono \_ tutti i \_ succhi sono impostati, questo diventa un elenco di eccezioni (includere tutti i succhi ad eccezione di questi).</span><span class="sxs-lookup"><span data-stu-id="d1af9-122">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (include all SAPS except these).</span></span>

</dd> <dt>

<span data-ttu-id="d1af9-123">**lpEtypeTable**</span><span class="sxs-lookup"><span data-stu-id="d1af9-123">**lpEtypeTable**</span></span>
</dt> <dd>

<span data-ttu-id="d1af9-124">Puntatore a una matrice di valori etype.</span><span class="sxs-lookup"><span data-stu-id="d1af9-124">Pointer to an array of Etype values.</span></span> <span data-ttu-id="d1af9-125">Ciò indica i valori ETYPE validi da passare al driver.</span><span class="sxs-lookup"><span data-stu-id="d1af9-125">This indicates those Etype values that are valid to pass to the driver.</span></span> <span data-ttu-id="d1af9-126">Se \_ i flag capturefilter \_ includono \_ tutti i \_ etype del impostati, questo diventa un elenco di eccezioni (includere tutti i ETYPE del ad eccezione di questi).</span><span class="sxs-lookup"><span data-stu-id="d1af9-126">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (include all Etypes except these).</span></span>

</dd> <dt>

<span data-ttu-id="d1af9-127">**nSaps**</span><span class="sxs-lookup"><span data-stu-id="d1af9-127">**nSaps**</span></span>
</dt> <dd>

<span data-ttu-id="d1af9-128">Numero di succhi nella tabella SAP.</span><span class="sxs-lookup"><span data-stu-id="d1af9-128">Number of SAPs in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="d1af9-129">**nEtypes**</span><span class="sxs-lookup"><span data-stu-id="d1af9-129">**nEtypes**</span></span>
</dt> <dd>

<span data-ttu-id="d1af9-130">Numero di ETYPE del nella tabella etype.</span><span class="sxs-lookup"><span data-stu-id="d1af9-130">Number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="d1af9-131">**AddressTable**</span><span class="sxs-lookup"><span data-stu-id="d1af9-131">**AddressTable**</span></span>
</dt> <dd>

<span data-ttu-id="d1af9-132">Nome della tabella degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="d1af9-132">Name of the address table.</span></span>

</dd> <dt>

<span data-ttu-id="d1af9-133">**FilterExpression**</span><span class="sxs-lookup"><span data-stu-id="d1af9-133">**FilterExpression**</span></span>
</dt> <dd>

<span data-ttu-id="d1af9-134">Struttura dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="d1af9-134">An EXPRESSION structure.</span></span> <span data-ttu-id="d1af9-135">Contiene la parte relativa alla corrispondenza dei criteri del filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d1af9-135">This contains the pattern match portion of the capture filter.</span></span>

</dd> <dt>

<span data-ttu-id="d1af9-136">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="d1af9-136">**Trigger**</span></span>
</dt> <dd>

<span data-ttu-id="d1af9-137">Riservato.</span><span class="sxs-lookup"><span data-stu-id="d1af9-137">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d1af9-138">**nFrameBytesToCopy**</span><span class="sxs-lookup"><span data-stu-id="d1af9-138">**nFrameBytesToCopy**</span></span>
</dt> <dd>

<span data-ttu-id="d1af9-139">Se il membro non è 0, specifica il numero di byte da memorizzare per ogni frame ricevuto.</span><span class="sxs-lookup"><span data-stu-id="d1af9-139">If this member is not 0, then it specifies how many bytes to keep of each frame received.</span></span> <span data-ttu-id="d1af9-140">Se è 0, Mantieni l'intero frame.</span><span class="sxs-lookup"><span data-stu-id="d1af9-140">If it is 0, then keep the whole frame.</span></span>

</dd> <dt>

<span data-ttu-id="d1af9-141">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="d1af9-141">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="d1af9-142">Riservato.</span><span class="sxs-lookup"><span data-stu-id="d1af9-142">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1af9-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1af9-143">Remarks</span></span>

<span data-ttu-id="d1af9-144">La combinazione di flag, valori ed espressioni determina quali frame verranno passati dal driver che utilizza i dati della struttura.</span><span class="sxs-lookup"><span data-stu-id="d1af9-144">The combination of flags, values, and expressions determine which frames will be passed by the driver that uses this structure data.</span></span> <span data-ttu-id="d1af9-145">Per ulteriori informazioni sull'implementazione di una struttura **capturefilter** , vedere [Capture filters](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d1af9-145">For more information about implementing a **CAPTUREFILTER** structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1af9-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1af9-146">Requirements</span></span>



| <span data-ttu-id="d1af9-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1af9-147">Requirement</span></span> | <span data-ttu-id="d1af9-148">Valore</span><span class="sxs-lookup"><span data-stu-id="d1af9-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d1af9-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1af9-149">Minimum supported client</span></span><br/> | <span data-ttu-id="d1af9-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d1af9-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d1af9-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1af9-151">Minimum supported server</span></span><br/> | <span data-ttu-id="d1af9-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d1af9-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d1af9-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1af9-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1af9-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1af9-154"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1af9-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1af9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1af9-156">ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="d1af9-156">ADDRESSTABLE</span></span>](addresstable.md)
</dt> <dt>

[<span data-ttu-id="d1af9-157">ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="d1af9-157">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="d1af9-158">ESPRESSIONE</span><span class="sxs-lookup"><span data-stu-id="d1af9-158">EXPRESSION</span></span>](expression.md)
</dt> <dt>

[<span data-ttu-id="d1af9-159">ANDEXP</span><span class="sxs-lookup"><span data-stu-id="d1af9-159">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="d1af9-160">PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="d1af9-160">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




