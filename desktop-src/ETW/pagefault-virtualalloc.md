---
description: Questa classe è la classe del tipo di evento per gli eventi di allocazione virtuale. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: Classe PageFault_VirtualAlloc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: f9e754bc3dc09f492682d5a522a6489cfde27ceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344001"
---
# <a name="pagefault_virtualalloc-class"></a><span data-ttu-id="e1dbd-104">\_Classe pagefault VirtualAlloc</span><span class="sxs-lookup"><span data-stu-id="e1dbd-104">PageFault\_VirtualAlloc class</span></span>

<span data-ttu-id="e1dbd-105">Questa classe è la classe del tipo di evento per gli eventi di allocazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-105">This class is the event type class for virtual allocation events.</span></span>

<span data-ttu-id="e1dbd-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1dbd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1dbd-107">Syntax</span></span>

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="e1dbd-108">Members</span><span class="sxs-lookup"><span data-stu-id="e1dbd-108">Members</span></span>

<span data-ttu-id="e1dbd-109">La **classe \_ VirtualAlloc di pagefault** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e1dbd-109">The **PageFault\_VirtualAlloc** class has these types of members:</span></span>

-   [<span data-ttu-id="e1dbd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1dbd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1dbd-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1dbd-111">Properties</span></span>

<span data-ttu-id="e1dbd-112">La **classe \_ VirtualAlloc di pagefault** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-112">The **PageFault\_VirtualAlloc** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1dbd-113">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-113">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1dbd-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1dbd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-116">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="e1dbd-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e1dbd-117">Indirizzo iniziale a cui è stata allocata o liberata la memoria.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-117">The starting address at which memory was allocated or freed.</span></span>

</dd> <dt>

<span data-ttu-id="e1dbd-118">**Flag**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-118">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1dbd-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1dbd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-121">Qualificatori: WmiDataId (4), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="e1dbd-121">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="e1dbd-122">Tipo di allocazione di memoria eseguita.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-122">The type of memory allocation that was performed.</span></span> <span data-ttu-id="e1dbd-123">Per i valori possibili, vedere il parametro *flAllocationType* della funzione [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) .</span><span class="sxs-lookup"><span data-stu-id="e1dbd-123">For possible values, see the *flAllocationType* parameter of the [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) function.</span></span>

</dd> <dt>

<span data-ttu-id="e1dbd-124">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-124">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1dbd-125">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1dbd-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-127">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="e1dbd-127">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e1dbd-128">Il processo che possiede la memoria (può essere diverso dal thread che ha eseguito l'allocazione).</span><span class="sxs-lookup"><span data-stu-id="e1dbd-128">The process that owned the memory (can be different from the thread that performed the allocation).</span></span>

</dd> <dt>

<span data-ttu-id="e1dbd-129">**RegionSize**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-129">**RegionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1dbd-130">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-130">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1dbd-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-132">Qualificatori: WmiDataId (2), Extension ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="e1dbd-132">Qualifiers: WmiDataId(2), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="e1dbd-133">Dimensione, in byte, della memoria allocata o liberata.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-133">The size, in bytes, of the memory that was allocated or freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1dbd-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1dbd-134">Requirements</span></span>



| <span data-ttu-id="e1dbd-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1dbd-135">Requirement</span></span> | <span data-ttu-id="e1dbd-136">Valore</span><span class="sxs-lookup"><span data-stu-id="e1dbd-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e1dbd-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1dbd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e1dbd-138">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e1dbd-138">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e1dbd-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1dbd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e1dbd-140">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1dbd-140">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1dbd-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1dbd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1dbd-142">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-142">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 
