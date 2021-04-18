---
description: La \_ struttura dell'evento Update aggiorna gli eventi. Questa struttura viene passata di nuovo all'applicazione chiamante tramite la procedura di callback dello stato dell'evento da parte di NPP.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: Struttura UPDATE_EVENT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310786"
---
# <a name="update_event-structure"></a><span data-ttu-id="b52e9-104">Aggiorna \_ struttura evento</span><span class="sxs-lookup"><span data-stu-id="b52e9-104">UPDATE\_EVENT structure</span></span>

<span data-ttu-id="b52e9-105">La struttura dell' **\_ evento Update** aggiorna gli eventi.</span><span class="sxs-lookup"><span data-stu-id="b52e9-105">The **UPDATE\_EVENT** structure updates events.</span></span> <span data-ttu-id="b52e9-106">Questa struttura viene passata di nuovo all'applicazione chiamante tramite la procedura di callback dello stato dell'evento da parte di NPP.</span><span class="sxs-lookup"><span data-stu-id="b52e9-106">This structure is passed back to the calling application via the event status callback procedure by the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="b52e9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b52e9-107">Syntax</span></span>


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a><span data-ttu-id="b52e9-108">Members</span><span class="sxs-lookup"><span data-stu-id="b52e9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b52e9-109">**Event**</span><span class="sxs-lookup"><span data-stu-id="b52e9-109">**Event**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-110">Evento effettivo registrato.</span><span class="sxs-lookup"><span data-stu-id="b52e9-110">Actual event being recorded.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-111">**Azione**</span><span class="sxs-lookup"><span data-stu-id="b52e9-111">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-112">Azione eseguita.</span><span class="sxs-lookup"><span data-stu-id="b52e9-112">The action taken.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-113">**Status**</span><span class="sxs-lookup"><span data-stu-id="b52e9-113">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-114">Indicazione sullo stato della rete.</span><span class="sxs-lookup"><span data-stu-id="b52e9-114">Network status indication.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-115">**Valore**</span><span class="sxs-lookup"><span data-stu-id="b52e9-115">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-116">Variabile contatore ausiliario.</span><span class="sxs-lookup"><span data-stu-id="b52e9-116">Auxiliary counter variable.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-117">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="b52e9-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-118">Eventi contrassegnati, in microsecondi.</span><span class="sxs-lookup"><span data-stu-id="b52e9-118">The marked events, in microseconds.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-119">**lpUserContext**</span><span class="sxs-lookup"><span data-stu-id="b52e9-119">**lpUserContext**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-120">Contesto utente fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b52e9-120">User context given by the application.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-121">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="b52e9-121">**lpReserved**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-122">Driver o NAL use.</span><span class="sxs-lookup"><span data-stu-id="b52e9-122">Driver or NAL use.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-123">**FramesDropped**</span><span class="sxs-lookup"><span data-stu-id="b52e9-123">**FramesDropped**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-124">Frame RTF rilasciati nel buffer specificato.</span><span class="sxs-lookup"><span data-stu-id="b52e9-124">RTF frames dropped in the specified buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="b52e9-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-126">Non viene restituito alcun dato con questa opzione switch.</span><span class="sxs-lookup"><span data-stu-id="b52e9-126">No data comes back with this switch option.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-127">**lpFrameTable**</span><span class="sxs-lookup"><span data-stu-id="b52e9-127">**lpFrameTable**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-128">Solo RTF.</span><span class="sxs-lookup"><span data-stu-id="b52e9-128">RTF only.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-129">**lpPacketQueue**</span><span class="sxs-lookup"><span data-stu-id="b52e9-129">**lpPacketQueue**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-130">Per le trasmissioni.</span><span class="sxs-lookup"><span data-stu-id="b52e9-130">For transmits.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-131">**SecurityResponse**</span><span class="sxs-lookup"><span data-stu-id="b52e9-131">**SecurityResponse**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-132">Risposta di monitoraggio sicurezza remota.</span><span class="sxs-lookup"><span data-stu-id="b52e9-132">Remote security monitor response.</span></span>

</dd> <dt>

<span data-ttu-id="b52e9-133">**lpFinalStats**</span><span class="sxs-lookup"><span data-stu-id="b52e9-133">**lpFinalStats**</span></span>
</dt> <dd>

<span data-ttu-id="b52e9-134">Questa operazione viene compilata solo in caso di interruzioni non correlate alla sicurezza (ad esempio, trigger).</span><span class="sxs-lookup"><span data-stu-id="b52e9-134">This is only filled in on non-security related stops (for example, triggers).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b52e9-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="b52e9-135">Remarks</span></span>

<span data-ttu-id="b52e9-136">Gli utenti di C++ devono tenere presente che la dichiarazione per questo callback deve trovarsi nella parte pubblica del file di intestazione:</span><span class="sxs-lookup"><span data-stu-id="b52e9-136">C++ users should note that the declaration for this callback should be in the public part of the header file:</span></span>

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

<span data-ttu-id="b52e9-137">L'implementazione deve trovarsi nella sezione protetta del file con estensione cpp:</span><span class="sxs-lookup"><span data-stu-id="b52e9-137">The implementation should be in the protected section of the .cpp file:</span></span>

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a><span data-ttu-id="b52e9-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b52e9-138">Requirements</span></span>



| <span data-ttu-id="b52e9-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b52e9-139">Requirement</span></span> | <span data-ttu-id="b52e9-140">Valore</span><span class="sxs-lookup"><span data-stu-id="b52e9-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b52e9-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b52e9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b52e9-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b52e9-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b52e9-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b52e9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b52e9-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b52e9-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b52e9-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b52e9-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b52e9-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b52e9-146"><dt>Netmon.h</dt></span></span> </dl> |



 

 




