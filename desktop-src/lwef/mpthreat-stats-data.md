---
title: Struttura MPTHREAT_STATS_DATA (MpClient. h)
description: Dati aggiuntivi sulle statistiche sulle minacce.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- Struttura MPTHREAT_STATS_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_STATS_DATA
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119666"
---
# <a name="mpthreat_stats_data-structure"></a><span data-ttu-id="944b3-105">\_ \_ Struttura dei dati delle statistiche MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="944b3-105">MPTHREAT\_STATS\_DATA structure</span></span>

<span data-ttu-id="944b3-106">Dati aggiuntivi sulle statistiche sulle minacce.</span><span class="sxs-lookup"><span data-stu-id="944b3-106">Additional threat statistics data.</span></span>

## <a name="syntax"></a><span data-ttu-id="944b3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="944b3-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a><span data-ttu-id="944b3-108">Members</span><span class="sxs-lookup"><span data-stu-id="944b3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="944b3-109">**dwThreatCount**</span><span class="sxs-lookup"><span data-stu-id="944b3-109">**dwThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="944b3-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="944b3-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="944b3-111">Numero di minacce.</span><span class="sxs-lookup"><span data-stu-id="944b3-111">Number of threats.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="944b3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="944b3-112">Requirements</span></span>



| <span data-ttu-id="944b3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="944b3-113">Requirement</span></span> | <span data-ttu-id="944b3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="944b3-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="944b3-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="944b3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="944b3-116">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="944b3-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="944b3-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="944b3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="944b3-118">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="944b3-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="944b3-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="944b3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="944b3-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="944b3-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





