---
description: La \_ classe di processo CIM rappresenta una singola istanza di un programma in esecuzione. Un utente visualizza in genere un processo come un'applicazione o un'attività.
ms.assetid: 8b00ef6e-5c7f-410c-9e48-1205ea6e5a4c
ms.tgt_platform: multiple
title: Classe CIM_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Process
- CIM_Process.Caption
- CIM_Process.CreationClassName
- CIM_Process.CreationDate
- CIM_Process.CSCreationClassName
- CIM_Process.CSName
- CIM_Process.Description
- CIM_Process.ExecutionState
- CIM_Process.Handle
- CIM_Process.InstallDate
- CIM_Process.KernelModeTime
- CIM_Process.Name
- CIM_Process.OSCreationClassName
- CIM_Process.OSName
- CIM_Process.Priority
- CIM_Process.Status
- CIM_Process.TerminationDate
- CIM_Process.UserModeTime
- CIM_Process.WorkingSetSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 355e29929dc05a701a2beac0919a28aca573ca9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966335"
---
# <a name="cim_process-class"></a><span data-ttu-id="9ee12-104">\_Classe di processo CIM</span><span class="sxs-lookup"><span data-stu-id="9ee12-104">CIM\_Process class</span></span>

<span data-ttu-id="9ee12-105">La classe di **\_ processo CIM** rappresenta una singola istanza di un programma in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9ee12-105">The **CIM\_Process** class represents a single instance of a running program.</span></span> <span data-ttu-id="9ee12-106">Un utente visualizza in genere un processo come un'applicazione o un'attività.</span><span class="sxs-lookup"><span data-stu-id="9ee12-106">A user typically sees a process as an application or task.</span></span> <span data-ttu-id="9ee12-107">Un processo è definito da un'area di lavoro di risorse di memoria e impostazioni ambientali allocate.</span><span class="sxs-lookup"><span data-stu-id="9ee12-107">A process is defined by a workspace of memory resources and environmental settings that are allocated to it.</span></span> <span data-ttu-id="9ee12-108">In un sistema multitasking, l'area di lavoro impedisce l'intrusione di risorse da parte di altri processi.</span><span class="sxs-lookup"><span data-stu-id="9ee12-108">On a multitasking system, the workspace prevents intrusion of resources by other processes.</span></span> <span data-ttu-id="9ee12-109">Inoltre, un processo può essere eseguito come più thread, tutti eseguiti nella stessa area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9ee12-109">Additionally, a process can execute as multiple threads, all which run within the same workspace.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ee12-110">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9ee12-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9ee12-111">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9ee12-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9ee12-112">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9ee12-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9ee12-113">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9ee12-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ee12-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ee12-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C566-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes (CIM)"), AMENDMENT]
class CIM_Process : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  datetime CreationDate;
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
  string   Status;
  datetime TerminationDate;
  uint64   UserModeTime;
  uint64   WorkingSetSize;
};
```

## <a name="members"></a><span data-ttu-id="9ee12-115">Members</span><span class="sxs-lookup"><span data-stu-id="9ee12-115">Members</span></span>

<span data-ttu-id="9ee12-116">La classe di **\_ processo CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9ee12-116">The **CIM\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="9ee12-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9ee12-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ee12-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9ee12-118">Properties</span></span>

<span data-ttu-id="9ee12-119">La classe di **\_ processo CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9ee12-119">The **CIM\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ee12-120">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="9ee12-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ee12-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-123">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9ee12-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-124">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9ee12-124">Short textual description of the object.</span></span>

<span data-ttu-id="9ee12-125">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee12-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-126">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9ee12-126">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ee12-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-129">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="9ee12-129">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-130">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="9ee12-130">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9ee12-131">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="9ee12-131">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-132">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="9ee12-132">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-133">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9ee12-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-135">Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span><span class="sxs-lookup"><span data-stu-id="9ee12-135">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-136">Ora di inizio dell'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="9ee12-136">Time that the process began executing.</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-137">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9ee12-137">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ee12-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-140">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="9ee12-140">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-141">Nome della classe di creazione dell'ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="9ee12-141">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-142">**CSName**</span><span class="sxs-lookup"><span data-stu-id="9ee12-142">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ee12-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-145">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema computer ")</span><span class="sxs-lookup"><span data-stu-id="9ee12-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-146">Nome del sistema del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="9ee12-146">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-147">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9ee12-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ee12-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-150">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9ee12-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-151">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9ee12-151">Textual description of the object.</span></span>

<span data-ttu-id="9ee12-152">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee12-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-153">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="9ee12-153">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-154">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ee12-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-156">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("stato esecuzione")</span><span class="sxs-lookup"><span data-stu-id="9ee12-156">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-157">Condizione operativa corrente del processo.</span><span class="sxs-lookup"><span data-stu-id="9ee12-157">Current operating condition of the process.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ee12-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="9ee12-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ee12-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9ee12-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="9ee12-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Pronto** (2)</span><span class="sxs-lookup"><span data-stu-id="9ee12-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="9ee12-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="9ee12-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="9ee12-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloccato** (4)</span><span class="sxs-lookup"><span data-stu-id="9ee12-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="9ee12-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Sospeso bloccato** (5)</span><span class="sxs-lookup"><span data-stu-id="9ee12-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9ee12-164">Sospeso bloccato</span><span class="sxs-lookup"><span data-stu-id="9ee12-164">Suspended blocked</span></span>

</dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="9ee12-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Pronto per sospensione** (6)</span><span class="sxs-lookup"><span data-stu-id="9ee12-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9ee12-166">Pronto per sospensione</span><span class="sxs-lookup"><span data-stu-id="9ee12-166">Suspended ready</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="9ee12-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminato** (7)</span><span class="sxs-lookup"><span data-stu-id="9ee12-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="9ee12-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (8)</span><span class="sxs-lookup"><span data-stu-id="9ee12-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="9ee12-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>In **crescita** (9)</span><span class="sxs-lookup"><span data-stu-id="9ee12-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ee12-170">**Handle**</span><span class="sxs-lookup"><span data-stu-id="9ee12-170">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ee12-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-173">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("handle")</span><span class="sxs-lookup"><span data-stu-id="9ee12-173">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-174">Identifica il processo.</span><span class="sxs-lookup"><span data-stu-id="9ee12-174">Identifies the process.</span></span> <span data-ttu-id="9ee12-175">Un identificatore di processo è un tipo di handle di processo.</span><span class="sxs-lookup"><span data-stu-id="9ee12-175">A process identifier is a kind of process handle.</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-176">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9ee12-176">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-177">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9ee12-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-179">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="9ee12-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-180">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9ee12-180">Date and time the object was installed.</span></span> <span data-ttu-id="9ee12-181">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="9ee12-181">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9ee12-182">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee12-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-183">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="9ee12-183">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-184">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ee12-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-186">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tempo del modello kernel"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="9ee12-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kernel Model Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-187">Tempo in modalità kernel, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="9ee12-187">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="9ee12-188">Se queste informazioni non sono disponibili, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9ee12-188">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="9ee12-189">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ee12-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-190">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9ee12-190">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ee12-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-193">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9ee12-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-194">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="9ee12-194">Label by which the object is known.</span></span> <span data-ttu-id="9ee12-195">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="9ee12-195">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9ee12-196">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee12-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-197">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9ee12-197">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ee12-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-200">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe sistema operativo ")</span><span class="sxs-lookup"><span data-stu-id="9ee12-200">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-201">Nome della classe di creazione dell'ambito del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9ee12-201">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-202">**OSName**</span><span class="sxs-lookup"><span data-stu-id="9ee12-202">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ee12-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-205">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema operativo ")</span><span class="sxs-lookup"><span data-stu-id="9ee12-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-206">Nome dell'ambito del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9ee12-206">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-207">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="9ee12-207">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-208">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ee12-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-210">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Priority")</span><span class="sxs-lookup"><span data-stu-id="9ee12-210">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-211">Urgenza o importanza per l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="9ee12-211">Urgency or importance for process execution.</span></span> <span data-ttu-id="9ee12-212">Se per un processo non è definita una priorità, è necessario utilizzare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9ee12-212">If a priority is not defined for a process, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-213">**Status**</span><span class="sxs-lookup"><span data-stu-id="9ee12-213">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9ee12-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-216">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9ee12-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-217">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9ee12-217">Current status of the object.</span></span>

<span data-ttu-id="9ee12-218">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee12-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9ee12-219">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9ee12-219">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9ee12-220">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9ee12-220">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9ee12-221">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="9ee12-221">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9ee12-222">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="9ee12-222">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ee12-223">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="9ee12-223">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9ee12-224">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="9ee12-224">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9ee12-225">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="9ee12-225">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9ee12-226">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="9ee12-226">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9ee12-227">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="9ee12-227">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9ee12-228">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="9ee12-228">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9ee12-229">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="9ee12-229">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9ee12-230">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="9ee12-230">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9ee12-231">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="9ee12-231">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ee12-232">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="9ee12-232">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-233">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9ee12-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-235">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("data di terminazione")</span><span class="sxs-lookup"><span data-stu-id="9ee12-235">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-236">Ora in cui il processo è stato interrotto o terminato.</span><span class="sxs-lookup"><span data-stu-id="9ee12-236">Time that the process was stopped or terminated.</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-237">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="9ee12-237">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-238">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ee12-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-240">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ora modalità utente"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="9ee12-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("User Mode Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-241">Tempo in modalità utente, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="9ee12-241">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="9ee12-242">Se queste informazioni non sono disponibili, è necessario usare un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9ee12-242">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="9ee12-243">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ee12-243">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9ee12-244">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="9ee12-244">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ee12-245">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ee12-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ee12-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ee12-247">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("working set size"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9ee12-247">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Working Set Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ee12-248">Quantità di memoria, in byte, che un processo deve eseguire in modo efficiente per un sistema operativo che utilizza la gestione della memoria basata su pagine.</span><span class="sxs-lookup"><span data-stu-id="9ee12-248">Amount of memory, in bytes, that a process needs to execute efficiently for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="9ee12-249">Se il sistema non dispone di memoria sufficiente (inferiore alla dimensione working set), si verifica il thrashing.</span><span class="sxs-lookup"><span data-stu-id="9ee12-249">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="9ee12-250">Se la dimensione dell'working set non è nota, utilizzare **null** o 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9ee12-250">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="9ee12-251">Se vengono forniti working set dati, è possibile monitorare le informazioni per comprendere i requisiti di memoria modificabili di un processo.</span><span class="sxs-lookup"><span data-stu-id="9ee12-251">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="9ee12-252">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ee12-252">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ee12-253">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ee12-253">Remarks</span></span>

<span data-ttu-id="9ee12-254">La classe di **\_ processo CIM** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ee12-254">The **CIM\_Process** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="9ee12-255">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="9ee12-255">WMI does not implement this class.</span></span> <span data-ttu-id="9ee12-256">Per le classi WMI derivate dal **\_ processo CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9ee12-256">For WMI classes derived from **CIM\_Process**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9ee12-257">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9ee12-257">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9ee12-258">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9ee12-258">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ee12-259">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ee12-259">Requirements</span></span>



| <span data-ttu-id="9ee12-260">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ee12-260">Requirement</span></span> | <span data-ttu-id="9ee12-261">Valore</span><span class="sxs-lookup"><span data-stu-id="9ee12-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee12-262">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ee12-262">Minimum supported client</span></span><br/> | <span data-ttu-id="9ee12-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ee12-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ee12-264">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ee12-264">Minimum supported server</span></span><br/> | <span data-ttu-id="9ee12-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ee12-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ee12-266">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9ee12-266">Namespace</span></span><br/>                | <span data-ttu-id="9ee12-267">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9ee12-267">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ee12-268">MOF</span><span class="sxs-lookup"><span data-stu-id="9ee12-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ee12-269"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ee12-269"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ee12-270">DLL</span><span class="sxs-lookup"><span data-stu-id="9ee12-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ee12-271"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ee12-271"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ee12-272">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ee12-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee12-273">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="9ee12-273">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

