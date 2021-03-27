---
description: Questa classe è la classe del tipo di evento per gli eventi di cambio di contesto. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: Classe CSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 91004ca276140271e8d73c3fc226e83c4e03d1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226361"
---
# <a name="cswitch-class"></a><span data-ttu-id="41e70-104">Classe CSwitch</span><span class="sxs-lookup"><span data-stu-id="41e70-104">CSwitch class</span></span>

<span data-ttu-id="41e70-105">Questa classe è la classe del tipo di evento per gli eventi di cambio di contesto.</span><span class="sxs-lookup"><span data-stu-id="41e70-105">This class is the event type class for context switch events.</span></span>

<span data-ttu-id="41e70-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="41e70-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e70-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41e70-107">Syntax</span></span>

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="41e70-108">Members</span><span class="sxs-lookup"><span data-stu-id="41e70-108">Members</span></span>

<span data-ttu-id="41e70-109">La classe **Cswitch** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="41e70-109">The **CSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="41e70-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="41e70-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41e70-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="41e70-111">Properties</span></span>

<span data-ttu-id="41e70-112">La classe **Cswitch** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="41e70-112">The **CSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41e70-113">**NewThreadId**</span><span class="sxs-lookup"><span data-stu-id="41e70-113">**NewThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41e70-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-116">Qualificatori: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="41e70-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="41e70-117">Nuovo ID thread dopo l'opzione.</span><span class="sxs-lookup"><span data-stu-id="41e70-117">New thread ID after the switch.</span></span>

</dd> <dt>

<span data-ttu-id="41e70-118">**NewThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="41e70-118">**NewThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-119">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="41e70-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-121">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="41e70-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="41e70-122">Priorità thread del nuovo thread.</span><span class="sxs-lookup"><span data-stu-id="41e70-122">Thread priority of the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="41e70-123">**NewThreadWaitTime**</span><span class="sxs-lookup"><span data-stu-id="41e70-123">**NewThreadWaitTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41e70-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-126">Qualificatori: WmiDataId (11), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="41e70-126">Qualifiers: WmiDataId(11), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="41e70-127">Tempo di attesa per il nuovo thread.</span><span class="sxs-lookup"><span data-stu-id="41e70-127">Wait time for the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="41e70-128">**OldThreadId**</span><span class="sxs-lookup"><span data-stu-id="41e70-128">**OldThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41e70-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-131">Qualificatori: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="41e70-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="41e70-132">ID thread precedente.</span><span class="sxs-lookup"><span data-stu-id="41e70-132">Previous thread ID.</span></span>

</dd> <dt>

<span data-ttu-id="41e70-133">**OldThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="41e70-133">**OldThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-134">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="41e70-134">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-136">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="41e70-136">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="41e70-137">Priorità del thread precedente.</span><span class="sxs-lookup"><span data-stu-id="41e70-137">Thread priority of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="41e70-138">**OldThreadState**</span><span class="sxs-lookup"><span data-stu-id="41e70-138">**OldThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-139">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="41e70-139">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-141">Qualificatori: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="41e70-141">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="41e70-142">Stato del thread precedente.</span><span class="sxs-lookup"><span data-stu-id="41e70-142">State of the previous thread.</span></span> <span data-ttu-id="41e70-143">Di seguito sono riportati i valori di stato possibili:</span><span class="sxs-lookup"><span data-stu-id="41e70-143">The following are the possible state values:</span></span>

