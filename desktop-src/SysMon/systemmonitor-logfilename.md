---
title: Proprietà SystemMonitor. LogFilename
description: Recupera o imposta il nome di un file di log da utilizzare come origine dei valori del contatore visualizzati nel monitor di sistema.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- Proprietà LogFilename SysMon
- Proprietà LogFilename SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà LogFilename
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400647"
---
# <a name="systemmonitorlogfilename-property"></a><span data-ttu-id="f3247-106">Proprietà SystemMonitor. LogFilename</span><span class="sxs-lookup"><span data-stu-id="f3247-106">SystemMonitor.LogFileName property</span></span>

<span data-ttu-id="f3247-107">Recupera o imposta il nome di un file di log da utilizzare come origine dei valori del contatore visualizzati nel monitor di sistema.</span><span class="sxs-lookup"><span data-stu-id="f3247-107">Retrieves or sets the name of a log file to use as the source of counter values displayed in the System Monitor.</span></span>

> [!Note]  
> <span data-ttu-id="f3247-108">Questa proprietà è stata resa obsoleta dalla proprietà [**LogFiles**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="f3247-108">This property has been made obsolete by the [**LogFiles**](systemmonitor-logfiles.md) property.</span></span>

 

<span data-ttu-id="f3247-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f3247-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3247-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3247-110">Syntax</span></span>


```VB
Property LogFileName As String
```



## <a name="property-value"></a><span data-ttu-id="f3247-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f3247-111">Property value</span></span>

<span data-ttu-id="f3247-112">Percorso del file di log.</span><span class="sxs-lookup"><span data-stu-id="f3247-112">Path to the log file.</span></span> <span data-ttu-id="f3247-113">È possibile specificare un percorso assoluto, relativo o UNC.</span><span class="sxs-lookup"><span data-stu-id="f3247-113">You can specify an absolute, relative, or UNC path.</span></span> <span data-ttu-id="f3247-114">L'estensione del nome del file di log deve essere CSV, TSV o.</span><span class="sxs-lookup"><span data-stu-id="f3247-114">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

## <a name="exceptions"></a><span data-ttu-id="f3247-115">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="f3247-115">Exceptions</span></span>



| <span data-ttu-id="f3247-116">Tipo di eccezione</span><span class="sxs-lookup"><span data-stu-id="f3247-116">Exception type</span></span>                                  | <span data-ttu-id="f3247-117">Condizione</span><span class="sxs-lookup"><span data-stu-id="f3247-117">Condition</span></span>                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="f3247-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="f3247-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="f3247-119">Impossibile trovare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="f3247-119">Unable to find the specified file.</span></span> <span data-ttu-id="f3247-120">Il valore ERR. Number è 0xC0000BD1.</span><span class="sxs-lookup"><span data-stu-id="f3247-120">The Err.Number value is 0xC0000BD1.</span></span> |
| <span data-ttu-id="f3247-121">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="f3247-121">**System.ArgumentException**</span></span>                    | <span data-ttu-id="f3247-122">Non è possibile specificare una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="f3247-122">You cannot specify an empty string.</span></span>                                    |



 

## <a name="remarks"></a><span data-ttu-id="f3247-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3247-123">Remarks</span></span>

<span data-ttu-id="f3247-124">Questa proprietà restituisce il nome del file di log dal primo membro della raccolta [**LogFiles**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="f3247-124">This property returns the log file name from the first member of the [**LogFiles**](systemmonitor-logfiles.md) collection.</span></span>

<span data-ttu-id="f3247-125">L'impostazione di questa proprietà avrà esito negativo se la raccolta [**LogFiles**](systemmonitor-logfiles.md) contiene uno o più membri.</span><span class="sxs-lookup"><span data-stu-id="f3247-125">Setting this property will fail if the [**LogFiles**](systemmonitor-logfiles.md) collection contains one or more members.</span></span>

<span data-ttu-id="f3247-126">È necessario utilizzare lo strumento Logman.exe o lo snap-in MMC Perfmon. msc per generare i file di log aggiunti a questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="f3247-126">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="f3247-127">Per PerfMon. msc, i registri dei contatori si trovano in **avvisi e registri di prestazioni**.</span><span class="sxs-lookup"><span data-stu-id="f3247-127">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="f3247-128">Per informazioni dettagliate sull'utilizzo di Logman.exe o Perfmon. msc, cercare rispettivamente logman o using performance in **Help and Support Center**.</span><span class="sxs-lookup"><span data-stu-id="f3247-128">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3247-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3247-129">Requirements</span></span>



| <span data-ttu-id="f3247-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3247-130">Requirement</span></span> | <span data-ttu-id="f3247-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f3247-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3247-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3247-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f3247-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f3247-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f3247-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3247-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f3247-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f3247-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3247-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f3247-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3247-137"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f3247-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3247-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3247-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3247-139">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="f3247-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="f3247-140">**SystemMonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="f3247-140">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





