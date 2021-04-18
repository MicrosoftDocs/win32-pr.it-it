---
description: Il \_ thread Win32&\# 8194; La classe WMI rappresenta un thread di esecuzione.
ms.assetid: a284616c-1977-441a-9173-dff4f56b2d39
ms.tgt_platform: multiple
title: Classe Win32_Thread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Thread
- Win32_Thread.Caption
- Win32_Thread.CreationClassName
- Win32_Thread.CSCreationClassName
- Win32_Thread.CSName
- Win32_Thread.Description
- Win32_Thread.ElapsedTime
- Win32_Thread.ExecutionState
- Win32_Thread.Handle
- Win32_Thread.InstallDate
- Win32_Thread.KernelModeTime
- Win32_Thread.Name
- Win32_Thread.OSCreationClassName
- Win32_Thread.OSName
- Win32_Thread.Priority
- Win32_Thread.PriorityBase
- Win32_Thread.ProcessCreationClassName
- Win32_Thread.ProcessHandle
- Win32_Thread.StartAddress
- Win32_Thread.Status
- Win32_Thread.ThreadState
- Win32_Thread.ThreadWaitReason
- Win32_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6e9f6a8c821aa327e8b810b634c85bb06459910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305239"
---
# <a name="win32_thread-class"></a><span data-ttu-id="03d7c-103">\_Classe thread Win32</span><span class="sxs-lookup"><span data-stu-id="03d7c-103">Win32\_Thread class</span></span>

<span data-ttu-id="03d7c-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) del **\_ thread Win32** rappresenta un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="03d7c-104">The **Win32\_Thread** [WMI class](../wmisdk/retrieving-a-class.md) represents a thread of execution.</span></span> <span data-ttu-id="03d7c-105">Mentre un processo deve avere un solo thread di esecuzione, il processo può creare altri thread per eseguire attività in parallelo.</span><span class="sxs-lookup"><span data-stu-id="03d7c-105">While a process must have one thread of execution, the process can create other threads to execute tasks in parallel.</span></span> <span data-ttu-id="03d7c-106">I thread condividono l'ambiente di elaborazione, pertanto più thread con lo stesso processo utilizzano meno memoria dello stesso numero di processi.</span><span class="sxs-lookup"><span data-stu-id="03d7c-106">Threads share the process environment, thus multiple threads under the same process use less memory than the same number of processes.</span></span>

<span data-ttu-id="03d7c-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="03d7c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="03d7c-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="03d7c-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d7c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03d7c-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4DD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Thread : CIM_Thread
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   ElapsedTime;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  uint32   PriorityBase;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  uint32   StartAddress;
  string   Status;
  uint32   ThreadState;
  uint32   ThreadWaitReason;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="03d7c-110">Members</span><span class="sxs-lookup"><span data-stu-id="03d7c-110">Members</span></span>

<span data-ttu-id="03d7c-111">La **classe \_ thread Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="03d7c-111">The **Win32\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="03d7c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03d7c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03d7c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03d7c-113">Properties</span></span>

<span data-ttu-id="03d7c-114">La **classe \_ thread Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="03d7c-114">The **Win32\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03d7c-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="03d7c-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-118">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="03d7c-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-119">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03d7c-119">Short description of the object.</span></span>