| <span data-ttu-id="41e70-144">State</span><span class="sxs-lookup"><span data-stu-id="41e70-144">State</span></span> | <span data-ttu-id="41e70-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41e70-145">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="41e70-146">0</span><span class="sxs-lookup"><span data-stu-id="41e70-146">0</span></span>     | <span data-ttu-id="41e70-147">Inizializzato</span><span class="sxs-lookup"><span data-stu-id="41e70-147">Initialized</span></span>                                   |
| <span data-ttu-id="41e70-148">1</span><span class="sxs-lookup"><span data-stu-id="41e70-148">1</span></span>     | <span data-ttu-id="41e70-149">Ready</span><span class="sxs-lookup"><span data-stu-id="41e70-149">Ready</span></span>                                         |
| <span data-ttu-id="41e70-150">2</span><span class="sxs-lookup"><span data-stu-id="41e70-150">2</span></span>     | <span data-ttu-id="41e70-151">In esecuzione</span><span class="sxs-lookup"><span data-stu-id="41e70-151">Running</span></span>                                       |
| <span data-ttu-id="41e70-152">3</span><span class="sxs-lookup"><span data-stu-id="41e70-152">3</span></span>     | <span data-ttu-id="41e70-153">Standby</span><span class="sxs-lookup"><span data-stu-id="41e70-153">Standby</span></span>                                       |
| <span data-ttu-id="41e70-154">4</span><span class="sxs-lookup"><span data-stu-id="41e70-154">4</span></span>     | <span data-ttu-id="41e70-155">Terminato</span><span class="sxs-lookup"><span data-stu-id="41e70-155">Terminated</span></span>                                    |
| <span data-ttu-id="41e70-156">5</span><span class="sxs-lookup"><span data-stu-id="41e70-156">5</span></span>     | <span data-ttu-id="41e70-157">Attesa</span><span class="sxs-lookup"><span data-stu-id="41e70-157">Waiting</span></span>                                       |
| <span data-ttu-id="41e70-158">6</span><span class="sxs-lookup"><span data-stu-id="41e70-158">6</span></span>     | <span data-ttu-id="41e70-159">Transizione</span><span class="sxs-lookup"><span data-stu-id="41e70-159">Transition</span></span>                                    |
| <span data-ttu-id="41e70-160">7</span><span class="sxs-lookup"><span data-stu-id="41e70-160">7</span></span>     | <span data-ttu-id="41e70-161">DeferredReady (aggiunto per Windows Server 2003)</span><span class="sxs-lookup"><span data-stu-id="41e70-161">DeferredReady (added for Windows Server 2003)</span></span> |



 

</dd> <dt>

<span data-ttu-id="41e70-162">**OldThreadWaitIdealProcessor**</span><span class="sxs-lookup"><span data-stu-id="41e70-162">**OldThreadWaitIdealProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-163">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="41e70-163">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-165">Qualificatori: WmiDataId (10), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="41e70-165">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="41e70-166">Tempo di attesa ideale del thread precedente.</span><span class="sxs-lookup"><span data-stu-id="41e70-166">Ideal wait time of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="41e70-167">**OldThreadWaitMode**</span><span class="sxs-lookup"><span data-stu-id="41e70-167">**OldThreadWaitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-168">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="41e70-168">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-170">Qualificatori: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="41e70-170">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="41e70-171">Modalità di attesa per il thread precedente.</span><span class="sxs-lookup"><span data-stu-id="41e70-171">Wait mode for the previous thread.</span></span> <span data-ttu-id="41e70-172">Di seguito sono indicati i valori possibili:</span><span class="sxs-lookup"><span data-stu-id="41e70-172">The following are the possible values:</span></span>

| <span data-ttu-id="41e70-173">State</span><span class="sxs-lookup"><span data-stu-id="41e70-173">State</span></span> | <span data-ttu-id="41e70-174">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41e70-174">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="41e70-175">0</span><span class="sxs-lookup"><span data-stu-id="41e70-175">0</span></span>     | <span data-ttu-id="41e70-176">KernelMode</span><span class="sxs-lookup"><span data-stu-id="41e70-176">KernelMode</span></span>  |
| <span data-ttu-id="41e70-177">1</span><span class="sxs-lookup"><span data-stu-id="41e70-177">1</span></span>     | <span data-ttu-id="41e70-178">UserMode</span><span class="sxs-lookup"><span data-stu-id="41e70-178">UserMode</span></span>    |



 

</dd> <dt>

<span data-ttu-id="41e70-179">**OldThreadWaitReason**</span><span class="sxs-lookup"><span data-stu-id="41e70-179">**OldThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-180">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="41e70-180">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-182">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="41e70-182">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="41e70-183">Motivo dell'attesa per il thread precedente.</span><span class="sxs-lookup"><span data-stu-id="41e70-183">Wait reason for the previous thread.</span></span> <span data-ttu-id="41e70-184">Di seguito sono indicati i valori possibili:</span><span class="sxs-lookup"><span data-stu-id="41e70-184">The following are the possible values:</span></span>

