---
description: Rappresenta un processo di operazione del servizio file Guest.
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Classe Msvm_CopyFileToGuestJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57e27b4ba610eea4559f3b045b2d823661cf4cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314334"
---
# <a name="msvm_copyfiletoguestjob-class"></a><span data-ttu-id="2d804-103">\_Classe MSVM CopyFileToGuestJob</span><span class="sxs-lookup"><span data-stu-id="2d804-103">Msvm\_CopyFileToGuestJob class</span></span>

<span data-ttu-id="2d804-104">Rappresenta un processo di operazione del servizio file Guest.</span><span class="sxs-lookup"><span data-stu-id="2d804-104">Represents a guest file service operation job.</span></span> <span data-ttu-id="2d804-105">Questa classe deriva da [**MSVM \_ GuestFileService**](msvm-guestfileservice.md).</span><span class="sxs-lookup"><span data-stu-id="2d804-105">This class derives from [**Msvm\_GuestFileService**](msvm-guestfileservice.md).</span></span>

<span data-ttu-id="2d804-106">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2d804-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d804-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d804-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a><span data-ttu-id="2d804-108">Members</span><span class="sxs-lookup"><span data-stu-id="2d804-108">Members</span></span>

<span data-ttu-id="2d804-109">La **classe \_ CopyFileToGuestJob di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2d804-109">The **Msvm\_CopyFileToGuestJob** class has these types of members:</span></span>

-   [<span data-ttu-id="2d804-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="2d804-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2d804-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d804-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2d804-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="2d804-112">Methods</span></span>

<span data-ttu-id="2d804-113">La **classe \_ CopyFileToGuestJob di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2d804-113">The **Msvm\_CopyFileToGuestJob** class has these methods.</span></span>



| <span data-ttu-id="2d804-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="2d804-114">Method</span></span>                                                                   | <span data-ttu-id="2d804-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d804-115">Description</span></span>                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="2d804-116">**CopyFilesToGuest**</span><span class="sxs-lookup"><span data-stu-id="2d804-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md)       | <span data-ttu-id="2d804-117">Copia i file dall'host Hyper-V alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2d804-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> |
| [<span data-ttu-id="2d804-118">**GetError**</span><span class="sxs-lookup"><span data-stu-id="2d804-118">**GetError**</span></span>](geterror-msvm-copyfiletoguestjob.md)                     | <span data-ttu-id="2d804-119">Recupera l'oggetto errore per il processo.</span><span class="sxs-lookup"><span data-stu-id="2d804-119">Retrieves the error object for the job.</span></span><br/>                    |
| [<span data-ttu-id="2d804-120">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="2d804-120">**GetErrorEx**</span></span>](geterrorex-msvm-copyfiletoguestjob.md)                 | <span data-ttu-id="2d804-121">Recupera gli oggetti Error per il processo.</span><span class="sxs-lookup"><span data-stu-id="2d804-121">Retrieves the error objects for the job.</span></span><br/>                   |
| [<span data-ttu-id="2d804-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2d804-122">**RequestStateChange**</span></span>](requeststatechange-msvm-copyfiletoguestjob.md) | <span data-ttu-id="2d804-123">Modifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="2d804-123">Changes the state of the job.</span></span><br/>                              |
| <span data-ttu-id="2d804-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="2d804-124">**StartService**</span></span>                                                         | <span data-ttu-id="2d804-125">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2d804-125">This method is not supported.</span></span><br/>                              |
| <span data-ttu-id="2d804-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="2d804-126">**StopService**</span></span>                                                          | <span data-ttu-id="2d804-127">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2d804-127">This method is not supported.</span></span><br/>                              |



 

### <a name="properties"></a><span data-ttu-id="2d804-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d804-128">Properties</span></span>

<span data-ttu-id="2d804-129">La **classe \_ CopyFileToGuestJob di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2d804-129">The **Msvm\_CopyFileToGuestJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d804-130">**Annullabili**</span><span class="sxs-lookup"><span data-stu-id="2d804-130">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-131">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2d804-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-133">Indica se il processo può essere annullato.</span><span class="sxs-lookup"><span data-stu-id="2d804-133">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="2d804-134">Il valore di questa proprietà non garantisce che una richiesta di annullamento del processo avrà esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2d804-134">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span> <span data-ttu-id="2d804-135">Se **true**, il processo può essere annullato. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="2d804-135">If **TRUE**, the job can be cancelled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2d804-136">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2d804-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d804-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-139">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2d804-139">Short textual description of the object.</span></span> <span data-ttu-id="2d804-140">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2d804-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2d804-141">**CopyFileToGuestSettingData**</span><span class="sxs-lookup"><span data-stu-id="2d804-141">**CopyFileToGuestSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-142">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2d804-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2d804-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-144">Impostazione dei dati utilizzati per la copia di un file.</span><span class="sxs-lookup"><span data-stu-id="2d804-144">Setting data that is used to copy a file.</span></span>

</dd> <dt>

