---
description: Versione concreta della classe di \_ processi CIM. Questa classe rappresenta un'unità di lavoro istanziabile generica da eseguire, ad esempio un batch o un processo di stampa.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: Classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 949d7c85643919f784a82e7722c9d49a9d9d2e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308366"
---
# <a name="cim_concretejob-class"></a><span data-ttu-id="f65a7-104">CIM \_ ConcreteJob (classe)</span><span class="sxs-lookup"><span data-stu-id="f65a7-104">CIM\_ConcreteJob class</span></span>

<span data-ttu-id="f65a7-105">Versione concreta della classe [**di \_ processi CIM**](cim-job.md) .</span><span class="sxs-lookup"><span data-stu-id="f65a7-105">A concrete version of the [**CIM\_Job**](cim-job.md) class.</span></span> <span data-ttu-id="f65a7-106">Questa classe rappresenta un'unità di lavoro istanziabile generica da eseguire, ad esempio un batch o un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="f65a7-106">This class represent a generic instantiable unit of work to run, such as a batch or a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="f65a7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f65a7-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a><span data-ttu-id="f65a7-108">Members</span><span class="sxs-lookup"><span data-stu-id="f65a7-108">Members</span></span>

<span data-ttu-id="f65a7-109">La classe **CIM \_ ConcreteJob** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f65a7-109">The **CIM\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="f65a7-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="f65a7-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f65a7-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f65a7-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f65a7-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="f65a7-112">Methods</span></span>

