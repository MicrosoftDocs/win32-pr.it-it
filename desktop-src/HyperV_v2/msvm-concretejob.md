---
description: Rappresenta un'unità di lavoro e viene utilizzata per tenere traccia dello stato di avanzamento delle operazioni asincrone.
ms.assetid: 33c13880-92a4-4367-8f0b-ecdf38b2ff8e
title: Classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob
- Msvm_ConcreteJob.KillJob
- Msvm_ConcreteJob.InstanceID
- Msvm_ConcreteJob.Caption
- Msvm_ConcreteJob.Description
- Msvm_ConcreteJob.ElementName
- Msvm_ConcreteJob.InstallDate
- Msvm_ConcreteJob.Name
- Msvm_ConcreteJob.OperationalStatus
- Msvm_ConcreteJob.StatusDescriptions
- Msvm_ConcreteJob.Status
- Msvm_ConcreteJob.HealthState
- Msvm_ConcreteJob.CommunicationStatus
- Msvm_ConcreteJob.DetailedStatus
- Msvm_ConcreteJob.OperatingStatus
- Msvm_ConcreteJob.PrimaryStatus
- Msvm_ConcreteJob.JobStatus
- Msvm_ConcreteJob.TimeSubmitted
- Msvm_ConcreteJob.ScheduledStartTime
- Msvm_ConcreteJob.StartTime
- Msvm_ConcreteJob.ElapsedTime
- Msvm_ConcreteJob.JobRunTimes
- Msvm_ConcreteJob.RunMonth
- Msvm_ConcreteJob.RunDay
- Msvm_ConcreteJob.RunDayOfWeek
- Msvm_ConcreteJob.RunStartInterval
- Msvm_ConcreteJob.LocalOrUtcTime
- Msvm_ConcreteJob.UntilTime
- Msvm_ConcreteJob.Notify
- Msvm_ConcreteJob.Owner
- Msvm_ConcreteJob.Priority
- Msvm_ConcreteJob.PercentComplete
- Msvm_ConcreteJob.DeleteOnCompletion
- Msvm_ConcreteJob.ErrorCode
- Msvm_ConcreteJob.ErrorDescription
- Msvm_ConcreteJob.ErrorSummaryDescription
- Msvm_ConcreteJob.RecoveryAction
- Msvm_ConcreteJob.OtherRecoveryAction
- Msvm_ConcreteJob.JobState
- Msvm_ConcreteJob.TimeOfLastStateChange
- Msvm_ConcreteJob.TimeBeforeRemoval
- Msvm_ConcreteJob.Cancellable
- Msvm_ConcreteJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2cff9594bfd39cf365020a1da8ae2f1ec0aea562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314341"
---
# <a name="msvm_concretejob-class"></a><span data-ttu-id="84f81-103">\_Classe MSVM ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="84f81-103">Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="84f81-104">Versione concreta di un processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-104">A concrete version of job.</span></span> <span data-ttu-id="84f81-105">Questa classe rappresenta un'unità di lavoro generica e di cui è possibile creare un'istanza, ad esempio un batch o un processo di stampa, ed è utilizzata in modo specifico in Hyper-V per tenere traccia dello stato di avanzamento delle operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="84f81-105">This class represents a generic and instantiatable unit of work, such as a batch or a print job, and is specifically used in Hyper-V to track the progress of asynchronous operations.</span></span>

<span data-ttu-id="84f81-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="84f81-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f81-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84f81-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
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
  string   ErrorSummaryDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 
                00000000000500.000000:000
              ;
  boolean  Cancellable;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="84f81-108">Members</span><span class="sxs-lookup"><span data-stu-id="84f81-108">Members</span></span>

<span data-ttu-id="84f81-109">La **classe \_ ConcreteJob di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="84f81-109">The **Msvm\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="84f81-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="84f81-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="84f81-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84f81-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="84f81-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="84f81-112">Methods</span></span>

