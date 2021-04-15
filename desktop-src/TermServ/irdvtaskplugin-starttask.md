---
title: Metodo IRDVTaskPlugin StartTask
description: Chiamato per avviare l'attività di aggiornamento nella macchina virtuale.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo StartTask
- Metodo StartTask Servizi Desktop remoto, interfaccia IRDVTaskPlugin
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto, metodo StartTask
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477428"
---
# <a name="irdvtaskpluginstarttask-method"></a><span data-ttu-id="3f0bd-106">Metodo IRDVTaskPlugin:: StartTask</span><span class="sxs-lookup"><span data-stu-id="3f0bd-106">IRDVTaskPlugin::StartTask method</span></span>

<span data-ttu-id="3f0bd-107">Chiamato per avviare l'attività di aggiornamento nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3f0bd-107">Called to start the update task on the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f0bd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f0bd-108">Syntax</span></span>


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a><span data-ttu-id="3f0bd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f0bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f0bd-110">*Etichetta* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3f0bd-110">*Label* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0bd-111">Etichetta per l'attività.</span><span class="sxs-lookup"><span data-stu-id="3f0bd-111">The label for the task.</span></span> <span data-ttu-id="3f0bd-112">Si tratta dell'etichetta passata all'agente trigger nel metodo [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="3f0bd-112">This is the label that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="3f0bd-113">*Identificatore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3f0bd-113">*Identifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0bd-114">Identificatore dell'attività.</span><span class="sxs-lookup"><span data-stu-id="3f0bd-114">The identifier of the task.</span></span> <span data-ttu-id="3f0bd-115">Si tratta dell'identificatore passato all'agente trigger nel metodo [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="3f0bd-115">This is the identifier that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="3f0bd-116">*Contesto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f0bd-116">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0bd-117">Dati facoltativi per l'attività.</span><span class="sxs-lookup"><span data-stu-id="3f0bd-117">Optional data for the task.</span></span> <span data-ttu-id="3f0bd-118">Si tratta dei dati passati all'agente trigger nel metodo [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="3f0bd-118">This is the data that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f0bd-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f0bd-119">Return value</span></span>

<span data-ttu-id="3f0bd-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3f0bd-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f0bd-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f0bd-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f0bd-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f0bd-122">Requirements</span></span>



| <span data-ttu-id="3f0bd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f0bd-123">Requirement</span></span> | <span data-ttu-id="3f0bd-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3f0bd-124">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="3f0bd-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f0bd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3f0bd-126">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="3f0bd-126">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="3f0bd-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f0bd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3f0bd-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f0bd-128">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f0bd-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f0bd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f0bd-130">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="3f0bd-130">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