<span data-ttu-id="03d7c-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="03d7c-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-124">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="03d7c-124">Qualifiers: [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-125">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="03d7c-125">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="03d7c-126">Se utilizzata con le altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="03d7c-126">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="03d7c-127">Questa proprietà viene ereditata [**dal \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-127">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-128">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="03d7c-128">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-131">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ processo CIM**](cim-process.md).**CSCreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="03d7c-131">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-132">Nome della classe di creazione del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="03d7c-132">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="03d7c-133">Questa proprietà viene ereditata [**dal \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-133">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="03d7c-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-137">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ processo CIM**](cim-process.md).**CSName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="03d7c-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-138">Nome del sistema di ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="03d7c-138">Name of the scoping computer system.</span></span>

<span data-ttu-id="03d7c-139">Questa proprietà viene ereditata [**dal \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-139">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-140">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="03d7c-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-143">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="03d7c-143">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-144">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03d7c-144">Description of the object.</span></span>

<span data-ttu-id="03d7c-145">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-146">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="03d7c-146">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-147">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03d7c-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-149">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Performance Data Structures \| [**\_ \_ tipo di oggetto Perf**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfTime"), [**unità**](../wmisdk/standard-qualifiers.md) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="03d7c-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-150">Tempo di esecuzione totale, espresso in millisecondi, assegnato al thread dalla relativa creazione.</span><span class="sxs-lookup"><span data-stu-id="03d7c-150">Total execution time, in milliseconds, given to this thread since its creation.</span></span>

<span data-ttu-id="03d7c-151">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-151">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-152">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="03d7c-152">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-153">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d7c-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-155">Condizione operativa corrente del thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-155">Current operating condition of the thread.</span></span>

<span data-ttu-id="03d7c-156">Questa proprietà viene ereditata [**dal \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-156">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03d7c-157">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="03d7c-157">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03d7c-158">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="03d7c-158">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="03d7c-159">**Pronto** (2)</span><span class="sxs-lookup"><span data-stu-id="03d7c-159">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="03d7c-160">**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="03d7c-160">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="03d7c-161">**Bloccato** (4)</span><span class="sxs-lookup"><span data-stu-id="03d7c-161">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="03d7c-162">**Sospeso bloccato** (5)</span><span class="sxs-lookup"><span data-stu-id="03d7c-162">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="03d7c-163">**Pronto per sospensione** (6)</span><span class="sxs-lookup"><span data-stu-id="03d7c-163">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03d7c-164">**Handle**</span><span class="sxs-lookup"><span data-stu-id="03d7c-164">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-167">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| strumenti della Guida di \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32ThreadID")</span><span class="sxs-lookup"><span data-stu-id="03d7c-167">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32ThreadID")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-168">Handle per un thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-168">Handle to a thread.</span></span> <span data-ttu-id="03d7c-169">Per impostazione predefinita, l'handle dispone di diritti di accesso completi.</span><span class="sxs-lookup"><span data-stu-id="03d7c-169">The handle has full access rights by default.</span></span> <span data-ttu-id="03d7c-170">Con l'accesso di sicurezza corretto, l'handle può essere usato in qualsiasi funzione che accetta un handle di thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-170">With the correct security access, the handle can be used in any function that accepts a thread handle.</span></span> <span data-ttu-id="03d7c-171">A seconda del flag di ereditarietà specificato quando viene creato, questo handle può essere ereditato dai processi figlio.</span><span class="sxs-lookup"><span data-stu-id="03d7c-171">Depending on the inheritance flag specified when it is created, this handle can be inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="03d7c-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-173">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03d7c-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-175">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="03d7c-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-176">L'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="03d7c-176">Object was installed.</span></span> <span data-ttu-id="03d7c-177">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="03d7c-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="03d7c-178">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-179">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="03d7c-179">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-180">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03d7c-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-182">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Performance Data Structures \| [**\_ \_ tipo oggetto Perf**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PrivilegedTime"), [**unità**](../wmisdk/standard-qualifiers.md) ("100 nanosecondi")</span><span class="sxs-lookup"><span data-stu-id="03d7c-182">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PrivilegedTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-183">Tempo in modalità kernel, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="03d7c-183">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="03d7c-184">Se queste informazioni non sono disponibili, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="03d7c-184">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="03d7c-185">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-186">**Nome**</span><span class="sxs-lookup"><span data-stu-id="03d7c-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-189">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="03d7c-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-190">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="03d7c-190">Label by which the object is known.</span></span> <span data-ttu-id="03d7c-191">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="03d7c-191">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="03d7c-192">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-193">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="03d7c-193">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-196">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ processo CIM**](cim-process.md).**OSCreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="03d7c-196">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-197">Nome della classe di creazione del sistema operativo di ambito.</span><span class="sxs-lookup"><span data-stu-id="03d7c-197">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="03d7c-198">Questa proprietà viene ereditata [**dal \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-198">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-199">**OSName**</span><span class="sxs-lookup"><span data-stu-id="03d7c-199">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-202">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ processo CIM**](cim-process.md).**OSName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="03d7c-202">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-203">Nome del sistema operativo di ambito.</span><span class="sxs-lookup"><span data-stu-id="03d7c-203">Name of the scoping operating system.</span></span>

