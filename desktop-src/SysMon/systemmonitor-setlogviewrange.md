---
title: SystemMonitor. SetLogViewRange, metodo
description: Imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- Metodo SetLogViewRange SysMon
- Metodo SetLogViewRange SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo SetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400415"
---
# <a name="systemmonitorsetlogviewrange-method"></a><span data-ttu-id="5da74-106">SystemMonitor. SetLogViewRange, metodo</span><span class="sxs-lookup"><span data-stu-id="5da74-106">SystemMonitor.SetLogViewRange method</span></span>

<span data-ttu-id="5da74-107">Imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.</span><span class="sxs-lookup"><span data-stu-id="5da74-107">Sets the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da74-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5da74-108">Syntax</span></span>


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="5da74-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5da74-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5da74-110">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5da74-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5da74-111">Data di inizio utilizzata per recuperare i valori dei contatori dai file di log.</span><span class="sxs-lookup"><span data-stu-id="5da74-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="5da74-112">*StopTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5da74-112">*StopTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5da74-113">Data di fine utilizzata per recuperare i valori dei contatori dai file di log.</span><span class="sxs-lookup"><span data-stu-id="5da74-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5da74-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5da74-114">Return value</span></span>

<span data-ttu-id="5da74-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5da74-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5da74-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5da74-116">Remarks</span></span>

<span data-ttu-id="5da74-117">SYSMON recupera i valori dei contatori dai file di log che rientrano nelle date di inizio e di fine, inclusi.</span><span class="sxs-lookup"><span data-stu-id="5da74-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="5da74-118">Se non si specifica una data di inizio o si imposta la data di inizio su un valore di data non compreso nell'intervallo dei valori di data presenti nei file di log, SYSMON modifica il valore in un valore di data meno recente trovato nei file di log.</span><span class="sxs-lookup"><span data-stu-id="5da74-118">If you do not specify a start date or if you set the start date to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span> <span data-ttu-id="5da74-119">Se il valore iniziale è maggiore del valore di arresto, SYSMON modifica il valore iniziale in modo che corrisponda al valore di stop.</span><span class="sxs-lookup"><span data-stu-id="5da74-119">If the start value is greater than the stop value, SYSMON changes the start value to be the same value as the stop value.</span></span>

<span data-ttu-id="5da74-120">Se non si specifica un valore di interruzione o si imposta il valore di interruzione su un valore di data successivo all'ultima data contenuta nel file di log, SYSMON modifica il valore con il valore di data più recente trovato nei file di log.</span><span class="sxs-lookup"><span data-stu-id="5da74-120">If you do not specify a stop value or you set the stop value to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span> <span data-ttu-id="5da74-121">Se il valore di arresto è inferiore al valore di arresto, SYSMON modifica il valore di interruzione in modo che corrisponda al valore iniziale.</span><span class="sxs-lookup"><span data-stu-id="5da74-121">If the stop value is less than the stop value, SYSMON changes the stop value to be the same value as the start value.</span></span>

<span data-ttu-id="5da74-122">Se si specifica una data di inizio e di fine, è necessario specificare le date prima di impostare [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="5da74-122">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span> <span data-ttu-id="5da74-123">Se si impostano le date dopo l'impostazione di **SystemMonitor. DataSourceType**, solo il primo valore del contatore viene recuperato dal file di log.</span><span class="sxs-lookup"><span data-stu-id="5da74-123">If you set the dates after setting **SystemMonitor.DataSourceType**, then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="5da74-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5da74-124">Requirements</span></span>



| <span data-ttu-id="5da74-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5da74-125">Requirement</span></span> | <span data-ttu-id="5da74-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5da74-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5da74-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5da74-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5da74-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5da74-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5da74-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5da74-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5da74-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5da74-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5da74-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5da74-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5da74-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5da74-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5da74-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5da74-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da74-134">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="5da74-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="5da74-135">**SystemMonitor. GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="5da74-135">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





