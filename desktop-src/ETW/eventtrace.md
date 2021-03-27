---
description: Classe astratta dalla quale vengono derivate tutte le classi di traccia degli eventi.
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: Classe EventTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752407"
---
# <a name="eventtrace-class"></a><span data-ttu-id="3fad8-103">Classe EventTrace</span><span class="sxs-lookup"><span data-stu-id="3fad8-103">EventTrace class</span></span>

<span data-ttu-id="3fad8-104">Classe astratta dalla quale vengono derivate tutte le classi di traccia degli eventi.</span><span class="sxs-lookup"><span data-stu-id="3fad8-104">An abstract class from which all event trace classes are derived.</span></span>

<span data-ttu-id="3fad8-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="3fad8-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fad8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fad8-106">Syntax</span></span>

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a><span data-ttu-id="3fad8-107">Members</span><span class="sxs-lookup"><span data-stu-id="3fad8-107">Members</span></span>

<span data-ttu-id="3fad8-108">La classe **EventTrace** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3fad8-108">The **EventTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="3fad8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fad8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3fad8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fad8-110">Properties</span></span>

<span data-ttu-id="3fad8-111">La classe **EventTrace** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3fad8-111">The **EventTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3fad8-112">**EventGuid**</span><span class="sxs-lookup"><span data-stu-id="3fad8-112">**EventGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-113">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3fad8-113">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-115">Qualificatori: **WmiDataId** (8), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="3fad8-115">Qualifiers: **WmiDataId** (8), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-116">GUID della classe di traccia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3fad8-116">Event trace class GUID of this event.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-117">**EventSize**</span><span class="sxs-lookup"><span data-stu-id="3fad8-117">**EventSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-118">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3fad8-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-120">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="3fad8-120">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-121">Numero totale di byte dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3fad8-121">Total number of bytes of the event.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-122">**EventType**</span><span class="sxs-lookup"><span data-stu-id="3fad8-122">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-123">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3fad8-123">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-125">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="3fad8-125">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-126">Tipo di evento definito dal provider.</span><span class="sxs-lookup"><span data-stu-id="3fad8-126">Provider-defined event type.</span></span> <span data-ttu-id="3fad8-127">Indica la classe del tipo di evento da usare per decifrare i dati degli eventi definiti dal provider (i dati a cui punta **MofData**.</span><span class="sxs-lookup"><span data-stu-id="3fad8-127">Tells you which event type class to use to decipher the provider-defined event data (the data pointed to by **MofData**.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-128">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="3fad8-128">**InstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3fad8-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-131">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="3fad8-131">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-132">Identificatore dell'istanza dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3fad8-132">Identifier of this event instance.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-133">**KernelTime**</span><span class="sxs-lookup"><span data-stu-id="3fad8-133">**KernelTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3fad8-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-136">Qualificatori: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="3fad8-136">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-137">Tempo di esecuzione trascorso per le istruzioni in modalità kernel, in cicli della CPU.</span><span class="sxs-lookup"><span data-stu-id="3fad8-137">Elapsed execution time for kernel-mode instructions, in CPU ticks.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-138">**MofData**</span><span class="sxs-lookup"><span data-stu-id="3fad8-138">**MofData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3fad8-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-141">Qualificatori: **WmiDataId** (14), **puntatore**</span><span class="sxs-lookup"><span data-stu-id="3fad8-141">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-142">Puntatore ai dati evento specifici del provider.</span><span class="sxs-lookup"><span data-stu-id="3fad8-142">Pointer to the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-143">**MofLength**</span><span class="sxs-lookup"><span data-stu-id="3fad8-143">**MofLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3fad8-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-146">Qualificatori: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="3fad8-146">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-147">Lunghezza dei dati dell'evento specifici del provider.</span><span class="sxs-lookup"><span data-stu-id="3fad8-147">Length of the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-148">**ParentGuid**</span><span class="sxs-lookup"><span data-stu-id="3fad8-148">**ParentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-149">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3fad8-149">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-151">Qualificatori: **WmiDataId** (12), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="3fad8-151">Qualifiers: **WmiDataId** (12), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-152">GUID della classe di traccia dell'evento dell'istanza padre.</span><span class="sxs-lookup"><span data-stu-id="3fad8-152">Event trace class GUID of the parent instance.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-153">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="3fad8-153">**ParentInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-154">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3fad8-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-156">Qualificatori: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="3fad8-156">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-157">Identificatore dei dati dell'istanza padre.</span><span class="sxs-lookup"><span data-stu-id="3fad8-157">Identifier of the parent instance data.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-158">**ReservedHeaderField**</span><span class="sxs-lookup"><span data-stu-id="3fad8-158">**ReservedHeaderField**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-159">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3fad8-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-161">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="3fad8-161">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-162">Riservato.</span><span class="sxs-lookup"><span data-stu-id="3fad8-162">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-163">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="3fad8-163">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-164">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3fad8-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-166">Qualificatori: **WmiDataId** (6), **puntatore**</span><span class="sxs-lookup"><span data-stu-id="3fad8-166">Qualifiers: **WmiDataId** (6), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-167">Identifica il thread che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="3fad8-167">Identifies the thread that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-168">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="3fad8-168">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-169">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3fad8-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-171">Qualificatori: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="3fad8-171">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-172">Contiene la data e l'ora in cui si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="3fad8-172">Contains the date and time when the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-173">**TraceLevel**</span><span class="sxs-lookup"><span data-stu-id="3fad8-173">**TraceLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-174">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3fad8-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-176">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="3fad8-176">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-177">Valore definito dal provider che definisce il livello di gravità utilizzato per generare l'evento.</span><span class="sxs-lookup"><span data-stu-id="3fad8-177">Provider-defined value that defines the severity level used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-178">**TraceVersion**</span><span class="sxs-lookup"><span data-stu-id="3fad8-178">**TraceVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-179">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3fad8-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-181">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="3fad8-181">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-182">Numero di versione definito dal provider della classe traccia eventi utilizzata per generare l'evento.</span><span class="sxs-lookup"><span data-stu-id="3fad8-182">Provider-defined version number of the event trace class used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="3fad8-183">**Tempi**</span><span class="sxs-lookup"><span data-stu-id="3fad8-183">**UserTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fad8-184">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3fad8-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fad8-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fad8-186">Qualificatori: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="3fad8-186">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="3fad8-187">Tempo di esecuzione trascorso per le istruzioni in modalità utente, in cicli della CPU.</span><span class="sxs-lookup"><span data-stu-id="3fad8-187">Elapsed execution time for user-mode instructions, in CPU ticks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fad8-188">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fad8-188">Remarks</span></span>

<span data-ttu-id="3fad8-189">Non usare queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3fad8-189">Do not use these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fad8-190">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fad8-190">Requirements</span></span>



| <span data-ttu-id="3fad8-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fad8-191">Requirement</span></span> | <span data-ttu-id="3fad8-192">Valore</span><span class="sxs-lookup"><span data-stu-id="3fad8-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3fad8-193">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fad8-193">Minimum supported client</span></span><br/> | <span data-ttu-id="3fad8-194">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3fad8-194">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3fad8-195">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fad8-195">Minimum supported server</span></span><br/> | <span data-ttu-id="3fad8-196">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3fad8-196">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3fad8-197">MOF</span><span class="sxs-lookup"><span data-stu-id="3fad8-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fad8-198"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fad8-198"><dt>Wmi.mof</dt></span></span> </dl> |



 

 




