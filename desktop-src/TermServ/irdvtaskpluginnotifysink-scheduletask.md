---
title: Metodo IRDVTaskPluginNotifySink ScheduleTask
description: Chiamato dall'agente attività per pianificare un'attività.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo ScheduleTask
- Metodo ScheduleTask Servizi Desktop remoto, interfaccia IRDVTaskPluginNotifySink
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto, Metodo ScheduleTask
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874506"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a><span data-ttu-id="5a6fd-106">Metodo IRDVTaskPluginNotifySink:: ScheduleTask</span><span class="sxs-lookup"><span data-stu-id="5a6fd-106">IRDVTaskPluginNotifySink::ScheduleTask method</span></span>

<span data-ttu-id="5a6fd-107">Chiamato dall'agente attività per pianificare un'attività.</span><span class="sxs-lookup"><span data-stu-id="5a6fd-107">Called by the task agent to schedule a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a6fd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a6fd-108">Syntax</span></span>


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a><span data-ttu-id="5a6fd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a6fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a6fd-110">*ftStartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a6fd-110">*ftStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6fd-111">Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="5a6fd-111">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="5a6fd-112">Ora di inizio dell'attività più recente, in formato UTC.</span><span class="sxs-lookup"><span data-stu-id="5a6fd-112">The earliest task start time, in UTC.</span></span>

</dd> <dt>

<span data-ttu-id="5a6fd-113">*ftEndTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a6fd-113">*ftEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6fd-114">Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="5a6fd-114">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="5a6fd-115">Ora di fine dell'attività, in formato UTC.</span><span class="sxs-lookup"><span data-stu-id="5a6fd-115">The task end time, in UTC.</span></span> <span data-ttu-id="5a6fd-116">Passare un oggetto [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) impostato su tutti gli zeri se non viene specificata alcuna ora di fine.</span><span class="sxs-lookup"><span data-stu-id="5a6fd-116">Pass a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) set to all zeros if no end time is specified.</span></span>

</dd> <dt>

<span data-ttu-id="5a6fd-117">*ftDeadline* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a6fd-117">*ftDeadline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6fd-118">Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="5a6fd-118">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="5a6fd-119">Scadenza dell'attività, in formato UTC.</span><span class="sxs-lookup"><span data-stu-id="5a6fd-119">The task deadline, in UTC.</span></span> <span data-ttu-id="5a6fd-120">Viene usato per impostare la priorità per più attività che si trovano all'interno della finestra di avvio.</span><span class="sxs-lookup"><span data-stu-id="5a6fd-120">This is used to set priority for multiple tasks that are within their start window.</span></span> <span data-ttu-id="5a6fd-121">Se deve essere avviata più di un'attività, quella con la prima scadenza verrà avviata per prima.</span><span class="sxs-lookup"><span data-stu-id="5a6fd-121">If more than one task should be started, the one with the earliest deadline will be started first.</span></span>

</dd> <dt>

<span data-ttu-id="5a6fd-122">*bstrLabel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a6fd-122">*bstrLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6fd-123">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5a6fd-123">Type: **BSTR**</span></span>

<span data-ttu-id="5a6fd-124">Etichetta per l'attività.</span><span class="sxs-lookup"><span data-stu-id="5a6fd-124">The label for the task.</span></span> <span data-ttu-id="5a6fd-125">Viene passato al metodo [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="5a6fd-125">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="5a6fd-126">*bstrIdentifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a6fd-126">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6fd-127">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5a6fd-127">Type: **BSTR**</span></span>

<span data-ttu-id="5a6fd-128">Identificatore dell'attività.</span><span class="sxs-lookup"><span data-stu-id="5a6fd-128">The identifier of the task.</span></span> <span data-ttu-id="5a6fd-129">Viene passato al metodo [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="5a6fd-129">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="5a6fd-130">*saContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a6fd-130">*saContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6fd-131">Tipo: **SAFEARRAY (byte)**</span><span class="sxs-lookup"><span data-stu-id="5a6fd-131">Type: **SAFEARRAY(BYTE)**</span></span>

<span data-ttu-id="5a6fd-132">Dati facoltativi per l'attività.</span><span class="sxs-lookup"><span data-stu-id="5a6fd-132">Optional data for the task.</span></span> <span data-ttu-id="5a6fd-133">Viene passato al metodo [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="5a6fd-133">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a6fd-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a6fd-134">Return value</span></span>

<span data-ttu-id="5a6fd-135">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5a6fd-135">Type: **HRESULT**</span></span>

<span data-ttu-id="5a6fd-136">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5a6fd-136">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a6fd-137">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a6fd-137">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a6fd-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a6fd-138">Requirements</span></span>



| <span data-ttu-id="5a6fd-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a6fd-139">Requirement</span></span> | <span data-ttu-id="5a6fd-140">Valore</span><span class="sxs-lookup"><span data-stu-id="5a6fd-140">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="5a6fd-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a6fd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5a6fd-142">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="5a6fd-142">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="5a6fd-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a6fd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5a6fd-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5a6fd-144">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a6fd-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a6fd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a6fd-146">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="5a6fd-146">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

