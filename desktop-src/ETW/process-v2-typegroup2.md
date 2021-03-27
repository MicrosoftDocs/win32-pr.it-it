---
description: Questa classe è la classe del tipo di evento per gli eventi del contatore di processi. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Classe Process_V2_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 284b77da03b53f9c2662c8729a7bf6606c45630a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884350"
---
# <a name="process_v2_typegroup2-class"></a><span data-ttu-id="2beee-104">\_ \_ Classe TypeGroup2 del processo V2</span><span class="sxs-lookup"><span data-stu-id="2beee-104">Process\_V2\_TypeGroup2 class</span></span>

<span data-ttu-id="2beee-105">Questa classe è la classe del tipo di evento per gli eventi del contatore di processi.</span><span class="sxs-lookup"><span data-stu-id="2beee-105">This class is the event type class for process counter events.</span></span>

<span data-ttu-id="2beee-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="2beee-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2beee-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2beee-107">Syntax</span></span>

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a><span data-ttu-id="2beee-108">Members</span><span class="sxs-lookup"><span data-stu-id="2beee-108">Members</span></span>

<span data-ttu-id="2beee-109">La **classe \_ \_ TypeGroup2 del processo v2** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2beee-109">The **Process\_V2\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="2beee-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2beee-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2beee-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2beee-111">Properties</span></span>

<span data-ttu-id="2beee-112">La classe **Process \_ v2 \_ TypeGroup2** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2beee-112">The **Process\_V2\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2beee-113">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="2beee-113">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2beee-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-116">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="2beee-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="2beee-117">Conteggio degli handle utilizzati.</span><span class="sxs-lookup"><span data-stu-id="2beee-117">Count of used handles.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-118">**PageFaultCount**</span><span class="sxs-lookup"><span data-stu-id="2beee-118">**PageFaultCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2beee-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-121">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="2beee-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="2beee-122">Numero di errori di pagina.</span><span class="sxs-lookup"><span data-stu-id="2beee-122">Count of page faults.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-123">**PagefileUsage**</span><span class="sxs-lookup"><span data-stu-id="2beee-123">**PagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-124">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2beee-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-126">Qualificatori: WmiDataId (12), estensione ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="2beee-126">Qualifiers: WmiDataId(12), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-127">Utilizzo del file di paging corrente.</span><span class="sxs-lookup"><span data-stu-id="2beee-127">Current page file usage.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-128">**PeakPagefileUsage**</span><span class="sxs-lookup"><span data-stu-id="2beee-128">**PeakPagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-129">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2beee-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-131">Qualificatori: WmiDataId (7), estensione ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="2beee-131">Qualifiers: WmiDataId(7), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-132">Dimensioni massime del file di paging utilizzate.</span><span class="sxs-lookup"><span data-stu-id="2beee-132">Largest page file size used.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-133">**PeakVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="2beee-133">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-134">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2beee-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-136">Qualificatori: WmiDataId (5), estensione ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="2beee-136">Qualifiers: WmiDataId(5), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-137">Dimensioni massime della pagina virtuale utilizzate.</span><span class="sxs-lookup"><span data-stu-id="2beee-137">Largest virtual page size used.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-138">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="2beee-138">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-139">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2beee-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-141">Qualificatori: WmiDataId (6), estensione ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="2beee-141">Qualifiers: WmiDataId(6), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-142">Dimensioni massime working set utilizzate.</span><span class="sxs-lookup"><span data-stu-id="2beee-142">Largest working set size used.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-143">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="2beee-143">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-144">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2beee-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-146">Qualificatori: WmiDataId (15), estensione ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="2beee-146">Qualifiers: WmiDataId(15), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-147">Conteggio delle pagine fisiche private correnti.</span><span class="sxs-lookup"><span data-stu-id="2beee-147">Current private physical page count.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-148">ProcessId</span><span class="sxs-lookup"><span data-stu-id="2beee-148">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2beee-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-151">Qualificatori: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="2beee-151">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-152">Identificatore di processo globale che è possibile utilizzare per identificare un processo.</span><span class="sxs-lookup"><span data-stu-id="2beee-152">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="2beee-153">Il valore è valido dal momento in cui un processo viene creato fino a quando non viene terminato.</span><span class="sxs-lookup"><span data-stu-id="2beee-153">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-154">**QuotaNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="2beee-154">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-155">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2beee-155">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-157">Qualificatori: WmiDataId (14), estensione ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="2beee-157">Qualifiers: WmiDataId(14), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-158">Utilizzo di memoria non di paging corrente.</span><span class="sxs-lookup"><span data-stu-id="2beee-158">Current committed non-paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-159">**QuotaPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="2beee-159">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-160">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2beee-160">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-162">Qualificatori: WmiDataId (13), estensione ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="2beee-162">Qualifiers: WmiDataId(13), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-163">Utilizzo corrente della memoria di paging vincolato.</span><span class="sxs-lookup"><span data-stu-id="2beee-163">Current committed paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-164">**QuotaPeakNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="2beee-164">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-165">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2beee-165">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-167">Qualificatori: WmiDataId (9), estensione ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="2beee-167">Qualifiers: WmiDataId(9), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-168">Memoria non di paging più grande utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2beee-168">Largest committed non-paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-169">**QuotaPeakPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="2beee-169">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-170">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2beee-170">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-172">Qualificatori: WmiDataId (8), estensione ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="2beee-172">Qualifiers: WmiDataId(8), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-173">Memoria di paging più grande utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2beee-173">Largest committed paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-174">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="2beee-174">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-175">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2beee-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-177">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="2beee-177">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="2beee-178">Riservato.</span><span class="sxs-lookup"><span data-stu-id="2beee-178">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-179">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="2beee-179">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-180">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2beee-180">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-182">Qualificatori: WmiDataId (10), estensione ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="2beee-182">Qualifiers: WmiDataId(10), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-183">Dimensioni correnti della pagina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2beee-183">Current virtual page size.</span></span>

</dd> <dt>

<span data-ttu-id="2beee-184">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="2beee-184">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2beee-185">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2beee-185">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2beee-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2beee-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2beee-187">Qualificatori: WmiDataId (11), estensione ("SizeT")</span><span class="sxs-lookup"><span data-stu-id="2beee-187">Qualifiers: WmiDataId(11), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="2beee-188">Dimensioni correnti del working set.</span><span class="sxs-lookup"><span data-stu-id="2beee-188">Current working set size.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2beee-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="2beee-189">Remarks</span></span>

<span data-ttu-id="2beee-190">Questi eventi vengono registrati al termine del processo.</span><span class="sxs-lookup"><span data-stu-id="2beee-190">These events are logged when the process ends.</span></span> <span data-ttu-id="2beee-191">L'evento indica il modo in cui un processo ha gestito l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="2beee-191">The event indicates how a process handled memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="2beee-192">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2beee-192">Requirements</span></span>



| <span data-ttu-id="2beee-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="2beee-193">Requirement</span></span> | <span data-ttu-id="2beee-194">Valore</span><span class="sxs-lookup"><span data-stu-id="2beee-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2beee-195">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2beee-195">Minimum supported client</span></span><br/> | <span data-ttu-id="2beee-196">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2beee-196">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2beee-197">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2beee-197">Minimum supported server</span></span><br/> | <span data-ttu-id="2beee-198">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2beee-198">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2beee-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2beee-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2beee-200">**Processo \_ v2**</span><span class="sxs-lookup"><span data-stu-id="2beee-200">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