<span data-ttu-id="03d7c-204">Questa proprietà viene ereditata [**dal \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-204">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-205">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="03d7c-205">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-206">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03d7c-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-208">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Helper tool Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| tpDeltaPri")</span><span class="sxs-lookup"><span data-stu-id="03d7c-208">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|tpDeltaPri")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-209">Priorità dinamica del thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-209">Dynamic priority of the thread.</span></span> <span data-ttu-id="03d7c-210">Ogni thread ha una priorità dinamica utilizzata dall'utilità di pianificazione per determinare il thread da eseguire.</span><span class="sxs-lookup"><span data-stu-id="03d7c-210">Each thread has a dynamic priority that the scheduler uses to determine which thread to execute.</span></span> <span data-ttu-id="03d7c-211">Inizialmente, la priorità dinamica di un thread corrisponde alla priorità di base.</span><span class="sxs-lookup"><span data-stu-id="03d7c-211">Initially, a thread's dynamic priority is the same as its base priority.</span></span> <span data-ttu-id="03d7c-212">Il sistema può aumentare e ridurre la priorità dinamica, per assicurarsi che sia reattivo (garantendo che nessun thread sia affamato per il tempo del processore).</span><span class="sxs-lookup"><span data-stu-id="03d7c-212">The system can raise and lower the dynamic priority, to ensure that it is responsive (guaranteeing that no threads are starved for processor time).</span></span> <span data-ttu-id="03d7c-213">Il sistema non incrementa la priorità dei thread con un livello di priorità di base compreso tra 16 e 31.</span><span class="sxs-lookup"><span data-stu-id="03d7c-213">The system does not boost the priority of threads with a base priority level between 16 and 31.</span></span> <span data-ttu-id="03d7c-214">Solo i thread con priorità di base compresa tra 0 e 15 ricevono Boost di priorità dinamica.</span><span class="sxs-lookup"><span data-stu-id="03d7c-214">Only threads with a base priority between 0 and 15 receive dynamic priority boosts.</span></span> <span data-ttu-id="03d7c-215">I numeri più alti indicano priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="03d7c-215">Higher numbers indicate higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-216">**PriorityBase**</span><span class="sxs-lookup"><span data-stu-id="03d7c-216">**PriorityBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-217">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03d7c-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-219">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Performance Data Structures \| [**\_ \_ tipo di oggetto Perf**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfPriorityBase")</span><span class="sxs-lookup"><span data-stu-id="03d7c-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfPriorityBase")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-220">Priorità di base corrente di un thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-220">Current base priority of a thread.</span></span> <span data-ttu-id="03d7c-221">Il sistema operativo può aumentare la priorità dinamica del thread sopra la priorità di base se il thread sta gestendo l'input dell'utente o diminuirlo verso la priorità di base se il thread diventa associato a un calcolo.</span><span class="sxs-lookup"><span data-stu-id="03d7c-221">The operating system may raise the thread's dynamic priority above the base priority if the thread is handling user input, or lower it toward the base priority if the thread becomes compute-bound.</span></span> <span data-ttu-id="03d7c-222">Il valore della proprietà **PriorityBase** può essere compreso tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="03d7c-222">The **PriorityBase** property can have a value between 0 and 31.</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-223">**ProcessCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="03d7c-223">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-224">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-226">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ processo CIM**](cim-process.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="03d7c-226">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-227">Valore della proprietà **CreationClassName** del processo di definizione dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="03d7c-227">Value of the scoping process **CreationClassName** property.</span></span>

