---
title: Struttura MPSTATUS_INFO (MpClient. h)
description: Informazioni sullo stato di malware Protection Manager.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- Struttura MPSTATUS_INFO le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSTATUS_INFO
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740130"
---
# <a name="mpstatus_info-structure"></a><span data-ttu-id="52a2d-105">Struttura delle informazioni di MPSTATUS \_</span><span class="sxs-lookup"><span data-stu-id="52a2d-105">MPSTATUS\_INFO structure</span></span>

<span data-ttu-id="52a2d-106">Informazioni sullo stato di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="52a2d-106">Status information for the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a2d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52a2d-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a><span data-ttu-id="52a2d-108">Members</span><span class="sxs-lookup"><span data-stu-id="52a2d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="52a2d-109">**ProductStatus**</span><span class="sxs-lookup"><span data-stu-id="52a2d-109">**ProductStatus**</span></span>
</dt> <dd>

<span data-ttu-id="52a2d-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="52a2d-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="52a2d-111">Stato generale del prodotto.</span><span class="sxs-lookup"><span data-stu-id="52a2d-111">Overall product status.</span></span> <span data-ttu-id="52a2d-112">Si tratta di una combinazione di flag di bit del [**\_ flag MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="52a2d-112">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="52a2d-113">**LastQuickScan**</span><span class="sxs-lookup"><span data-stu-id="52a2d-113">**LastQuickScan**</span></span>
</dt> <dd>

<span data-ttu-id="52a2d-114">Tipo: **[ **\_ risultato MPSCAN**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="52a2d-114">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52a2d-115">Risultati dell'ultima analisi da parte di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="52a2d-115">Results of the last scan by the malware protection manager.</span></span> <span data-ttu-id="52a2d-116">Vedere [**il \_ risultato di MPSCAN**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="52a2d-116">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="52a2d-117">**LastFullScan**</span><span class="sxs-lookup"><span data-stu-id="52a2d-117">**LastFullScan**</span></span>
</dt> <dd>

<span data-ttu-id="52a2d-118">Tipo: **[ **\_ risultato MPSCAN**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="52a2d-118">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52a2d-119">Risultati dell'ultima analisi completa da parte di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="52a2d-119">Results of the last full scan by the malware protection manager.</span></span> <span data-ttu-id="52a2d-120">Vedere [**il \_ risultato di MPSCAN**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="52a2d-120">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="52a2d-121">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="52a2d-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="52a2d-122">Tipo: **[ **MPTHREAT \_ stats**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="52a2d-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52a2d-123">Statistiche sulle minacce attive.</span><span class="sxs-lookup"><span data-stu-id="52a2d-123">Active threat statistics.</span></span> <span data-ttu-id="52a2d-124">Vedere [**MPTHREAT \_ Statistics**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="52a2d-124">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="52a2d-125">**ThreatState**</span><span class="sxs-lookup"><span data-stu-id="52a2d-125">**ThreatState**</span></span>
</dt> <dd>

<span data-ttu-id="52a2d-126">Tipo: **[**MPTHREAT \_ stats \_ Data**](mpthreat-stats-data.md) \[ MP \_ Threat \_ Stat \_ Max \_ value + 1\]**</span><span class="sxs-lookup"><span data-stu-id="52a2d-126">Type: **[**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md)\[MP\_THREAT\_STAT\_MAX\_VALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="52a2d-127">Dati aggiuntivi sulle statistiche sulle minacce, ad esempio il numero di minacce.</span><span class="sxs-lookup"><span data-stu-id="52a2d-127">Additional threat statistics data, such as the number of threats.</span></span> <span data-ttu-id="52a2d-128">Vedere [**MPTHREAT \_ stats \_ Data**](mpthreat-stats-data.md).</span><span class="sxs-lookup"><span data-stu-id="52a2d-128">See [**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="52a2d-129">**Componente**</span><span class="sxs-lookup"><span data-stu-id="52a2d-129">**Component**</span></span>
</dt> <dd>

<span data-ttu-id="52a2d-130">Tipo: **[**MPCOMPONENT \_ stato**](mpcomponent-status.md) \[ MPCOMPONENT \_ MaxValue + 1\]**</span><span class="sxs-lookup"><span data-stu-id="52a2d-130">Type: **[**MPCOMPONENT\_STATUS**](mpcomponent-status.md)\[MPCOMPONENT\_MAXVALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="52a2d-131">Matrice di stati per più componenti.</span><span class="sxs-lookup"><span data-stu-id="52a2d-131">An array of statuses for multiple components.</span></span> <span data-ttu-id="52a2d-132">Usare un valore dall'enumerazione [**\_ ID MPCOMPONENT**](mpcomponent-id.md) come indice nella matrice.</span><span class="sxs-lookup"><span data-stu-id="52a2d-132">Use a value from the [**MPCOMPONENT\_ID**](mpcomponent-id.md) enumeration as an index into the array.</span></span>

</dd> <dt>

<span data-ttu-id="52a2d-133">**ProductExpirationTime**</span><span class="sxs-lookup"><span data-stu-id="52a2d-133">**ProductExpirationTime**</span></span>
</dt> <dd>

<span data-ttu-id="52a2d-134">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="52a2d-134">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="52a2d-135">Timestamp scadenza prodotto in UNC.</span><span class="sxs-lookup"><span data-stu-id="52a2d-135">Product expiration timestamp in UNC.</span></span> <span data-ttu-id="52a2d-136">Questa operazione è valida solo se lo stato di scadenza è impostato.</span><span class="sxs-lookup"><span data-stu-id="52a2d-136">This is valid only if the expiration status is set.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52a2d-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52a2d-137">Requirements</span></span>



| <span data-ttu-id="52a2d-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="52a2d-138">Requirement</span></span> | <span data-ttu-id="52a2d-139">Valore</span><span class="sxs-lookup"><span data-stu-id="52a2d-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52a2d-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52a2d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="52a2d-141">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="52a2d-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="52a2d-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52a2d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="52a2d-143">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="52a2d-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52a2d-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52a2d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="52a2d-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="52a2d-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a2d-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52a2d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a2d-147">**\_ID MPCOMPONENT**</span><span class="sxs-lookup"><span data-stu-id="52a2d-147">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="52a2d-148">**\_stato MPCOMPONENT**</span><span class="sxs-lookup"><span data-stu-id="52a2d-148">**MPCOMPONENT\_STATUS**</span></span>](mpcomponent-status.md)
</dt> <dt>

[<span data-ttu-id="52a2d-149">**risultato di MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="52a2d-149">**MPSCAN\_RESULT**</span></span>](mpscan-result.md)
</dt> <dt>

[<span data-ttu-id="52a2d-150">**\_flag MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="52a2d-150">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="52a2d-151">**\_statistiche MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="52a2d-151">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> <dt>

[<span data-ttu-id="52a2d-152">**\_dati statistiche \_ MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="52a2d-152">**MPTHREAT\_STATS\_DATA**</span></span>](mpthreat-stats-data.md)
</dt> </dl>

 

 





