---
description: Elemento logico che rappresenta un'unità di lavoro da eseguire, ad esempio uno script o un processo di stampa. Un processo è diverso da un processo perché un processo può essere pianificato o accodato e l'esecuzione non è limitata a un singolo sistema.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: Classe CIM_Job (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968028"
---
# <a name="cim_job-class-hyper-v-management"></a><span data-ttu-id="6a1aa-104">Classe CIM_Job (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-104">CIM_Job class (Hyper-V management)</span></span>

<span data-ttu-id="6a1aa-105">Elemento logico che rappresenta un'unità di lavoro da eseguire, ad esempio uno script o un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-105">A logical element that represents a unit of work to execute, such as a script or a print job.</span></span> <span data-ttu-id="6a1aa-106">Un processo è diverso da un processo perché un processo può essere pianificato o accodato e l'esecuzione non è limitata a un singolo sistema.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-106">A job is distinct from a process because a job can be scheduled or queued, and its execution is not limited to a single system.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a1aa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a1aa-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
};
```

## <a name="members"></a><span data-ttu-id="6a1aa-108">Members</span><span class="sxs-lookup"><span data-stu-id="6a1aa-108">Members</span></span>

<span data-ttu-id="6a1aa-109">La classe del **\_ processo CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6a1aa-109">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="6a1aa-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6a1aa-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6a1aa-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6a1aa-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6a1aa-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="6a1aa-112">Methods</span></span>

<span data-ttu-id="6a1aa-113">La classe del **\_ processo CIM** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-113">The **CIM\_Job** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="6a1aa-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="6a1aa-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="6a1aa-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a1aa-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6a1aa-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span><span class="sxs-lookup"><span data-stu-id="6a1aa-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6a1aa-117">Questo metodo è deprecato.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-117">This method is deprecated.</span></span> <span data-ttu-id="6a1aa-118">Usare invece il metodo <strong>RequestStateChange</strong> .</span><span class="sxs-lookup"><span data-stu-id="6a1aa-118">Instead, use the <strong>RequestStateChange</strong> method.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6a1aa-119">Descrizione deprecata: arresta un processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-119">Deprecated description: Shuts down a job.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="6a1aa-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6a1aa-120">Properties</span></span>

<span data-ttu-id="6a1aa-121">La classe del **\_ processo CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-121">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a1aa-122">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-122">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-123">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-125">**True** per eliminare il processo al completamento; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-125">**True** to delete the job upon completion; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="6a1aa-126">Questa proprietà non eliminerà i processi che vengono completati prima che questa proprietà sia impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-126">This property will not delete jobs that complete before this property is set to **True**.</span></span>

 

</dd> <dt>

<span data-ttu-id="6a1aa-127">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-127">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-128">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-130">Durata dell'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-130">The duration for which the job has run.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-131">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-131">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-132">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-134">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**ErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-135">Codice di errore specifico del fornitore che acquisisce le informazioni di elaborazione per i processi ricorrenti.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-135">A vendor-specific error code that captures processing information for recurring jobs.</span></span> <span data-ttu-id="6a1aa-136">Se il processo è stato completato senza errori, il valore deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-136">The value must be set to zero if the job completed without error.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-137">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-137">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-140">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-140">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-141">Stringa in formato libero che contiene una descrizione del codice di errore corrispondente nella proprietà **ErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="6a1aa-141">A free-form string that contains a description of the corresponding error code in the **ErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-142">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-142">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-143">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-145">Il numero di volte in cui eseguire il processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-145">The number of times to run the job.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-146">**Stato processo**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-146">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-149">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-150">Stringa in formato libero che rappresenta lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-150">A free-form string that represents the status of the job.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-151">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-151">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-152">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-154">Indica se le ore nelle proprietà **RunStartInterval** e **UntilTime** rappresentano le ore locali o l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-154">Indicates whether the times in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

<span data-ttu-id="6a1aa-155">**Ora locale** (1)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-155">**Local Time** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

<span data-ttu-id="6a1aa-156">**Ora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-156">**UTC Time** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a1aa-157">**Notificare**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-157">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-159">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-160">Utente a cui inviare una notifica quando un processo viene completato o ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-160">The user to notify when a job completes or fails.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-161">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-161">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-164">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**RecoveryAction**")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-165">Stringa che descrive l'azione di ripristino quando la proprietà **RecoveryAction** è **diversa** ("1").</span><span class="sxs-lookup"><span data-stu-id="6a1aa-165">A string that describes the recovery action when the **RecoveryAction** property is **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-166">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-166">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-169">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OwningJobElement**](cim-owningjobelement.md).")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OwningJobElement**](cim-owningjobelement.md).")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-170">Utente che ha inviato il processo oppure il nome del servizio o del metodo che ha richiesto il processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-170">The user that submitted the Job, or the service or method name that requested the job.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-171">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-171">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-172">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-174">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("percentuale"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **punito** ("percentuale")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-174">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-175">Percentuale del processo completato.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-175">The percentage of the job that is complete.</span></span>

> [!Note]  
> <span data-ttu-id="6a1aa-176">Il valore "101" non è definito e non sarà consentito nella successiva revisione principale della specifica.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-176">The value "101" is undefined and will be not be allowed in the next major revision of the specification.</span></span>

 

</dd> <dt>

<span data-ttu-id="6a1aa-177">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-177">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-178">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-179">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-180">Importanza del processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-180">The importance of the job.</span></span> <span data-ttu-id="6a1aa-181">Più è basso il numero, maggiore sarà la priorità.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-181">The lower the number, the higher the priority.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-182">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-182">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-183">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-185">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**OtherRecoveryAction**")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**OtherRecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-186">Descrive l'azione di ripristino da eseguire in caso di esito negativo di un processo di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-186">Describes the recovery action to take when a run job fails.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6a1aa-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6a1aa-188">Non è noto come azione di ripristino da eseguire.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-188">It is unknown as to what recovery action to take.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6a1aa-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6a1aa-190">L'azione di ripristino verrà specificata nella proprietà **OtherRecoveryAction** .</span><span class="sxs-lookup"><span data-stu-id="6a1aa-190">The recovery action will be specified in the **OtherRecoveryAction** property.</span></span>

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span data-ttu-id="6a1aa-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Non continuare** (2)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a1aa-192">Arrestare l'esecuzione del processo e aggiornarne lo stato in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-192">Stop the execution of the job and appropriately update its status.</span></span>

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span data-ttu-id="6a1aa-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continua con il processo successivo** (3)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6a1aa-194">Continuare con il processo successivo nella coda.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-194">Continue with the next job in the queue.</span></span>

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span data-ttu-id="6a1aa-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Esegui di nuovo il processo** (4)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6a1aa-196">Il processo deve essere eseguito nuovamente.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-196">The job should be re-run.</span></span>

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span data-ttu-id="6a1aa-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Esegui processo di ripristino** (5)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Run Recovery Job** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6a1aa-198">Eseguire il processo associato usando la relazione di **RecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="6a1aa-198">Run the Job associated using the **RecoveryJob** relationship.</span></span> <span data-ttu-id="6a1aa-199">Si noti che il processo di ripristino deve essere già presente nella coda da cui verrà eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-199">Note that the recovery Job must already be in the queue from which it will run.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6a1aa-200">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-200">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-201">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-201">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-202">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-203">Qualificatori: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**RunMonth**","**\_ processo CIM**.**RunDayOfWeek**","**\_ processo CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-203">Qualifiers: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-204">Intero utilizzato in combinazione con la proprietà **RunDayOfWeek** per indicare il giorno in cui il processo viene elaborato; in alternativa, se **RunDayOfWeek** è impostato su zero, **RunDay** indica il giorno del mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-204">An integer that is used on conjunction with the **RunDayOfWeek** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span> <span data-ttu-id="6a1aa-205">Se **RunDay** è un numero intero negativo, specifica un giorno relativo alla fine del mese o, se **RunDay** è un numero intero positivo, specifica un giorno relativo all'inizio del mese.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-205">If **RunDay** is a negative integer, it specifies a day relative to the end of the month, or if **RunDay** is a positive integer, it specifies a day relative to the beginning of the month.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-206">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-206">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-207">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-207">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-208">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-208">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-209">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**RunMonth**","**\_ processo CIM**.**RunDay**","**\_ processo CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-209">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-210">Intero utilizzato in combinazione con la proprietà **RunDay** per indicare il giorno in cui il processo viene elaborato; in alternativa, se **RunDayOfWeek** è impostato su zero, **RunDay** indica il giorno del mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-210">An integer that is used on conjunction with the **RunDay** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span>

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

<span data-ttu-id="6a1aa-211">**-Sabato** (-7)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-211">**-Saturday** (-7)</span></span>


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

<span data-ttu-id="6a1aa-212">**-Venerdì** (-6)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-212">**-Friday** (-6)</span></span>


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

<span data-ttu-id="6a1aa-213">**-Giovedi** (-5)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-213">**-Thursday** (-5)</span></span>


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

<span data-ttu-id="6a1aa-214">**-Mercoledì** (-4)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-214">**-Wednesday** (-4)</span></span>


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

<span data-ttu-id="6a1aa-215">**-Martedì** (-3)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-215">**-Tuesday** (-3)</span></span>


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

<span data-ttu-id="6a1aa-216">**-Lunedì** (-2)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-216">**-Monday** (-2)</span></span>


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

<span data-ttu-id="6a1aa-217">**-Domenica** (-1)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-217">**-Sunday** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

<span data-ttu-id="6a1aa-218">**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-218">**ExactDayOfMonth** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="6a1aa-219">**Domenica** (1)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-219">**Sunday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="6a1aa-220">**Lunedì** (2)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-220">**Monday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="6a1aa-221">**Martedì** (3)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-221">**Tuesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="6a1aa-222">**Mercoledì** (4)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-222">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="6a1aa-223">**Giovedi** (5)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-223">**Thursday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="6a1aa-224">**Venerdì** (6)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-224">**Friday** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="6a1aa-225">**Sabato** (7)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-225">**Saturday** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a1aa-226">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-226">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-227">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-227">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-228">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-229">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**RunDay**","**\_ processo CIM**.**RunDayOfWeek**","**\_ processo CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-229">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-230">Mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-230">The month when the job is processed.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="6a1aa-231">**Gennaio** (0)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-231">**January** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="6a1aa-232">**Febbraio** (1)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-232">**February** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="6a1aa-233">**Marzo** (2)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-233">**March** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="6a1aa-234">**Aprile** (3)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-234">**April** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="6a1aa-235">**Maggio** (4)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-235">**May** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="6a1aa-236">**Giugno** (5)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-236">**June** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="6a1aa-237">**Luglio** (6)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-237">**July** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="6a1aa-238">**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-238">**August** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="6a1aa-239">**Settembre** (8)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-239">**September** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="6a1aa-240">**Ottobre** (9)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-240">**October** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="6a1aa-241">**Novembre** (10)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-241">**November** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="6a1aa-242">**Dicembre** (11)</span><span class="sxs-lookup"><span data-stu-id="6a1aa-242">**December** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a1aa-243">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-243">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-244">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-244">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-245">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-246">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**RunMonth**","**\_ processo CIM**.**RunDay**","**\_ processo CIM**.**RunDayOfWeek**","**\_ processo CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-246">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-247">Intervallo di tempo dopo la mezzanotte di elaborazione del processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-247">The time interval after midnight when the job is be processed.</span></span> <span data-ttu-id="6a1aa-248">Ad esempio, "00000000020000.000000:000" indica che il processo viene eseguito in data o dopo due ore o ora locale o ora UTC (UTC viene specificato con la proprietà **LocalOrUtcTime** ).</span><span class="sxs-lookup"><span data-stu-id="6a1aa-248">For example, "00000000020000.000000:000" indicates that the job is be run on or after two o'clock local time, or UTC time (UTC is specified with the **LocalOrUtcTime** property).</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-249">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-249">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-250">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-251">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-251">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-252">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ processo CIM**.**RunMonth**","**\_ processo CIM**.**RunDay**","**\_ processo CIM**.**RunDayOfWeek**","**\_ processo CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-252">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="6a1aa-253">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-253">This property is deprecated.</span></span> <span data-ttu-id="6a1aa-254">È invece consigliabile usare le proprietà **RunMonth**, **RunDay**, **RunDayOfWeek** e **RunStartInterval** .</span><span class="sxs-lookup"><span data-stu-id="6a1aa-254">Instead we recommend that you use the **RunMonth**, **RunDay**, **RunDayOfWeek**, and **RunStartInterval** properties.</span></span>

 

<span data-ttu-id="6a1aa-255">Ora pianificata per l'avvio del processo corrente.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-255">The time when the current job is scheduled to start.</span></span> <span data-ttu-id="6a1aa-256">Questa ora può essere rappresentata da una data e un'ora oppure da un intervallo relativo all'ora in cui la proprietà viene richiesta.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-256">This time can be represented by a date and time, or an interval relative to the time when the property is requested.</span></span> <span data-ttu-id="6a1aa-257">Un valore di tutti gli zeri indica che il processo è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-257">A value of all zeroes indicates that the job is already executing.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-258">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-258">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-259">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-261">Ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-261">The time when the job started.</span></span> <span data-ttu-id="6a1aa-262">Questa ora può essere rappresentata da una data e un'ora o da un intervallo relativo all'ora in cui è richiesta la proprietà.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-262">This time can be represented by a date and time, or by an interval relative to the time when the property is requested.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-263">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-263">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-264">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-264">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-266">Ora di invio del processo.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-266">The time when the job was submitted.</span></span> <span data-ttu-id="6a1aa-267">Un valore di tutti gli zeri indica che l'elemento padre non è in grado di segnalare una data e un'ora.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-267">A value of all zeroes indicates that the parent element is not capable of reporting a date and time.</span></span>

</dd> <dt>

<span data-ttu-id="6a1aa-268">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-268">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a1aa-269">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-270">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6a1aa-270">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6a1aa-271">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**LocalOrUtcTime**")</span><span class="sxs-lookup"><span data-stu-id="6a1aa-271">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**LocalOrUtcTime**")</span></span>
</dt> </dl>

<span data-ttu-id="6a1aa-272">Tempo trascorso il quale il processo diventa non valido o deve essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-272">The time after which the job becomes invalid or should be stopped.</span></span> <span data-ttu-id="6a1aa-273">L'ora può essere rappresentata da una data e un'ora o da un intervallo relativo all'ora in cui questa proprietà è richiesta.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-273">The time can be represented by a date and time, or by an interval relative to the time when this property is requested.</span></span> <span data-ttu-id="6a1aa-274">Un valore di tutte le nove indica che il processo può essere eseguito A tempo indefinito.</span><span class="sxs-lookup"><span data-stu-id="6a1aa-274">A value of all nines indicates that the job can run indefinitely.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a1aa-275">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a1aa-275">Requirements</span></span>



| <span data-ttu-id="6a1aa-276">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a1aa-276">Requirement</span></span> | <span data-ttu-id="6a1aa-277">Valore</span><span class="sxs-lookup"><span data-stu-id="6a1aa-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1aa-278">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a1aa-278">Minimum supported client</span></span><br/> | <span data-ttu-id="6a1aa-279">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a1aa-279">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6a1aa-280">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a1aa-280">Minimum supported server</span></span><br/> | <span data-ttu-id="6a1aa-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a1aa-281">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6a1aa-282">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a1aa-282">Namespace</span></span><br/>                | <span data-ttu-id="6a1aa-283">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6a1aa-283">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6a1aa-284">MOF</span><span class="sxs-lookup"><span data-stu-id="6a1aa-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a1aa-285"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a1aa-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a1aa-286">DLL</span><span class="sxs-lookup"><span data-stu-id="6a1aa-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a1aa-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a1aa-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6a1aa-288">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a1aa-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1aa-289">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="6a1aa-289">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