<span data-ttu-id="2d804-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2d804-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d804-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-148">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="2d804-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2d804-149">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="2d804-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="2d804-150">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2d804-150">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d804-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-153">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2d804-153">Textual description of the object.</span></span> <span data-ttu-id="2d804-154">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2d804-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2d804-155">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="2d804-155">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d804-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d804-158">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="2d804-158">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="2d804-159">Descrizione di riepilogo dell'errore, se presente.</span><span class="sxs-lookup"><span data-stu-id="2d804-159">A summary description of the error, if present.</span></span> <span data-ttu-id="2d804-160">Questa proprietà viene ereditata [**dal \_ processo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="2d804-160">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="2d804-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2d804-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-162">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2d804-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-164">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2d804-164">Date and time the object was installed.</span></span> <span data-ttu-id="2d804-165">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="2d804-165">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="2d804-166">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2d804-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2d804-167">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2d804-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d804-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-170">Identificatore univoco per il servizio che fornisce anche un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="2d804-170">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="2d804-171">Per ulteriori informazioni sulla funzionalità, vedere la proprietà **Description** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2d804-171">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="2d804-172">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2d804-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2d804-173">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="2d804-173">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-174">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2d804-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-176">Se **true**, il servizio è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="2d804-176">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="2d804-177">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="2d804-177">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d804-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-180">Indica se il servizio viene avviato automaticamente, ad esempio da un sistema operativo, o se è stato avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="2d804-180">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="2d804-181">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d804-181">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="2d804-182">**Automatica**</span><span class="sxs-lookup"><span data-stu-id="2d804-182">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="2d804-183">**Manuale**</span><span class="sxs-lookup"><span data-stu-id="2d804-183">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2d804-184">**Status**</span><span class="sxs-lookup"><span data-stu-id="2d804-184">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d804-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-187">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2d804-187">Current status of the object.</span></span> <span data-ttu-id="2d804-188">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2d804-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="2d804-189">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d804-189">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="2d804-190">**OK**</span><span class="sxs-lookup"><span data-stu-id="2d804-190">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="2d804-191">**Errore**</span><span class="sxs-lookup"><span data-stu-id="2d804-191">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="2d804-192">**Degradato**</span><span class="sxs-lookup"><span data-stu-id="2d804-192">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="2d804-193">**Sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="2d804-193">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="2d804-194">**"Errore di predazione"**</span><span class="sxs-lookup"><span data-stu-id="2d804-194">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="2d804-195">**Avvio**</span><span class="sxs-lookup"><span data-stu-id="2d804-195">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="2d804-196">**Arresto**</span><span class="sxs-lookup"><span data-stu-id="2d804-196">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="2d804-197">**Servizio**</span><span class="sxs-lookup"><span data-stu-id="2d804-197">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="2d804-198">**Sottolineato**</span><span class="sxs-lookup"><span data-stu-id="2d804-198">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="2d804-199">**"Non ripristino"**</span><span class="sxs-lookup"><span data-stu-id="2d804-199">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="2d804-200">**"Nessun contatto"**</span><span class="sxs-lookup"><span data-stu-id="2d804-200">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="2d804-201">**"Lost comm"**</span><span class="sxs-lookup"><span data-stu-id="2d804-201">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2d804-202">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2d804-202">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d804-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-205">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2d804-205">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="2d804-206">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2d804-206">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d804-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-209">Nome del sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="2d804-209">Name of the system that hosts the service.</span></span>

</dd> <dt>

<span data-ttu-id="2d804-210">**VirtualSystemName**</span><span class="sxs-lookup"><span data-stu-id="2d804-210">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d804-211">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d804-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d804-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d804-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d804-213">GUID del sistema virtuale interessato.</span><span class="sxs-lookup"><span data-stu-id="2d804-213">GUID of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d804-214">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d804-214">Requirements</span></span>



| <span data-ttu-id="2d804-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d804-215">Requirement</span></span> | <span data-ttu-id="2d804-216">Valore</span><span class="sxs-lookup"><span data-stu-id="2d804-216">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d804-217">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d804-217">Minimum supported client</span></span><br/> | <span data-ttu-id="2d804-218">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d804-218">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2d804-219">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d804-219">Minimum supported server</span></span><br/> | <span data-ttu-id="2d804-220">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2d804-220">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2d804-221">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2d804-221">Namespace</span></span><br/>                | <span data-ttu-id="2d804-222">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2d804-222">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2d804-223">MOF</span><span class="sxs-lookup"><span data-stu-id="2d804-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d804-224"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d804-224"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d804-225">DLL</span><span class="sxs-lookup"><span data-stu-id="2d804-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d804-226"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d804-226"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d804-227">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d804-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d804-228">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="2d804-228">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

[<span data-ttu-id="2d804-229">**\_GuestFileService MSVM**</span><span class="sxs-lookup"><span data-stu-id="2d804-229">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> <dt>

[<span data-ttu-id="2d804-230">**\_GuestService MSVM**</span><span class="sxs-lookup"><span data-stu-id="2d804-230">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

