---
title: Struttura ORPC_INIT_ARGS
description: La \_ struttura ORPC init \_ args contiene le informazioni usate per inizializzare il debug remoto usando l'interfaccia IOrpcDebugNotify.
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- COM struttura ORPC_INIT_ARGS
- Puntatore a struttura LPORPC_INIT_ARGS COM
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119362"
---
# <a name="orpc_init_args-structure"></a><span data-ttu-id="7c5a3-105">\_Struttura ORPC init \_ args</span><span class="sxs-lookup"><span data-stu-id="7c5a3-105">ORPC\_INIT\_ARGS structure</span></span>

<span data-ttu-id="7c5a3-106">La struttura **ORPC \_ init \_ args** contiene le informazioni usate per inizializzare il debug remoto usando l'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="7c5a3-106">The **ORPC\_INIT\_ARGS** structure contains information used to initialize remote debugging using the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c5a3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c5a3-107">Syntax</span></span>


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a><span data-ttu-id="7c5a3-108">Members</span><span class="sxs-lookup"><span data-stu-id="7c5a3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c5a3-109">**lpIntfOrpcDebug**</span><span class="sxs-lookup"><span data-stu-id="7c5a3-109">**lpIntfOrpcDebug**</span></span>
</dt> <dd>

<span data-ttu-id="7c5a3-110">Puntatore all'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) per l'uso da parte dei debugger in-process.</span><span class="sxs-lookup"><span data-stu-id="7c5a3-110">A pointer to the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface for use by in-process debuggers.</span></span> <span data-ttu-id="7c5a3-111">Se il debugger non è in-process o è un sistema Macintosh, questo campo deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="7c5a3-111">If the debugger is not in-process or is a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7c5a3-112">**pvPSN**</span><span class="sxs-lookup"><span data-stu-id="7c5a3-112">**pvPSN**</span></span>
</dt> <dd>

<span data-ttu-id="7c5a3-113">Puntatore al numero di serie del processo Macintosh del processo del debug.</span><span class="sxs-lookup"><span data-stu-id="7c5a3-113">A pointer to the Macintosh process serial number of the debuggee's process.</span></span> <span data-ttu-id="7c5a3-114">Se l'oggetto del debug non è un sistema Macintosh, questo campo deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="7c5a3-114">If the debuggee is not a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7c5a3-115">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="7c5a3-115">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="7c5a3-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7c5a3-116">Reserved.</span></span> <span data-ttu-id="7c5a3-117">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="7c5a3-117">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="7c5a3-118">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="7c5a3-118">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="7c5a3-119">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7c5a3-119">Reserved.</span></span> <span data-ttu-id="7c5a3-120">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="7c5a3-120">Must be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c5a3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c5a3-121">Requirements</span></span>



| <span data-ttu-id="7c5a3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c5a3-122">Requirement</span></span> | <span data-ttu-id="7c5a3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7c5a3-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="7c5a3-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c5a3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7c5a3-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c5a3-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="7c5a3-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c5a3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7c5a3-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c5a3-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7c5a3-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c5a3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c5a3-129"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="7c5a3-129"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c5a3-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c5a3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c5a3-131">**ORPC \_ dbg \_ All**</span><span class="sxs-lookup"><span data-stu-id="7c5a3-131">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="7c5a3-132">**\_buffer dbg \_ ORPC**</span><span class="sxs-lookup"><span data-stu-id="7c5a3-132">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="7c5a3-133">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="7c5a3-133">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="7c5a3-134">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="7c5a3-134">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





