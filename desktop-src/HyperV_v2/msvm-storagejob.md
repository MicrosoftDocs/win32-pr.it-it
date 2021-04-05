---
description: Rappresenta un processo dell'operazione di archiviazione creato dal servizio gestione immagini Microsoft Hyper-V.
ms.assetid: a1517c1f-7fb6-4203-a5ec-2ecdfcbc4e8c
title: Classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob
- Msvm_StorageJob.KillJob
- Msvm_StorageJob.InstanceID
- Msvm_StorageJob.Caption
- Msvm_StorageJob.Description
- Msvm_StorageJob.ElementName
- Msvm_StorageJob.InstallDate
- Msvm_StorageJob.Name
- Msvm_StorageJob.OperationalStatus
- Msvm_StorageJob.StatusDescriptions
- Msvm_StorageJob.Status
- Msvm_StorageJob.HealthState
- Msvm_StorageJob.CommunicationStatus
- Msvm_StorageJob.DetailedStatus
- Msvm_StorageJob.OperatingStatus
- Msvm_StorageJob.PrimaryStatus
- Msvm_StorageJob.JobStatus
- Msvm_StorageJob.TimeSubmitted
- Msvm_StorageJob.ScheduledStartTime
- Msvm_StorageJob.StartTime
- Msvm_StorageJob.ElapsedTime
- Msvm_StorageJob.JobRunTimes
- Msvm_StorageJob.RunMonth
- Msvm_StorageJob.RunDay
- Msvm_StorageJob.RunDayOfWeek
- Msvm_StorageJob.RunStartInterval
- Msvm_StorageJob.LocalOrUtcTime
- Msvm_StorageJob.UntilTime
- Msvm_StorageJob.Notify
- Msvm_StorageJob.Owner
- Msvm_StorageJob.Priority
- Msvm_StorageJob.PercentComplete
- Msvm_StorageJob.DeleteOnCompletion
- Msvm_StorageJob.ErrorCode
- Msvm_StorageJob.ErrorDescription
- Msvm_StorageJob.ErrorSummaryDescription
- Msvm_StorageJob.RecoveryAction
- Msvm_StorageJob.OtherRecoveryAction
- Msvm_StorageJob.JobState
- Msvm_StorageJob.TimeOfLastStateChange
- Msvm_StorageJob.TimeBeforeRemoval
- Msvm_StorageJob.Cancellable
- Msvm_StorageJob.Child
- Msvm_StorageJob.JobCompletionStatusCode
- Msvm_StorageJob.Parent
- Msvm_StorageJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3014cb9a8201d7baceaf39bb760b17c33844abeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885726"
---
# <a name="msvm_storagejob-class"></a><span data-ttu-id="311dd-103">\_Classe MSVM StorageJob</span><span class="sxs-lookup"><span data-stu-id="311dd-103">Msvm\_StorageJob class</span></span>

<span data-ttu-id="311dd-104">Rappresenta un processo dell'operazione di archiviazione creato dal servizio gestione immagini Microsoft Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="311dd-104">Represents a storage operation job created by the Microsoft Hyper-V Image Management Service.</span></span>

<span data-ttu-id="311dd-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="311dd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="311dd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="311dd-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
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
  datetime TimeBeforeRemoval = 00000000000500.000000:000";
  boolean  Cancellable;
  string   Child;
  UINT32   JobCompletionStatusCode;
  string   Parent;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="311dd-107">Members</span><span class="sxs-lookup"><span data-stu-id="311dd-107">Members</span></span>

<span data-ttu-id="311dd-108">La **classe \_ StorageJob di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="311dd-108">The **Msvm\_StorageJob** class has these types of members:</span></span>

