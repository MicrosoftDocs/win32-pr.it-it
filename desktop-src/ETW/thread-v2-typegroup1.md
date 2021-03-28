---
description: Questa classe è la classe del tipo di evento per gli eventi di inizio e di fine del thread. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Classe Thread_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: c89d573f4eda2580002bedfd0ad17eb9b50c1575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232086"
---
# <a name="thread_v2_typegroup1-class"></a><span data-ttu-id="0ee5f-104">\_Classe thread v2 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="0ee5f-104">Thread\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="0ee5f-105">Questa classe è la classe del tipo di evento per gli eventi di inizio e di fine del thread.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="0ee5f-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee5f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ee5f-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a><span data-ttu-id="0ee5f-108">Members</span><span class="sxs-lookup"><span data-stu-id="0ee5f-108">Members</span></span>

<span data-ttu-id="0ee5f-109">La classe **thread \_ v2 \_ TypeGroup1** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0ee5f-109">The **Thread\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="0ee5f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0ee5f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ee5f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0ee5f-111">Properties</span></span>

<span data-ttu-id="0ee5f-112">La classe **thread \_ v2 \_ TypeGroup1** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-112">The **Thread\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ee5f-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="0ee5f-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee5f-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ee5f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-116">Qualificatori: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="0ee5f-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="0ee5f-117">Identificatore del processo del thread che interessano l'evento.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="0ee5f-118">StackBase</span><span class="sxs-lookup"><span data-stu-id="0ee5f-118">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee5f-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ee5f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-121">Qualificatori: WmiDataId (3), puntatore</span><span class="sxs-lookup"><span data-stu-id="0ee5f-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0ee5f-122">Indirizzo di base dello stack del thread.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-122">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="0ee5f-123">StackLimit</span><span class="sxs-lookup"><span data-stu-id="0ee5f-123">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee5f-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ee5f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-126">Qualificatori: WmiDataId (4), puntatore</span><span class="sxs-lookup"><span data-stu-id="0ee5f-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0ee5f-127">Limite dello stack del thread.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-127">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="0ee5f-128">StartAddr</span><span class="sxs-lookup"><span data-stu-id="0ee5f-128">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee5f-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ee5f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-131">Qualificatori: WmiDataId (7), puntatore</span><span class="sxs-lookup"><span data-stu-id="0ee5f-131">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0ee5f-132">Indirizzo di memoria in cui viene avviata la traccia.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-132">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="0ee5f-133">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="0ee5f-133">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee5f-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ee5f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-136">Qualificatori: WmiDataId (10), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="0ee5f-136">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="0ee5f-137">Identifica il servizio se il thread è di proprietà di un servizio. in caso contrario, zero.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-137">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="0ee5f-138">TebBase</span><span class="sxs-lookup"><span data-stu-id="0ee5f-138">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee5f-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ee5f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-141">Qualificatori: WmiDataId (9), puntatore</span><span class="sxs-lookup"><span data-stu-id="0ee5f-141">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0ee5f-142">Indirizzo di base blocco ambiente thread.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-142">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="0ee5f-143">TThreadId</span><span class="sxs-lookup"><span data-stu-id="0ee5f-143">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee5f-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ee5f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-146">Qualificatori: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="0ee5f-146">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="0ee5f-147">Identificatore del thread associato all'evento.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-147">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="0ee5f-148">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="0ee5f-148">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee5f-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ee5f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-151">Qualificatori: WmiDataId (5), puntatore</span><span class="sxs-lookup"><span data-stu-id="0ee5f-151">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0ee5f-152">Indirizzo di base dello stack in modalità utente del thread.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-152">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="0ee5f-153">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="0ee5f-153">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee5f-154">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ee5f-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-156">Qualificatori: WmiDataId (6), puntatore</span><span class="sxs-lookup"><span data-stu-id="0ee5f-156">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0ee5f-157">Limite dello stack in modalità utente del thread.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-157">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="0ee5f-158">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="0ee5f-158">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee5f-159">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ee5f-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee5f-161">Qualificatori: WmiDataId (8), puntatore</span><span class="sxs-lookup"><span data-stu-id="0ee5f-161">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0ee5f-162">Indirizzo iniziale della funzione che deve essere eseguita da questo thread.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-162">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ee5f-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ee5f-163">Remarks</span></span>

<span data-ttu-id="0ee5f-164">I tipi di evento DCStart e DCEnd enumerano i thread attualmente in esecuzione nel momento in cui la sessione kernel inizia e termina, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-164">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee5f-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ee5f-165">Requirements</span></span>



| <span data-ttu-id="0ee5f-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ee5f-166">Requirement</span></span> | <span data-ttu-id="0ee5f-167">Valore</span><span class="sxs-lookup"><span data-stu-id="0ee5f-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0ee5f-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ee5f-168">Minimum supported client</span></span><br/> | <span data-ttu-id="0ee5f-169">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ee5f-169">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0ee5f-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ee5f-170">Minimum supported server</span></span><br/> | <span data-ttu-id="0ee5f-171">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ee5f-171">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ee5f-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ee5f-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee5f-173">**Thread**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-173">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="0ee5f-174">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-174">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




