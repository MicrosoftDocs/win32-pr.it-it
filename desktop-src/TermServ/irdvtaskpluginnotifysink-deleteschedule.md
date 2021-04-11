---
title: Metodo IRDVTaskPluginNotifySink DeleteSchedule
description: Chiamato dall'agente attività per eliminare un'attività pianificata.
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo DeleteSchedule
- Metodo DeleteSchedule Servizi Desktop remoto, interfaccia IRDVTaskPluginNotifySink
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto, Metodo DeleteSchedule
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f00bcc740f87acb7f051decd5f2fc9b55ffbf642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121430"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a><span data-ttu-id="fc14c-106">IRDVTaskPluginNotifySink::D Metodo eleteSchedule</span><span class="sxs-lookup"><span data-stu-id="fc14c-106">IRDVTaskPluginNotifySink::DeleteSchedule method</span></span>

<span data-ttu-id="fc14c-107">Chiamato dall'agente attività per eliminare un'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="fc14c-107">Called by the task agent to delete a scheduled task.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc14c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc14c-108">Syntax</span></span>


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a><span data-ttu-id="fc14c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc14c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc14c-110">*bstrIdentifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc14c-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc14c-111">Identificatore dell'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="fc14c-111">The identifier of the scheduled task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc14c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc14c-112">Return value</span></span>

<span data-ttu-id="fc14c-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fc14c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fc14c-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fc14c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc14c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc14c-115">Requirements</span></span>



| <span data-ttu-id="fc14c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc14c-116">Requirement</span></span> | <span data-ttu-id="fc14c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fc14c-117">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="fc14c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc14c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fc14c-119">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="fc14c-119">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="fc14c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc14c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fc14c-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fc14c-121">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc14c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc14c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc14c-123">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="fc14c-123">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





