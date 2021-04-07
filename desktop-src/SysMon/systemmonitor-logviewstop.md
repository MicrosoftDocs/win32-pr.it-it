---
title: Proprietà SystemMonitor. LogViewStop
description: Recupera o imposta la data di fine utilizzata per recuperare i valori dei contatori dai file di log.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Proprietà LogViewStop SysMon
- Proprietà LogViewStop SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà LogViewStop
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b725ee2efba22453d44f1e15fb9ce231b07cdb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964180"
---
# <a name="systemmonitorlogviewstop-property"></a><span data-ttu-id="823c9-106">Proprietà SystemMonitor. LogViewStop</span><span class="sxs-lookup"><span data-stu-id="823c9-106">SystemMonitor.LogViewStop property</span></span>

<span data-ttu-id="823c9-107">Recupera o imposta la data di fine utilizzata per recuperare i valori dei contatori dai file di log.</span><span class="sxs-lookup"><span data-stu-id="823c9-107">Retrieves or sets the ending date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="823c9-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="823c9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="823c9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="823c9-109">Syntax</span></span>


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a><span data-ttu-id="823c9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="823c9-110">Property value</span></span>

<span data-ttu-id="823c9-111">Data di fine utilizzata per recuperare i valori dei contatori dai file di log.</span><span class="sxs-lookup"><span data-stu-id="823c9-111">Ending date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="823c9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="823c9-112">Remarks</span></span>

<span data-ttu-id="823c9-113">SYSMON recupera i valori dei contatori dai file di log che rientrano in [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) e le date di arresto, inclusi.</span><span class="sxs-lookup"><span data-stu-id="823c9-113">SYSMON retrieves counter values from the log files that falls within the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and stop dates, inclusively.</span></span>

<span data-ttu-id="823c9-114">Se non si specifica un valore di interruzione o si imposta questa proprietà su un valore di data successivo all'ultima data contenuta nel file di log, SYSMON modifica il valore con il valore di data più recente trovato nei file di log.</span><span class="sxs-lookup"><span data-stu-id="823c9-114">If you do not specify a stop value or you set this property to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span>

<span data-ttu-id="823c9-115">Se questa proprietà è impostata su un valore di data minore di [**LogViewStart**](systemmonitor-logviewstart.md), Sysmon modifica il valore nel valore di **LogViewStart**.</span><span class="sxs-lookup"><span data-stu-id="823c9-115">If this property is set to a date value that is less than [**LogViewStart**](systemmonitor-logviewstart.md), SYSMON changes the value to the value of **LogViewStart**.</span></span>

<span data-ttu-id="823c9-116">Prima di impostare la data di arresto, è necessario impostare la data di inizio. in caso contrario, entrambi i valori vengono impostati su date. MinValue e se si impostano le date dopo l'impostazione di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md), solo il primo valore del contatore viene recuperato dal file di log.</span><span class="sxs-lookup"><span data-stu-id="823c9-116">You must set the start date before you set the stop date; otherwise, both values are set to Date.MinValue, and if you set the dates after setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md), then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="823c9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="823c9-117">Requirements</span></span>



| <span data-ttu-id="823c9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="823c9-118">Requirement</span></span> | <span data-ttu-id="823c9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="823c9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="823c9-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="823c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="823c9-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="823c9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="823c9-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="823c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="823c9-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="823c9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="823c9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="823c9-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="823c9-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="823c9-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="823c9-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="823c9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823c9-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="823c9-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="823c9-128">**SystemMonitor. GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="823c9-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="823c9-129">**SystemMonitor. LogSourceStopTime**</span><span class="sxs-lookup"><span data-stu-id="823c9-129">**SystemMonitor.LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[<span data-ttu-id="823c9-130">**SystemMonitor. LogViewStart**</span><span class="sxs-lookup"><span data-stu-id="823c9-130">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="823c9-131">**SystemMonitor. SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="823c9-131">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





