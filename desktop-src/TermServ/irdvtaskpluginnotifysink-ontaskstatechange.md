---
title: Metodo IRDVTaskPluginNotifySink OnTaskStateChange
description: Utilizzato per notificare all'agente del trigger che lo stato di un'attività è stato modificato.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnTaskStateChange
- Metodo OnTaskStateChange Servizi Desktop remoto, interfaccia IRDVTaskPluginNotifySink
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto, metodo OnTaskStateChange
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302574"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a><span data-ttu-id="4a4ff-106">Metodo IRDVTaskPluginNotifySink:: OnTaskStateChange</span><span class="sxs-lookup"><span data-stu-id="4a4ff-106">IRDVTaskPluginNotifySink::OnTaskStateChange method</span></span>

<span data-ttu-id="4a4ff-107">Utilizzato per notificare all'agente del trigger che lo stato di un'attività è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="4a4ff-107">Used to notify the trigger agent that the state of a task has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4ff-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a4ff-108">Syntax</span></span>


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a><span data-ttu-id="4a4ff-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a4ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a4ff-110">*bstrIdentifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a4ff-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4ff-111">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4a4ff-111">Type: **BSTR**</span></span>

<span data-ttu-id="4a4ff-112">Identificatore dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4a4ff-112">The identifier of the task.</span></span> <span data-ttu-id="4a4ff-113">Si tratta dell'identificatore passato al metodo [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="4a4ff-113">This is the identifier passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="4a4ff-114">*stato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4a4ff-114">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4ff-115">Tipo: **[ **\_ \_ stato attività RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span><span class="sxs-lookup"><span data-stu-id="4a4ff-115">Type: **[**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span></span>

<span data-ttu-id="4a4ff-116">Valore dell'enumerazione dello [**\_ \_ stato dell'attività RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) che specifica il nuovo stato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4a4ff-116">A value of the [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration that specifies the new state of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a4ff-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a4ff-117">Return value</span></span>

<span data-ttu-id="4a4ff-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a4ff-118">Type: **HRESULT**</span></span>

<span data-ttu-id="4a4ff-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4a4ff-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a4ff-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a4ff-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a4ff-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a4ff-121">Requirements</span></span>



| <span data-ttu-id="4a4ff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a4ff-122">Requirement</span></span> | <span data-ttu-id="4a4ff-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4a4ff-123">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="4a4ff-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a4ff-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4a4ff-125">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="4a4ff-125">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="4a4ff-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a4ff-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4a4ff-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4a4ff-127">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a4ff-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a4ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4ff-129">**\_stato attività \_ RDV**</span><span class="sxs-lookup"><span data-stu-id="4a4ff-129">**RDV\_TASK\_STATUS**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[<span data-ttu-id="4a4ff-130">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="4a4ff-130">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