<span data-ttu-id="03d7c-228">Questa proprietà viene ereditata [**dal \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-228">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-229">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="03d7c-229">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-232">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ processo CIM**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" Win32API \| Guida dello strumento \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32OwnerProcessID ")</span><span class="sxs-lookup"><span data-stu-id="03d7c-232">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32OwnerProcessID")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-233">Processo che ha creato il thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-233">Process that created the thread.</span></span> <span data-ttu-id="03d7c-234">Il contenuto di questa proprietà può essere utilizzato dagli elementi Application Programming Interface (API) di Windows.</span><span class="sxs-lookup"><span data-stu-id="03d7c-234">The contents of this property can be used by Windows application programming interface (API) elements.</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-235">**StartAddress**</span><span class="sxs-lookup"><span data-stu-id="03d7c-235">**StartAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-236">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03d7c-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-238">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIn32API \| thread Object \| LPTHREAD \_ Start \_ routine \| lpStartAddress")</span><span class="sxs-lookup"><span data-stu-id="03d7c-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIn32API\|Thread Object\|LPTHREAD\_START\_ROUTINE\|lpStartAddress")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-239">Indirizzo iniziale del thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-239">Starting address of the thread.</span></span> <span data-ttu-id="03d7c-240">Poiché qualsiasi applicazione con accesso appropriato al thread può modificare il contesto del thread, questo valore può essere solo un'approssimazione dell'indirizzo iniziale del thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-240">Because any application with appropriate access to the thread can change the thread's context, this value may only be an approximation of the thread's starting address.</span></span>

</dd> <dt>

<span data-ttu-id="03d7c-241">**Status**</span><span class="sxs-lookup"><span data-stu-id="03d7c-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03d7c-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-244">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="03d7c-244">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-245">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03d7c-245">Current status of the object.</span></span> <span data-ttu-id="03d7c-246">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="03d7c-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="03d7c-247">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="03d7c-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="03d7c-248">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="03d7c-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="03d7c-249">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="03d7c-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="03d7c-250">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="03d7c-250">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="03d7c-251">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="03d7c-252">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="03d7c-252">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="03d7c-253">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="03d7c-253">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="03d7c-254">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="03d7c-254">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="03d7c-255">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="03d7c-255">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03d7c-256">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="03d7c-256">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="03d7c-257">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="03d7c-257">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="03d7c-258">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="03d7c-258">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="03d7c-259">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="03d7c-259">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="03d7c-260">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="03d7c-260">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="03d7c-261">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="03d7c-261">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="03d7c-262">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="03d7c-262">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="03d7c-263">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="03d7c-263">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="03d7c-264">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="03d7c-264">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03d7c-265">**ThreadState**</span><span class="sxs-lookup"><span data-stu-id="03d7c-265">**ThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-266">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03d7c-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-268">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| stato thread Win32API")</span><span class="sxs-lookup"><span data-stu-id="03d7c-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread State")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-269">Stato di esecuzione corrente per il thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-269">Current execution state for the thread.</span></span>

<dt>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>

<span data-ttu-id="03d7c-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Inizializzato** (0)</span><span class="sxs-lookup"><span data-stu-id="03d7c-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Initialized** (0)</span></span>


</dt> <dd>

<span data-ttu-id="03d7c-271">Initialized: viene riconosciuta dal microkernel.</span><span class="sxs-lookup"><span data-stu-id="03d7c-271">Initialized — It is recognized by the microkernel.</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="03d7c-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Pronto** (1)</span><span class="sxs-lookup"><span data-stu-id="03d7c-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (1)</span></span>


</dt> <dd>

<span data-ttu-id="03d7c-273">Pronto: è pronto per l'esecuzione nel processore disponibile successivo.</span><span class="sxs-lookup"><span data-stu-id="03d7c-273">Ready — It is prepared to run on the next available processor.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="03d7c-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (2)</span><span class="sxs-lookup"><span data-stu-id="03d7c-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (2)</span></span>


</dt> <dd>

<span data-ttu-id="03d7c-275">Running: è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="03d7c-275">Running — It is executing.</span></span>

</dd> <dt>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>

<span data-ttu-id="03d7c-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Standby** (3)</span><span class="sxs-lookup"><span data-stu-id="03d7c-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="03d7c-277">Standby: sta per essere eseguito, un solo thread potrebbe trovarsi in questo stato alla volta.</span><span class="sxs-lookup"><span data-stu-id="03d7c-277">Standby — It is about to run, only one thread may be in this state at a time.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="03d7c-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminata** (4)</span><span class="sxs-lookup"><span data-stu-id="03d7c-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (4)</span></span>


