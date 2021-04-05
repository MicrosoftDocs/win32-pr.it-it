---
title: Struttura MPTHREAT_STATS (MpClient. h)
description: Statistiche correlate alle minacce.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- Struttura MPTHREAT_STATS le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_STATS
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873729"
---
# <a name="mpthreat_stats-structure"></a><span data-ttu-id="c30d0-105">\_Struttura statistiche MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="c30d0-105">MPTHREAT\_STATS structure</span></span>

<span data-ttu-id="c30d0-106">Statistiche correlate alle minacce.</span><span class="sxs-lookup"><span data-stu-id="c30d0-106">Threat-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="c30d0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c30d0-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a><span data-ttu-id="c30d0-108">Members</span><span class="sxs-lookup"><span data-stu-id="c30d0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c30d0-109">**ThreatCount**</span><span class="sxs-lookup"><span data-stu-id="c30d0-109">**ThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="c30d0-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c30d0-110">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="c30d0-111">Numero di minacce rilevate.</span><span class="sxs-lookup"><span data-stu-id="c30d0-111">Number of threats detected.</span></span>

</dd> <dt>

<span data-ttu-id="c30d0-112">**SuspiciousThreatCount**</span><span class="sxs-lookup"><span data-stu-id="c30d0-112">**SuspiciousThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="c30d0-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c30d0-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="c30d0-114">Numero di minacce rilevate con monitoraggio del comportamento.</span><span class="sxs-lookup"><span data-stu-id="c30d0-114">Number of threats detected with behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="c30d0-115">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="c30d0-115">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="c30d0-116">Tipo: **uint \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="c30d0-116">Type: **UINT\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="c30d0-117">Campi riservati per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="c30d0-117">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c30d0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c30d0-118">Requirements</span></span>



| <span data-ttu-id="c30d0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c30d0-119">Requirement</span></span> | <span data-ttu-id="c30d0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c30d0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c30d0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c30d0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c30d0-122">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c30d0-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c30d0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c30d0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c30d0-124">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c30d0-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c30d0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c30d0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c30d0-126"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c30d0-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





