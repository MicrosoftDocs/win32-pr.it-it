---
title: LogFiles. Add (metodo)
description: Aggiunge un file di log alla raccolta.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Aggiungere il metodo SysMon
- Add Method SysMon, classe LogFiles
- Classe LogFiles SysMon, Add (metodo)
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119870"
---
# <a name="logfilesadd-method"></a><span data-ttu-id="ce6f1-106">LogFiles. Add (metodo)</span><span class="sxs-lookup"><span data-stu-id="ce6f1-106">LogFiles.Add method</span></span>

<span data-ttu-id="ce6f1-107">Aggiunge un file di log alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="ce6f1-107">Adds a log file to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce6f1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce6f1-108">Syntax</span></span>


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a><span data-ttu-id="ce6f1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce6f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce6f1-110">*nome percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce6f1-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce6f1-111">Percorso del file di log.</span><span class="sxs-lookup"><span data-stu-id="ce6f1-111">Path to the log file.</span></span> <span data-ttu-id="ce6f1-112">È possibile specificare il percorso come percorso assoluto, relativo o UNC.</span><span class="sxs-lookup"><span data-stu-id="ce6f1-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="ce6f1-113">L'estensione del nome del file di log deve essere CSV, TSV o.</span><span class="sxs-lookup"><span data-stu-id="ce6f1-113">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce6f1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce6f1-114">Remarks</span></span>

<span data-ttu-id="ce6f1-115">È necessario utilizzare lo strumento Logman.exe o lo snap-in MMC Perfmon. msc per generare i file di log aggiunti a questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="ce6f1-115">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="ce6f1-116">Per PerfMon. msc, i registri dei contatori si trovano in **avvisi e registri di prestazioni**.</span><span class="sxs-lookup"><span data-stu-id="ce6f1-116">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="ce6f1-117">Per informazioni dettagliate sull'utilizzo di Logman.exe o Perfmon. msc, cercare rispettivamente logman o using performance in **Help and Support Center**.</span><span class="sxs-lookup"><span data-stu-id="ce6f1-117">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

<span data-ttu-id="ce6f1-118">**Prima di Windows Vista:** Non è possibile aggiungere file di log alla [**raccolta di file di log**](systemmonitor-logfiles.md) se il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="ce6f1-118">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="ce6f1-119">Per prima cosa, impostare **SystemMonitor. DataSourceType** su **DataSourceTypeConstants.sysmonNullDataSource**, aggiungere i file di log e i contatori, quindi impostare **SystemMonitor. DataSourceType** su **DataSourceTypeConstants.sysmonLogFiles**.</span><span class="sxs-lookup"><span data-stu-id="ce6f1-119">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6f1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce6f1-120">Requirements</span></span>



| <span data-ttu-id="ce6f1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce6f1-121">Requirement</span></span> | <span data-ttu-id="ce6f1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ce6f1-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6f1-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce6f1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6f1-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce6f1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ce6f1-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce6f1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6f1-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce6f1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce6f1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ce6f1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce6f1-128"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ce6f1-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce6f1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce6f1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6f1-130">LogFiles</span><span class="sxs-lookup"><span data-stu-id="ce6f1-130">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="ce6f1-131">**LogFileItem**</span><span class="sxs-lookup"><span data-stu-id="ce6f1-131">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="ce6f1-132">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="ce6f1-132">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