</dt> <dd>

<span data-ttu-id="03d7c-279">Terminato: l'esecuzione è terminata.</span><span class="sxs-lookup"><span data-stu-id="03d7c-279">Terminated — It is finished executing.</span></span>

</dd> <dt>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>

<span data-ttu-id="03d7c-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**In attesa** (5)</span><span class="sxs-lookup"><span data-stu-id="03d7c-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**Waiting** (5)</span></span>


</dt> <dd>

<span data-ttu-id="03d7c-281">In attesa: non è pronto per il processore, quando è pronto, verrà ripianificato.</span><span class="sxs-lookup"><span data-stu-id="03d7c-281">Waiting — It is not ready for the processor, when ready, it will be rescheduled.</span></span>

</dd> <dt>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>

<span data-ttu-id="03d7c-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transizione** (6)</span><span class="sxs-lookup"><span data-stu-id="03d7c-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transition** (6)</span></span>


</dt> <dd>

<span data-ttu-id="03d7c-283">Transizione: il thread è in attesa di risorse diverse dal processore,</span><span class="sxs-lookup"><span data-stu-id="03d7c-283">Transition — The thread is waiting for resources other than the processor,</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03d7c-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (7)</span><span class="sxs-lookup"><span data-stu-id="03d7c-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (7)</span></span>


</dt> <dd>

<span data-ttu-id="03d7c-285">Sconosciuto: lo stato del thread è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="03d7c-285">Unknown — The thread state is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="03d7c-286">**ThreadWaitReason**</span><span class="sxs-lookup"><span data-stu-id="03d7c-286">**ThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-287">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03d7c-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-289">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| thread Wait Reason")</span><span class="sxs-lookup"><span data-stu-id="03d7c-289">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread Wait Reason")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-290">Motivo per cui il thread è in attesa.</span><span class="sxs-lookup"><span data-stu-id="03d7c-290">Reason why the thread is waiting.</span></span> <span data-ttu-id="03d7c-291">Questo valore è valido solo se il membro **ThreadState** è impostato su Transition (6).</span><span class="sxs-lookup"><span data-stu-id="03d7c-291">This value is only valid if the **ThreadState** member is set to Transition (6).</span></span> <span data-ttu-id="03d7c-292">Le coppie di eventi consentono la comunicazione con i sottosistemi protetti.</span><span class="sxs-lookup"><span data-stu-id="03d7c-292">Event pairs allow communication with protected subsystems.</span></span>

<dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="03d7c-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Dirigente** (0)</span><span class="sxs-lookup"><span data-stu-id="03d7c-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="03d7c-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)</span><span class="sxs-lookup"><span data-stu-id="03d7c-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)</span></span>


</dt> <dd>

<span data-ttu-id="03d7c-295">FreePage</span><span class="sxs-lookup"><span data-stu-id="03d7c-295">FreePage</span></span>

</dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="03d7c-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Pagina** in (2)</span><span class="sxs-lookup"><span data-stu-id="03d7c-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="03d7c-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)</span><span class="sxs-lookup"><span data-stu-id="03d7c-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="03d7c-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)</span><span class="sxs-lookup"><span data-stu-id="03d7c-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="03d7c-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)</span><span class="sxs-lookup"><span data-stu-id="03d7c-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="03d7c-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Pagina** (6)</span><span class="sxs-lookup"><span data-stu-id="03d7c-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="03d7c-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)</span><span class="sxs-lookup"><span data-stu-id="03d7c-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="03d7c-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)</span><span class="sxs-lookup"><span data-stu-id="03d7c-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="03d7c-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9)</span><span class="sxs-lookup"><span data-stu-id="03d7c-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="03d7c-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)</span><span class="sxs-lookup"><span data-stu-id="03d7c-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="03d7c-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)</span><span class="sxs-lookup"><span data-stu-id="03d7c-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="03d7c-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)</span><span class="sxs-lookup"><span data-stu-id="03d7c-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="03d7c-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13)</span><span class="sxs-lookup"><span data-stu-id="03d7c-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>

<span data-ttu-id="03d7c-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)</span><span class="sxs-lookup"><span data-stu-id="03d7c-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>

