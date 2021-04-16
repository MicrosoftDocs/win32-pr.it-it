---
title: Struttura MPSCAN_DATA (MpClient. h)
description: Analizza i dati passati al callback.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- Struttura MPSCAN_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSCAN_DATA
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479168"
---
# <a name="mpscan_data-structure"></a><span data-ttu-id="e058f-105">\_Struttura dei dati MPSCAN</span><span class="sxs-lookup"><span data-stu-id="e058f-105">MPSCAN\_DATA structure</span></span>

<span data-ttu-id="e058f-106">Analizza i dati passati al callback.</span><span class="sxs-lookup"><span data-stu-id="e058f-106">Scan data passed to the callback.</span></span>

<span data-ttu-id="e058f-107">Questa struttura contiene statistiche sulle risorse e sulle minacce cumulative.</span><span class="sxs-lookup"><span data-stu-id="e058f-107">This structure contains cumulative threat and resource statistics.</span></span> <span data-ttu-id="e058f-108">Questi campi stat sono sempre validi.</span><span class="sxs-lookup"><span data-stu-id="e058f-108">These stat fields are always valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="e058f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e058f-109">Syntax</span></span>


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a><span data-ttu-id="e058f-110">Members</span><span class="sxs-lookup"><span data-stu-id="e058f-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e058f-111">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="e058f-111">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="e058f-112">Tipo: **[ **MPSCAN \_**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="e058f-112">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e058f-113">Tipo di analisi.</span><span class="sxs-lookup"><span data-stu-id="e058f-113">Scan type.</span></span>

</dd> <dt>

<span data-ttu-id="e058f-114">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="e058f-114">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e058f-115">Tipo: **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="e058f-115">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="e058f-116">Informazioni sulla risorsa.</span><span class="sxs-lookup"><span data-stu-id="e058f-116">Resource information.</span></span> <span data-ttu-id="e058f-117">Vedere [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="e058f-117">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="e058f-118">**ResourceStats**</span><span class="sxs-lookup"><span data-stu-id="e058f-118">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="e058f-119">Tipo: **[ **MPRESOURCE \_ stats**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="e058f-119">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e058f-120">Statistiche cumulative correlate alle risorse.</span><span class="sxs-lookup"><span data-stu-id="e058f-120">Resource-related cumulative statistics.</span></span>

</dd> <dt>

<span data-ttu-id="e058f-121">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="e058f-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="e058f-122">Tipo: **[ **MPTHREAT \_ stats**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="e058f-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e058f-123">Statistiche sulle minacce con completamenti riusciti di analisi.</span><span class="sxs-lookup"><span data-stu-id="e058f-123">Threat statistics with successful scan completions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e058f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e058f-124">Requirements</span></span>



| <span data-ttu-id="e058f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e058f-125">Requirement</span></span> | <span data-ttu-id="e058f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e058f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e058f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e058f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e058f-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e058f-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e058f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e058f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e058f-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e058f-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e058f-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e058f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e058f-132"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e058f-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e058f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e058f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e058f-134">**\_informazioni MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="e058f-134">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="e058f-135">**\_statistiche MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="e058f-135">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="e058f-136">**\_tipo MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="e058f-136">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="e058f-137">**\_statistiche MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="e058f-137">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





