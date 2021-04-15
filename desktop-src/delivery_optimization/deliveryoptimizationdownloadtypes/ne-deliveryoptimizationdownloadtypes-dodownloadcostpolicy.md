---
title: Enumerazione DODownloadCostPolicy
description: Specifica l'ID delle opzioni dei criteri di costo associate alla proprietà **DODownloadProperty_CostPolicy** .
keywords:
- Enumerazione DODownloadCostPolicy, DODownloadCostPolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400294"
---
# <a name="dodownloadcostpolicy-enumeration"></a><span data-ttu-id="55564-104">Enumerazione DODownloadCostPolicy</span><span class="sxs-lookup"><span data-stu-id="55564-104">DODownloadCostPolicy enumeration</span></span>

<span data-ttu-id="55564-105">L'enumerazione **DODownloadCostPolicy** specifica l'ID delle opzioni dei criteri di costo associate alla proprietà **DODownloadProperty_CostPolicy** .</span><span class="sxs-lookup"><span data-stu-id="55564-105">The **DODownloadCostPolicy** enumeration specifies the ID of cost policies options associated with the **DODownloadProperty_CostPolicy** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="55564-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55564-106">Syntax</span></span>

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a><span data-ttu-id="55564-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="55564-107">Constants</span></span>

| <span data-ttu-id="55564-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="55564-108">Requirement</span></span> | <span data-ttu-id="55564-109">Valore</span><span class="sxs-lookup"><span data-stu-id="55564-109">Value</span></span> |
|-|-|
| <span data-ttu-id="55564-110">DODownloadCostPolicy_Always</span><span class="sxs-lookup"><span data-stu-id="55564-110">DODownloadCostPolicy_Always</span></span> | <span data-ttu-id="55564-111">Il download viene eseguito indipendentemente dal costo.</span><span class="sxs-lookup"><span data-stu-id="55564-111">Download runs regardless of the cost.</span></span> |
| <span data-ttu-id="55564-112">DODownloadCostPolicy_Unrestricted</span><span class="sxs-lookup"><span data-stu-id="55564-112">DODownloadCostPolicy_Unrestricted</span></span> | <span data-ttu-id="55564-113">Il download viene eseguito solo se impone costi o limiti di traffico.</span><span class="sxs-lookup"><span data-stu-id="55564-113">Download runs unless imposes costs or traffic limits.</span></span> |
| <span data-ttu-id="55564-114">DODownloadCostPolicy_Standard</span><span class="sxs-lookup"><span data-stu-id="55564-114">DODownloadCostPolicy_Standard</span></span> | <span data-ttu-id="55564-115">Il download viene eseguito a meno che non sia soggetto a un sovrapprezzo né a un esaurimento.</span><span class="sxs-lookup"><span data-stu-id="55564-115">Download runs unless neither subject to a surcharge nor near exhaustion.</span></span> |
| <span data-ttu-id="55564-116">DODownloadCostPolicy_NoRoaming</span><span class="sxs-lookup"><span data-stu-id="55564-116">DODownloadCostPolicy_NoRoaming</span></span> | <span data-ttu-id="55564-117">Il download viene eseguito a meno che la connettività non sia soggetta a sovrapprezzi in roaming.</span><span class="sxs-lookup"><span data-stu-id="55564-117">Download runs unless that connectivity is subject to roaming surcharges.</span></span> |
| <span data-ttu-id="55564-118">DODownloadCostPolicy_NoSurcharge</span><span class="sxs-lookup"><span data-stu-id="55564-118">DODownloadCostPolicy_NoSurcharge</span></span> | <span data-ttu-id="55564-119">Il download viene eseguito a meno che non sia soggetto a un supplemento.</span><span class="sxs-lookup"><span data-stu-id="55564-119">Download runs unless subject to a surcharge.</span></span> |
| <span data-ttu-id="55564-120">DODownloadCostPolicy_NoCellular</span><span class="sxs-lookup"><span data-stu-id="55564-120">DODownloadCostPolicy_NoCellular</span></span> | <span data-ttu-id="55564-121">Il download viene eseguito a meno che la rete non sia attiva.</span><span class="sxs-lookup"><span data-stu-id="55564-121">Download runs unless network is on cellular.</span></span> |

## <a name="requirements"></a><span data-ttu-id="55564-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55564-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="55564-123">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="55564-123">**Minimum supported client**</span></span> | <span data-ttu-id="55564-124">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="55564-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="55564-125">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="55564-125">**Minimum supported server**</span></span> | <span data-ttu-id="55564-126">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="55564-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="55564-127">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="55564-127">**Header**</span></span> | <span data-ttu-id="55564-128">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="55564-128">DeliveryOptimizationDownloadTypes.h</span></span> |
