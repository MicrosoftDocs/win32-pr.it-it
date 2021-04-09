---
title: Enumerazione SwarmStatus (Deliveryoptimization. h)
description: Definisce lo stato di un file all'interno del client di ottimizzazione recapito.
ms.assetid: D40ABDD3-5573-4A8D-8608-4CB0F396CCAD
keywords:
- Enumerazione SwarmStatus
topic_type:
- apiref
api_name:
- SwarmStatus
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3622f819679c2fd2b28d66e371a8b88e0a2d2f70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120863"
---
# <a name="swarmstatus-enumeration"></a><span data-ttu-id="75d0e-104">Enumerazione SwarmStatus</span><span class="sxs-lookup"><span data-stu-id="75d0e-104">SwarmStatus enumeration</span></span>

<span data-ttu-id="75d0e-105">Definisce lo stato di un file all'interno del client di ottimizzazione recapito.</span><span class="sxs-lookup"><span data-stu-id="75d0e-105">Defines the status of a file within the delivery optimization client.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d0e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75d0e-106">Syntax</span></span>


```C++
typedef enum _SwarmStatus { 
  SwarmStatus_Downloading  = 0,
  SwarmStatus_Complete     = 1,
  SwarmStatus_Caching      = 2,
  SwarmStatus_Paused       = 3
} SwarmStatus;
```



## <a name="constants"></a><span data-ttu-id="75d0e-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="75d0e-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="75d0e-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span><span class="sxs-lookup"><span data-stu-id="75d0e-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span></span>
</dt> <dd>

<span data-ttu-id="75d0e-109">Il file sta per essere scaricato.</span><span class="sxs-lookup"><span data-stu-id="75d0e-109">The file is downloading.</span></span>

</dd> <dt>

<span data-ttu-id="75d0e-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span><span class="sxs-lookup"><span data-stu-id="75d0e-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span></span>
</dt> <dd>

<span data-ttu-id="75d0e-111">Il download del file è stato completato.</span><span class="sxs-lookup"><span data-stu-id="75d0e-111">The file download is complete.</span></span>

</dd> <dt>

<span data-ttu-id="75d0e-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span><span class="sxs-lookup"><span data-stu-id="75d0e-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span></span>
</dt> <dd>

<span data-ttu-id="75d0e-113">Il file viene memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="75d0e-113">The file is being cached.</span></span>

</dd> <dt>

<span data-ttu-id="75d0e-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span><span class="sxs-lookup"><span data-stu-id="75d0e-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="75d0e-115">Il download del file è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="75d0e-115">The file download is paused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75d0e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75d0e-116">Requirements</span></span>



| <span data-ttu-id="75d0e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="75d0e-117">Requirement</span></span> | <span data-ttu-id="75d0e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="75d0e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d0e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75d0e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="75d0e-120">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="75d0e-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="75d0e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75d0e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="75d0e-122">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75d0e-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="75d0e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75d0e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="75d0e-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="75d0e-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





