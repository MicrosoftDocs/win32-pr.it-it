---
title: Enumerazione MPTHREAT_SEVERITY (MpClient. h)
description: Possibili livelli di gravità della minaccia.
ms.assetid: 7C50AC74-16CB-4198-ABB2-D6999429F2EA
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPTHREAT_SEVERITY
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPTHREAT_SEVERITY
topic_type:
- apiref
api_name:
- MPTHREAT_SEVERITY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eec7bff3b23a89ce8187798d8a69a9968cbc2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301538"
---
# <a name="mpthreat_severity-enumeration"></a><span data-ttu-id="a402d-105">\_Enumerazione gravità MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="a402d-105">MPTHREAT\_SEVERITY enumeration</span></span>

<span data-ttu-id="a402d-106">Possibili livelli di gravità della minaccia.</span><span class="sxs-lookup"><span data-stu-id="a402d-106">Possible threat severities.</span></span>

## <a name="syntax"></a><span data-ttu-id="a402d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a402d-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_SEVERITY { 
  MP_THREAT_SEVERITY_UNKNOWN   = 0,
  MP_THREAT_SEVERITY_LOW       = 1,
  MP_THREAT_SEVERITY_MODERATE  = 2,
  MP_THREAT_SEVERITY_HIGH      = 4,
  MP_THREAT_SEVERITY_SEVERE    = 5,
  MP_THREAT_SEVERITY_MAXVALUE  = 5
} MPTHREAT_SEVERITY, *PMPTHREAT_SEVERITY;
```



## <a name="constants"></a><span data-ttu-id="a402d-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="a402d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a402d-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**\_gravità minaccia \_ MP \_ sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="a402d-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**MP\_THREAT\_SEVERITY\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a402d-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**\_gravità minacce \_ MP \_ bassa**</span><span class="sxs-lookup"><span data-stu-id="a402d-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**MP\_THREAT\_SEVERITY\_LOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a402d-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**\_gravità della minaccia MP \_ \_ moderata**</span><span class="sxs-lookup"><span data-stu-id="a402d-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**MP\_THREAT\_SEVERITY\_MODERATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a402d-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**\_gravità della minaccia MP \_ \_ elevata**</span><span class="sxs-lookup"><span data-stu-id="a402d-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**MP\_THREAT\_SEVERITY\_HIGH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a402d-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**\_gravità della minaccia MP \_ \_ grave**</span><span class="sxs-lookup"><span data-stu-id="a402d-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**MP\_THREAT\_SEVERITY\_SEVERE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a402d-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**\_gravità della minaccia MP \_ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="a402d-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**MP\_THREAT\_SEVERITY\_MAXVALUE**</span></span>
<span data-ttu-id="a402d-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a402d-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a402d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a402d-116">Requirements</span></span>



| <span data-ttu-id="a402d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a402d-117">Requirement</span></span> | <span data-ttu-id="a402d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a402d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a402d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a402d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a402d-120">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a402d-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a402d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a402d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a402d-122">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a402d-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a402d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a402d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a402d-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a402d-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