<span data-ttu-id="84f81-113">La **classe \_ ConcreteJob di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="84f81-113">The **Msvm\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="84f81-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="84f81-114">Method</span></span>                                                            | <span data-ttu-id="84f81-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84f81-115">Description</span></span>                                                                      |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="84f81-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="84f81-116">**GetError**</span></span>](geterror-msvm-concretejob.md)                     | <span data-ttu-id="84f81-117">Recupera l'oggetto errore per il processo, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="84f81-117">Retrieves the error object for the job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="84f81-118">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="84f81-118">**GetErrorEx**</span></span>](geterrorex-msvm-concretejob.md)                 | <span data-ttu-id="84f81-119">Recupera gli oggetti Error per il processo, se presenti.</span><span class="sxs-lookup"><span data-stu-id="84f81-119">Retrieves the error objects for the job, if any exist.</span></span><br/>                |
| <span data-ttu-id="84f81-120">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="84f81-120">**KillJob**</span></span>                                                       | <span data-ttu-id="84f81-121">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="84f81-121">This method is not supported.</span></span><br/>                                         |
| [<span data-ttu-id="84f81-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="84f81-122">**RequestStateChange**</span></span>](requeststatechange-msvm-concretejob.md) | <span data-ttu-id="84f81-123">Richiede che lo stato del processo venga modificato nello stato specificato.</span><span class="sxs-lookup"><span data-stu-id="84f81-123">Requests that the state of the job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="84f81-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84f81-124">Properties</span></span>

<span data-ttu-id="84f81-125">La **classe \_ ConcreteJob di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="84f81-125">The **Msvm\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84f81-126">**Annullabili**</span><span class="sxs-lookup"><span data-stu-id="84f81-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-127">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="84f81-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-129">Indica se il processo può essere annullato.</span><span class="sxs-lookup"><span data-stu-id="84f81-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="84f81-130">Il valore di questa proprietà non garantisce che una richiesta di annullamento del processo avrà esito positivo.</span><span class="sxs-lookup"><span data-stu-id="84f81-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="84f81-131">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="84f81-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-134">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84f81-134">A short description of the object.</span></span> <span data-ttu-id="84f81-135">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="84f81-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-136">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="84f81-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-137">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-139">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="84f81-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="84f81-140">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="84f81-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f81-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f81-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-142">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="84f81-142">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-143">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="84f81-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-145">Specifica se il processo deve essere eliminato automaticamente al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="84f81-145">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="84f81-146">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-146">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-147">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="84f81-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-150">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="84f81-150">A description of the object.</span></span> <span data-ttu-id="84f81-151">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="84f81-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-152">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="84f81-152">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-153">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-155">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="84f81-155">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="84f81-156">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="84f81-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f81-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f81-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-158">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-158">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-159">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-161">Intervallo di tempo durante il quale il processo è stato eseguito o il tempo di esecuzione totale se il processo è stato completato.</span><span class="sxs-lookup"><span data-stu-id="84f81-161">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="84f81-162">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-162">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="84f81-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-166">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84f81-166">A display name for the object.</span></span> <span data-ttu-id="84f81-167">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="84f81-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-168">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="84f81-168">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-169">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-171">Codice di errore specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="84f81-171">A vendor-specific error code.</span></span> <span data-ttu-id="84f81-172">Se il processo è stato completato senza errori, il valore deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="84f81-172">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="84f81-173">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-173">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-174">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="84f81-174">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-177">Stringa che contiene la descrizione dell'errore del fornitore.</span><span class="sxs-lookup"><span data-stu-id="84f81-177">A string that contains the vendor error description.</span></span> <span data-ttu-id="84f81-178">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-178">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-179">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="84f81-179">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f81-182">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="84f81-182">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="84f81-183">Descrizione di riepilogo dell'errore, se presente.</span><span class="sxs-lookup"><span data-stu-id="84f81-183">A summary description of the error, if present.</span></span> <span data-ttu-id="84f81-184">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-184">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-185">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="84f81-185">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-186">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-188">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="84f81-188">The current health of the element.</span></span> <span data-ttu-id="84f81-189">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="84f81-189">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="84f81-190">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="84f81-190">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="84f81-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5.</span><span class="sxs-lookup"><span data-stu-id="84f81-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="84f81-192">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="84f81-192">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-193">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-195">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84f81-195">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="84f81-196">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f81-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="84f81-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f81-200">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="84f81-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="84f81-201">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="84f81-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="84f81-202">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="84f81-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f81-203">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="84f81-203">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-204">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84f81-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-206">Il numero di volte in cui il processo deve essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="84f81-206">The number of times that the job should be run.</span></span> <span data-ttu-id="84f81-207">Il valore 1 indica che il processo non è ricorrente, mentre un valore diverso da zero indica un limite al numero di volte che il processo ricorrerà.</span><span class="sxs-lookup"><span data-stu-id="84f81-207">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="84f81-208">Zero indica che non esiste alcun limite per il numero di volte in cui il processo può essere elaborato, ma verrà terminato dopo il raggiungimento di **UntilTime** o se il processo viene terminato manualmente.</span><span class="sxs-lookup"><span data-stu-id="84f81-208">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="84f81-209">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-209">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-210">**JobState**</span><span class="sxs-lookup"><span data-stu-id="84f81-210">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-211">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-213">**JobState** è un'enumerazione Integer che indica lo stato operativo di un processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-213">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="84f81-214">Può inoltre indicare transizioni tra questi Stati, ad esempio, "chiusura in corso" e "avvio".</span><span class="sxs-lookup"><span data-stu-id="84f81-214">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="84f81-215">Questa proprietà viene ereditata da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="84f81-215">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="84f81-216">Valore</span><span class="sxs-lookup"><span data-stu-id="84f81-216">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="84f81-217">Significato</span><span class="sxs-lookup"><span data-stu-id="84f81-217">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="84f81-218"><dt>**Nuovo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-218"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="84f81-219">Il processo non è mai stato avviato.</span><span class="sxs-lookup"><span data-stu-id="84f81-219">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="84f81-220"><dt>**A partire**</dt> da <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-220"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="84f81-221">Il processo viene spostato dagli stati 2 (nuovo), 5 (sospeso) o 11 (servizio) nello stato 4 (in esecuzione).</span><span class="sxs-lookup"><span data-stu-id="84f81-221">The job is moving from the 2 (New), 5 (Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                   |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="84f81-222"><dt>**Esecuzione**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-222"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="84f81-223">Il processo è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="84f81-223">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="84f81-224"><dt>**Sospeso**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-224"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="84f81-225">Il processo è stato interrotto, ma può essere riavviato in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="84f81-225">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="84f81-226"><dt>**Chiusura**</dt> di <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-226"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="84f81-227">Il processo viene spostato in uno stato 7 (completato), 8 (terminato) o 9 (terminato).</span><span class="sxs-lookup"><span data-stu-id="84f81-227">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="84f81-228"><dt>**Completato**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-228"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="84f81-229">Il processo è stato completato normalmente.</span><span class="sxs-lookup"><span data-stu-id="84f81-229">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="84f81-230"><dt>**Terminato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-230"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="84f81-231">Il processo è stato interrotto da una richiesta di modifica dello stato "Terminate".</span><span class="sxs-lookup"><span data-stu-id="84f81-231">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="84f81-232">Il processo e tutti i processi sottostanti sono terminati e possono essere riavviati solo come nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-232">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="84f81-233">Il requisito che il processo venga riavviato solo come nuovo processo è specifico del processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-233">The requirement that the job be restarted only as a new job is job-specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="84f81-234"><dt>**Ucciso**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-234"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="84f81-235">Il processo è stato interrotto da una richiesta di modifica dello stato "Kill".</span><span class="sxs-lookup"><span data-stu-id="84f81-235">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="84f81-236">È possibile che i processi sottostanti siano ancora in esecuzione e che sia necessario eseguire una pulizia per liberare risorse.</span><span class="sxs-lookup"><span data-stu-id="84f81-236">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="84f81-237"><dt>**Eccezione**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-237"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="84f81-238">Il processo è in uno stato anomalo che potrebbe essere indicativo di una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="84f81-238">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="84f81-239">Lo stato effettivo del processo potrebbe essere disponibile tramite oggetti specifici del processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-239">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="84f81-240"><dt>**Servizio**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-240"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="84f81-241">Il processo è in uno stato specifico del fornitore che supporta l'individuazione o la risoluzione dei problemi o entrambi.</span><span class="sxs-lookup"><span data-stu-id="84f81-241">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="84f81-242"><dt>**DMTF riservato**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-242"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="84f81-243">Riservato.</span><span class="sxs-lookup"><span data-stu-id="84f81-243">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="84f81-244"><dt>**Fornitore riservato**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-244"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="84f81-245">Riservato.</span><span class="sxs-lookup"><span data-stu-id="84f81-245">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="84f81-246">**Stato processo**</span><span class="sxs-lookup"><span data-stu-id="84f81-246">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-249">Stringa che rappresenta lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-249">A string that represents the job status.</span></span> <span data-ttu-id="84f81-250">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-250">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-251">**JobType**</span><span class="sxs-lookup"><span data-stu-id="84f81-251">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-252">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-254">Indica il tipo di processo rilevato da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="84f81-254">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84f81-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="84f81-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Definisci macchina virtuale** (1)</span><span class="sxs-lookup"><span data-stu-id="84f81-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Define Virtual Machine** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modificare la macchina virtuale** (2)</span><span class="sxs-lookup"><span data-stu-id="84f81-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modify Virtual Machine** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Elimina macchina virtuale** (3)</span><span class="sxs-lookup"><span data-stu-id="84f81-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Destroy Virtual Machine** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>

<span data-ttu-id="84f81-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modificare le impostazioni del servizio di gestione** (4)</span><span class="sxs-lookup"><span data-stu-id="84f81-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modify Management Service Settings** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Inizializza macchina virtuale** (10)</span><span class="sxs-lookup"><span data-stu-id="84f81-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Initialize Virtual Machine** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**In attesa di avvio della macchina virtuale** (11)</span><span class="sxs-lookup"><span data-stu-id="84f81-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**Waiting to Start Virtual Machine** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Avvia macchina virtuale** (12)</span><span class="sxs-lookup"><span data-stu-id="84f81-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Start Virtual Machine** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>Spegnere la **macchina virtuale** (13)</span><span class="sxs-lookup"><span data-stu-id="84f81-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Power Off Virtual Machine** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Salva macchina virtuale** (14)</span><span class="sxs-lookup"><span data-stu-id="84f81-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Save Virtual Machine** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Ripristina macchina virtuale** (15)</span><span class="sxs-lookup"><span data-stu-id="84f81-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Restore Virtual Machine** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Arresta macchina virtuale** (16)</span><span class="sxs-lookup"><span data-stu-id="84f81-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Shut Down Virtual Machine** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Sospendi macchina virtuale** (26)</span><span class="sxs-lookup"><span data-stu-id="84f81-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Pause Virtual Machine** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Riprendi macchina virtuale** (27)</span><span class="sxs-lookup"><span data-stu-id="84f81-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Resume Virtual Machine** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Reimposta macchina virtuale** (28)</span><span class="sxs-lookup"><span data-stu-id="84f81-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Reset Virtual Machine** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Riavvia macchina virtuale** (29)</span><span class="sxs-lookup"><span data-stu-id="84f81-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Reboot Virtual Machine** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="84f81-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Aggiungi risorse macchina virtuale** (30)</span><span class="sxs-lookup"><span data-stu-id="84f81-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Add Virtual Machine Resources** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="84f81-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modificare le risorse della macchina virtuale** (31)</span><span class="sxs-lookup"><span data-stu-id="84f81-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modify Virtual Machine Resources** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="84f81-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Rimuovere le risorse della macchina virtuale** (32)</span><span class="sxs-lookup"><span data-stu-id="84f81-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Remove Virtual Machine Resources** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>

<span data-ttu-id="84f81-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Richiedi memoria della macchina virtuale iniziale** (40)</span><span class="sxs-lookup"><span data-stu-id="84f81-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Request Initial Virtual Machine Memory** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Aggiungi memoria alla macchina virtuale** (41)</span><span class="sxs-lookup"><span data-stu-id="84f81-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Add Memory to Virtual Machine** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Rimuovi memoria dalla macchina virtuale** (42)</span><span class="sxs-lookup"><span data-stu-id="84f81-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Remove Memory from Virtual Machine** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>

<span data-ttu-id="84f81-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Unione di dischi VHD** (50)</span><span class="sxs-lookup"><span data-stu-id="84f81-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Merging VHD Disks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Crea snapshot VSS all'interno della macchina virtuale** (51)</span><span class="sxs-lookup"><span data-stu-id="84f81-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Create VSS Snapshot inside Virtual Machine** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>

<span data-ttu-id="84f81-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Ottenere i dati delle impostazioni di importazione** (60)</span><span class="sxs-lookup"><span data-stu-id="84f81-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Get Import Setting Data** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Importa macchina virtuale** (61)</span><span class="sxs-lookup"><span data-stu-id="84f81-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Import Virtual Machine** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Esporta macchina virtuale** (62)</span><span class="sxs-lookup"><span data-stu-id="84f81-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Export Virtual Machine** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>

<span data-ttu-id="84f81-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Configurazione registrazione** (63)</span><span class="sxs-lookup"><span data-stu-id="84f81-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Register Configuration** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>

<span data-ttu-id="84f81-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Annulla registrazione configurazione** (64)</span><span class="sxs-lookup"><span data-stu-id="84f81-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Unregister Configuration** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Macchina virtuale snapshot** (70)</span><span class="sxs-lookup"><span data-stu-id="84f81-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Snapshot Virtual Machine** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="84f81-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Applica snapshot macchina virtuale** (71)</span><span class="sxs-lookup"><span data-stu-id="84f81-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Apply Virtual Machine Snapshot** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="84f81-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Elimina snapshot macchina virtuale** (72)</span><span class="sxs-lookup"><span data-stu-id="84f81-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Delete Virtual Machine Snapshot** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>

<span data-ttu-id="84f81-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Cancella stato snapshot macchina virtuale** (73)</span><span class="sxs-lookup"><span data-stu-id="84f81-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Clear Virtual Machine Snapshot State** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>

<span data-ttu-id="84f81-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Aggiungere risorse al pool di risorse** (80)</span><span class="sxs-lookup"><span data-stu-id="84f81-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Add Resources to Resource Pool** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>

<span data-ttu-id="84f81-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Rimuovere le risorse dal pool di risorse** (81)</span><span class="sxs-lookup"><span data-stu-id="84f81-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Remove Resources from Resource Pool** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>

<span data-ttu-id="84f81-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modificare le impostazioni del server di replica** (90)</span><span class="sxs-lookup"><span data-stu-id="84f81-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modify Replication Server Settings** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="84f81-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Creazione relazione di replica** (91)</span><span class="sxs-lookup"><span data-stu-id="84f81-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Create Replication Relationship** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>

<span data-ttu-id="84f81-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modificare le impostazioni delle relazioni di replica** (92)</span><span class="sxs-lookup"><span data-stu-id="84f81-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modify Replication Relationship Settings** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="84f81-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Rimuovere la relazione di replica** (93)</span><span class="sxs-lookup"><span data-stu-id="84f81-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Remove Replication Relationship** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>

<span data-ttu-id="84f81-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Avviare la replica iniziale inband** (94)</span><span class="sxs-lookup"><span data-stu-id="84f81-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Start Inband Initial Replication** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>

<span data-ttu-id="84f81-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Importazione replica** (95)</span><span class="sxs-lookup"><span data-stu-id="84f81-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Import Replication** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>

<span data-ttu-id="84f81-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Modifica stato replica** (96)</span><span class="sxs-lookup"><span data-stu-id="84f81-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Replicate State Change** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>

<span data-ttu-id="84f81-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Avviare il failover** (97)</span><span class="sxs-lookup"><span data-stu-id="84f81-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Initiate Failover** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>

<span data-ttu-id="84f81-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Ripristino del failover** (98)</span><span class="sxs-lookup"><span data-stu-id="84f81-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Revert Failover** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>

<span data-ttu-id="84f81-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Failover di commit** (99)</span><span class="sxs-lookup"><span data-stu-id="84f81-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Commit Failover** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>

<span data-ttu-id="84f81-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Replica Inititate sincronizzata** (100)</span><span class="sxs-lookup"><span data-stu-id="84f81-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Inititate Synced Replication** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>

<span data-ttu-id="84f81-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Annulla replica sincronizzata** (101)</span><span class="sxs-lookup"><span data-stu-id="84f81-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Cancel Synced Replication** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>

<span data-ttu-id="84f81-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Avviare la replica di test** (102)</span><span class="sxs-lookup"><span data-stu-id="84f81-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Initiate Test Replica** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>

<span data-ttu-id="84f81-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Rimuovere la replica di test** (103)</span><span class="sxs-lookup"><span data-stu-id="84f81-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Remove Test Replica** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>

<span data-ttu-id="84f81-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Replica inversa** (104)</span><span class="sxs-lookup"><span data-stu-id="84f81-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Reverse Replication** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>

<span data-ttu-id="84f81-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Delta di invio della replica** (105)</span><span class="sxs-lookup"><span data-stu-id="84f81-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Replication Sending Delta** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>

<span data-ttu-id="84f81-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Delta di ricezione della replica** (106)</span><span class="sxs-lookup"><span data-stu-id="84f81-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Replication Receiving Delta** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="84f81-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Risincronizzazione** (107)</span><span class="sxs-lookup"><span data-stu-id="84f81-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>

<span data-ttu-id="84f81-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Applica log modifiche** (108)</span><span class="sxs-lookup"><span data-stu-id="84f81-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Apply change log** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>

<span data-ttu-id="84f81-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Arrestare la replica iniziale** (109)</span><span class="sxs-lookup"><span data-stu-id="84f81-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Stop Initial Replication** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>

<span data-ttu-id="84f81-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Interrompi risincronizzazione** (110)</span><span class="sxs-lookup"><span data-stu-id="84f81-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Stop Resynchronizing** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>

<span data-ttu-id="84f81-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Ottenere le statistiche di replica** (111)</span><span class="sxs-lookup"><span data-stu-id="84f81-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Get Replica statistics** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="84f81-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Prepara per verifica coerenza** (112)</span><span class="sxs-lookup"><span data-stu-id="84f81-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Prepare for Consistency Checker** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>

<span data-ttu-id="84f81-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Verifica coerenza** (113)</span><span class="sxs-lookup"><span data-stu-id="84f81-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Consistency Checker** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="84f81-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Arresta verifica coerenza** (114)</span><span class="sxs-lookup"><span data-stu-id="84f81-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Stop Consistency Checker** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>

<span data-ttu-id="84f81-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Test della connessione di replica** (115)</span><span class="sxs-lookup"><span data-stu-id="84f81-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Test Replication Connection** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>

<span data-ttu-id="84f81-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Invio della replica iniziale** (116)</span><span class="sxs-lookup"><span data-stu-id="84f81-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Sending Initial Replica** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>

<span data-ttu-id="84f81-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Avviare la risincronizzazione iniziale della replica** (117)</span><span class="sxs-lookup"><span data-stu-id="84f81-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Start Resync Initial Replication** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>

<span data-ttu-id="84f81-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Avviare l'esportazione della replica iniziale** (118)</span><span class="sxs-lookup"><span data-stu-id="84f81-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Start Export Initial Replication** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>

<span data-ttu-id="84f81-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Reimposta statistiche replica** (119)</span><span class="sxs-lookup"><span data-stu-id="84f81-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Reset Replica Statistics** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>

<span data-ttu-id="84f81-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Applica Delta registrati** (120)</span><span class="sxs-lookup"><span data-stu-id="84f81-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Apply Registered Deltas** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>

<span data-ttu-id="84f81-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Risincronizzazione della replica estesa** (121)</span><span class="sxs-lookup"><span data-stu-id="84f81-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Resynchronizing Extended Replication** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>

<span data-ttu-id="84f81-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Lettura della configurazione della replica di test** (122)</span><span class="sxs-lookup"><span data-stu-id="84f81-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Reading Test Replica Configuration** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>

<span data-ttu-id="84f81-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Impostare la modalità di replica su Primary** (123)</span><span class="sxs-lookup"><span data-stu-id="84f81-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Change the replication mode to primary** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>

<span data-ttu-id="84f81-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Avvio del failback** (124)</span><span class="sxs-lookup"><span data-stu-id="84f81-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Initiate Failback** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>

<span data-ttu-id="84f81-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Aggiornamento del set di dischi** (125)</span><span class="sxs-lookup"><span data-stu-id="84f81-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Update Disk Set** (125)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-326">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-326">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>

<span data-ttu-id="84f81-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Definisci switch Ethernet** (130)</span><span class="sxs-lookup"><span data-stu-id="84f81-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Define Ethernet Switch** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>

<span data-ttu-id="84f81-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modificare le impostazioni del Comcambio Ethernet** (131)</span><span class="sxs-lookup"><span data-stu-id="84f81-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modify Ethernet Switch Settings** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>

<span data-ttu-id="84f81-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Switch Ethernet Destroy** (132)</span><span class="sxs-lookup"><span data-stu-id="84f81-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Destroy Ethernet Switch** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="84f81-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Aggiungi risorse switch Ethernet** (133)</span><span class="sxs-lookup"><span data-stu-id="84f81-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Add Ethernet Switch Resources** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="84f81-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modifica risorse Commuti Ethernet** (134)</span><span class="sxs-lookup"><span data-stu-id="84f81-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modify Ethernet Switch Resources** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="84f81-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Rimuovi risorse commute Ethernet** (135)</span><span class="sxs-lookup"><span data-stu-id="84f81-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Remove Ethernet Switch Resources** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Convalida macchina virtuale pianificata** (140)</span><span class="sxs-lookup"><span data-stu-id="84f81-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Validate Planned Virtual Machine** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Realizzazione della macchina virtuale** (141)</span><span class="sxs-lookup"><span data-stu-id="84f81-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Realizing Virtual Machine** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>

<span data-ttu-id="84f81-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Creazione di un pool di risorse** (150)</span><span class="sxs-lookup"><span data-stu-id="84f81-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Creating a Resource Pool** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="84f81-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Modifica delle risorse padre di un pool di risorse** (151)</span><span class="sxs-lookup"><span data-stu-id="84f81-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Changing the Parent Resources of a Resource Pool** (151)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="84f81-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Modifica delle impostazioni non alloction di un pool di risorse** (152)</span><span class="sxs-lookup"><span data-stu-id="84f81-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Changing the Non-alloction Settings of a Resource Pool** (152)</span></span>


</dt> <dd></dd> <dt>

<span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>

<span data-ttu-id="84f81-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Eliminazione di un pool di risorse** (153)</span><span class="sxs-lookup"><span data-stu-id="84f81-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Deleting a Resource Pool** (153)</span></span>


</dt> <dd></dd> <dt>

<span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="84f81-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Abilita GPU RemoteFx** (160)</span><span class="sxs-lookup"><span data-stu-id="84f81-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Enable RemoteFx GPU** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="84f81-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Disabilitare GPU RemoteFx** (161)</span><span class="sxs-lookup"><span data-stu-id="84f81-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Disable RemoteFx GPU** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>

<span data-ttu-id="84f81-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modificare le impostazioni del servizio 3D** (162)</span><span class="sxs-lookup"><span data-stu-id="84f81-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modify 3D Service Settings** (162)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-342">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-342">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>

<span data-ttu-id="84f81-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Macchina virtuale di backup** (170)</span><span class="sxs-lookup"><span data-stu-id="84f81-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Backup Virtual Machine** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>

<span data-ttu-id="84f81-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Interfaccia del servizio Guest** (180)</span><span class="sxs-lookup"><span data-stu-id="84f81-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Guest Service Interface** (180)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-345">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-345">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>

<span data-ttu-id="84f81-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Informazioni sul cluster guest di query** (181)</span><span class="sxs-lookup"><span data-stu-id="84f81-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Query Guest Cluster Information** (181)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-347">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-347">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>

<span data-ttu-id="84f81-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Definisci raccolta** (190)</span><span class="sxs-lookup"><span data-stu-id="84f81-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Define Collection** (190)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-349">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-349">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>

<span data-ttu-id="84f81-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Elimina raccolta** (191)</span><span class="sxs-lookup"><span data-stu-id="84f81-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Destroy Collection** (191)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-351">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-351">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>

<span data-ttu-id="84f81-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Rinomina raccolta** (192)</span><span class="sxs-lookup"><span data-stu-id="84f81-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Rename Collection** (192)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-353">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-353">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>

<span data-ttu-id="84f81-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Aggiungere un membro alla raccolta** (193)</span><span class="sxs-lookup"><span data-stu-id="84f81-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Add Member to Collection** (193)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-355">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-355">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>

<span data-ttu-id="84f81-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Rimuovi membro dalla raccolta** (194)</span><span class="sxs-lookup"><span data-stu-id="84f81-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Remove Member from Collection** (194)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-357">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-357">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>

<span data-ttu-id="84f81-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Aggiungi impostazione alla raccolta** (195)</span><span class="sxs-lookup"><span data-stu-id="84f81-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Add Setting to Collection** (195)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-359">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-359">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>

<span data-ttu-id="84f81-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Rimuovi impostazione dalla raccolta** (196)</span><span class="sxs-lookup"><span data-stu-id="84f81-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Remove Setting from Collection** (196)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-361">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-361">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>

<span data-ttu-id="84f81-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modifica impostazione sulla raccolta** (197)</span><span class="sxs-lookup"><span data-stu-id="84f81-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modify Setting on Collection** (197)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-363">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-363">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>

<span data-ttu-id="84f81-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Raccolta snapshot** (198)</span><span class="sxs-lookup"><span data-stu-id="84f81-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Snapshot Collection** (198)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-365">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-365">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>

<span data-ttu-id="84f81-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Converti snapshot in punto di riferimento** (200)</span><span class="sxs-lookup"><span data-stu-id="84f81-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Convert Snapshot to Reference Point** (200)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-367">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-367">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>

<span data-ttu-id="84f81-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Crea punto di riferimento** (201)</span><span class="sxs-lookup"><span data-stu-id="84f81-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Create Reference Point** (201)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-369">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-369">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>

<span data-ttu-id="84f81-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Elimina punto di riferimento** (202)</span><span class="sxs-lookup"><span data-stu-id="84f81-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Delete Reference Point** (202)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-371">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-371">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>

<span data-ttu-id="84f81-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Esporta punto di riferimento** (203)</span><span class="sxs-lookup"><span data-stu-id="84f81-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Export Reference Point** (203)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-373">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-373">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>

<span data-ttu-id="84f81-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Rimuovere i dati associati dal punto di riferimento** (204)</span><span class="sxs-lookup"><span data-stu-id="84f81-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Remove Associated Data from Reference Point** (204)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-375">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-375">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="84f81-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Crea punto di riferimento sulla raccolta** (205)</span><span class="sxs-lookup"><span data-stu-id="84f81-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Create Reference Point on Collection** (205)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-377">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-377">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="84f81-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Esporta punto di riferimento nella raccolta** (206)</span><span class="sxs-lookup"><span data-stu-id="84f81-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Export Reference Point on Collection** (206)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-379">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-379">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="84f81-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Rimuovere i dati associati dal punto di riferimento nella raccolta** (207)</span><span class="sxs-lookup"><span data-stu-id="84f81-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Remove Associated Data from Reference Point on Collection** (207)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-381">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-381">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="84f81-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Elimina punto di riferimento nella raccolta** (208)</span><span class="sxs-lookup"><span data-stu-id="84f81-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Delete Reference Point on Collection** (208)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-383">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-383">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>

<span data-ttu-id="84f81-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Importa metadati dei punti di riferimento** (209)</span><span class="sxs-lookup"><span data-stu-id="84f81-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Import Reference Point metadata** (209)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-385">Valore aggiunto in Windows 10 come **punto di riferimento della pulizia**.</span><span class="sxs-lookup"><span data-stu-id="84f81-385">Value added in Windows 10 as **Cleanup Reference Point**.</span></span>

 

</dd> <dt>

<span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>

<span data-ttu-id="84f81-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Montaggio o smontaggio del dispositivo assegnabile** (260)</span><span class="sxs-lookup"><span data-stu-id="84f81-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Mount or Dismount Assignable Device** (260)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84f81-387">Valore aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84f81-387">Value added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="84f81-388">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-388">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-389">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-391">Indica se le ore rappresentate nelle proprietà **RunStartInterval** e **UntilTime** rappresentano le ore locali o l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="84f81-391">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="84f81-392">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="84f81-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Ora locale** (1)</span><span class="sxs-lookup"><span data-stu-id="84f81-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Ora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="84f81-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f81-395">**Nome**</span><span class="sxs-lookup"><span data-stu-id="84f81-395">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-396">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f81-398">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="84f81-398">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="84f81-399">Nome visualizzato per questa istanza di un processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-399">The display name for this instance of a job.</span></span> <span data-ttu-id="84f81-400">Inoltre, il nome visualizzato può essere utilizzato come proprietà per una ricerca o una query.</span><span class="sxs-lookup"><span data-stu-id="84f81-400">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="84f81-401">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f81-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-402">**Notificare**</span><span class="sxs-lookup"><span data-stu-id="84f81-402">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-403">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-405">Utente che riceve una notifica al completamento o all'esito negativo del processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-405">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="84f81-406">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-406">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-407">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="84f81-407">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-408">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-410">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="84f81-410">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="84f81-411">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="84f81-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f81-412">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f81-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="84f81-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-414">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="84f81-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-416">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84f81-416">The current statuses of the object.</span></span> <span data-ttu-id="84f81-417">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="84f81-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-418">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="84f81-418">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-419">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-420">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-421">Stringa che descrive l'azione di ripristino quando la proprietà **RecoveryAction** dell'istanza è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="84f81-421">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="84f81-422">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-422">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-423">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="84f81-423">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-424">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-426">Utente che ha inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-426">The user who submitted the job.</span></span> <span data-ttu-id="84f81-427">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-427">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-428">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="84f81-428">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-429">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f81-431">Qualificatori: **MinValue** (0), **MaxValue** (100), **unità** ("percentuale")</span><span class="sxs-lookup"><span data-stu-id="84f81-431">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="84f81-432">Percentuale di completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-432">The completion percentage of the job.</span></span> <span data-ttu-id="84f81-433">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-433">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-434">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="84f81-434">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-435">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-436">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-437">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="84f81-437">Provides high level status information.</span></span> <span data-ttu-id="84f81-438">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="84f81-438">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="84f81-439">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="84f81-439">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f81-440">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f81-440">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-441">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="84f81-441">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-442">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84f81-442">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-443">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-444">Importanza dell'esecuzione di un processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-444">The importance of a job's execution.</span></span> <span data-ttu-id="84f81-445">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-445">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-446">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="84f81-446">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-447">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f81-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-448">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-449">Descrive l'azione di ripristino da intraprendere per un processo che non è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="84f81-449">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="84f81-450">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-450">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="84f81-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="84f81-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="84f81-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Non continuare** (2)</span><span class="sxs-lookup"><span data-stu-id="84f81-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continua con il processo successivo** (3)</span><span class="sxs-lookup"><span data-stu-id="84f81-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Esegui di nuovo il processo** (4)</span><span class="sxs-lookup"><span data-stu-id="84f81-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Esegui processo di ripristino** (5)</span><span class="sxs-lookup"><span data-stu-id="84f81-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f81-457">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="84f81-457">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-458">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="84f81-458">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-459">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f81-460">Qualificatori: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="84f81-460">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="84f81-461">Giorno del mese in cui deve essere elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-461">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="84f81-462">Sono disponibili diverse interpretazioni per questa proprietà, a seconda del valore di **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="84f81-462">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="84f81-463">Quando **RunDayOfWeek** è 0 e **RunDay** è un valore positivo, **RunDay** definisce il giorno del mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-463">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="84f81-464">Ad esempio, se **RunDayOfWeek** è 0 e **RunDay** è 12, il processo verrà elaborato <sup>il giorno 12</sup> del mese.</span><span class="sxs-lookup"><span data-stu-id="84f81-464">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="84f81-465">Quando **RunDayOfWeek** è 0 e **RunDay** è negativo, **RunDay** definisce il numero di giorni prima dell'ultimo giorno del mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-465">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="84f81-466">1 indica l'ultimo giorno del mese, 2 indica un giorno prima dell'ultimo giorno del mese e così via.</span><span class="sxs-lookup"><span data-stu-id="84f81-466">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="84f81-467">Se, ad esempio, **RunDayOfWeek** è 0 e **RunDay** è 1, il processo verrà elaborato l'ultimo giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="84f81-467">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="84f81-468">Quando **RunDayOfWeek** è diverso da 0, **RunDayOfWeek** è il giorno della settimana in cui verrà elaborato il processo, relativo a **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="84f81-468">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="84f81-469">Se, ad esempio, **RunDay** è 15 e **RunDayOfWeek** è 7 (+ sabato), il processo verrà elaborato il primo sabato il o dopo il 15 <sup>°</sup> giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="84f81-469">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="84f81-470">Se **RunDay** è 20 e **RunDayOfWeek** è 7 (sabato), il processo verrà elaborato il primo sabato il o prima del 20 <sup>°</sup> giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="84f81-470">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="84f81-471">Se **RunDay** è 1 e **RunDayOfWeek** è 1 (domenica), il processo verrà elaborato l'ultima domenica del mese.</span><span class="sxs-lookup"><span data-stu-id="84f81-471">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="84f81-472">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-472">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-473">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="84f81-473">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-474">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="84f81-474">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-476">Intero positivo o negativo utilizzato insieme a **RunDay** per indicare il giorno della settimana o il mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-476">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="84f81-477">Per ulteriori informazioni, vedere la descrizione della proprietà **RunDay** .</span><span class="sxs-lookup"><span data-stu-id="84f81-477">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="84f81-478">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-478">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="84f81-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Sabato** (7)</span><span class="sxs-lookup"><span data-stu-id="84f81-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Venerdì** (6)</span><span class="sxs-lookup"><span data-stu-id="84f81-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Giovedi** (5)</span><span class="sxs-lookup"><span data-stu-id="84f81-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mercoledì** (4)</span><span class="sxs-lookup"><span data-stu-id="84f81-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Martedì** (3)</span><span class="sxs-lookup"><span data-stu-id="84f81-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Lunedì** (2)</span><span class="sxs-lookup"><span data-stu-id="84f81-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Domenica** (1)</span><span class="sxs-lookup"><span data-stu-id="84f81-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="84f81-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domenica** (1)</span><span class="sxs-lookup"><span data-stu-id="84f81-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lunedì** (2)</span><span class="sxs-lookup"><span data-stu-id="84f81-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Martedì** (3)</span><span class="sxs-lookup"><span data-stu-id="84f81-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mercoledì** (4)</span><span class="sxs-lookup"><span data-stu-id="84f81-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Giovedi** (5)</span><span class="sxs-lookup"><span data-stu-id="84f81-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Venerdì** (6)</span><span class="sxs-lookup"><span data-stu-id="84f81-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sabato** (7)</span><span class="sxs-lookup"><span data-stu-id="84f81-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f81-494">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="84f81-494">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-495">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="84f81-495">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-496">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-497">Mese durante il quale deve essere elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-497">The month during which the job should be processed.</span></span> <span data-ttu-id="84f81-498">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-498">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="84f81-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Gennaio** (0)</span><span class="sxs-lookup"><span data-stu-id="84f81-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Febbraio** (1)</span><span class="sxs-lookup"><span data-stu-id="84f81-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Marzo** (2)</span><span class="sxs-lookup"><span data-stu-id="84f81-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Aprile** (3)</span><span class="sxs-lookup"><span data-stu-id="84f81-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Maggio** (4)</span><span class="sxs-lookup"><span data-stu-id="84f81-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Giugno** (5)</span><span class="sxs-lookup"><span data-stu-id="84f81-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Luglio** (6)</span><span class="sxs-lookup"><span data-stu-id="84f81-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="84f81-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Settembre** (8)</span><span class="sxs-lookup"><span data-stu-id="84f81-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Ottobre** (9)</span><span class="sxs-lookup"><span data-stu-id="84f81-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembre** (10)</span><span class="sxs-lookup"><span data-stu-id="84f81-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="84f81-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dicembre** (11)</span><span class="sxs-lookup"><span data-stu-id="84f81-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f81-511">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="84f81-511">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-512">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-512">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-513">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-514">Intervallo di tempo dopo la mezzanotte di elaborazione del processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-514">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="84f81-515">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-515">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-516">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-516">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-517">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-517">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-518">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-519">Ora di inizio pianificata per il processo, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="84f81-519">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="84f81-520">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-520">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-521">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-521">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-522">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-522">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-523">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-524">Ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-524">The time that the job began.</span></span> <span data-ttu-id="84f81-525">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-525">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-526">**Status**</span><span class="sxs-lookup"><span data-stu-id="84f81-526">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-527">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f81-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-528">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-528">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-529">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="84f81-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84f81-530">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="84f81-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-531">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="84f81-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="84f81-532">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-533">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="84f81-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="84f81-534">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="84f81-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="84f81-535">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="84f81-535">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-536">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-536">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-537">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-538">Quantità di tempo, in minuti, durante la quale il processo viene mantenuto dopo il completamento dell'esecuzione, ovvero esito positivo o negativo dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="84f81-538">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="84f81-539">Il processo deve rimanere in esistenza per un certo periodo di tempo indipendentemente dal valore della proprietà **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="84f81-539">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="84f81-540">Il valore predefinito è 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="84f81-540">The default is five minutes.</span></span> <span data-ttu-id="84f81-541">Questa proprietà viene ereditata da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))ed è sempre impostata su 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="84f81-541">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="84f81-542">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="84f81-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-543">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-544">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-545">Data o ora dell'Ultima modifica apportata allo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-545">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="84f81-546">Se lo stato del processo non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo 0.</span><span class="sxs-lookup"><span data-stu-id="84f81-546">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="84f81-547">Se una modifica dello stato è stata richiesta ma rifiutata o non ancora elaborata, la proprietà non deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="84f81-547">If a state change was requested but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="84f81-548">Questa proprietà viene ereditata da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="84f81-548">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-549">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="84f81-549">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-550">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-550">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-551">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-551">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-552">Ora di invio del processo.</span><span class="sxs-lookup"><span data-stu-id="84f81-552">The time that the job was submitted.</span></span> <span data-ttu-id="84f81-553">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-553">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="84f81-554">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-554">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f81-555">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f81-555">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f81-556">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f81-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f81-557">L'ora in cui il processo non è valido o deve essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="84f81-557">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="84f81-558">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="84f81-558">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84f81-559">Commenti</span><span class="sxs-lookup"><span data-stu-id="84f81-559">Remarks</span></span>

<span data-ttu-id="84f81-560">L'accesso alla **classe \_ ConcreteJob di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="84f81-560">Access to the **Msvm\_ConcreteJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="84f81-561">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="84f81-561">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="84f81-562">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84f81-562">Requirements</span></span>



| <span data-ttu-id="84f81-563">Requisito</span><span class="sxs-lookup"><span data-stu-id="84f81-563">Requirement</span></span> | <span data-ttu-id="84f81-564">Valore</span><span class="sxs-lookup"><span data-stu-id="84f81-564">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f81-565">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84f81-565">Minimum supported client</span></span><br/> | <span data-ttu-id="84f81-566">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="84f81-566">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="84f81-567">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84f81-567">Minimum supported server</span></span><br/> | <span data-ttu-id="84f81-568">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="84f81-568">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84f81-569">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="84f81-569">Namespace</span></span><br/>                | <span data-ttu-id="84f81-570">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="84f81-570">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="84f81-571">MOF</span><span class="sxs-lookup"><span data-stu-id="84f81-571">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84f81-572"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-572"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84f81-573">DLL</span><span class="sxs-lookup"><span data-stu-id="84f81-573">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f81-574"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84f81-574"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84f81-575">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84f81-575">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f81-576">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="84f81-576">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="84f81-577">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84f81-577">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="84f81-578">Classi di gestione del sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="84f81-578">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

