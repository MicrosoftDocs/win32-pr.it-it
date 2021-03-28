---
description: Questa classe è la classe del tipo di evento per gli eventi di traccia dello stack.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: Classe StackWalk_Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980082"
---
# <a name="stackwalk_event-class"></a><span data-ttu-id="6f107-103">\_Classe di evento StackWalk</span><span class="sxs-lookup"><span data-stu-id="6f107-103">StackWalk\_Event class</span></span>

<span data-ttu-id="6f107-104">Questa classe è la classe del tipo di evento per gli eventi di traccia dello stack.</span><span class="sxs-lookup"><span data-stu-id="6f107-104">This class is the event type class for stack tracing events.</span></span>

<span data-ttu-id="6f107-105">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6f107-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f107-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f107-106">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a><span data-ttu-id="6f107-107">Members</span><span class="sxs-lookup"><span data-stu-id="6f107-107">Members</span></span>

<span data-ttu-id="6f107-108">La classe di **\_ evento StackWalk** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6f107-108">The **StackWalk\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="6f107-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f107-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f107-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f107-110">Properties</span></span>

<span data-ttu-id="6f107-111">La classe di **\_ evento StackWalk** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6f107-111">The **StackWalk\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f107-112">**EventTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="6f107-112">**EventTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f107-113">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f107-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f107-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f107-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f107-115">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="6f107-115">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="6f107-116">Timestamp dell'evento originale dall'intestazione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="6f107-116">Original event time stamp from the event header.</span></span> <span data-ttu-id="6f107-117">Utilizzare questo timestamp per associare lo stack a un evento.</span><span class="sxs-lookup"><span data-stu-id="6f107-117">Use this time stamp to match the stack to an event.</span></span>

</dd> <dt>

<span data-ttu-id="6f107-118">**Stack1**</span><span class="sxs-lookup"><span data-stu-id="6f107-118">**Stack1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f107-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f107-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f107-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f107-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f107-121">Qualificatori: WmiDataId (4), puntatore</span><span class="sxs-lookup"><span data-stu-id="6f107-121">Qualifiers: WmiDataId(4), pointer</span></span>
</dt> </dl>

<span data-ttu-id="6f107-122">Indirizzo della chiamata.</span><span class="sxs-lookup"><span data-stu-id="6f107-122">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="6f107-123">**Stack192**</span><span class="sxs-lookup"><span data-stu-id="6f107-123">**Stack192**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f107-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f107-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f107-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f107-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f107-126">Qualificatori: WmiDataId (195), puntatore</span><span class="sxs-lookup"><span data-stu-id="6f107-126">Qualifiers: WmiDataId(195), pointer</span></span>
</dt> </dl>

<span data-ttu-id="6f107-127">Indirizzo della chiamata.</span><span class="sxs-lookup"><span data-stu-id="6f107-127">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="6f107-128">**StackProcess**</span><span class="sxs-lookup"><span data-stu-id="6f107-128">**StackProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f107-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f107-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f107-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f107-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f107-131">Qualificatori: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="6f107-131">Qualifiers: WmiDataId(2), format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6f107-132">Identificatore del processo dell'evento originale.</span><span class="sxs-lookup"><span data-stu-id="6f107-132">The process identifier of the original event.</span></span>

</dd> <dt>

<span data-ttu-id="6f107-133">**StackThread**</span><span class="sxs-lookup"><span data-stu-id="6f107-133">**StackThread**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f107-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f107-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f107-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f107-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f107-136">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="6f107-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="6f107-137">Identificatore del thread dell'evento originale.</span><span class="sxs-lookup"><span data-stu-id="6f107-137">The thread identifier of the original event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f107-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f107-138">Remarks</span></span>

<span data-ttu-id="6f107-139">Si noti che la classe non Mostra tutte le proprietà **stack \* n**\* presenti tra **Stack1** e **Stack192**.</span><span class="sxs-lookup"><span data-stu-id="6f107-139">Note that the class does not show all of the **Stack\*n**\* properties that exist between **Stack1** and **Stack192**.</span></span> <span data-ttu-id="6f107-140">Usare le dimensioni dell'evento per determinare il numero di proprietà \*\*\* n \* dello stack\*\* che contengono indirizzi validi.</span><span class="sxs-lookup"><span data-stu-id="6f107-140">Use the size of the event to determine how many **Stack\*n**\* properties contain valid addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f107-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f107-141">Requirements</span></span>



| <span data-ttu-id="6f107-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f107-142">Requirement</span></span> | <span data-ttu-id="6f107-143">Valore</span><span class="sxs-lookup"><span data-stu-id="6f107-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6f107-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f107-144">Minimum supported client</span></span><br/> | <span data-ttu-id="6f107-145">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6f107-145">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6f107-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f107-146">Minimum supported server</span></span><br/> | <span data-ttu-id="6f107-147">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f107-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




