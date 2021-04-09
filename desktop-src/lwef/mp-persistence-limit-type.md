---
title: Enumerazione MP_PERSISTENCE_LIMIT_TYPE (MpClient. h)
description: Tipo di limite di persistenza.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MP_PERSISTENCE_LIMIT_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMP_PERSISTENCE_LIMIT_TYPE
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fb52bc6ee630590ca189b88c1fdde5a30e17747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048676"
---
# <a name="mp_persistence_limit_type-enumeration"></a><span data-ttu-id="27c84-105">\_Enumerazione del \_ tipo di limite di PERSISTEnza MP \_</span><span class="sxs-lookup"><span data-stu-id="27c84-105">MP\_PERSISTENCE\_LIMIT\_TYPE enumeration</span></span>

<span data-ttu-id="27c84-106">Tipo di limite di persistenza.</span><span class="sxs-lookup"><span data-stu-id="27c84-106">Persistence limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c84-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27c84-107">Syntax</span></span>


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="27c84-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="27c84-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="27c84-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**\_persistenza MP \_ sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="27c84-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP\_PERSISTENCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="27c84-110">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="27c84-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="27c84-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**\_ \_ Nessun limite di PERSISTEnza MP \_**</span><span class="sxs-lookup"><span data-stu-id="27c84-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP\_PERSISTENCE\_NO\_LIMIT**</span></span>
</dt> <dd>

<span data-ttu-id="27c84-112">Nessun limite.</span><span class="sxs-lookup"><span data-stu-id="27c84-112">No limit.</span></span>

</dd> <dt>

<span data-ttu-id="27c84-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**\_durata di persistenza MP \_**</span><span class="sxs-lookup"><span data-stu-id="27c84-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**MP\_PERSISTENCE\_DURATION**</span></span>
</dt> <dd>

<span data-ttu-id="27c84-114">Durata.</span><span class="sxs-lookup"><span data-stu-id="27c84-114">Duration.</span></span>

</dd> <dt>

<span data-ttu-id="27c84-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**\_versione di \_ VDM PERSISTEnza MP \_**</span><span class="sxs-lookup"><span data-stu-id="27c84-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**MP\_PERSISTENCE\_VDM\_VERSION**</span></span>
</dt> <dd>

<span data-ttu-id="27c84-116">Versione di VDM.</span><span class="sxs-lookup"><span data-stu-id="27c84-116">VDM version.</span></span>

</dd> <dt>

<span data-ttu-id="27c84-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**\_timestamp di persistenza MP \_**</span><span class="sxs-lookup"><span data-stu-id="27c84-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP\_PERSISTENCE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="27c84-118">Timestamp.</span><span class="sxs-lookup"><span data-stu-id="27c84-118">Timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="27c84-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**\_persistenza MP \_ forzata**</span><span class="sxs-lookup"><span data-stu-id="27c84-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**MP\_PERSISTENCE\_FORCED**</span></span>
</dt> <dd>

<span data-ttu-id="27c84-120">Forzato.</span><span class="sxs-lookup"><span data-stu-id="27c84-120">Forced.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27c84-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27c84-121">Requirements</span></span>



| <span data-ttu-id="27c84-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="27c84-122">Requirement</span></span> | <span data-ttu-id="27c84-123">Valore</span><span class="sxs-lookup"><span data-stu-id="27c84-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27c84-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27c84-124">Minimum supported client</span></span><br/> | <span data-ttu-id="27c84-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="27c84-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="27c84-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27c84-126">Minimum supported server</span></span><br/> | <span data-ttu-id="27c84-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="27c84-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27c84-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27c84-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="27c84-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="27c84-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





