---
title: Enumerazione BITS_JOB_TRANSFER_POLICY (Deliveryoptimization. h)
description: L'enumerazione BITS_JOB_TRANSFER_POLICY definisce i valori ID corrispondenti alle proprietà DO.
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- Enumerazione BITS_JOB_TRANSFER_POLICY
- Enumerazione BITS_JOB_TRANSFER_POLICY
topic_type:
- apiref
api_name:
- BITS_JOB_TRANSFER_POLICY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 455752375b76e574923ccdd96d1d05fc9142c16c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119350"
---
# <a name="bits_job_transfer_policy-enumeration"></a><span data-ttu-id="653e4-105">Enumerazione BITS_JOB_TRANSFER_POLICY</span><span class="sxs-lookup"><span data-stu-id="653e4-105">BITS_JOB_TRANSFER_POLICY enumeration</span></span>

<span data-ttu-id="653e4-106">L'enumerazione **BITS_JOB_TRANSFER_POLICY** definisce i valori ID corrispondenti alle proprietà do.</span><span class="sxs-lookup"><span data-stu-id="653e4-106">The **BITS_JOB_TRANSFER_POLICY** enumeration defines ID values corresponding to DO properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="653e4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="653e4-107">Syntax</span></span>


```C++
typedef enum _BITS_JOB_TRANSFER_POLICY { 
  BITS_JOB_TRANSFER_POLICY_ALWAYS        = 0x800000ff,
  BITS_JOB_TRANSFER_POLICY_NOT_ROAMING   = 0x8000007f,
  BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE  = 0x8000006f,
  BITS_JOB_TRANSFER_POLICY_STANDARD      = 0x80000067,
  BITS_JOB_TRANSFER_POLICY_UNRESTRICTED  = 0x80000021
} BITS_JOB_TRANSFER_POLICY;
```



## <a name="constants"></a><span data-ttu-id="653e4-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="653e4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="653e4-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span><span class="sxs-lookup"><span data-stu-id="653e4-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="653e4-110">Specifica che il processo verrà trasferito quando la connettività è disponibile, indipendentemente dal costo.</span><span class="sxs-lookup"><span data-stu-id="653e4-110">Specifies that the job will be transferred when connectivity is available, regardless of the cost.</span></span>

</dd> <dt>

<span data-ttu-id="653e4-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span><span class="sxs-lookup"><span data-stu-id="653e4-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span></span>
</dt> <dd>

<span data-ttu-id="653e4-112">Specifica che il processo verrà trasferito quando è disponibile la connettività, a meno che la connettività non sia soggetta a sovrapprezzi in roaming.</span><span class="sxs-lookup"><span data-stu-id="653e4-112">Specifies that the job will be transferred when connectivity is available, unless that connectivity is subject to roaming surcharges.</span></span>

</dd> <dt>

<span data-ttu-id="653e4-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span><span class="sxs-lookup"><span data-stu-id="653e4-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span></span>
</dt> <dd>

<span data-ttu-id="653e4-114">Specifica che il processo verrà trasferito solo quando è disponibile la connettività, che non è soggetta a un supplemento.</span><span class="sxs-lookup"><span data-stu-id="653e4-114">Specifies that the job will be transferred only when connectivity is available which is not subject to a surcharge.</span></span>

</dd> <dt>

<span data-ttu-id="653e4-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span><span class="sxs-lookup"><span data-stu-id="653e4-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="653e4-116">Specifica che il processo verrà trasferito solo quando è disponibile la connettività, che non è soggetta a un sovrapprezzo né a un esaurimento.</span><span class="sxs-lookup"><span data-stu-id="653e4-116">Specifies that the job will be transferred only when connectivity is available which is neither subject to a surcharge nor near exhaustion.</span></span>

</dd> <dt>

<span data-ttu-id="653e4-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span><span class="sxs-lookup"><span data-stu-id="653e4-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span></span>
</dt> <dd>

<span data-ttu-id="653e4-118">Specifica che il processo verrà trasferito solo quando è disponibile la connettività che non impone costi o limiti di traffico.</span><span class="sxs-lookup"><span data-stu-id="653e4-118">Specifies that the job will be transferred only when connectivity is available which does not impose costs or traffic limits.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="653e4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="653e4-119">Requirements</span></span>



| <span data-ttu-id="653e4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="653e4-120">Requirement</span></span> | <span data-ttu-id="653e4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="653e4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="653e4-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="653e4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="653e4-123">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="653e4-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="653e4-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="653e4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="653e4-125">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="653e4-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="653e4-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="653e4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="653e4-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="653e4-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