| <span data-ttu-id="41e70-185">State</span><span class="sxs-lookup"><span data-stu-id="41e70-185">State</span></span> | <span data-ttu-id="41e70-186">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41e70-186">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="41e70-187">0</span><span class="sxs-lookup"><span data-stu-id="41e70-187">0</span></span>     | <span data-ttu-id="41e70-188">Executive</span><span class="sxs-lookup"><span data-stu-id="41e70-188">Executive</span></span>         |
| <span data-ttu-id="41e70-189">1</span><span class="sxs-lookup"><span data-stu-id="41e70-189">1</span></span>     | <span data-ttu-id="41e70-190">FreePage</span><span class="sxs-lookup"><span data-stu-id="41e70-190">FreePage</span></span>          |
| <span data-ttu-id="41e70-191">2</span><span class="sxs-lookup"><span data-stu-id="41e70-191">2</span></span>     | <span data-ttu-id="41e70-192">Inizio PageIn</span><span class="sxs-lookup"><span data-stu-id="41e70-192">PageIn</span></span>            |
| <span data-ttu-id="41e70-193">3</span><span class="sxs-lookup"><span data-stu-id="41e70-193">3</span></span>     | <span data-ttu-id="41e70-194">PoolAllocation</span><span class="sxs-lookup"><span data-stu-id="41e70-194">PoolAllocation</span></span>    |
| <span data-ttu-id="41e70-195">4</span><span class="sxs-lookup"><span data-stu-id="41e70-195">4</span></span>     | <span data-ttu-id="41e70-196">DelayExecution</span><span class="sxs-lookup"><span data-stu-id="41e70-196">DelayExecution</span></span>    |
| <span data-ttu-id="41e70-197">5</span><span class="sxs-lookup"><span data-stu-id="41e70-197">5</span></span>     | <span data-ttu-id="41e70-198">Suspended</span><span class="sxs-lookup"><span data-stu-id="41e70-198">Suspended</span></span>         |
| <span data-ttu-id="41e70-199">6</span><span class="sxs-lookup"><span data-stu-id="41e70-199">6</span></span>     | <span data-ttu-id="41e70-200">UserRequest</span><span class="sxs-lookup"><span data-stu-id="41e70-200">UserRequest</span></span>       |
| <span data-ttu-id="41e70-201">7</span><span class="sxs-lookup"><span data-stu-id="41e70-201">7</span></span>     | <span data-ttu-id="41e70-202">WrExecutive</span><span class="sxs-lookup"><span data-stu-id="41e70-202">WrExecutive</span></span>       |
| <span data-ttu-id="41e70-203">8</span><span class="sxs-lookup"><span data-stu-id="41e70-203">8</span></span>     | <span data-ttu-id="41e70-204">WrFreePage</span><span class="sxs-lookup"><span data-stu-id="41e70-204">WrFreePage</span></span>        |
| <span data-ttu-id="41e70-205">9</span><span class="sxs-lookup"><span data-stu-id="41e70-205">9</span></span>     | <span data-ttu-id="41e70-206">WrPageIn</span><span class="sxs-lookup"><span data-stu-id="41e70-206">WrPageIn</span></span>          |
| <span data-ttu-id="41e70-207">10</span><span class="sxs-lookup"><span data-stu-id="41e70-207">10</span></span>    | <span data-ttu-id="41e70-208">WrPoolAllocation</span><span class="sxs-lookup"><span data-stu-id="41e70-208">WrPoolAllocation</span></span>  |
| <span data-ttu-id="41e70-209">11</span><span class="sxs-lookup"><span data-stu-id="41e70-209">11</span></span>    | <span data-ttu-id="41e70-210">WrDelayExecution</span><span class="sxs-lookup"><span data-stu-id="41e70-210">WrDelayExecution</span></span>  |
| <span data-ttu-id="41e70-211">12</span><span class="sxs-lookup"><span data-stu-id="41e70-211">12</span></span>    | <span data-ttu-id="41e70-212">WrSuspended</span><span class="sxs-lookup"><span data-stu-id="41e70-212">WrSuspended</span></span>       |
| <span data-ttu-id="41e70-213">13</span><span class="sxs-lookup"><span data-stu-id="41e70-213">13</span></span>    | <span data-ttu-id="41e70-214">WrUserRequest</span><span class="sxs-lookup"><span data-stu-id="41e70-214">WrUserRequest</span></span>     |
| <span data-ttu-id="41e70-215">14</span><span class="sxs-lookup"><span data-stu-id="41e70-215">14</span></span>    | <span data-ttu-id="41e70-216">WrEventPair</span><span class="sxs-lookup"><span data-stu-id="41e70-216">WrEventPair</span></span>       |
| <span data-ttu-id="41e70-217">15</span><span class="sxs-lookup"><span data-stu-id="41e70-217">15</span></span>    | <span data-ttu-id="41e70-218">WrQueue</span><span class="sxs-lookup"><span data-stu-id="41e70-218">WrQueue</span></span>           |
| <span data-ttu-id="41e70-219">16</span><span class="sxs-lookup"><span data-stu-id="41e70-219">16</span></span>    | <span data-ttu-id="41e70-220">WrLpcReceive</span><span class="sxs-lookup"><span data-stu-id="41e70-220">WrLpcReceive</span></span>      |
| <span data-ttu-id="41e70-221">17</span><span class="sxs-lookup"><span data-stu-id="41e70-221">17</span></span>    | <span data-ttu-id="41e70-222">WrLpcReply</span><span class="sxs-lookup"><span data-stu-id="41e70-222">WrLpcReply</span></span>        |
| <span data-ttu-id="41e70-223">18</span><span class="sxs-lookup"><span data-stu-id="41e70-223">18</span></span>    | <span data-ttu-id="41e70-224">WrVirtualMemory</span><span class="sxs-lookup"><span data-stu-id="41e70-224">WrVirtualMemory</span></span>   |
| <span data-ttu-id="41e70-225">19</span><span class="sxs-lookup"><span data-stu-id="41e70-225">19</span></span>    | <span data-ttu-id="41e70-226">WrPageOut</span><span class="sxs-lookup"><span data-stu-id="41e70-226">WrPageOut</span></span>         |
| <span data-ttu-id="41e70-227">20</span><span class="sxs-lookup"><span data-stu-id="41e70-227">20</span></span>    | <span data-ttu-id="41e70-228">WrRendezvous</span><span class="sxs-lookup"><span data-stu-id="41e70-228">WrRendezvous</span></span>      |
| <span data-ttu-id="41e70-229">21</span><span class="sxs-lookup"><span data-stu-id="41e70-229">21</span></span>    | <span data-ttu-id="41e70-230">WrKeyedEvent</span><span class="sxs-lookup"><span data-stu-id="41e70-230">WrKeyedEvent</span></span>      |
| <span data-ttu-id="41e70-231">22</span><span class="sxs-lookup"><span data-stu-id="41e70-231">22</span></span>    | <span data-ttu-id="41e70-232">WrTerminated</span><span class="sxs-lookup"><span data-stu-id="41e70-232">WrTerminated</span></span>      |
| <span data-ttu-id="41e70-233">23</span><span class="sxs-lookup"><span data-stu-id="41e70-233">23</span></span>    | <span data-ttu-id="41e70-234">WrProcessInSwap</span><span class="sxs-lookup"><span data-stu-id="41e70-234">WrProcessInSwap</span></span>   |
| <span data-ttu-id="41e70-235">24</span><span class="sxs-lookup"><span data-stu-id="41e70-235">24</span></span>    | <span data-ttu-id="41e70-236">WrCpuRateControl</span><span class="sxs-lookup"><span data-stu-id="41e70-236">WrCpuRateControl</span></span>  |
| <span data-ttu-id="41e70-237">25</span><span class="sxs-lookup"><span data-stu-id="41e70-237">25</span></span>    | <span data-ttu-id="41e70-238">WrCalloutStack</span><span class="sxs-lookup"><span data-stu-id="41e70-238">WrCalloutStack</span></span>    |
| <span data-ttu-id="41e70-239">26</span><span class="sxs-lookup"><span data-stu-id="41e70-239">26</span></span>    | <span data-ttu-id="41e70-240">WrKernel</span><span class="sxs-lookup"><span data-stu-id="41e70-240">WrKernel</span></span>          |
| <span data-ttu-id="41e70-241">27</span><span class="sxs-lookup"><span data-stu-id="41e70-241">27</span></span>    | <span data-ttu-id="41e70-242">WrResource</span><span class="sxs-lookup"><span data-stu-id="41e70-242">WrResource</span></span>        |
| <span data-ttu-id="41e70-243">28</span><span class="sxs-lookup"><span data-stu-id="41e70-243">28</span></span>    | <span data-ttu-id="41e70-244">WrPushLock</span><span class="sxs-lookup"><span data-stu-id="41e70-244">WrPushLock</span></span>        |
| <span data-ttu-id="41e70-245">29</span><span class="sxs-lookup"><span data-stu-id="41e70-245">29</span></span>    | <span data-ttu-id="41e70-246">WrMutex</span><span class="sxs-lookup"><span data-stu-id="41e70-246">WrMutex</span></span>           |
| <span data-ttu-id="41e70-247">30</span><span class="sxs-lookup"><span data-stu-id="41e70-247">30</span></span>    | <span data-ttu-id="41e70-248">WrQuantumEnd</span><span class="sxs-lookup"><span data-stu-id="41e70-248">WrQuantumEnd</span></span>      |
| <span data-ttu-id="41e70-249">31</span><span class="sxs-lookup"><span data-stu-id="41e70-249">31</span></span>    | <span data-ttu-id="41e70-250">WrDispatchInt</span><span class="sxs-lookup"><span data-stu-id="41e70-250">WrDispatchInt</span></span>     |
| <span data-ttu-id="41e70-251">32</span><span class="sxs-lookup"><span data-stu-id="41e70-251">32</span></span>    | <span data-ttu-id="41e70-252">WrPreempted</span><span class="sxs-lookup"><span data-stu-id="41e70-252">WrPreempted</span></span>       |
| <span data-ttu-id="41e70-253">33</span><span class="sxs-lookup"><span data-stu-id="41e70-253">33</span></span>    | <span data-ttu-id="41e70-254">WrYieldExecution</span><span class="sxs-lookup"><span data-stu-id="41e70-254">WrYieldExecution</span></span>  |
| <span data-ttu-id="41e70-255">34</span><span class="sxs-lookup"><span data-stu-id="41e70-255">34</span></span>    | <span data-ttu-id="41e70-256">WrFastMutex</span><span class="sxs-lookup"><span data-stu-id="41e70-256">WrFastMutex</span></span>       |
| <span data-ttu-id="41e70-257">35</span><span class="sxs-lookup"><span data-stu-id="41e70-257">35</span></span>    | <span data-ttu-id="41e70-258">WrGuardedMutex</span><span class="sxs-lookup"><span data-stu-id="41e70-258">WrGuardedMutex</span></span>    |
| <span data-ttu-id="41e70-259">36</span><span class="sxs-lookup"><span data-stu-id="41e70-259">36</span></span>    | <span data-ttu-id="41e70-260">WrRundown</span><span class="sxs-lookup"><span data-stu-id="41e70-260">WrRundown</span></span>         |
| <span data-ttu-id="41e70-261">37</span><span class="sxs-lookup"><span data-stu-id="41e70-261">37</span></span>    | <span data-ttu-id="41e70-262">MaximumWaitReason</span><span class="sxs-lookup"><span data-stu-id="41e70-262">MaximumWaitReason</span></span> |



 

