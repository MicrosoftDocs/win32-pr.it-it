---
title: Enumerazione BG_JOB_TYPE (Deliveryoptimization. h)
description: L'enumerazione BG_JOB_TYPE definisce valori costanti che specificano il tipo di processo di trasferimento, ad esempio download.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- Enumerazione BG_JOB_TYPE
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476174"
---
# <a name="bg_job_type-enumeration"></a><span data-ttu-id="5de73-104">Enumerazione BG_JOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="5de73-104">BG_JOB_TYPE enumeration</span></span>

<span data-ttu-id="5de73-105">L'enumerazione **BG_JOB_TYPE** definisce valori costanti che specificano il tipo di processo di trasferimento, ad esempio download.</span><span class="sxs-lookup"><span data-stu-id="5de73-105">The **BG_JOB_TYPE** enumeration defines constant values that specify the type of transfer job, such as download.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de73-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5de73-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a><span data-ttu-id="5de73-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="5de73-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5de73-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span><span class="sxs-lookup"><span data-stu-id="5de73-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="5de73-109">Specifica che il processo Scarica i file nel client.</span><span class="sxs-lookup"><span data-stu-id="5de73-109">Specifies that the job downloads files to the client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5de73-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5de73-110">Requirements</span></span>



| <span data-ttu-id="5de73-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5de73-111">Requirement</span></span> | <span data-ttu-id="5de73-112">Valore</span><span class="sxs-lookup"><span data-stu-id="5de73-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5de73-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5de73-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5de73-114">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="5de73-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5de73-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5de73-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5de73-116">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5de73-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5de73-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5de73-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5de73-118"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5de73-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5de73-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5de73-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de73-120">**Metodo ibackgroundcopyjob:: GetType**</span><span class="sxs-lookup"><span data-stu-id="5de73-120">**IBackgroundCopyJob::GetType**</span></span>](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[<span data-ttu-id="5de73-121">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="5de73-121">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





