---
title: Struttura MPRESOURCE_STATS (MpClient. h)
description: Statistiche correlate alle risorse.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- Struttura MPRESOURCE_STATS le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPRESOURCE_STATS
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477657"
---
# <a name="mpresource_stats-structure"></a><span data-ttu-id="d88fa-105">\_Struttura statistiche MPRESOURCE</span><span class="sxs-lookup"><span data-stu-id="d88fa-105">MPRESOURCE\_STATS structure</span></span>

<span data-ttu-id="d88fa-106">Statistiche correlate alle risorse.</span><span class="sxs-lookup"><span data-stu-id="d88fa-106">Resource-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88fa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d88fa-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a><span data-ttu-id="d88fa-108">Members</span><span class="sxs-lookup"><span data-stu-id="d88fa-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d88fa-109">**PPMProgress**</span><span class="sxs-lookup"><span data-stu-id="d88fa-109">**PPMProgress**</span></span>
</dt> <dd>

<span data-ttu-id="d88fa-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d88fa-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d88fa-111">Avanzamento approssimativo per l'analisi in ppm (parti per milione).</span><span class="sxs-lookup"><span data-stu-id="d88fa-111">Approximate progress for scan in ppm (parts per million).</span></span> <span data-ttu-id="d88fa-112">Impostare su **MPPROGRESS \_ non valido** se le informazioni sullo stato non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="d88fa-112">Set to **MPPROGRESS\_INVALID** if progress information is not available.</span></span>

</dd> <dt>

<span data-ttu-id="d88fa-113">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="d88fa-113">**ProcessCount**</span></span>
</dt> <dd>

<span data-ttu-id="d88fa-114">Tipo: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d88fa-114">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="d88fa-115">Numero di processi analizzati.</span><span class="sxs-lookup"><span data-stu-id="d88fa-115">Number of processes scanned.</span></span>

</dd> <dt>

<span data-ttu-id="d88fa-116">**FileCount**</span><span class="sxs-lookup"><span data-stu-id="d88fa-116">**FileCount**</span></span>
</dt> <dd>

<span data-ttu-id="d88fa-117">Tipo: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d88fa-117">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="d88fa-118">Numero di file analizzati.</span><span class="sxs-lookup"><span data-stu-id="d88fa-118">Number of files scanned.</span></span>

</dd> <dt>

<span data-ttu-id="d88fa-119">**FileBytesCount**</span><span class="sxs-lookup"><span data-stu-id="d88fa-119">**FileBytesCount**</span></span>
</dt> <dd>

<span data-ttu-id="d88fa-120">Tipo: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d88fa-120">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="d88fa-121">Numero di byte analizzati per i file.</span><span class="sxs-lookup"><span data-stu-id="d88fa-121">Number of bytes scanned for files.</span></span>

</dd> <dt>

<span data-ttu-id="d88fa-122">**RegKeyCount**</span><span class="sxs-lookup"><span data-stu-id="d88fa-122">**RegKeyCount**</span></span>
</dt> <dd>

<span data-ttu-id="d88fa-123">Tipo: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d88fa-123">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="d88fa-124">Numero di RegKeys analizzati.</span><span class="sxs-lookup"><span data-stu-id="d88fa-124">Number of RegKeys scanned.</span></span>

</dd> <dt>

<span data-ttu-id="d88fa-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="d88fa-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="d88fa-126">Tipo: **UInt64 \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="d88fa-126">Type: **UINT64\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="d88fa-127">Campi riservati per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="d88fa-127">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d88fa-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d88fa-128">Requirements</span></span>



| <span data-ttu-id="d88fa-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d88fa-129">Requirement</span></span> | <span data-ttu-id="d88fa-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d88fa-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d88fa-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d88fa-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d88fa-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d88fa-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d88fa-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d88fa-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d88fa-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d88fa-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d88fa-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d88fa-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d88fa-136"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="d88fa-136"><dt>MpClient.h</dt></span></span> </dl> |



 

 





