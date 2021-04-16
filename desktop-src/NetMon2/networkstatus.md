---
description: La struttura NETWORKSTATUS descrive lo stato corrente dell'oggetto NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Struttura NETWORKSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530228"
---
# <a name="networkstatus-structure"></a><span data-ttu-id="21d52-103">Struttura NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="21d52-103">NETWORKSTATUS structure</span></span>

<span data-ttu-id="21d52-104">La struttura **NETWORKSTATUS** descrive lo stato corrente dell'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="21d52-104">The **NETWORKSTATUS** structure describes the current status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="21d52-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21d52-105">Syntax</span></span>


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a><span data-ttu-id="21d52-106">Members</span><span class="sxs-lookup"><span data-stu-id="21d52-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="21d52-107">**State**</span><span class="sxs-lookup"><span data-stu-id="21d52-107">**State**</span></span>
</dt> <dd>

<span data-ttu-id="21d52-108">Indica lo stato corrente dell'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="21d52-108">Indicates the current state of the NPP.</span></span>



| <span data-ttu-id="21d52-109">Valore</span><span class="sxs-lookup"><span data-stu-id="21d52-109">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="21d52-110">Significato</span><span class="sxs-lookup"><span data-stu-id="21d52-110">Meaning</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <span data-ttu-id="21d52-111"><dt>**\_stato NETWORKSTATUS \_ void**</dt></span><span class="sxs-lookup"><span data-stu-id="21d52-111"><dt>**NETWORKSTATUS\_STATE\_VOID**</dt></span></span> </dl>                | <span data-ttu-id="21d52-112">L'oggetto NPP non è connesso oppure è connesso e l'acquisizione non è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="21d52-112">The NPP is not connected, or it is connected and the capture is not started.</span></span><br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <span data-ttu-id="21d52-113"><dt>**\_acquisizione stato \_ NETWORKSTATUS**</dt></span><span class="sxs-lookup"><span data-stu-id="21d52-113"><dt>**NETWORKSTATUS\_STATE\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="21d52-114">L'oggetto NPP sta acquisendo i dati.</span><span class="sxs-lookup"><span data-stu-id="21d52-114">The NPP is capturing data.</span></span><br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <span data-ttu-id="21d52-115"><dt>**\_stato NETWORKSTATUS \_ sospeso**</dt></span><span class="sxs-lookup"><span data-stu-id="21d52-115"><dt>**NETWORKSTATUS\_STATE\_PAUSED**</dt></span></span> </dl>          | <span data-ttu-id="21d52-116">L'oggetto NPP è stato sospeso durante l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="21d52-116">The NPP has paused while capturing data.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="21d52-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="21d52-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="21d52-118">Flag che descrivono lo stato corrente dell'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="21d52-118">Flags that describe the current state of the NPP.</span></span>



| <span data-ttu-id="21d52-119">Valore</span><span class="sxs-lookup"><span data-stu-id="21d52-119">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="21d52-120">Significato</span><span class="sxs-lookup"><span data-stu-id="21d52-120">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <span data-ttu-id="21d52-121"><dt>**\_trigger flag \_ NETWORKSTATUS \_ in sospeso**</dt></span><span class="sxs-lookup"><span data-stu-id="21d52-121"><dt>**NETWORKSTATUS\_FLAGS\_TRIGGER\_PENDING**</dt></span></span> </dl> | <span data-ttu-id="21d52-122">È presente un trigger in sospeso per l'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="21d52-122">There is a trigger pending for the NPP.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21d52-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="21d52-123">Remarks</span></span>

<span data-ttu-id="21d52-124">Quando si usa questa struttura, è necessario allocare la memoria per la struttura prima di poterla usare e liberare la memoria quando la struttura non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="21d52-124">When using this structure, you must allocate the memory for the structure before it can be used and free the memory when the structure is no longer needed.</span></span>

<span data-ttu-id="21d52-125">L'elenco vedere anche nella parte inferiore di questo argomento elenca tutti i metodi che utilizzano questa struttura.</span><span class="sxs-lookup"><span data-stu-id="21d52-125">The See Also list at the bottom of this topic lists all the methods that use this structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="21d52-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21d52-126">Requirements</span></span>



| <span data-ttu-id="21d52-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="21d52-127">Requirement</span></span> | <span data-ttu-id="21d52-128">Valore</span><span class="sxs-lookup"><span data-stu-id="21d52-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="21d52-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21d52-129">Minimum supported client</span></span><br/> | <span data-ttu-id="21d52-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="21d52-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="21d52-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21d52-131">Minimum supported server</span></span><br/> | <span data-ttu-id="21d52-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="21d52-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="21d52-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21d52-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="21d52-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="21d52-134"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21d52-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21d52-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d52-136">IDelaydC:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="21d52-136">IDelaydC::QueryStatus</span></span>](idelaydc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="21d52-137">IESP:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="21d52-137">IESP::QueryStatus</span></span>](iesp-querystatus.md)
</dt> <dt>

[<span data-ttu-id="21d52-138">IRTC:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="21d52-138">IRTC::QueryStatus</span></span>](irtc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="21d52-139">IStats:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="21d52-139">IStats::QueryStatus</span></span>](istats-querystatus.md)
</dt> </dl>

 

 




