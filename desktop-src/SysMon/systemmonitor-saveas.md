---
title: Metodo SystemMonitor. SaveAs
description: Salva i valori dei contatori nella visualizzazione grafico in un file di log.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- Metodo SaveAs SysMon
- Metodo SaveAs SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo SaveAs
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301572"
---
# <a name="systemmonitorsaveas-method"></a><span data-ttu-id="07d2a-106">Metodo SystemMonitor. SaveAs</span><span class="sxs-lookup"><span data-stu-id="07d2a-106">SystemMonitor.SaveAs method</span></span>

<span data-ttu-id="07d2a-107">Salva i valori dei contatori nella visualizzazione grafico in un file di log.</span><span class="sxs-lookup"><span data-stu-id="07d2a-107">Saves the counter values in the graph view to a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d2a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07d2a-108">Syntax</span></span>


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a><span data-ttu-id="07d2a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="07d2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d2a-110">*nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07d2a-110">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d2a-111">Percorso del file di log.</span><span class="sxs-lookup"><span data-stu-id="07d2a-111">File path of the log file.</span></span> <span data-ttu-id="07d2a-112">È possibile specificare il percorso come percorso assoluto, relativo o UNC.</span><span class="sxs-lookup"><span data-stu-id="07d2a-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="07d2a-113">L'estensione del nome del file di log deve essere. TSV o. htm.</span><span class="sxs-lookup"><span data-stu-id="07d2a-113">The log file name extension must be either .tsv or .htm.</span></span> <span data-ttu-id="07d2a-114">Se una cartella nel percorso non esiste, verrà creata da SYSMON.</span><span class="sxs-lookup"><span data-stu-id="07d2a-114">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="07d2a-115">Se il file esiste, il file viene sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="07d2a-115">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="07d2a-116">SYSMON applica gli ACL predefiniti dalla directory padre.</span><span class="sxs-lookup"><span data-stu-id="07d2a-116">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="07d2a-117">*FileType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07d2a-117">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d2a-118">Formato dei dati del contatore salvati nel file di log.</span><span class="sxs-lookup"><span data-stu-id="07d2a-118">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="07d2a-119">È possibile specificare [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) o **SysmonFileType.sysmonFileTsv**.</span><span class="sxs-lookup"><span data-stu-id="07d2a-119">You can specify either [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d2a-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07d2a-120">Return value</span></span>

<span data-ttu-id="07d2a-121">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="07d2a-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07d2a-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="07d2a-122">Remarks</span></span>

<span data-ttu-id="07d2a-123">Vengono salvati solo i dati del contatore visibili nella visualizzazione grafico (per il numero effettivo di punti dati salvati, vedere [**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md)).</span><span class="sxs-lookup"><span data-stu-id="07d2a-123">Only the counter data visible in the graph view is saved (for the actual number of data points saved, see [**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="07d2a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07d2a-124">Requirements</span></span>



| <span data-ttu-id="07d2a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d2a-125">Requirement</span></span> | <span data-ttu-id="07d2a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="07d2a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07d2a-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07d2a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="07d2a-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07d2a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07d2a-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07d2a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="07d2a-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07d2a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07d2a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="07d2a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07d2a-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="07d2a-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07d2a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07d2a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d2a-134">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="07d2a-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="07d2a-135">**SystemMonitor. relog**</span><span class="sxs-lookup"><span data-stu-id="07d2a-135">**SystemMonitor.Relog**</span></span>](systemmonitor-relog.md)
</dt> </dl>

 

 





