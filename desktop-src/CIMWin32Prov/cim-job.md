---
description: La \_ classe del processo CIM rappresenta un'unità di lavoro per un sistema, ad esempio un processo di stampa. Un processo è diverso da un processo perché è possibile pianificare un processo.
ms.assetid: a689230e-2a62-4f0d-9961-9bbc055d3c6e
ms.tgt_platform: multiple
title: Classe CIM_Job (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.Caption
- CIM_Job.Description
- CIM_Job.InstallDate
- CIM_Job.Name
- CIM_Job.Status
- CIM_Job.ElapsedTime
- CIM_Job.JobStatus
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.StartTime
- CIM_Job.TimeSubmitted
- CIM_Job.UntilTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd527474309802a4c6d2315d8a9e61b6733e70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126955"
---
# <a name="cim_job-class-cimwin32-wmi-providers"></a><span data-ttu-id="e7de2-104">Classe CIM_Job (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="e7de2-104">CIM_Job class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e7de2-105">La classe del **\_ processo CIM** rappresenta un'unità di lavoro per un sistema, ad esempio un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="e7de2-105">The **CIM\_Job** class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="e7de2-106">Un processo è diverso da un processo perché è possibile pianificare un processo.</span><span class="sxs-lookup"><span data-stu-id="e7de2-106">A job is distinct from a process because a job can be scheduled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7de2-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="e7de2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e7de2-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e7de2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e7de2-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e7de2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e7de2-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e7de2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7de2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7de2-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C564-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
};
```

## <a name="members"></a><span data-ttu-id="e7de2-112">Members</span><span class="sxs-lookup"><span data-stu-id="e7de2-112">Members</span></span>

<span data-ttu-id="e7de2-113">La classe del **\_ processo CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e7de2-113">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="e7de2-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7de2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7de2-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7de2-115">Properties</span></span>

<span data-ttu-id="e7de2-116">La classe del **\_ processo CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e7de2-116">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7de2-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e7de2-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7de2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e7de2-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-121">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e7de2-121">A short textual description of the object.</span></span>

<span data-ttu-id="e7de2-122">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e7de2-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7de2-123">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e7de2-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7de2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-126">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e7de2-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-127">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e7de2-127">A textual description of the object.</span></span>

<span data-ttu-id="e7de2-128">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e7de2-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7de2-129">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="e7de2-129">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-130">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e7de2-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-132">Periodo di tempo durante il quale il processo è stato eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7de2-132">Length of time the job has been executing.</span></span>

</dd> <dt>

<span data-ttu-id="e7de2-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e7de2-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-134">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e7de2-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-136">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="e7de2-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-137">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="e7de2-137">Indicates when the object was installed.</span></span> <span data-ttu-id="e7de2-138">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="e7de2-138">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e7de2-139">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e7de2-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7de2-140">**Stato processo**</span><span class="sxs-lookup"><span data-stu-id="e7de2-140">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7de2-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-143">Stringa in formato libero che rappresenta lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="e7de2-143">Free-form string that represents the job status.</span></span>

</dd> <dt>

<span data-ttu-id="e7de2-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e7de2-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7de2-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-147">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e7de2-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-148">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="e7de2-148">Label by which the object is known.</span></span> <span data-ttu-id="e7de2-149">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="e7de2-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e7de2-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e7de2-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7de2-151">**Notificare**</span><span class="sxs-lookup"><span data-stu-id="e7de2-151">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7de2-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-154">L'utente riceve una notifica al completamento o all'esito negativo del processo.</span><span class="sxs-lookup"><span data-stu-id="e7de2-154">User is notified upon job completion or failure.</span></span>

</dd> <dt>

<span data-ttu-id="e7de2-155">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="e7de2-155">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7de2-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-158">Utente che ha inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="e7de2-158">User who submitted the job.</span></span>

</dd> <dt>

<span data-ttu-id="e7de2-159">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="e7de2-159">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-160">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7de2-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-162">Importanza dell'esecuzione di un processo.</span><span class="sxs-lookup"><span data-stu-id="e7de2-162">Importance of a job's execution.</span></span>

</dd> <dt>

<span data-ttu-id="e7de2-163">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="e7de2-163">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-164">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e7de2-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-166">Ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="e7de2-166">Time that the job began.</span></span>

</dd> <dt>

<span data-ttu-id="e7de2-167">**Status**</span><span class="sxs-lookup"><span data-stu-id="e7de2-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7de2-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-170">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e7de2-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-171">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e7de2-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="e7de2-172">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="e7de2-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e7de2-173">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="e7de2-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e7de2-174">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="e7de2-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e7de2-175">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="e7de2-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e7de2-176">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="e7de2-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e7de2-177">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="e7de2-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e7de2-178">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e7de2-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e7de2-179">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7de2-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e7de2-180">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e7de2-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e7de2-181">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="e7de2-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e7de2-182">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="e7de2-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e7de2-183">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="e7de2-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e7de2-184">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="e7de2-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e7de2-185">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="e7de2-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e7de2-186">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="e7de2-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e7de2-187">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="e7de2-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e7de2-188">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="e7de2-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e7de2-189">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="e7de2-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e7de2-190">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="e7de2-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e7de2-191">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="e7de2-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e7de2-192">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="e7de2-192">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-193">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e7de2-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-195">Ora di invio del processo.</span><span class="sxs-lookup"><span data-stu-id="e7de2-195">Time that the job was submitted.</span></span>

</dd> <dt>

<span data-ttu-id="e7de2-196">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="e7de2-196">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7de2-197">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e7de2-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e7de2-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7de2-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7de2-199">Ora in cui il processo non è valido o deve essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="e7de2-199">Time at which the job is invalid or should be stopped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7de2-200">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7de2-200">Remarks</span></span>

<span data-ttu-id="e7de2-201">La classe del **\_ processo CIM** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e7de2-201">The **CIM\_Job** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="e7de2-202">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="e7de2-202">WMI does not implement this class.</span></span> <span data-ttu-id="e7de2-203">Per le classi derivate dal **\_ processo CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e7de2-203">For classes derived from **CIM\_Job**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e7de2-204">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="e7de2-204">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e7de2-205">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="e7de2-205">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7de2-206">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7de2-206">Requirements</span></span>



| <span data-ttu-id="e7de2-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7de2-207">Requirement</span></span> | <span data-ttu-id="e7de2-208">Valore</span><span class="sxs-lookup"><span data-stu-id="e7de2-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7de2-209">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7de2-209">Minimum supported client</span></span><br/> | <span data-ttu-id="e7de2-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7de2-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7de2-211">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7de2-211">Minimum supported server</span></span><br/> | <span data-ttu-id="e7de2-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7de2-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7de2-213">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e7de2-213">Namespace</span></span><br/>                | <span data-ttu-id="e7de2-214">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e7de2-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e7de2-215">MOF</span><span class="sxs-lookup"><span data-stu-id="e7de2-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7de2-216"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7de2-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7de2-217">DLL</span><span class="sxs-lookup"><span data-stu-id="e7de2-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7de2-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7de2-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7de2-219">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7de2-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7de2-220">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="e7de2-220">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

