---
title: Proprietà SystemMonitor. LogFiles
description: Raccolta di uno o più file di log da utilizzare come origine dei valori del contatore visualizzati nel monitor di sistema.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Proprietà LogFiles SysMon
- Proprietà LogFiles SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, Proprietà LogFiles
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301578"
---
# <a name="systemmonitorlogfiles-property"></a><span data-ttu-id="fc2ef-106">Proprietà SystemMonitor. LogFiles</span><span class="sxs-lookup"><span data-stu-id="fc2ef-106">SystemMonitor.LogFiles property</span></span>

<span data-ttu-id="fc2ef-107">Raccolta di uno o più file di log da utilizzare come origine dei valori del contatore visualizzati nel monitor di sistema.</span><span class="sxs-lookup"><span data-stu-id="fc2ef-107">Collection of one or more log files to use as the source of counter values displayed in the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc2ef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc2ef-108">Syntax</span></span>


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a><span data-ttu-id="fc2ef-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fc2ef-109">Property value</span></span>

<span data-ttu-id="fc2ef-110">Raccolta di oggetti [**LogFileItem**](logfileitem.md) che specificano i file di log utilizzati come origine dati per il grafico.</span><span class="sxs-lookup"><span data-stu-id="fc2ef-110">Collection of [**LogFileItem**](logfileitem.md) objects that specify the log files used as the data source for the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc2ef-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc2ef-111">Remarks</span></span>

<span data-ttu-id="fc2ef-112">Per aggiungere o rimuovere un file di log dalla raccolta dei file di log, il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) non deve essere impostato su sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="fc2ef-112">To add or remove a log file from the log file collection, the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) must not be set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc2ef-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc2ef-113">Requirements</span></span>



| <span data-ttu-id="fc2ef-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc2ef-114">Requirement</span></span> | <span data-ttu-id="fc2ef-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fc2ef-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2ef-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc2ef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fc2ef-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fc2ef-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="fc2ef-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc2ef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fc2ef-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fc2ef-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc2ef-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fc2ef-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc2ef-121"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="fc2ef-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc2ef-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc2ef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2ef-123">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="fc2ef-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="fc2ef-124">**SystemMonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="fc2ef-124">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> <dt>

[<span data-ttu-id="fc2ef-125">**SystemMonitor. LogViewStart**</span><span class="sxs-lookup"><span data-stu-id="fc2ef-125">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="fc2ef-126">**SystemMonitor. LogViewStop**</span><span class="sxs-lookup"><span data-stu-id="fc2ef-126">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="fc2ef-127">**SystemMonitor. SqlLogSetName**</span><span class="sxs-lookup"><span data-stu-id="fc2ef-127">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