<span data-ttu-id="f65a7-113">La classe **CIM \_ ConcreteJob** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f65a7-113">The **CIM\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="f65a7-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="f65a7-114">Method</span></span>                                                           | <span data-ttu-id="f65a7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f65a7-115">Description</span></span>                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="f65a7-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="f65a7-116">**GetError**</span></span>](cim-concretejob-geterror.md)                     | <span data-ttu-id="f65a7-117">Recupera le informazioni sull'errore per lo stato operativo di un processo concreto.</span><span class="sxs-lookup"><span data-stu-id="f65a7-117">Retrieves error information for the operational status of a concrete job.</span></span><br/> |
| [<span data-ttu-id="f65a7-118">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f65a7-118">**RequestStateChange**</span></span>](cim-concretejob-requeststatechange.md) | <span data-ttu-id="f65a7-119">Richiede la modifica dello stato specificato in un processo concreto.</span><span class="sxs-lookup"><span data-stu-id="f65a7-119">Requests the specified state change to a concrete job.</span></span><br/>                    |



 

### <a name="properties"></a><span data-ttu-id="f65a7-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f65a7-120">Properties</span></span>

<span data-ttu-id="f65a7-121">La classe **CIM \_ ConcreteJob** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f65a7-121">The **CIM\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f65a7-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f65a7-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65a7-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f65a7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f65a7-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f65a7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f65a7-125">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="f65a7-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="f65a7-126">Identifica in modo univoco e opaco un'istanza di questa classe nell'ambito dello spazio dei nomi che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="f65a7-126">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f65a7-127">Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="f65a7-127">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="f65a7-128">*OrgID* deve includere un nome con copyright, marchio o in altro modo univoco, di proprietà dell'entità di business che definisce **InstanceID**, oppure essere un ID registrato assegnato da un'autorità globale riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="f65a7-128">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="f65a7-129">Questo modello è simile alla struttura dei nomi delle classi dello schema.</span><span class="sxs-lookup"><span data-stu-id="f65a7-129">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="f65a7-130">Inoltre, per garantire l'univocità, i primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="f65a7-130">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="f65a7-131">Pertanto *OrgID* non deve contenere i due punti (':').</span><span class="sxs-lookup"><span data-stu-id="f65a7-131">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="f65a7-132">Il *localizzato* viene scelto dall'entità di business e non deve essere riutilizzato per identificare diversi elementi reali sottostanti.</span><span class="sxs-lookup"><span data-stu-id="f65a7-132">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="f65a7-133">Se il criterio precedente non viene utilizzato, l'entità di definizione deve assicurare che il valore **InstanceID** risultante non venga riutilizzato nelle proprietà **InstanceID** generate dal provider o da altri provider per questo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f65a7-133">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="f65a7-134">Per le istanze definite DMTF (Distributed Management Task Force), il modello deve essere usato con *OrgID* impostato su CIM.</span><span class="sxs-lookup"><span data-stu-id="f65a7-134">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="f65a7-135">**JobState**</span><span class="sxs-lookup"><span data-stu-id="f65a7-135">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65a7-136">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f65a7-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f65a7-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f65a7-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f65a7-138">Lo stato operativo del processo e la transizione tra questi Stati.</span><span class="sxs-lookup"><span data-stu-id="f65a7-138">The operational state of the job, and the transition between those states.</span></span>

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span data-ttu-id="f65a7-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**Nuovo** (2)</span><span class="sxs-lookup"><span data-stu-id="f65a7-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**New** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f65a7-140">il processo non è mai stato avviato.</span><span class="sxs-lookup"><span data-stu-id="f65a7-140">the job has never been started.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f65a7-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="f65a7-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f65a7-142">Il processo viene spostato dagli Stati ' New ',' suspended ' o ' Service ' nello stato ' running '.</span><span class="sxs-lookup"><span data-stu-id="f65a7-142">The job is moving from the 'New', 'Suspended', or 'Service' states into the 'Running' state.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="f65a7-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (4)</span><span class="sxs-lookup"><span data-stu-id="f65a7-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f65a7-144">Il processo è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f65a7-144">The Job is running.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="f65a7-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Sospeso** (5)</span><span class="sxs-lookup"><span data-stu-id="f65a7-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f65a7-146">Il processo è stato interrotto, ma può essere riavviato in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="f65a7-146">The Job is stopped, but can be restarted in a seamless manner.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="f65a7-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (6)</span><span class="sxs-lookup"><span data-stu-id="f65a7-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f65a7-148">Lo stato del processo è' completed ',' terminate ' o ' Killed '.</span><span class="sxs-lookup"><span data-stu-id="f65a7-148">The job is moving to a 'Completed', 'Terminated', or 'Killed' state.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="f65a7-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (7)</span><span class="sxs-lookup"><span data-stu-id="f65a7-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f65a7-150">Il processo è stato completato normalmente.</span><span class="sxs-lookup"><span data-stu-id="f65a7-150">The job has completed normally.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="f65a7-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminata** (8)</span><span class="sxs-lookup"><span data-stu-id="f65a7-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f65a7-152">Il processo è stato interrotto da una richiesta di modifica dello stato ' terminate '.</span><span class="sxs-lookup"><span data-stu-id="f65a7-152">The job has been stopped by a 'Terminate' state change request.</span></span> <span data-ttu-id="f65a7-153">Il processo e tutti i processi sottostanti sono terminati e possono essere riavviati (specifici del processo) solo come nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="f65a7-153">The job and all its underlying processes are ended and can be restarted (this is job-specific) only as a new job.</span></span>

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span data-ttu-id="f65a7-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Terminata (9** )</span><span class="sxs-lookup"><span data-stu-id="f65a7-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Killed** (9)</span></span>


</dt> <dd>

<span data-ttu-id="f65a7-155">Il processo è stato interrotto da una richiesta di modifica dello stato ' Kill '.</span><span class="sxs-lookup"><span data-stu-id="f65a7-155">The job has been stopped by a 'Kill' state change request.</span></span> <span data-ttu-id="f65a7-156">I processi sottostanti potrebbero essere stati lasciati in esecuzione e la pulizia potrebbe essere necessaria per liberare risorse.</span><span class="sxs-lookup"><span data-stu-id="f65a7-156">Underlying processes might have been left running, and cleanup might be required to free up resources.</span></span>

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span data-ttu-id="f65a7-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Eccezione** (10)</span><span class="sxs-lookup"><span data-stu-id="f65a7-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Exception** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f65a7-158">Il processo è in uno stato anomalo che potrebbe essere indicativo di una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="f65a7-158">The Job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="f65a7-159">Lo stato effettivo potrebbe essere visualizzato anche se gli oggetti specifici del processo.</span><span class="sxs-lookup"><span data-stu-id="f65a7-159">Actual status might be displayed though job-specific objects.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f65a7-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (11)</span><span class="sxs-lookup"><span data-stu-id="f65a7-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="f65a7-161">Il processo è in uno stato specifico del fornitore che supporta l'individuazione o la risoluzione dei problemi o entrambi</span><span class="sxs-lookup"><span data-stu-id="f65a7-161">The Job is in a vendor-specific state that supports problem discovery, or resolution, or both</span></span>

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span data-ttu-id="f65a7-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Query in sospeso** (12)</span><span class="sxs-lookup"><span data-stu-id="f65a7-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Query Pending** (12)</span></span>


</dt> <dd>

<span data-ttu-id="f65a7-163">In attesa della risoluzione di una query da un client.</span><span class="sxs-lookup"><span data-stu-id="f65a7-163">Waiting for a client to resolve a query.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f65a7-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (13.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f65a7-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (13..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f65a7-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f65a7-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f65a7-166">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f65a7-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65a7-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f65a7-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f65a7-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f65a7-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f65a7-169">Qualificatori: [**obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f65a7-169">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f65a7-170">Nome descrittivo dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f65a7-170">The user-friendly name of the instance.</span></span> <span data-ttu-id="f65a7-171">Inoltre, è possibile utilizzare il nome descrittivo come proprietà per una ricerca o una query.</span><span class="sxs-lookup"><span data-stu-id="f65a7-171">In addition, the user-friendly name can be used as a property for a search or query.</span></span>

> [!Note]  
> <span data-ttu-id="f65a7-172">Non è necessario che il nome sia univoco all'interno dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f65a7-172">The name does not have to be unique within the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="f65a7-173">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="f65a7-173">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65a7-174">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f65a7-174">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f65a7-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f65a7-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f65a7-176">Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f65a7-176">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f65a7-177">Indica per quanto tempo viene mantenuto un processo completato.</span><span class="sxs-lookup"><span data-stu-id="f65a7-177">Indicates how long a completed job is retained.</span></span> <span data-ttu-id="f65a7-178">Il valore predefinito è "00000000000500.000000:000" (cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="f65a7-178">The default value is "00000000000500.000000:000" (five minutes).</span></span>

</dd> <dt>

<span data-ttu-id="f65a7-179">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="f65a7-179">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65a7-180">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f65a7-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f65a7-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f65a7-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f65a7-182">Data o ora dell'Ultima modifica apportata allo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="f65a7-182">The date or time when the state of the job last changed.</span></span>

> [!Note]  
> <span data-ttu-id="f65a7-183">Se lo stato del processo non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo zero.</span><span class="sxs-lookup"><span data-stu-id="f65a7-183">If the state of the Job has not changed and this property is populated, then it must be set to a zero interval value.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f65a7-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f65a7-184">Requirements</span></span>



| <span data-ttu-id="f65a7-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="f65a7-185">Requirement</span></span> | <span data-ttu-id="f65a7-186">Valore</span><span class="sxs-lookup"><span data-stu-id="f65a7-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f65a7-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f65a7-187">Minimum supported client</span></span><br/> | <span data-ttu-id="f65a7-188">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f65a7-188">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f65a7-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f65a7-189">Minimum supported server</span></span><br/> | <span data-ttu-id="f65a7-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f65a7-190">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f65a7-191">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f65a7-191">Namespace</span></span><br/>                | <span data-ttu-id="f65a7-192">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f65a7-192">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f65a7-193">MOF</span><span class="sxs-lookup"><span data-stu-id="f65a7-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f65a7-194"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f65a7-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f65a7-195">DLL</span><span class="sxs-lookup"><span data-stu-id="f65a7-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f65a7-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f65a7-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f65a7-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f65a7-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f65a7-198">**\_Processo CIM**</span><span class="sxs-lookup"><span data-stu-id="f65a7-198">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