-   [<span data-ttu-id="311dd-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="311dd-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="311dd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="311dd-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="311dd-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="311dd-111">Methods</span></span>

<span data-ttu-id="311dd-112">La **classe \_ StorageJob di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="311dd-112">The **Msvm\_StorageJob** class has these methods.</span></span>



| <span data-ttu-id="311dd-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="311dd-113">Method</span></span>                                                           | <span data-ttu-id="311dd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="311dd-114">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="311dd-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="311dd-115">**GetError**</span></span>](msvm-storagejob-geterror.md)                     | <span data-ttu-id="311dd-116">Recupera l'errore che descrive il motivo per cui il processo non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="311dd-116">Retrieves the error that describes the reason why the job failed.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="311dd-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="311dd-117">**GetErrorEx**</span></span>](geterrorex-msvm-storagejob.md)                 | <span data-ttu-id="311dd-118">Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna istanza di [**\_ errore MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="311dd-118">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="311dd-119">Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, vengono restituite una o più istanze di **\_ errore MSVM** .</span><span class="sxs-lookup"><span data-stu-id="311dd-119">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span><br/> |
| <span data-ttu-id="311dd-120">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="311dd-120">**KillJob**</span></span>                                                      | <span data-ttu-id="311dd-121">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="311dd-121">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="311dd-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="311dd-122">**RequestStateChange**</span></span>](msvm-storagejob-requeststatechange.md) | <span data-ttu-id="311dd-123">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="311dd-123">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="311dd-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="311dd-124">Properties</span></span>

<span data-ttu-id="311dd-125">La **classe \_ StorageJob di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="311dd-125">The **Msvm\_StorageJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="311dd-126">**Annullabili**</span><span class="sxs-lookup"><span data-stu-id="311dd-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-127">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="311dd-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-129">Indica se il processo può essere annullato.</span><span class="sxs-lookup"><span data-stu-id="311dd-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="311dd-130">Il valore di questa proprietà non garantisce che una richiesta di annullamento del processo avrà esito positivo.</span><span class="sxs-lookup"><span data-stu-id="311dd-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="311dd-131">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="311dd-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-134">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="311dd-134">A short description of the object.</span></span> <span data-ttu-id="311dd-135">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-136">**Figlio**</span><span class="sxs-lookup"><span data-stu-id="311dd-136">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-139">In caso di errore dell'operazione asincrona, questa proprietà contiene il percorso completo dell'elemento figlio del disco rigido virtuale interessato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="311dd-139">On failure of the asynchronous operation, this property contains the full path of the child of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="311dd-140">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="311dd-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-141">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-143">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="311dd-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="311dd-144">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="311dd-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="311dd-145">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-146">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="311dd-146">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-147">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="311dd-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-149">Specifica se il processo deve essere eliminato automaticamente al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="311dd-149">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="311dd-150">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-150">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-151">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="311dd-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-154">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="311dd-154">A description of the object.</span></span> <span data-ttu-id="311dd-155">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="311dd-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-157">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-159">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="311dd-159">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="311dd-160">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="311dd-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="311dd-161">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-162">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-163">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-165">Periodo di tempo durante il quale il processo è stato eseguito.</span><span class="sxs-lookup"><span data-stu-id="311dd-165">The length of time that the job has been executing.</span></span> <span data-ttu-id="311dd-166">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="311dd-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-170">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="311dd-170">A display name for the object.</span></span> <span data-ttu-id="311dd-171">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="311dd-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-173">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-175">Codice di errore specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="311dd-175">A vendor-specific error code.</span></span> <span data-ttu-id="311dd-176">Se il processo è stato completato senza errori, il valore deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="311dd-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="311dd-177">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="311dd-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-181">Stringa che contiene la descrizione dell'errore del fornitore.</span><span class="sxs-lookup"><span data-stu-id="311dd-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="311dd-182">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="311dd-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="311dd-186">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="311dd-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="311dd-187">Descrizione di riepilogo dell'errore, se presente.</span><span class="sxs-lookup"><span data-stu-id="311dd-187">A summary description of the error, if present.</span></span> <span data-ttu-id="311dd-188">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-188">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="311dd-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-190">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-192">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="311dd-192">The current health of the element.</span></span> <span data-ttu-id="311dd-193">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="311dd-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="311dd-194">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="311dd-194">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="311dd-195">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5.</span><span class="sxs-lookup"><span data-stu-id="311dd-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="311dd-196">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="311dd-196">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-197">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-199">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="311dd-199">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="311dd-200">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-201">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="311dd-201">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-204">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="311dd-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="311dd-205">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-206">**JobCompletionStatusCode**</span><span class="sxs-lookup"><span data-stu-id="311dd-206">**JobCompletionStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-207">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="311dd-207">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-209">Codice **HRESULT** che descrive lo stato di completamento dell'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="311dd-209">The **HRESULT** code that describes the completion status for the asynchronous operation.</span></span>

</dd> <dt>

<span data-ttu-id="311dd-210">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="311dd-210">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-211">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="311dd-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-213">Il numero di volte in cui il processo deve essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="311dd-213">The number of times that the job should be run.</span></span> <span data-ttu-id="311dd-214">Il valore 1 indica che il processo non è ricorrente, mentre un valore diverso da zero indica un limite al numero di volte che il processo ricorrerà.</span><span class="sxs-lookup"><span data-stu-id="311dd-214">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="311dd-215">Zero indica che non esiste alcun limite per il numero di volte in cui il processo può essere elaborato, ma verrà terminato dopo il raggiungimento di **UntilTime** o se il processo viene terminato manualmente.</span><span class="sxs-lookup"><span data-stu-id="311dd-215">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="311dd-216">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-216">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-217">**JobState**</span><span class="sxs-lookup"><span data-stu-id="311dd-217">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-218">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-220">Stato operativo di un processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-220">The operational state of a job.</span></span> <span data-ttu-id="311dd-221">Può inoltre indicare transizioni tra questi Stati, ad esempio 6 (chiusura) e 3 (avvio).</span><span class="sxs-lookup"><span data-stu-id="311dd-221">It can also indicate transitions between these states, for example, 6 (Shutting Down) and 3 (Starting).</span></span> <span data-ttu-id="311dd-222">Questa proprietà viene ereditata da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="311dd-222">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="311dd-223">Valore</span><span class="sxs-lookup"><span data-stu-id="311dd-223">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="311dd-224">Significato</span><span class="sxs-lookup"><span data-stu-id="311dd-224">Meaning</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="311dd-225"><dt>**Nuovo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-225"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                               | <span data-ttu-id="311dd-226">Il processo non è mai stato avviato.</span><span class="sxs-lookup"><span data-stu-id="311dd-226">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="311dd-227"><dt>**A partire**</dt> da <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-227"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                           | <span data-ttu-id="311dd-228">Il processo viene spostato dagli Stati "New", "Suspended" o "Service" nello stato "Running".</span><span class="sxs-lookup"><span data-stu-id="311dd-228">The job is moving from the "New", "Suspended", or "Service" states into the "Running" state.</span></span><br/>                                                                                                                                            |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="311dd-229"><dt>**Esecuzione**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-229"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                               | <span data-ttu-id="311dd-230">Il processo è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="311dd-230">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="311dd-231"><dt>**Sospeso**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-231"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                       | <span data-ttu-id="311dd-232">Il processo è stato interrotto, ma può essere riavviato in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="311dd-232">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="311dd-233"><dt>**Chiusura**</dt> di <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-233"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                       | <span data-ttu-id="311dd-234">Il processo viene spostato in uno stato "completed", "Terminated" o "Killed".</span><span class="sxs-lookup"><span data-stu-id="311dd-234">The job is moving to a "Completed", "Terminated", or "Killed" state.</span></span><br/>                                                                                                                                                                    |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="311dd-235"><dt>**Completato**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-235"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                       | <span data-ttu-id="311dd-236">Il processo è stato completato normalmente.</span><span class="sxs-lookup"><span data-stu-id="311dd-236">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="311dd-237"><dt>**Terminato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-237"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                                   | <span data-ttu-id="311dd-238">Il processo è stato interrotto da una richiesta di modifica dello stato "Terminate".</span><span class="sxs-lookup"><span data-stu-id="311dd-238">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="311dd-239">Il processo e tutti i processi sottostanti sono terminati e possono essere riavviati solo come nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-239">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="311dd-240">Il requisito che il processo venga riavviato solo come nuovo processo è specifico del processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-240">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="311dd-241"><dt>**Ucciso**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-241"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                                   | <span data-ttu-id="311dd-242">Il processo è stato interrotto da una richiesta di modifica dello stato "Kill".</span><span class="sxs-lookup"><span data-stu-id="311dd-242">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="311dd-243">È possibile che i processi sottostanti siano ancora in esecuzione e che sia necessario eseguire una pulizia per liberare risorse.</span><span class="sxs-lookup"><span data-stu-id="311dd-243">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="311dd-244"><dt>**Eccezione**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-244"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                      | <span data-ttu-id="311dd-245">Il processo è in uno stato anomalo che potrebbe essere indicativo di una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="311dd-245">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="311dd-246">Lo stato effettivo del processo potrebbe essere disponibile tramite oggetti specifici del processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-246">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="311dd-247"><dt>**Servizio**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-247"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                              | <span data-ttu-id="311dd-248">Il processo è in uno stato specifico del fornitore che supporta l'individuazione o la risoluzione dei problemi o entrambi.</span><span class="sxs-lookup"><span data-stu-id="311dd-248">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="311dd-249"><dt>**DMTF riservato**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-249"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>                | <span data-ttu-id="311dd-250">Riservato.</span><span class="sxs-lookup"><span data-stu-id="311dd-250">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="311dd-251"><dt> **Fornitore riservato**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-251"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="311dd-252">Riservato.</span><span class="sxs-lookup"><span data-stu-id="311dd-252">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="311dd-253">**Stato processo**</span><span class="sxs-lookup"><span data-stu-id="311dd-253">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-254">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-256">Stringa che rappresenta lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-256">A string that represents the job status.</span></span> <span data-ttu-id="311dd-257">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-257">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-258">**JobType**</span><span class="sxs-lookup"><span data-stu-id="311dd-258">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-259">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-261">Tipo di operazione asincrona rilevata da questa istanza di **MSVM \_ StorageJob**.</span><span class="sxs-lookup"><span data-stu-id="311dd-261">The type of asynchronous operation being tracked by this instance of **Msvm\_StorageJob**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="311dd-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="311dd-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>

<span data-ttu-id="311dd-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**Creazione VHD** (1)</span><span class="sxs-lookup"><span data-stu-id="311dd-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**VHD Creation** (1)</span></span>


</dt> <dd>

<span data-ttu-id="311dd-264">Creazione di un'immagine del disco rigido virtuale (VHD).</span><span class="sxs-lookup"><span data-stu-id="311dd-264">Creating a virtual hard disk (VHD) image.</span></span>

</dd> <dt>

<span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>

<span data-ttu-id="311dd-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Creazione floppy** (2)</span><span class="sxs-lookup"><span data-stu-id="311dd-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Floppy Creation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="311dd-266">Creazione di un'immagine di disco floppy virtuale (VFD).</span><span class="sxs-lookup"><span data-stu-id="311dd-266">Creating a virtual floppy disk image (VFD).</span></span>

</dd> <dt>

<span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>

<span data-ttu-id="311dd-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compattazione** (3)</span><span class="sxs-lookup"><span data-stu-id="311dd-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compaction** (3)</span></span>


</dt> <dd>

<span data-ttu-id="311dd-268">Compattazione delle dimensioni di un'immagine del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="311dd-268">Compacting the size of a VHD image.</span></span>

</dd> <dt>

<span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>

<span data-ttu-id="311dd-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Espansione** (4)</span><span class="sxs-lookup"><span data-stu-id="311dd-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Expansion** (4)</span></span>


</dt> <dd>

<span data-ttu-id="311dd-270">Espansione delle dimensioni di un'immagine del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="311dd-270">Expanding the size of a VHD image.</span></span>

</dd> <dt>

<span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>

<span data-ttu-id="311dd-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Unione** (5)</span><span class="sxs-lookup"><span data-stu-id="311dd-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Merging** (5)</span></span>


</dt> <dd>

<span data-ttu-id="311dd-272">Unione di più immagini VHD in un'unica immagine.</span><span class="sxs-lookup"><span data-stu-id="311dd-272">Merging multiple VHD images into a single image.</span></span>

</dd> <dt>

<span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>

<span data-ttu-id="311dd-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Conversione** (6)</span><span class="sxs-lookup"><span data-stu-id="311dd-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Conversion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="311dd-274">Conversione del tipo di un'immagine del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="311dd-274">Converting the type of a virtual hard disk image.</span></span>

</dd> <dt>

<span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>

<span data-ttu-id="311dd-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Montaggio loopback** (7)</span><span class="sxs-lookup"><span data-stu-id="311dd-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Loopback Mount** (7)</span></span>


</dt> <dd>

<span data-ttu-id="311dd-276">Montaggio del disco rigido virtuale nella partizione padre</span><span class="sxs-lookup"><span data-stu-id="311dd-276">Mounting the virtual hard disk on the parent partition</span></span>

</dd> <dt>

<span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>

<span data-ttu-id="311dd-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Ottenere informazioni sul disco rigido virtuale** (8)</span><span class="sxs-lookup"><span data-stu-id="311dd-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Get VHD Info** (8)</span></span>


</dt> <dd>

<span data-ttu-id="311dd-278">Montaggio del disco rigido virtuale nel sistema operativo di gestione.</span><span class="sxs-lookup"><span data-stu-id="311dd-278">Mounting the VHD on the management operating system.</span></span>

</dd> <dt>

<span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>

<span data-ttu-id="311dd-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Convalida immagine VHD** (9)</span><span class="sxs-lookup"><span data-stu-id="311dd-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Validate VHD Image** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="311dd-280">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-280">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-281">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-283">Indica se le ore rappresentate nelle proprietà **RunStartInterval** e **UntilTime** rappresentano le ore locali o l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="311dd-283">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="311dd-284">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-284">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="311dd-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Ora locale** (1)</span><span class="sxs-lookup"><span data-stu-id="311dd-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Ora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="311dd-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="311dd-287">**Nome**</span><span class="sxs-lookup"><span data-stu-id="311dd-287">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-290">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="311dd-290">The label by which the object is known.</span></span> <span data-ttu-id="311dd-291">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-292">**Notificare**</span><span class="sxs-lookup"><span data-stu-id="311dd-292">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-295">Utente che riceve una notifica al completamento o all'errore del processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-295">The user who is notified upon job completion or failure.</span></span> <span data-ttu-id="311dd-296">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-296">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-297">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="311dd-297">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-298">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-300">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="311dd-300">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="311dd-301">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="311dd-301">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="311dd-302">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-303">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="311dd-303">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-304">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-304">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="311dd-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-306">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="311dd-306">The current statuses of the object.</span></span> <span data-ttu-id="311dd-307">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-308">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="311dd-308">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-311">Stringa che descrive l'azione di ripristino quando la proprietà **RecoveryAction** dell'istanza è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="311dd-311">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="311dd-312">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-312">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-313">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="311dd-313">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-314">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-316">Utente che ha inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-316">The user who submitted the job.</span></span> <span data-ttu-id="311dd-317">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-317">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-318">**Parent**</span><span class="sxs-lookup"><span data-stu-id="311dd-318">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-319">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-321">In caso di errore dell'operazione asincrona, questa proprietà contiene il percorso del file dell'elemento padre del disco rigido virtuale interessato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="311dd-321">On failure of the asynchronous operation, this property contains the file path to the parent of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="311dd-322">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="311dd-322">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-323">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="311dd-325">Qualificatori: **MinValue** (0), **MaxValue** (100), **unità** ("percentuale")</span><span class="sxs-lookup"><span data-stu-id="311dd-325">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="311dd-326">Percentuale di completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-326">The completion percentage of the job.</span></span> <span data-ttu-id="311dd-327">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-327">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-328">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="311dd-328">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-329">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-329">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-331">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="311dd-331">Provides high level status information.</span></span> <span data-ttu-id="311dd-332">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="311dd-332">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="311dd-333">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="311dd-333">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="311dd-334">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-335">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="311dd-335">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-336">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="311dd-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-338">Importanza dell'esecuzione di un processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-338">The importance of a job's execution.</span></span> <span data-ttu-id="311dd-339">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-339">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-340">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="311dd-340">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-341">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="311dd-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-343">Descrive l'azione di ripristino da intraprendere per un processo che non è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="311dd-343">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="311dd-344">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-344">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="311dd-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="311dd-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="311dd-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Non continuare** (2)</span><span class="sxs-lookup"><span data-stu-id="311dd-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continua con il processo successivo** (3)</span><span class="sxs-lookup"><span data-stu-id="311dd-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Esegui di nuovo il processo** (4)</span><span class="sxs-lookup"><span data-stu-id="311dd-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Esegui processo di ripristino** (5)</span><span class="sxs-lookup"><span data-stu-id="311dd-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="311dd-351">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="311dd-351">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-352">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="311dd-352">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="311dd-354">Qualificatori: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="311dd-354">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="311dd-355">Giorno del mese in cui deve essere elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-355">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="311dd-356">Sono disponibili diverse interpretazioni per questa proprietà, a seconda del valore di **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="311dd-356">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="311dd-357">Quando **RunDayOfWeek** è 0 e **RunDay** è un valore positivo, **RunDay** definisce il giorno del mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-357">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="311dd-358">Ad esempio, se **RunDayOfWeek** è 0 e **RunDay** è 12, il processo verrà elaborato <sup>il giorno 12</sup> del mese.</span><span class="sxs-lookup"><span data-stu-id="311dd-358">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="311dd-359">Quando **RunDayOfWeek** è 0 e **RunDay** è negativo, **RunDay** definisce il numero di giorni prima dell'ultimo giorno del mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-359">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="311dd-360">1 indica l'ultimo giorno del mese, 2 indica un giorno prima dell'ultimo giorno del mese e così via.</span><span class="sxs-lookup"><span data-stu-id="311dd-360">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="311dd-361">Se, ad esempio, **RunDayOfWeek** è 0 e **RunDay** è 1, il processo verrà elaborato l'ultimo giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="311dd-361">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="311dd-362">Quando **RunDayOfWeek** è diverso da 0, **RunDayOfWeek** è il giorno della settimana in cui verrà elaborato il processo, relativo a **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="311dd-362">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="311dd-363">Se, ad esempio, **RunDay** è 15 e **RunDayOfWeek** è 7 (+ sabato), il processo verrà elaborato il primo sabato il o dopo il 15 <sup>°</sup> giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="311dd-363">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="311dd-364">Se **RunDay** è 20 e **RunDayOfWeek** è 7 (sabato), il processo verrà elaborato il primo sabato il o prima del 20 <sup>°</sup> giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="311dd-364">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="311dd-365">Se **RunDay** è 1 e **RunDayOfWeek** è 1 (domenica), il processo verrà elaborato l'ultima domenica del mese.</span><span class="sxs-lookup"><span data-stu-id="311dd-365">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="311dd-366">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-366">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-367">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="311dd-367">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-368">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="311dd-368">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-370">Intero positivo o negativo utilizzato insieme a **RunDay** per indicare il giorno della settimana o il mese in cui viene elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-370">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="311dd-371">Per ulteriori informazioni, vedere la descrizione della proprietà **RunDay** .</span><span class="sxs-lookup"><span data-stu-id="311dd-371">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="311dd-372">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-372">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="311dd-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Sabato** (7)</span><span class="sxs-lookup"><span data-stu-id="311dd-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Venerdì** (6)</span><span class="sxs-lookup"><span data-stu-id="311dd-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Giovedi** (5)</span><span class="sxs-lookup"><span data-stu-id="311dd-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mercoledì** (4)</span><span class="sxs-lookup"><span data-stu-id="311dd-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Martedì** (3)</span><span class="sxs-lookup"><span data-stu-id="311dd-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Lunedì** (2)</span><span class="sxs-lookup"><span data-stu-id="311dd-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Domenica** (1)</span><span class="sxs-lookup"><span data-stu-id="311dd-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="311dd-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domenica** (1)</span><span class="sxs-lookup"><span data-stu-id="311dd-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lunedì** (2)</span><span class="sxs-lookup"><span data-stu-id="311dd-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Martedì** (3)</span><span class="sxs-lookup"><span data-stu-id="311dd-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mercoledì** (4)</span><span class="sxs-lookup"><span data-stu-id="311dd-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Giovedi** (5)</span><span class="sxs-lookup"><span data-stu-id="311dd-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Venerdì** (6)</span><span class="sxs-lookup"><span data-stu-id="311dd-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sabato** (7)</span><span class="sxs-lookup"><span data-stu-id="311dd-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="311dd-388">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="311dd-388">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-389">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="311dd-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-391">Mese durante il quale deve essere elaborato il processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-391">The month during which the job should be processed.</span></span> <span data-ttu-id="311dd-392">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="311dd-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Gennaio** (0)</span><span class="sxs-lookup"><span data-stu-id="311dd-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Febbraio** (1)</span><span class="sxs-lookup"><span data-stu-id="311dd-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Marzo** (2)</span><span class="sxs-lookup"><span data-stu-id="311dd-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Aprile** (3)</span><span class="sxs-lookup"><span data-stu-id="311dd-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Maggio** (4)</span><span class="sxs-lookup"><span data-stu-id="311dd-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Giugno** (5)</span><span class="sxs-lookup"><span data-stu-id="311dd-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Luglio** (6)</span><span class="sxs-lookup"><span data-stu-id="311dd-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="311dd-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Settembre** (8)</span><span class="sxs-lookup"><span data-stu-id="311dd-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Ottobre** (9)</span><span class="sxs-lookup"><span data-stu-id="311dd-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembre** (10)</span><span class="sxs-lookup"><span data-stu-id="311dd-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="311dd-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dicembre** (11)</span><span class="sxs-lookup"><span data-stu-id="311dd-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="311dd-405">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="311dd-405">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-406">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-408">Intervallo di tempo dopo la mezzanotte di elaborazione del processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-408">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="311dd-409">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-409">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-410">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-410">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-411">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-411">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-412">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-413">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-414">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-414">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-415">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-417">Ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-417">The time that the job began.</span></span> <span data-ttu-id="311dd-418">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-419">**Status**</span><span class="sxs-lookup"><span data-stu-id="311dd-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-420">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="311dd-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-422">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="311dd-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="311dd-423">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="311dd-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-424">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="311dd-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="311dd-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-426">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="311dd-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="311dd-427">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="311dd-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-428">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="311dd-428">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-429">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-431">Quantità di tempo, in minuti, durante la quale il processo viene mantenuto dopo il completamento dell'esecuzione, ovvero esito positivo o negativo dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="311dd-431">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="311dd-432">Il processo deve rimanere in esistenza per un certo periodo di tempo indipendentemente dal valore della proprietà **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="311dd-432">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="311dd-433">Il valore predefinito è 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="311dd-433">The default is five minutes.</span></span> <span data-ttu-id="311dd-434">Questa proprietà viene ereditata da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))ed è sempre impostata su 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="311dd-434">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="311dd-435">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="311dd-435">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-436">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-436">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-438">Ora dell'Ultima modifica dello stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="311dd-438">The time at which the virtual machine's state was last modified.</span></span> <span data-ttu-id="311dd-439">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="311dd-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-440">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="311dd-440">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-441">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-442">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-443">Ora di invio del processo.</span><span class="sxs-lookup"><span data-stu-id="311dd-443">The time that the job was submitted.</span></span> <span data-ttu-id="311dd-444">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-444">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="311dd-445">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-445">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="311dd-446">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="311dd-446">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="311dd-447">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="311dd-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="311dd-448">L'ora in cui il processo non è valido o deve essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="311dd-448">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="311dd-449">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="311dd-449">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="311dd-450">Commenti</span><span class="sxs-lookup"><span data-stu-id="311dd-450">Remarks</span></span>

<span data-ttu-id="311dd-451">L'accesso alla **classe \_ StorageJob di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="311dd-451">Access to the **Msvm\_StorageJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="311dd-452">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="311dd-452">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="311dd-453">Requisiti</span><span class="sxs-lookup"><span data-stu-id="311dd-453">Requirements</span></span>



| <span data-ttu-id="311dd-454">Requisito</span><span class="sxs-lookup"><span data-stu-id="311dd-454">Requirement</span></span> | <span data-ttu-id="311dd-455">Valore</span><span class="sxs-lookup"><span data-stu-id="311dd-455">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="311dd-456">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="311dd-456">Minimum supported client</span></span><br/> | <span data-ttu-id="311dd-457">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="311dd-457">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="311dd-458">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="311dd-458">Minimum supported server</span></span><br/> | <span data-ttu-id="311dd-459">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="311dd-459">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="311dd-460">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="311dd-460">Namespace</span></span><br/>                | <span data-ttu-id="311dd-461">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="311dd-461">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="311dd-462">MOF</span><span class="sxs-lookup"><span data-stu-id="311dd-462">MOF</span></span><br/>                      | <dl> <span data-ttu-id="311dd-463"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-463"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="311dd-464">DLL</span><span class="sxs-lookup"><span data-stu-id="311dd-464">DLL</span></span><br/>                      | <dl> <span data-ttu-id="311dd-465"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="311dd-465"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="311dd-466">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="311dd-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="311dd-467">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="311dd-467">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="311dd-468">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="311dd-468">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="311dd-469">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="311dd-469">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

