---
title: SystemMonitor. relog, metodo
description: Registra i dati del contatore in un nuovo file. È inoltre possibile utilizzare questo metodo per specificare un nuovo tipo di file e per ridurre il numero di campioni contenuti nel file di log.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Metodo relog SysMon
- Metodo relog SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo relog
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d0a6e44ef73652bd563099929ce601670610b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119523"
---
# <a name="systemmonitorrelog-method"></a><span data-ttu-id="cb936-107">SystemMonitor. relog, metodo</span><span class="sxs-lookup"><span data-stu-id="cb936-107">SystemMonitor.Relog method</span></span>

<span data-ttu-id="cb936-108">Registra i dati del contatore in un nuovo file.</span><span class="sxs-lookup"><span data-stu-id="cb936-108">Relogs the counter data to a new file.</span></span> <span data-ttu-id="cb936-109">È inoltre possibile utilizzare questo metodo per specificare un nuovo tipo di file e per ridurre il numero di campioni contenuti nel file di log.</span><span class="sxs-lookup"><span data-stu-id="cb936-109">You can also use this method to specify a new file type and to reduce the number of samples contained in the log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb936-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb936-110">Syntax</span></span>


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="cb936-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb936-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb936-112">*nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb936-112">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb936-113">Percorso del file di log.</span><span class="sxs-lookup"><span data-stu-id="cb936-113">File path of the log file.</span></span> <span data-ttu-id="cb936-114">È possibile specificare il percorso come percorso assoluto, relativo o UNC.</span><span class="sxs-lookup"><span data-stu-id="cb936-114">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="cb936-115">L'estensione del nome del file di log deve essere. grosso,. TSV o. csv.</span><span class="sxs-lookup"><span data-stu-id="cb936-115">The log file name extension must be either .blg, .tsv, or .csv.</span></span> <span data-ttu-id="cb936-116">Se una cartella nel percorso non esiste, verrà creata da SYSMON.</span><span class="sxs-lookup"><span data-stu-id="cb936-116">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="cb936-117">Se il file esiste, il file viene sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="cb936-117">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="cb936-118">SYSMON applica gli ACL predefiniti dalla directory padre.</span><span class="sxs-lookup"><span data-stu-id="cb936-118">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="cb936-119">*FileType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb936-119">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb936-120">Formato dei dati del contatore salvati nel file di log.</span><span class="sxs-lookup"><span data-stu-id="cb936-120">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="cb936-121">È possibile specificare [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysMonFileCsv** o **SysmonFileType.sysmonFileTsv**.</span><span class="sxs-lookup"><span data-stu-id="cb936-121">You can specify either [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysmonFileCsv**, or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> <dt>

<span data-ttu-id="cb936-122">*filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="cb936-122">*filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb936-123">Numero di campioni dei vecchi file di log da salvare nel nuovo file di log.</span><span class="sxs-lookup"><span data-stu-id="cb936-123">Number of samples from the old log files to save in the new log file.</span></span> <span data-ttu-id="cb936-124">Specificare 1 per salvare ogni esempio dai file precedenti ai nuovi file.</span><span class="sxs-lookup"><span data-stu-id="cb936-124">Specify 1 to save every sample from the old files to the new files.</span></span> <span data-ttu-id="cb936-125">Specificare 2 per salvare uno dei due campioni dal file precedente.</span><span class="sxs-lookup"><span data-stu-id="cb936-125">Specify 2 to save one out of every two samples from the old file.</span></span> <span data-ttu-id="cb936-126">Specificare 3 per salvare uno dei tre campioni dal file precedente.</span><span class="sxs-lookup"><span data-stu-id="cb936-126">Specify 3 to save one out of every three samples from the old file.</span></span> <span data-ttu-id="cb936-127">e così via.</span><span class="sxs-lookup"><span data-stu-id="cb936-127">And so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb936-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb936-128">Return value</span></span>

<span data-ttu-id="cb936-129">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cb936-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb936-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb936-130">Remarks</span></span>

<span data-ttu-id="cb936-131">Questo metodo utilizza i file di log contenuti nella raccolta [**SystemMonitor. LogFiles**](systemmonitor-logfiles.md) per relog i dati del contatore.</span><span class="sxs-lookup"><span data-stu-id="cb936-131">This method uses the log files contained in the [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md) collection to relog the counter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb936-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb936-132">Requirements</span></span>



| <span data-ttu-id="cb936-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb936-133">Requirement</span></span> | <span data-ttu-id="cb936-134">Valore</span><span class="sxs-lookup"><span data-stu-id="cb936-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb936-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb936-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cb936-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb936-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb936-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb936-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cb936-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb936-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb936-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cb936-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb936-140"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cb936-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb936-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb936-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb936-142">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="cb936-142">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="cb936-143">**SystemMonitor. SaveAs**</span><span class="sxs-lookup"><span data-stu-id="cb936-143">**SystemMonitor.SaveAs**</span></span>](systemmonitor-saveas.md)
</dt> </dl>

 

 