<span data-ttu-id="03d7c-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)</span><span class="sxs-lookup"><span data-stu-id="03d7c-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>

<span data-ttu-id="03d7c-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)</span><span class="sxs-lookup"><span data-stu-id="03d7c-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>

<span data-ttu-id="03d7c-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)</span><span class="sxs-lookup"><span data-stu-id="03d7c-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>

<span data-ttu-id="03d7c-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)</span><span class="sxs-lookup"><span data-stu-id="03d7c-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>

<span data-ttu-id="03d7c-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**Paging** (19)</span><span class="sxs-lookup"><span data-stu-id="03d7c-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03d7c-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (20)</span><span class="sxs-lookup"><span data-stu-id="03d7c-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (20)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03d7c-315">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="03d7c-315">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d7c-316">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03d7c-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03d7c-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d7c-318">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Performance Data Structures \| [**\_ \_ tipo oggetto Perf**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| UserTime"), [**unità**](../wmisdk/standard-qualifiers.md) ("100 nanosecondi")</span><span class="sxs-lookup"><span data-stu-id="03d7c-318">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|UserTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="03d7c-319">Tempo in modalità utente, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="03d7c-319">Time in user mode, in 100 nanoseconds units.</span></span> <span data-ttu-id="03d7c-320">Se queste informazioni non sono disponibili, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="03d7c-320">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="03d7c-321">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03d7c-322">Commenti</span><span class="sxs-lookup"><span data-stu-id="03d7c-322">Remarks</span></span>

<span data-ttu-id="03d7c-323">La **classe \_ thread Win32** è derivata dal [**\_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="03d7c-323">The **Win32\_Thread** class is derived from [**CIM\_Thread**](cim-thread.md).</span></span>

<span data-ttu-id="03d7c-324">**Overview**</span><span class="sxs-lookup"><span data-stu-id="03d7c-324">**Overview**</span></span>

<span data-ttu-id="03d7c-325">Per il monitoraggio giornaliero di routine, non è in genere necessario avere un elenco dettagliato dei thread e delle proprietà associate.</span><span class="sxs-lookup"><span data-stu-id="03d7c-325">For routine day-to-day monitoring, there is usually little reason to have a detailed list of threads and their associated properties.</span></span> <span data-ttu-id="03d7c-326">I computer creano ed eliminano migliaia di thread durante il corso di un giorno e alcune di queste creazioni o eliminazioni sono significative per chiunque, tranne per gli sviluppatori che hanno scritto il software.</span><span class="sxs-lookup"><span data-stu-id="03d7c-326">Computers create and delete thousands of threads during the course of a day, and few of these creations or deletions are meaningful to anyone but the developer who wrote the software.</span></span>

<span data-ttu-id="03d7c-327">Tuttavia, quando si risolvono i problemi relativi a un'applicazione, il rilevamento dei singoli thread per un processo consente di identificare quando vengono creati i thread e quando (o se) vengono eliminati definitivamente.</span><span class="sxs-lookup"><span data-stu-id="03d7c-327">However, when you are troubleshooting problems with an application, tracking the individual threads for a process allows you to identify when threads are created and when (or if) they are destroyed.</span></span> <span data-ttu-id="03d7c-328">Poiché i thread creati ma non distrutti causano perdite di memoria, il rilevamento dei singoli thread può essere utile per i tecnici di supporto.</span><span class="sxs-lookup"><span data-stu-id="03d7c-328">Because threads that are created but not destroyed cause memory leaks, tracking individual threads can be useful information for support technicians.</span></span> <span data-ttu-id="03d7c-329">Analogamente, l'identificazione delle priorità dei thread può aiutare a individuare i thread che, eseguendo a una priorità eccessivamente elevata, prevedono la precedenza dei cicli della CPU richiesti da altri thread e altri processi.</span><span class="sxs-lookup"><span data-stu-id="03d7c-329">Likewise, identifying thread priorities can help pinpoint threads that, by running at an abnormally high priority, are preempting CPU cycles needed by other threads and other processes.</span></span>

<span data-ttu-id="03d7c-330">**Uso del \_ thread Win32**</span><span class="sxs-lookup"><span data-stu-id="03d7c-330">**Using Win32\_Thread**</span></span>

<span data-ttu-id="03d7c-331">Come implicito nel blocco di sintassi precedente, la classe **\_ thread Win32** non segnala il nome del processo in cui viene eseguito ogni thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-331">As implied in the preceding syntax block, the **Win32\_Thread** class does not report the name of the process under which each thread runs.</span></span> <span data-ttu-id="03d7c-332">Indica invece l'ID del processo in cui viene eseguito il thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-332">Instead, it reports the ID of the process under which the thread runs.</span></span> <span data-ttu-id="03d7c-333">Per restituire il nome di un processo e un elenco di tutti i relativi thread, lo script deve:</span><span class="sxs-lookup"><span data-stu-id="03d7c-333">To return the name of a process and a list of all its threads, your script must:</span></span>

1.  <span data-ttu-id="03d7c-334">Connettersi alla classe [**di \_ processo Win32**](win32-process.md) e restituire l'elenco dei processi e i relativi ID del processo.</span><span class="sxs-lookup"><span data-stu-id="03d7c-334">Connect to the [**Win32\_Process**](win32-process.md) class and return the list of processes and their process IDs.</span></span>
2.  <span data-ttu-id="03d7c-335">Archiviare temporaneamente queste informazioni in un oggetto Array o Dictionary.</span><span class="sxs-lookup"><span data-stu-id="03d7c-335">Temporarily store this information in an array or Dictionary object.</span></span>
3.  <span data-ttu-id="03d7c-336">Per ogni ID di processo, restituire l'elenco dei thread per il processo e quindi visualizzare il nome del processo e l'elenco dei thread.</span><span class="sxs-lookup"><span data-stu-id="03d7c-336">For each process ID, return the list of threads for that process, and then display the process name and the list of threads.</span></span>

## <a name="examples"></a><span data-ttu-id="03d7c-337">Esempio</span><span class="sxs-lookup"><span data-stu-id="03d7c-337">Examples</span></span>

<span data-ttu-id="03d7c-338">Nell'esempio VBScript seguente vengono monitorati i thread in esecuzione in un computer.</span><span class="sxs-lookup"><span data-stu-id="03d7c-338">The following VBScript sample monitors the threads running on a computer.</span></span>


```VB
Set objDictionary = CreateObject("Scripting.Dictionary")
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcesses
 objDictionary.Add objProcess.ProcessID, objProcess.Name
Next
Set colThreads = objWMIService.ExecQuery("SELECT * FROM Win32_Thread")
For Each objThread in colThreads
 intProcessID = CInt(objThread.ProcessHandle)
 strProcessName = objDictionary.Item(intProcessID)
 Wscript.Echo strProcessName & VbTab & objThread.ProcessHandle & _
              VbTab & objThread.Handle & VbTab & objThread.ThreadState
Next
```



## <a name="requirements"></a><span data-ttu-id="03d7c-339">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03d7c-339">Requirements</span></span>



| <span data-ttu-id="03d7c-340">Requisito</span><span class="sxs-lookup"><span data-stu-id="03d7c-340">Requirement</span></span> | <span data-ttu-id="03d7c-341">Valore</span><span class="sxs-lookup"><span data-stu-id="03d7c-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03d7c-342">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03d7c-342">Minimum supported client</span></span><br/> | <span data-ttu-id="03d7c-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03d7c-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03d7c-344">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03d7c-344">Minimum supported server</span></span><br/> | <span data-ttu-id="03d7c-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03d7c-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03d7c-346">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03d7c-346">Namespace</span></span><br/>                | <span data-ttu-id="03d7c-347">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="03d7c-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03d7c-348">MOF</span><span class="sxs-lookup"><span data-stu-id="03d7c-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03d7c-349"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03d7c-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03d7c-350">DLL</span><span class="sxs-lookup"><span data-stu-id="03d7c-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03d7c-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03d7c-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03d7c-352">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03d7c-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d7c-353">**\_Thread CIM**</span><span class="sxs-lookup"><span data-stu-id="03d7c-353">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dt>

[<span data-ttu-id="03d7c-354">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="03d7c-354">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
