---
title: Enumerazione MPTHREAT_TYPE (MpClient. h)
description: Tipi di minacce possibili.
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPTHREAT_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPTHREAT_TYPE
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed823b100c91f259252d7cad71e554099caf6a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400498"
---
# <a name="mpthreat_type-enumeration"></a><span data-ttu-id="35ba7-105">\_Enumerazione del tipo MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="35ba7-105">MPTHREAT\_TYPE enumeration</span></span>

<span data-ttu-id="35ba7-106">Tipi di minacce possibili.</span><span class="sxs-lookup"><span data-stu-id="35ba7-106">Possible threat types.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ba7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35ba7-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="35ba7-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="35ba7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="35ba7-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT \_ tipo \_ KNOWNBAD**</span><span class="sxs-lookup"><span data-stu-id="35ba7-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT\_TYPE\_KNOWNBAD**</span></span>
</dt> <dd>

<span data-ttu-id="35ba7-110">È stata rilevata una cattiva minaccia nota tramite firma.</span><span class="sxs-lookup"><span data-stu-id="35ba7-110">Known bad threat detected via signature.</span></span>

</dd> <dt>

<span data-ttu-id="35ba7-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**\_comportamento del tipo MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="35ba7-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**MPTHREAT\_TYPE\_BEHAVIOR**</span></span>
</dt> <dd>

<span data-ttu-id="35ba7-112">Minaccia sospetta rilevata tramite il monitoraggio del comportamento.</span><span class="sxs-lookup"><span data-stu-id="35ba7-112">Suspicious threat detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="35ba7-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**\_tipo MPTHREAT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="35ba7-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**MPTHREAT\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="35ba7-114">Minacce sconosciute (non classificate).</span><span class="sxs-lookup"><span data-stu-id="35ba7-114">Unknown threats (unclassified).</span></span>

</dd> <dt>

<span data-ttu-id="35ba7-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT \_ tipo \_ KNOWNGOOD**</span><span class="sxs-lookup"><span data-stu-id="35ba7-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT\_TYPE\_KNOWNGOOD**</span></span>
</dt> <dd>

<span data-ttu-id="35ba7-116">Una minaccia nota.</span><span class="sxs-lookup"><span data-stu-id="35ba7-116">Known good threat.</span></span>

</dd> <dt>

<span data-ttu-id="35ba7-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT di \_ tipo \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="35ba7-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT\_TYPE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="35ba7-118">Rilevamento delle minacce NIS.</span><span class="sxs-lookup"><span data-stu-id="35ba7-118">NIS threat detection.</span></span>

</dd> <dt>

<span data-ttu-id="35ba7-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT di \_ tipo \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="35ba7-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="35ba7-120">Valore massimo possibile.</span><span class="sxs-lookup"><span data-stu-id="35ba7-120">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35ba7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35ba7-121">Requirements</span></span>



| <span data-ttu-id="35ba7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ba7-122">Requirement</span></span> | <span data-ttu-id="35ba7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="35ba7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35ba7-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35ba7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="35ba7-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="35ba7-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="35ba7-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35ba7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="35ba7-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="35ba7-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35ba7-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35ba7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="35ba7-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="35ba7-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