</dd> <dt>

<span data-ttu-id="41e70-263">**PreviousCState**</span><span class="sxs-lookup"><span data-stu-id="41e70-263">**PreviousCState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-264">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="41e70-264">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-266">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="41e70-266">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="41e70-267">Indice dello stato C utilizzato per ultimo dal processore.</span><span class="sxs-lookup"><span data-stu-id="41e70-267">The index of the C-state that was last used by the processor.</span></span> <span data-ttu-id="41e70-268">Un valore pari a 0 rappresenta lo stato di inattività più chiaro con valori più alti che rappresentano stati C più profondi.</span><span class="sxs-lookup"><span data-stu-id="41e70-268">A value of 0 represents the lightest idle state with higher values representing deeper C-states.</span></span>

</dd> <dt>

<span data-ttu-id="41e70-269">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="41e70-269">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-270">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41e70-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-272">Qualificatori: WmiDataId (12)</span><span class="sxs-lookup"><span data-stu-id="41e70-272">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="41e70-273">Riservato.</span><span class="sxs-lookup"><span data-stu-id="41e70-273">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="41e70-274">**SpareByte**</span><span class="sxs-lookup"><span data-stu-id="41e70-274">**SpareByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41e70-275">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="41e70-275">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="41e70-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41e70-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41e70-277">Qualificatori: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="41e70-277">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="41e70-278">Non usato.</span><span class="sxs-lookup"><span data-stu-id="41e70-278">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41e70-279">Commenti</span><span class="sxs-lookup"><span data-stu-id="41e70-279">Remarks</span></span>

<span data-ttu-id="41e70-280">Questi eventi producono un volume elevato di eventi.</span><span class="sxs-lookup"><span data-stu-id="41e70-280">These events produce a high volume of events.</span></span>

## <a name="requirements"></a><span data-ttu-id="41e70-281">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41e70-281">Requirements</span></span>



| <span data-ttu-id="41e70-282">Requisito</span><span class="sxs-lookup"><span data-stu-id="41e70-282">Requirement</span></span> | <span data-ttu-id="41e70-283">Valore</span><span class="sxs-lookup"><span data-stu-id="41e70-283">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="41e70-284">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41e70-284">Minimum supported client</span></span><br/> | <span data-ttu-id="41e70-285">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41e70-285">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="41e70-286">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41e70-286">Minimum supported server</span></span><br/> | <span data-ttu-id="41e70-287">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41e70-287">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41e70-288">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41e70-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e70-289">**Thread**</span><span class="sxs-lookup"><span data-stu-id="41e70-289">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="41e70-290">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="41e70-290">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




