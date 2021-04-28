---
description: 'Thread_TypeGroup1 classe: questa classe è la classe del tipo di evento per gli eventi di inizio e fine del thread. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Thread_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_TypeGroup1
- Thread_TypeGroup1.ProcessId
- Thread_TypeGroup1.TThreadId
- Thread_TypeGroup1.StackBase
- Thread_TypeGroup1.StackLimit
- Thread_TypeGroup1.UserStackBase
- Thread_TypeGroup1.UserStackLimit
- Thread_TypeGroup1.Affinity
- Thread_TypeGroup1.Win32StartAddr
- Thread_TypeGroup1.TebBase
- Thread_TypeGroup1.SubProcessTag
- Thread_TypeGroup1.BasePriority
- Thread_TypeGroup1.PagePriority
- Thread_TypeGroup1.IoPriority
- Thread_TypeGroup1.ThreadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9693bef4449cc076710a74dd9cef88ae608754b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105709"
---
# <a name="thread_typegroup1-class"></a><span data-ttu-id="aea19-104">Classe \_ TypeGroup1 del thread</span><span class="sxs-lookup"><span data-stu-id="aea19-104">Thread\_TypeGroup1 class</span></span>

<span data-ttu-id="aea19-105">Questa classe è la classe del tipo di evento per gli eventi di inizio e fine del thread.</span><span class="sxs-lookup"><span data-stu-id="aea19-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="aea19-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="aea19-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea19-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aea19-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_TypeGroup1 : Thread
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 Affinity;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
  uint8  BasePriority;
  uint8  PagePriority;
  uint8  IoPriority;
  uint8  ThreadFlags;
};
```

## <a name="members"></a><span data-ttu-id="aea19-108">Members</span><span class="sxs-lookup"><span data-stu-id="aea19-108">Members</span></span>

<span data-ttu-id="aea19-109">La **classe \_ Thread TypeGroup1** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="aea19-109">The **Thread\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="aea19-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aea19-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aea19-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aea19-111">Properties</span></span>

<span data-ttu-id="aea19-112">La **classe \_ Thread TypeGroup1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="aea19-112">The **Thread\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aea19-113">Affinità</span><span class="sxs-lookup"><span data-stu-id="aea19-113">Affinity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-114">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="aea19-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-116">Qualificatori: WmiDataId(7), Pointer</span><span class="sxs-lookup"><span data-stu-id="aea19-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aea19-117">Set di processori in cui è consentita l'esecuzione del thread.</span><span class="sxs-lookup"><span data-stu-id="aea19-117">The set of processors on which the thread is allowed to run.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-118">BasePriority</span><span class="sxs-lookup"><span data-stu-id="aea19-118">BasePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-119">Tipo di dati: **uint8**</span><span class="sxs-lookup"><span data-stu-id="aea19-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-121">Qualificatori: WmiDataId(11)</span><span class="sxs-lookup"><span data-stu-id="aea19-121">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="aea19-122">Priorità dell'utilità di pianificazione del thread (vedere la [**funzione SetThreadPriority).**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)</span><span class="sxs-lookup"><span data-stu-id="aea19-122">The scheduler priority of the thread (see the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function).</span></span>

</dd> <dt>

<span data-ttu-id="aea19-123">IoPriority</span><span class="sxs-lookup"><span data-stu-id="aea19-123">IoPriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-124">Tipo di dati: **uint8**</span><span class="sxs-lookup"><span data-stu-id="aea19-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-126">Qualificatori: WmiDataId(13)</span><span class="sxs-lookup"><span data-stu-id="aea19-126">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="aea19-127">Hint di priorità di I/O per la pianificazione degli I/O generati dal thread.</span><span class="sxs-lookup"><span data-stu-id="aea19-127">An IO priority hint for scheduling IOs generated by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-128">PagePriority</span><span class="sxs-lookup"><span data-stu-id="aea19-128">PagePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-129">Tipo di dati: **uint8**</span><span class="sxs-lookup"><span data-stu-id="aea19-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-131">Qualificatori: WmiDataId(12)</span><span class="sxs-lookup"><span data-stu-id="aea19-131">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="aea19-132">Hint di priorità della pagina di memoria per le pagine di memoria a cui accede il thread.</span><span class="sxs-lookup"><span data-stu-id="aea19-132">A memory page priority hint for memory pages accessed by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-133">ProcessId</span><span class="sxs-lookup"><span data-stu-id="aea19-133">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-134">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="aea19-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-136">Qualificatori: WmiDataId(1), Format("x")</span><span class="sxs-lookup"><span data-stu-id="aea19-136">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="aea19-137">Identificatore del processo del thread coinvolto nell'evento.</span><span class="sxs-lookup"><span data-stu-id="aea19-137">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-138">StackBase</span><span class="sxs-lookup"><span data-stu-id="aea19-138">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-139">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="aea19-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-141">Qualificatori: WmiDataId(3), Pointer</span><span class="sxs-lookup"><span data-stu-id="aea19-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aea19-142">Indirizzo di base dello stack del thread.</span><span class="sxs-lookup"><span data-stu-id="aea19-142">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-143">StackLimit</span><span class="sxs-lookup"><span data-stu-id="aea19-143">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-144">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="aea19-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-146">Qualificatori: WmiDataId(4), Pointer</span><span class="sxs-lookup"><span data-stu-id="aea19-146">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aea19-147">Limite dello stack del thread.</span><span class="sxs-lookup"><span data-stu-id="aea19-147">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-148">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="aea19-148">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-149">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="aea19-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-151">Qualificatori: WmiDataId(10), Format("x")</span><span class="sxs-lookup"><span data-stu-id="aea19-151">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="aea19-152">Identifica il servizio se il thread è di proprietà di un servizio; in caso contrario, zero.</span><span class="sxs-lookup"><span data-stu-id="aea19-152">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-153">TebBase</span><span class="sxs-lookup"><span data-stu-id="aea19-153">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-154">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="aea19-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-156">Qualificatori: WmiDataId(9), Puntatore</span><span class="sxs-lookup"><span data-stu-id="aea19-156">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aea19-157">Indirizzo di base del blocco dell'ambiente thread.</span><span class="sxs-lookup"><span data-stu-id="aea19-157">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-158">ThreadFlags</span><span class="sxs-lookup"><span data-stu-id="aea19-158">ThreadFlags</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-159">Tipo di dati: **uint8**</span><span class="sxs-lookup"><span data-stu-id="aea19-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-161">Qualificatori: WmiDataId(14)</span><span class="sxs-lookup"><span data-stu-id="aea19-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="aea19-162">Non usato.</span><span class="sxs-lookup"><span data-stu-id="aea19-162">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-163">TThreadId</span><span class="sxs-lookup"><span data-stu-id="aea19-163">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-164">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="aea19-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-166">Qualificatori: WmiDataId(2), Format("x")</span><span class="sxs-lookup"><span data-stu-id="aea19-166">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="aea19-167">Identificatore di thread del thread coinvolto nell'evento.</span><span class="sxs-lookup"><span data-stu-id="aea19-167">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-168">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="aea19-168">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-169">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="aea19-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-171">Qualificatori: WmiDataId(5), Puntatore</span><span class="sxs-lookup"><span data-stu-id="aea19-171">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aea19-172">Indirizzo di base dello stack in modalità utente del thread.</span><span class="sxs-lookup"><span data-stu-id="aea19-172">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-173">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="aea19-173">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-174">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="aea19-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-176">Qualificatori: WmiDataId(6), Puntatore</span><span class="sxs-lookup"><span data-stu-id="aea19-176">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aea19-177">Limite dello stack in modalità utente del thread.</span><span class="sxs-lookup"><span data-stu-id="aea19-177">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="aea19-178">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="aea19-178">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea19-179">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="aea19-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea19-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aea19-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea19-181">Qualificatori: WmiDataId(8), Puntatore</span><span class="sxs-lookup"><span data-stu-id="aea19-181">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aea19-182">Indirizzo iniziale della funzione che deve essere eseguita da questo thread.</span><span class="sxs-lookup"><span data-stu-id="aea19-182">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aea19-183">Commenti</span><span class="sxs-lookup"><span data-stu-id="aea19-183">Remarks</span></span>

<span data-ttu-id="aea19-184">I tipi di evento DCStart e DCEnd enumerano rispettivamente i thread attualmente in esecuzione al momento dell'avvio e della fine della sessione del kernel.</span><span class="sxs-lookup"><span data-stu-id="aea19-184">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="aea19-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aea19-185">Requirements</span></span>



| <span data-ttu-id="aea19-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="aea19-186">Requirement</span></span> | <span data-ttu-id="aea19-187">Valore</span><span class="sxs-lookup"><span data-stu-id="aea19-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aea19-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aea19-188">Minimum supported client</span></span><br/> | <span data-ttu-id="aea19-189">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aea19-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aea19-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aea19-190">Minimum supported server</span></span><br/> | <span data-ttu-id="aea19-191">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="aea19-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aea19-192">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aea19-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea19-193">**Thread**</span><span class="sxs-lookup"><span data-stu-id="aea19-193">**Thread**</span></span>](thread.md)
</dt> </dl>

 

 
