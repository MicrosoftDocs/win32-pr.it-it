---
title: Proprietà SystemMonitor. MonitorDuplicateInstances
description: Recupera o imposta un valore che determina se è possibile monitorare più istanze di un contatore.
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- Proprietà MonitorDuplicateInstances SysMon
- Proprietà MonitorDuplicateInstances SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà MonitorDuplicateInstances
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400522"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a><span data-ttu-id="3a5db-106">Proprietà SystemMonitor. MonitorDuplicateInstances</span><span class="sxs-lookup"><span data-stu-id="3a5db-106">SystemMonitor.MonitorDuplicateInstances property</span></span>

<span data-ttu-id="3a5db-107">Recupera o imposta un valore che determina se è possibile monitorare più istanze di un contatore.</span><span class="sxs-lookup"><span data-stu-id="3a5db-107">Retrieves or sets a value that determines whether multiple instances of a counter can be monitored.</span></span>

<span data-ttu-id="3a5db-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3a5db-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5db-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a5db-109">Syntax</span></span>


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a><span data-ttu-id="3a5db-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3a5db-110">Property value</span></span>

<span data-ttu-id="3a5db-111">True indica che è possibile monitorare più istanze di un contatore (il valore predefinito è true).</span><span class="sxs-lookup"><span data-stu-id="3a5db-111">True indicates that multiple instances of a counter can be monitored (True is the default).</span></span> <span data-ttu-id="3a5db-112">False indica che è possibile monitorare solo un'istanza di un contatore.</span><span class="sxs-lookup"><span data-stu-id="3a5db-112">False indicates that only one instance of a counter can be monitored.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a5db-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a5db-113">Remarks</span></span>

<span data-ttu-id="3a5db-114">Il monitoraggio di sistema aggiunge \# n a ogni nome di istanza, eccetto il primo, se esistono più istanze.</span><span class="sxs-lookup"><span data-stu-id="3a5db-114">System Monitor appends \#n to every instance name, except the first, if multiple instances exist.</span></span> <span data-ttu-id="3a5db-115">Il numero di serie, n, inizia con uno e viene incrementato di uno per ogni nuova istanza.</span><span class="sxs-lookup"><span data-stu-id="3a5db-115">The serial number, n, begins with one and is incremented by one for each new instance.</span></span> <span data-ttu-id="3a5db-116">Se ad esempio si specifica " \\ Process ( \* ) \\ % Processor Time", l'insieme di contatori deve contenere più istanze di svchost.</span><span class="sxs-lookup"><span data-stu-id="3a5db-116">For example, if you specify "\\Process(\*)\\% Processor Time", the counter collection should contain multiple instances of svchost.</span></span> <span data-ttu-id="3a5db-117">La prima occorrenza sarà svchost, l'occorrenza successiva sarà svchost \# 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="3a5db-117">The first occurrence will be svchost, the next occurrence will be svchost\#1, and so on.</span></span>

<span data-ttu-id="3a5db-118">Le istanze duplicate vengono monitorate solo se si usa il carattere jolly ( \* ) per il nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="3a5db-118">Duplicate instances are monitored only if you use the wildcard character (\*) for the instance name.</span></span> <span data-ttu-id="3a5db-119">Se è stato specificato " \\ Process (SVCHOST) \\ % Processor Time", viene monitorata solo la prima istanza trovata di svchost, non tutte le istanze di svchost.</span><span class="sxs-lookup"><span data-stu-id="3a5db-119">If you specified "\\Process(svchost)\\% Processor Time" only the first instance found of svchost is monitored, not all instances of svchost.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a5db-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a5db-120">Requirements</span></span>



| <span data-ttu-id="3a5db-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a5db-121">Requirement</span></span> | <span data-ttu-id="3a5db-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3a5db-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5db-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a5db-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5db-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a5db-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3a5db-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a5db-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5db-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a5db-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a5db-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3a5db-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a5db-128"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="3a5db-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a5db-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a5db-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a5db-130">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="3a5db-130">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





