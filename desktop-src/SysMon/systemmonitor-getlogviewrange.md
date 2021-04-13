---
title: SystemMonitor. GetLogViewRange, metodo
description: Recupera la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Metodo GetLogViewRange SysMon
- Metodo GetLogViewRange SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo GetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517799"
---
# <a name="systemmonitorgetlogviewrange-method"></a><span data-ttu-id="8f244-106">SystemMonitor. GetLogViewRange, metodo</span><span class="sxs-lookup"><span data-stu-id="8f244-106">SystemMonitor.GetLogViewRange method</span></span>

<span data-ttu-id="8f244-107">Recupera la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.</span><span class="sxs-lookup"><span data-stu-id="8f244-107">Retrieves the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f244-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f244-108">Syntax</span></span>


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="8f244-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f244-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f244-110">*StartTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8f244-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f244-111">Data di inizio utilizzata per recuperare i valori dei contatori dai file di log.</span><span class="sxs-lookup"><span data-stu-id="8f244-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="8f244-112">*StopTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8f244-112">*StopTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f244-113">Data di fine utilizzata per recuperare i valori dei contatori dai file di log.</span><span class="sxs-lookup"><span data-stu-id="8f244-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f244-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f244-114">Return value</span></span>

<span data-ttu-id="8f244-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8f244-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f244-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f244-116">Remarks</span></span>

<span data-ttu-id="8f244-117">SYSMON recupera i valori dei contatori dai file di log che rientrano nelle date di inizio e di fine, inclusi.</span><span class="sxs-lookup"><span data-stu-id="8f244-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="8f244-118">L'utilizzo di questo metodo è analogo all'accesso alle proprietà [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) .</span><span class="sxs-lookup"><span data-stu-id="8f244-118">Using this method is the same as accessing the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f244-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f244-119">Requirements</span></span>



| <span data-ttu-id="8f244-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f244-120">Requirement</span></span> | <span data-ttu-id="8f244-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8f244-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f244-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f244-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8f244-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f244-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f244-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f244-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8f244-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8f244-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f244-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8f244-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f244-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8f244-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f244-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f244-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f244-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="8f244-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="8f244-130">**SystemMonitor. SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="8f244-130">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





