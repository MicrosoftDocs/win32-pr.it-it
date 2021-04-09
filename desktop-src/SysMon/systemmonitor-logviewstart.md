---
title: Proprietà SystemMonitor. LogViewStart
description: Recupera o imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Proprietà LogViewStart SysMon
- Proprietà LogViewStart SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà LogViewStart
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967c44940b195c4d8ddd3028e1d4f307827bbbfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964088"
---
# <a name="systemmonitorlogviewstart-property"></a><span data-ttu-id="311e0-106">Proprietà SystemMonitor. LogViewStart</span><span class="sxs-lookup"><span data-stu-id="311e0-106">SystemMonitor.LogViewStart property</span></span>

<span data-ttu-id="311e0-107">Recupera o imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.</span><span class="sxs-lookup"><span data-stu-id="311e0-107">Retrieves or sets the starting date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="311e0-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="311e0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="311e0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="311e0-109">Syntax</span></span>


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a><span data-ttu-id="311e0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="311e0-110">Property value</span></span>

<span data-ttu-id="311e0-111">Data di inizio utilizzata per recuperare i valori dei contatori dai file di log.</span><span class="sxs-lookup"><span data-stu-id="311e0-111">Starting date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="311e0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="311e0-112">Remarks</span></span>

<span data-ttu-id="311e0-113">SYSMON recupera i valori dei contatori dai file di log che rientrano tra le date Start e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) , inclusi.</span><span class="sxs-lookup"><span data-stu-id="311e0-113">SYSMON retrieves counter values from the log files that falls within the start and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) dates, inclusively.</span></span>

<span data-ttu-id="311e0-114">Se non si specifica una data di inizio o si imposta questa proprietà su un valore di data non compreso nell'intervallo dei valori di data presenti nei file di log, SYSMON modifica il valore in un valore di data meno recente trovato nei file di log.</span><span class="sxs-lookup"><span data-stu-id="311e0-114">If you do not specify a start date or if you set this property to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span>

<span data-ttu-id="311e0-115">Se questa proprietà è impostata su un valore di data maggiore di [**LogViewStop**](systemmonitor-logviewstop.md), Sysmon modifica il valore nel valore di **LogViewStop**.</span><span class="sxs-lookup"><span data-stu-id="311e0-115">If this property is set to a date value that is greater than [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON changes the value to the value of **LogViewStop**.</span></span>

<span data-ttu-id="311e0-116">Se si specifica una data di inizio e di fine, è necessario specificare le date prima di impostare [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="311e0-116">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="311e0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="311e0-117">Requirements</span></span>



| <span data-ttu-id="311e0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="311e0-118">Requirement</span></span> | <span data-ttu-id="311e0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="311e0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="311e0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="311e0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="311e0-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="311e0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="311e0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="311e0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="311e0-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="311e0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="311e0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="311e0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="311e0-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="311e0-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="311e0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="311e0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="311e0-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="311e0-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="311e0-128">**SystemMonitor. GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="311e0-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="311e0-129">**SystemMonitor. LogFiles**</span><span class="sxs-lookup"><span data-stu-id="311e0-129">**SystemMonitor.LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> <dt>

[<span data-ttu-id="311e0-130">**SystemMonitor. LogViewStop**</span><span class="sxs-lookup"><span data-stu-id="311e0-130">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="311e0-131">**SystemMonitor. LogSourceStartTime**</span><span class="sxs-lookup"><span data-stu-id="311e0-131">**SystemMonitor.LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[<span data-ttu-id="311e0-132">**SystemMonitor. SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="311e0-132">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





