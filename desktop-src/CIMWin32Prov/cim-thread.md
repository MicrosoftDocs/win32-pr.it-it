---
description: La \_ classe di thread CIM rappresenta la possibilità di eseguire unità di un processo o di un'attività, in parallelo. Un processo può avere molti thread, ognuno dei quali è debole per il processo.
ms.assetid: 57222d57-61bd-4641-a77c-805263be04b7
ms.tgt_platform: multiple
title: Classe CIM_Thread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Thread
- CIM_Thread.Caption
- CIM_Thread.CreationClassName
- CIM_Thread.CSCreationClassName
- CIM_Thread.CSName
- CIM_Thread.Description
- CIM_Thread.ExecutionState
- CIM_Thread.Handle
- CIM_Thread.InstallDate
- CIM_Thread.KernelModeTime
- CIM_Thread.Name
- CIM_Thread.OSCreationClassName
- CIM_Thread.OSName
- CIM_Thread.Priority
- CIM_Thread.ProcessCreationClassName
- CIM_Thread.ProcessHandle
- CIM_Thread.Status
- CIM_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0a69554ef50a82695d2904b11f4189c3aab11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305299"
---
# <a name="cim_thread-class"></a><span data-ttu-id="a5a3b-104">\_Classe thread CIM</span><span class="sxs-lookup"><span data-stu-id="a5a3b-104">CIM\_Thread class</span></span>

<span data-ttu-id="a5a3b-105">La classe di **\_ thread CIM** rappresenta la possibilità di eseguire unità di un processo o di un'attività, in parallelo.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-105">The **CIM\_Thread** class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="a5a3b-106">Un processo può avere molti thread, ognuno dei quali è debole per il processo.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-106">A process can have many threads, each of which is weak to the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5a3b-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a5a3b-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a5a3b-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a5a3b-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5a3b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5a3b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C571-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Thread : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  string   Status;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="a5a3b-112">Members</span><span class="sxs-lookup"><span data-stu-id="a5a3b-112">Members</span></span>

<span data-ttu-id="a5a3b-113">La classe di **\_ thread CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a5a3b-113">The **CIM\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="a5a3b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a5a3b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5a3b-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a5a3b-115">Properties</span></span>

<span data-ttu-id="a5a3b-116">La classe di **\_ thread CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-116">The **CIM\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5a3b-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-121">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-121">Short textual description of the object.</span></span>

<span data-ttu-id="a5a3b-122">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-126">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-126">Qualifiers: [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-127">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a5a3b-128">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-128">When used with other key properties of the class, this property allow all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-132">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-process.md).**CSCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-133">Nome della classe di creazione dell'ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-133">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-137">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-process.md).**CSName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-138">Nome del sistema del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-138">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-139">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-142">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-143">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-143">Textual description of the object.</span></span>

<span data-ttu-id="a5a3b-144">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-145">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-145">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-146">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-148">Indica la condizione operativa corrente del thread.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-148">Indicates the current operating condition of the thread.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a5a3b-149">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a5a3b-150">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="a5a3b-151">**Pronto** (2)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-151">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="a5a3b-152">**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-152">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="a5a3b-153">**Bloccato** (4)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-153">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="a5a3b-154">**Sospeso bloccato** (5)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-154">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="a5a3b-155">**Pronto per sospensione** (6)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-155">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5a3b-156">**Handle**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-156">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-159">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-159">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-160">Identificatore del thread.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-160">Identifier for the thread.</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-162">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-164">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-165">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-165">Date and time the object was installed.</span></span> <span data-ttu-id="a5a3b-166">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a5a3b-167">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-168">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-168">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-169">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-171">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-171">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-172">Tempo, in modalità kernel, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-172">Time, in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="a5a3b-173">Se queste informazioni non sono disponibili, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-173">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="a5a3b-174">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-174">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-175">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-178">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-178">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-179">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-179">Label by which the object is known.</span></span> <span data-ttu-id="a5a3b-180">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-180">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a5a3b-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-182">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-182">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-185">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-process.md).**OSCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-186">Nome della classe di creazione dell'ambito del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-186">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-187">**OSName**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-187">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-190">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-process.md).**OSName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-190">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-191">Nome dell'ambito del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-191">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-192">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-192">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-193">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-195">Urgenza per l'esecuzione di un thread.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-195">Urgency for execution of a thread.</span></span> <span data-ttu-id="a5a3b-196">Un thread può avere una priorità diversa rispetto al processo proprietario.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-196">A thread can have a different priority than its owning process.</span></span> <span data-ttu-id="a5a3b-197">Se queste informazioni non sono disponibili per un thread, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-197">If this information is not available for a thread, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-198">**ProcessCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-198">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-201">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-process.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-202">Nome della classe di creazione del processo di definizione dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-202">Scoping process's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-203">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-203">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-206">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-process.md).**Handle**"), [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-206">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-207">Handle del processo di definizione dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-207">Scoping process's handle.</span></span>

</dd> <dt>

<span data-ttu-id="a5a3b-208">**Status**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-208">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-209">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-211">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-211">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-212">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-212">Current status of the object.</span></span> <span data-ttu-id="a5a3b-213">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a5a3b-214">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5a3b-214">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a5a3b-215">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-215">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a5a3b-216">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-216">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a5a3b-217">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a5a3b-217">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a5a3b-218">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-218">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a5a3b-219">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-219">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a5a3b-220">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-220">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a5a3b-221">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-221">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a5a3b-222">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-222">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a5a3b-223">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a5a3b-223">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a5a3b-224">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-224">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a5a3b-225">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-225">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a5a3b-226">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-226">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5a3b-227">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-227">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5a3b-228">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5a3b-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5a3b-230">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="a5a3b-230">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="a5a3b-231">Tempo, in modalità utente, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-231">Time, in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="a5a3b-232">Se queste informazioni non sono disponibili, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-232">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="a5a3b-233">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5a3b-234">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5a3b-234">Remarks</span></span>

<span data-ttu-id="a5a3b-235">La classe di **\_ thread CIM** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-235">The **CIM\_Thread** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="a5a3b-236">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-236">WMI does not implement this class.</span></span> <span data-ttu-id="a5a3b-237">Per le classi WMI derivate dal **\_ thread CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a5a3b-237">For WMI classes derived from **CIM\_Thread**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a5a3b-238">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-238">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a5a3b-239">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a5a3b-239">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5a3b-240">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5a3b-240">Requirements</span></span>



| <span data-ttu-id="a5a3b-241">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5a3b-241">Requirement</span></span> | <span data-ttu-id="a5a3b-242">Valore</span><span class="sxs-lookup"><span data-stu-id="a5a3b-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a3b-243">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5a3b-243">Minimum supported client</span></span><br/> | <span data-ttu-id="a5a3b-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5a3b-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a5a3b-245">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5a3b-245">Minimum supported server</span></span><br/> | <span data-ttu-id="a5a3b-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5a3b-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a5a3b-247">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a5a3b-247">Namespace</span></span><br/>                | <span data-ttu-id="a5a3b-248">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a5a3b-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a5a3b-249">MOF</span><span class="sxs-lookup"><span data-stu-id="a5a3b-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5a3b-250"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5a3b-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5a3b-251">DLL</span><span class="sxs-lookup"><span data-stu-id="a5a3b-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5a3b-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5a3b-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5a3b-253">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5a3b-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5a3b-254">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="a5a3b-254">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

