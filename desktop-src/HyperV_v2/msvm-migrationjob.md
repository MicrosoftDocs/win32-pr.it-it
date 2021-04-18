---
description: Questa classe rappresenta un processo dell'operazione di migrazione creato per la migrazione dell'archiviazione o del sistema virtuale da parte del servizio di migrazione del sistema virtuale.
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddecf34148e3ef07dc78af9b4f2dd45950644cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310011"
---
# <a name="msvm_migrationjob-class"></a><span data-ttu-id="793f9-103">\_Classe MSVM MigrationJob</span><span class="sxs-lookup"><span data-stu-id="793f9-103">Msvm\_MigrationJob class</span></span>

<span data-ttu-id="793f9-104">Questa classe rappresenta un processo dell'operazione di migrazione creato per la migrazione dell'archiviazione o del sistema virtuale da parte del servizio di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="793f9-104">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span>

<span data-ttu-id="793f9-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="793f9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="793f9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="793f9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
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
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="793f9-107">Members</span><span class="sxs-lookup"><span data-stu-id="793f9-107">Members</span></span>

<span data-ttu-id="793f9-108">La **classe \_ MigrationJob di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="793f9-108">The **Msvm\_MigrationJob** class has these types of members:</span></span>

-   [<span data-ttu-id="793f9-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="793f9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="793f9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="793f9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="793f9-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="793f9-111">Methods</span></span>

<span data-ttu-id="793f9-112">La **classe \_ MigrationJob di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="793f9-112">The **Msvm\_MigrationJob** class has these methods.</span></span>



| <span data-ttu-id="793f9-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="793f9-113">Method</span></span>                                                             | <span data-ttu-id="793f9-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="793f9-114">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="793f9-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="793f9-115">**GetError**</span></span>](geterror-msvm-migrationjob.md)                     | <span data-ttu-id="793f9-116">Recupera l'oggetto errore per il processo di migrazione, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="793f9-116">Retrieves the error object for the migration job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="793f9-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="793f9-117">**GetErrorEx**</span></span>](geterrorex-msvm-migrationjob.md)                 | <span data-ttu-id="793f9-118">Recupera gli oggetti errore per il processo di migrazione, se presenti.</span><span class="sxs-lookup"><span data-stu-id="793f9-118">Retrieves the error objects for the migration job, if any exist.</span></span><br/>                |
| <span data-ttu-id="793f9-119">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="793f9-119">**KillJob**</span></span>                                                        | <span data-ttu-id="793f9-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="793f9-120">This method is not supported.</span></span><br/>                                                   |
| [<span data-ttu-id="793f9-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="793f9-121">**RequestStateChange**</span></span>](requeststatechange-msvm-migrationjob.md) | <span data-ttu-id="793f9-122">Richiede che lo stato del processo di migrazione venga modificato nello stato specificato.</span><span class="sxs-lookup"><span data-stu-id="793f9-122">Requests that the state of the migration job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="793f9-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="793f9-123">Properties</span></span>

<span data-ttu-id="793f9-124">La **classe \_ MigrationJob di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="793f9-124">The **Msvm\_MigrationJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="793f9-125">**Annullabili**</span><span class="sxs-lookup"><span data-stu-id="793f9-125">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-126">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="793f9-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-128">Indica se il processo può essere annullato.</span><span class="sxs-lookup"><span data-stu-id="793f9-128">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="793f9-129">Il valore di questa proprietà non garantisce che una richiesta di annullamento del processo avrà esito positivo.</span><span class="sxs-lookup"><span data-stu-id="793f9-129">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="793f9-130">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="793f9-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-133">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="793f9-133">A short description of the object.</span></span> <span data-ttu-id="793f9-134">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="793f9-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-135">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="793f9-135">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-136">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-138">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="793f9-138">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="793f9-139">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="793f9-139">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="793f9-140">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="793f9-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-141">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="793f9-141">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-142">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="793f9-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-144">Specifica se il processo deve essere eliminato automaticamente al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="793f9-144">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="793f9-145">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-145">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-146">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="793f9-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-149">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="793f9-149">A description of the object.</span></span> <span data-ttu-id="793f9-150">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="793f9-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-151">**DestinationHost**</span><span class="sxs-lookup"><span data-stu-id="793f9-151">**DestinationHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-154">Nome host della piattaforma di virtualizzazione di destinazione in cui viene eseguita la migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="793f9-154">The hostname of the destination virtualization platform that the virtual system is migrating to.</span></span> <span data-ttu-id="793f9-155">Questa operazione sarà **null** per la migrazione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="793f9-155">This will be **Null** for storage migration.</span></span>

</dd> <dt>

<span data-ttu-id="793f9-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="793f9-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-157">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-159">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="793f9-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="793f9-160">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="793f9-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="793f9-161">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="793f9-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-162">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-163">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-165">Intervallo di tempo durante il quale il processo è stato eseguito o il tempo di esecuzione totale se il processo è stato completato.</span><span class="sxs-lookup"><span data-stu-id="793f9-165">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="793f9-166">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="793f9-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-170">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="793f9-170">A display name for the object.</span></span> <span data-ttu-id="793f9-171">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="793f9-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="793f9-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-173">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-175">Codice di errore specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="793f9-175">A vendor-specific error code.</span></span> <span data-ttu-id="793f9-176">Se il processo è stato completato senza errori, il valore deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="793f9-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="793f9-177">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="793f9-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-181">Stringa che contiene la descrizione dell'errore del fornitore.</span><span class="sxs-lookup"><span data-stu-id="793f9-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="793f9-182">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="793f9-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="793f9-186">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="793f9-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="793f9-187">Descrizione di riepilogo dell'errore, se presente.</span><span class="sxs-lookup"><span data-stu-id="793f9-187">A summary description of the error, if present.</span></span>

</dd> <dt>

<span data-ttu-id="793f9-188">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="793f9-188">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-189">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-191">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="793f9-191">The current health of the element.</span></span> <span data-ttu-id="793f9-192">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="793f9-192">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="793f9-193">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="793f9-193">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="793f9-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5.</span><span class="sxs-lookup"><span data-stu-id="793f9-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="793f9-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="793f9-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-196">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-198">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="793f9-198">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="793f9-199">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="793f9-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-200">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="793f9-200">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="793f9-203">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="793f9-203">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="793f9-204">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="793f9-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="793f9-205">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="793f9-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="793f9-206">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="793f9-206">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-207">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="793f9-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-209">Il numero di volte in cui il processo deve essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="793f9-209">The number of times that the job should be run.</span></span> <span data-ttu-id="793f9-210">Il valore 1 indica che il processo non è ricorrente, mentre un valore diverso da zero indica un limite al numero di volte che il processo ricorrerà.</span><span class="sxs-lookup"><span data-stu-id="793f9-210">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="793f9-211">Zero indica che non esiste alcun limite per il numero di volte in cui il processo può essere elaborato, ma verrà terminato dopo il raggiungimento di **UntilTime** o se il processo viene terminato manualmente.</span><span class="sxs-lookup"><span data-stu-id="793f9-211">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="793f9-212">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-212">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-213">**JobState**</span><span class="sxs-lookup"><span data-stu-id="793f9-213">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-214">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-216">**JobState** è un'enumerazione Integer che indica lo stato operativo di un processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-216">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="793f9-217">Può inoltre indicare transizioni tra questi Stati, ad esempio, "chiusura in corso" e "avvio".</span><span class="sxs-lookup"><span data-stu-id="793f9-217">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="793f9-218">Questa proprietà viene ereditata da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="793f9-218">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="793f9-219">Valore</span><span class="sxs-lookup"><span data-stu-id="793f9-219">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="793f9-220">Significato</span><span class="sxs-lookup"><span data-stu-id="793f9-220">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="793f9-221"><dt>**Nuovo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-221"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="793f9-222">Il processo non è mai stato avviato.</span><span class="sxs-lookup"><span data-stu-id="793f9-222">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="793f9-223"><dt>**A partire**</dt> da <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-223"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="793f9-224">Il processo viene spostato dagli stati 2 (nuovo), 5 (sospeso) o 11 (servizio) nello stato 4 (in esecuzione).</span><span class="sxs-lookup"><span data-stu-id="793f9-224">The job is moving from the 2 (New), 5(Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="793f9-225"><dt>**Esecuzione**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-225"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="793f9-226">Il processo è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="793f9-226">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="793f9-227"><dt>**Sospeso**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-227"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="793f9-228">Il processo è stato interrotto, ma può essere riavviato in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="793f9-228">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="793f9-229"><dt>**Chiusura**</dt> di <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-229"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="793f9-230">Il processo viene spostato in uno stato 7 (completato), 8 (terminato) o 9 (terminato).</span><span class="sxs-lookup"><span data-stu-id="793f9-230">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="793f9-231"><dt>**Completato**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-231"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="793f9-232">Il processo è stato completato normalmente.</span><span class="sxs-lookup"><span data-stu-id="793f9-232">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="793f9-233"><dt>**Terminato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-233"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="793f9-234">Il processo è stato interrotto da una richiesta di modifica dello stato "Terminate".</span><span class="sxs-lookup"><span data-stu-id="793f9-234">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="793f9-235">Il processo e tutti i processi sottostanti sono terminati e possono essere riavviati solo come nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-235">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="793f9-236">Il requisito che il processo venga riavviato solo come nuovo processo è specifico del processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-236">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="793f9-237"><dt>**Ucciso**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-237"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="793f9-238">Il processo è stato interrotto da una richiesta di modifica dello stato "Kill".</span><span class="sxs-lookup"><span data-stu-id="793f9-238">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="793f9-239">È possibile che i processi sottostanti siano ancora in esecuzione e che sia necessario eseguire una pulizia per liberare risorse.</span><span class="sxs-lookup"><span data-stu-id="793f9-239">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="793f9-240"><dt>**Eccezione**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-240"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="793f9-241">Il processo è in uno stato anomalo che potrebbe essere indicativo di una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="793f9-241">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="793f9-242">Lo stato effettivo del processo potrebbe essere disponibile tramite oggetti specifici del processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-242">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="793f9-243"><dt>**Servizio**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-243"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="793f9-244">Il processo è in uno stato specifico del fornitore che supporta l'individuazione o la risoluzione dei problemi o entrambi.</span><span class="sxs-lookup"><span data-stu-id="793f9-244">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="793f9-245"><dt>**DMTF riservato**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-245"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="793f9-246">Riservato.</span><span class="sxs-lookup"><span data-stu-id="793f9-246">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="793f9-247"><dt>**Fornitore riservato**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-247"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="793f9-248">Riservato.</span><span class="sxs-lookup"><span data-stu-id="793f9-248">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="793f9-249">**Stato processo**</span><span class="sxs-lookup"><span data-stu-id="793f9-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-250">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-252">Stringa che rappresenta lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-252">A string that represents the job status.</span></span> <span data-ttu-id="793f9-253">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-253">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-254">**JobType**</span><span class="sxs-lookup"><span data-stu-id="793f9-254">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-255">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-257">Indica il tipo di processo rilevato da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="793f9-257">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="793f9-258">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="793f9-258">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="793f9-259">**Creazione della macchina virtuale remota** (300)</span><span class="sxs-lookup"><span data-stu-id="793f9-259">**Creating Remote Virtual Machine** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

<span data-ttu-id="793f9-260">**Verifica della compatibilità della macchina virtuale** (301)</span><span class="sxs-lookup"><span data-stu-id="793f9-260">**Checking Virtual Machine Compatibility** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="793f9-261">**Verifica della compatibilità della macchina virtuale e dello spazio di archiviazione** (302)</span><span class="sxs-lookup"><span data-stu-id="793f9-261">**Checking Virtual Machine and Storage Compatibility** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="793f9-262">**Verifica della compatibilità di archiviazione** (303)</span><span class="sxs-lookup"><span data-stu-id="793f9-262">**Checking Storage Compatibility** (303)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

<span data-ttu-id="793f9-263">**Verifica della migrazione dell'archiviazione** (304)</span><span class="sxs-lookup"><span data-stu-id="793f9-263">**Checking Storage Migration** (304)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="793f9-264">**Trasferimento della macchina virtuale** (305)</span><span class="sxs-lookup"><span data-stu-id="793f9-264">**Moving Virtual Machine** (305)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

<span data-ttu-id="793f9-265">**Trasferimento di macchine virtuali e archiviazione** (306)</span><span class="sxs-lookup"><span data-stu-id="793f9-265">**Moving Virtual Machine and Storage** (306)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

<span data-ttu-id="793f9-266">**Trasferimento dello spazio di archiviazione** (307)</span><span class="sxs-lookup"><span data-stu-id="793f9-266">**Moving Storage** (307)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="793f9-267">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-267">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-268">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-270">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-270">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<span data-ttu-id="793f9-271">Indica se le ore rappresentate nelle proprietà **RunStartInterval** e **UntilTime** rappresentano le ore locali o l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="793f9-271">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dl> <dt>

<span data-ttu-id="793f9-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Ora locale** (1)</span><span class="sxs-lookup"><span data-stu-id="793f9-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Ora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="793f9-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="793f9-274">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="793f9-274">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-275">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="793f9-277">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")</span><span class="sxs-lookup"><span data-stu-id="793f9-277">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")</span></span>
</dt> </dl>

<span data-ttu-id="793f9-278">Tipo di migrazione rappresentato da questo oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-278">The migration type represented by this job object.</span></span> <span data-ttu-id="793f9-279">Si tratta di uno dei valori definiti per la proprietà **MigrationType** della classe [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="793f9-279">This will be one of the values defined for the **MigrationType** property of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="793f9-280">**Nome**</span><span class="sxs-lookup"><span data-stu-id="793f9-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-281">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="793f9-283">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="793f9-283">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="793f9-284">Nome visualizzato per questa istanza di un processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-284">The display name for this instance of a job.</span></span> <span data-ttu-id="793f9-285">Inoltre, il nome visualizzato può essere utilizzato come proprietà per una ricerca o una query.</span><span class="sxs-lookup"><span data-stu-id="793f9-285">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="793f9-286">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="793f9-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-287">**NewResourceSettingData**</span><span class="sxs-lookup"><span data-stu-id="793f9-287">**NewResourceSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-288">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="793f9-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="793f9-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-290">Per una migrazione in tempo reale, questo valore sarà sempre impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="793f9-290">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="793f9-291">Per una migrazione dell'archiviazione, se il **valore è null**, non verrà spostato alcun disco rigido virtuale (VHD) della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="793f9-291">For a storage migration, if this is **Null**, none of the virtual machine's virtual hard disks (VHDs) will be moved.</span></span> <span data-ttu-id="793f9-292">In caso contrario, conterrà una matrice di istanze incorporate della classe [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) che rappresentano i VHD da spostare.</span><span class="sxs-lookup"><span data-stu-id="793f9-292">Otherwise, this will contain an array of embedded instances of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class that represent the VHDs to be moved.</span></span> <span data-ttu-id="793f9-293">Nella proprietà di **connessione** di queste istanze viene specificato il percorso di destinazione del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="793f9-293">The **Connection** property of these instances will specify the destination location of the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="793f9-294">**NewSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="793f9-294">**NewSystemSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-295">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-297">Per una migrazione in tempo reale, questo valore sarà sempre impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="793f9-297">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="793f9-298">Per una migrazione dell'archiviazione, se è **null**, le radici dei dati della macchina virtuale non vengono spostate.</span><span class="sxs-lookup"><span data-stu-id="793f9-298">For a storage migration, if this is **Null**, the virtual machine's data roots are not moving.</span></span> <span data-ttu-id="793f9-299">In caso contrario, conterrà un'istanza incorporata della classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) , in cui le proprietà **ExternalDataRoot**, **SnapshotDataRoot** e **SwapFileDataRoot** specificano le nuove radici di dati.</span><span class="sxs-lookup"><span data-stu-id="793f9-299">Otherwise, this will contain an embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class, where the **ExternalDataRoot**, **SnapshotDataRoot**, and **SwapFileDataRoot** properties will specify the new data roots.</span></span>

</dd> <dt>

<span data-ttu-id="793f9-300">**Notificare**</span><span class="sxs-lookup"><span data-stu-id="793f9-300">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-303">Utente che riceve una notifica al completamento o all'esito negativo del processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-303">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="793f9-304">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-304">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-305">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="793f9-305">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-306">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-308">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="793f9-308">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="793f9-309">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="793f9-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="793f9-310">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="793f9-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="793f9-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-312">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="793f9-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-314">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="793f9-314">The current statuses of the object.</span></span> <span data-ttu-id="793f9-315">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="793f9-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-316">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="793f9-316">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-319">Stringa che descrive l'azione di ripristino quando la proprietà **RecoveryAction** dell'istanza è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="793f9-319">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="793f9-320">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-320">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-321">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="793f9-321">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-324">Utente che ha inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-324">The user who submitted the job.</span></span> <span data-ttu-id="793f9-325">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-325">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-326">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="793f9-326">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-327">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="793f9-329">Qualificatori: **MinValue** (0), **MaxValue** (100), **unità** ("percentuale")</span><span class="sxs-lookup"><span data-stu-id="793f9-329">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="793f9-330">Percentuale di completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-330">The completion percentage of the job.</span></span> <span data-ttu-id="793f9-331">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-331">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-332">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="793f9-332">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-333">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-333">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-335">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="793f9-335">Provides high level status information.</span></span> <span data-ttu-id="793f9-336">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="793f9-336">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="793f9-337">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="793f9-337">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="793f9-338">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="793f9-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-339">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="793f9-339">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-340">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="793f9-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-342">Importanza dell'esecuzione di un processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-342">The importance of a job's execution.</span></span> <span data-ttu-id="793f9-343">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-343">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-344">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="793f9-344">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-345">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="793f9-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-347">Descrive l'azione di ripristino da eseguire per un processo non riuscito.</span><span class="sxs-lookup"><span data-stu-id="793f9-347">Describes the recovery action to be taken for an unsuccessfully run job.</span></span> <span data-ttu-id="793f9-348">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-348">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="793f9-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="793f9-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="793f9-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Non continuare** (2)</span><span class="sxs-lookup"><span data-stu-id="793f9-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continua con il processo successivo** (3)</span><span class="sxs-lookup"><span data-stu-id="793f9-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Esegui di nuovo il processo** (4)</span><span class="sxs-lookup"><span data-stu-id="793f9-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Esegui processo di ripristino** (5)</span><span class="sxs-lookup"><span data-stu-id="793f9-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="793f9-355">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="793f9-355">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-356">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="793f9-356">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="793f9-358">Qualificatori: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="793f9-358">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="793f9-359">Giorno del mese in cui deve essere elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-359">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="793f9-360">Sono disponibili diverse interpretazioni per questa proprietà, a seconda del valore di **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="793f9-360">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="793f9-361">Quando **RunDayOfWeek** è 0 e **RunDay** è un valore positivo, **RunDay** definisce il giorno del mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-361">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="793f9-362">Ad esempio, se **RunDayOfWeek** è 0 e **RunDay** è 12, il processo verrà elaborato <sup>il giorno 12</sup> del mese.</span><span class="sxs-lookup"><span data-stu-id="793f9-362">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="793f9-363">Quando **RunDayOfWeek** è 0 e **RunDay** è negativo, **RunDay** definisce il numero di giorni prima dell'ultimo giorno del mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-363">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="793f9-364">1 indica l'ultimo giorno del mese, 2 indica un giorno prima dell'ultimo giorno del mese e così via.</span><span class="sxs-lookup"><span data-stu-id="793f9-364">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="793f9-365">Se, ad esempio, **RunDayOfWeek** è 0 e **RunDay** è 1, il processo verrà elaborato l'ultimo giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="793f9-365">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="793f9-366">Quando **RunDayOfWeek** è diverso da 0, **RunDayOfWeek** è il giorno della settimana in cui verrà elaborato il processo, relativo a **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="793f9-366">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="793f9-367">Se, ad esempio, **RunDay** è 15 e **RunDayOfWeek** è 7 (+ sabato), il processo verrà elaborato il primo sabato il o dopo il 15 <sup>°</sup> giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="793f9-367">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="793f9-368">Se **RunDay** è 20 e **RunDayOfWeek** è 7 (sabato), il processo verrà elaborato il primo sabato il o prima del 20 <sup>°</sup> giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="793f9-368">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="793f9-369">Se **RunDay** è 1 e **RunDayOfWeek** è 1 (domenica), il processo verrà elaborato l'ultima domenica del mese.</span><span class="sxs-lookup"><span data-stu-id="793f9-369">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="793f9-370">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-370">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-371">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="793f9-371">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-372">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="793f9-372">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-374">Intero positivo o negativo utilizzato insieme a **RunDay** per indicare il giorno della settimana o il mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-374">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="793f9-375">Per ulteriori informazioni, vedere la descrizione della proprietà **RunDay** .</span><span class="sxs-lookup"><span data-stu-id="793f9-375">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="793f9-376">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-376">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="793f9-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Sabato** (7)</span><span class="sxs-lookup"><span data-stu-id="793f9-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Venerdì** (6)</span><span class="sxs-lookup"><span data-stu-id="793f9-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Giovedi** (5)</span><span class="sxs-lookup"><span data-stu-id="793f9-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mercoledì** (4)</span><span class="sxs-lookup"><span data-stu-id="793f9-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Martedì** (3)</span><span class="sxs-lookup"><span data-stu-id="793f9-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Lunedì** (2)</span><span class="sxs-lookup"><span data-stu-id="793f9-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Domenica** (1)</span><span class="sxs-lookup"><span data-stu-id="793f9-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="793f9-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domenica** (1)</span><span class="sxs-lookup"><span data-stu-id="793f9-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lunedì** (2)</span><span class="sxs-lookup"><span data-stu-id="793f9-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Martedì** (3)</span><span class="sxs-lookup"><span data-stu-id="793f9-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mercoledì** (4)</span><span class="sxs-lookup"><span data-stu-id="793f9-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Giovedi** (5)</span><span class="sxs-lookup"><span data-stu-id="793f9-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Venerdì** (6)</span><span class="sxs-lookup"><span data-stu-id="793f9-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sabato** (7)</span><span class="sxs-lookup"><span data-stu-id="793f9-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="793f9-392">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="793f9-392">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-393">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="793f9-393">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-395">Mese durante il quale deve essere elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-395">The month during which the job should be processed.</span></span> <span data-ttu-id="793f9-396">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-396">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="793f9-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Gennaio** (0)</span><span class="sxs-lookup"><span data-stu-id="793f9-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Febbraio** (1)</span><span class="sxs-lookup"><span data-stu-id="793f9-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Marzo** (2)</span><span class="sxs-lookup"><span data-stu-id="793f9-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Aprile** (3)</span><span class="sxs-lookup"><span data-stu-id="793f9-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Maggio** (4)</span><span class="sxs-lookup"><span data-stu-id="793f9-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Giugno** (5)</span><span class="sxs-lookup"><span data-stu-id="793f9-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Luglio** (6)</span><span class="sxs-lookup"><span data-stu-id="793f9-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="793f9-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Settembre** (8)</span><span class="sxs-lookup"><span data-stu-id="793f9-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Ottobre** (9)</span><span class="sxs-lookup"><span data-stu-id="793f9-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembre** (10)</span><span class="sxs-lookup"><span data-stu-id="793f9-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="793f9-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dicembre** (11)</span><span class="sxs-lookup"><span data-stu-id="793f9-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="793f9-409">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="793f9-409">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-410">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-411">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-412">Intervallo di tempo dopo la mezzanotte di elaborazione del processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-412">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="793f9-413">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-414">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-414">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-415">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-417">Ora di inizio pianificata per il processo, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="793f9-417">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="793f9-418">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-419">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-419">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-420">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-420">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-422">Ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-422">The time that the job began.</span></span> <span data-ttu-id="793f9-423">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-423">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-424">**Status**</span><span class="sxs-lookup"><span data-stu-id="793f9-424">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-425">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-426">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-427">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="793f9-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="793f9-428">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="793f9-428">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-429">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="793f9-429">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="793f9-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-431">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="793f9-431">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="793f9-432">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="793f9-432">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="793f9-433">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="793f9-433">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-434">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-436">Quantità di tempo, in minuti, durante la quale il processo viene mantenuto dopo il completamento dell'esecuzione, ovvero esito positivo o negativo dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="793f9-436">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="793f9-437">Il processo deve rimanere in esistenza per un certo periodo di tempo indipendentemente dal valore della proprietà **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="793f9-437">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="793f9-438">Il valore predefinito è 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="793f9-438">The default is five minutes.</span></span> <span data-ttu-id="793f9-439">Questa proprietà viene ereditata da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))ed è sempre impostata su 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="793f9-439">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="793f9-440">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="793f9-440">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-441">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-442">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-443">Data o ora dell'Ultima modifica apportata allo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-443">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="793f9-444">Se lo stato del processo non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo 0.</span><span class="sxs-lookup"><span data-stu-id="793f9-444">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="793f9-445">Se è stata richiesta una modifica di stato, ma è stata rifiutata o non ancora elaborata, la proprietà non deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="793f9-445">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="793f9-446">Questa proprietà viene ereditata da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="793f9-446">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-447">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="793f9-447">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-448">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-448">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-449">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-450">Ora di invio del processo.</span><span class="sxs-lookup"><span data-stu-id="793f9-450">The time that the job was submitted.</span></span> <span data-ttu-id="793f9-451">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-451">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-452">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-452">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-453">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="793f9-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-454">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-455">L'ora in cui il processo non è valido o deve essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="793f9-455">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="793f9-456">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="793f9-456">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="793f9-457">**VirtualSystemName**</span><span class="sxs-lookup"><span data-stu-id="793f9-457">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793f9-458">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="793f9-458">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="793f9-459">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793f9-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="793f9-460">Nome univoco del sistema virtuale interessato.</span><span class="sxs-lookup"><span data-stu-id="793f9-460">The unique name of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="793f9-461">Requisiti</span><span class="sxs-lookup"><span data-stu-id="793f9-461">Requirements</span></span>



| <span data-ttu-id="793f9-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="793f9-462">Requirement</span></span> | <span data-ttu-id="793f9-463">Valore</span><span class="sxs-lookup"><span data-stu-id="793f9-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="793f9-464">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="793f9-464">Minimum supported client</span></span><br/> | <span data-ttu-id="793f9-465">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="793f9-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="793f9-466">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="793f9-466">Minimum supported server</span></span><br/> | <span data-ttu-id="793f9-467">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="793f9-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="793f9-468">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="793f9-468">Namespace</span></span><br/>                | <span data-ttu-id="793f9-469">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="793f9-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="793f9-470">MOF</span><span class="sxs-lookup"><span data-stu-id="793f9-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="793f9-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="793f9-472">DLL</span><span class="sxs-lookup"><span data-stu-id="793f9-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="793f9-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="793f9-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

