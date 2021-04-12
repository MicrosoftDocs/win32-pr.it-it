---
title: Struttura MPSCAN_RESULT (MpClient. h)
description: Risultati di un'analisi.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- Struttura MPSCAN_RESULT le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSCAN_RESULT
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225240"
---
# <a name="mpscan_result-structure"></a><span data-ttu-id="dbcc1-105">\_Struttura di risultati MPSCAN</span><span class="sxs-lookup"><span data-stu-id="dbcc1-105">MPSCAN\_RESULT structure</span></span>

<span data-ttu-id="dbcc1-106">Risultati di un'analisi.</span><span class="sxs-lookup"><span data-stu-id="dbcc1-106">The results of a scan.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbcc1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbcc1-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a><span data-ttu-id="dbcc1-108">Members</span><span class="sxs-lookup"><span data-stu-id="dbcc1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dbcc1-109">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-109">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="dbcc1-110">Tipo: **[ **MPSCAN \_**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-110">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dbcc1-111">Tipo di analisi.</span><span class="sxs-lookup"><span data-stu-id="dbcc1-111">Scan type.</span></span> <span data-ttu-id="dbcc1-112">Vedere [**MPSCAN \_ Type**](mpscan-type.md).</span><span class="sxs-lookup"><span data-stu-id="dbcc1-112">See [**MPSCAN\_TYPE**](mpscan-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbcc1-113">**Origine**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-113">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="dbcc1-114">Tipo: **[ **MPSOURCE**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-114">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dbcc1-115">Origine dell'analisi, ad esempio avviata dall'utente o dal sistema.</span><span class="sxs-lookup"><span data-stu-id="dbcc1-115">Scan source, such as user or system initiated.</span></span> <span data-ttu-id="dbcc1-116">Vedere [**MPSOURCE**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="dbcc1-116">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbcc1-117">**ScanGuid**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-117">**ScanGuid**</span></span>
</dt> <dd>

<span data-ttu-id="dbcc1-118">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-118">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="dbcc1-119">Identificatore di analisi.</span><span class="sxs-lookup"><span data-stu-id="dbcc1-119">Scan identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dbcc1-120">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-120">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="dbcc1-121">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-121">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="dbcc1-122">Ora di inizio dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="dbcc1-122">Scan start time.</span></span>

</dd> <dt>

<span data-ttu-id="dbcc1-123">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-123">**EndTime**</span></span>
</dt> <dd>

<span data-ttu-id="dbcc1-124">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-124">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="dbcc1-125">Ora di fine dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="dbcc1-125">Scan end time.</span></span>

</dd> <dt>

<span data-ttu-id="dbcc1-126">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-126">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="dbcc1-127">Tipo: **[ **MPTHREAT \_ stats**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-127">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dbcc1-128">Statistiche correlate alle minacce.</span><span class="sxs-lookup"><span data-stu-id="dbcc1-128">Threat-related statistics.</span></span> <span data-ttu-id="dbcc1-129">Vedere [**MPTHREAT \_ Statistics**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="dbcc1-129">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbcc1-130">**ResourceStats**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-130">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="dbcc1-131">Tipo: **[ **MPRESOURCE \_ stats**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-131">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dbcc1-132">Statistiche correlate alle risorse.</span><span class="sxs-lookup"><span data-stu-id="dbcc1-132">Resource-related statistics.</span></span> <span data-ttu-id="dbcc1-133">Vedere [**MPRESOURCE \_ Statistics**](mpresource-stats.md).</span><span class="sxs-lookup"><span data-stu-id="dbcc1-133">See [**MPRESOURCE\_STATS**](mpresource-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbcc1-134">**SignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-134">**SignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="dbcc1-135">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-135">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="dbcc1-136">Versione della firma utilizzata per l'analisi.</span><span class="sxs-lookup"><span data-stu-id="dbcc1-136">Version of signature used for scan.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbcc1-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbcc1-137">Requirements</span></span>



| <span data-ttu-id="dbcc1-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbcc1-138">Requirement</span></span> | <span data-ttu-id="dbcc1-139">Valore</span><span class="sxs-lookup"><span data-stu-id="dbcc1-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbcc1-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbcc1-140">Minimum supported client</span></span><br/> | <span data-ttu-id="dbcc1-141">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dbcc1-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dbcc1-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbcc1-142">Minimum supported server</span></span><br/> | <span data-ttu-id="dbcc1-143">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dbcc1-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dbcc1-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbcc1-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbcc1-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbcc1-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbcc1-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbcc1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbcc1-147">**\_statistiche MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-147">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="dbcc1-148">**\_tipo MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-148">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="dbcc1-149">**MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-149">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="dbcc1-150">**\_statistiche MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="dbcc1-150">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





