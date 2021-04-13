---
description: Rappresenta una raccolta di sistemi virtuali.
ms.assetid: acf51beb-1103-43a4-8dc5-1a7f2a0482be
title: Classe Msvm_VirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCollection
- Msvm_VirtualSystemCollection.CollectionID
- Msvm_VirtualSystemCollection.ElementName
- Msvm_VirtualSystemCollection.LastApplyConsistencyLevel
- Msvm_VirtualSystemCollection.LastApplyVirtualMachineIds
- Msvm_VirtualSystemCollection.LastApplyTime
- Msvm_VirtualSystemCollection.FailedOverReplicationType
- Msvm_VirtualSystemCollection.ReplicationMode
- Msvm_VirtualSystemCollection.ReplicationState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a9746356744f2743a8d6656ef4c61044223be113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401610"
---
# <a name="msvm_virtualsystemcollection-class"></a><span data-ttu-id="5b142-103">\_Classe MSVM VirtualSystemCollection</span><span class="sxs-lookup"><span data-stu-id="5b142-103">Msvm\_VirtualSystemCollection class</span></span>

<span data-ttu-id="5b142-104">Rappresenta una raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="5b142-104">Represents a collection of virtual systems.</span></span>

<span data-ttu-id="5b142-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5b142-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b142-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b142-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCollection : CIM_CollectionOfMSEs
{
  string   CollectionID;
  string   ElementName;
  uint16   LastApplyConsistencyLevel;
  String   LastApplyVirtualMachineIds[];
  DateTime LastApplyTime;
  uint16   FailedOverReplicationType;
  uint16   ReplicationMode;
  uint16   ReplicationState;
};
```

## <a name="members"></a><span data-ttu-id="5b142-107">Members</span><span class="sxs-lookup"><span data-stu-id="5b142-107">Members</span></span>

<span data-ttu-id="5b142-108">La **classe \_ VirtualSystemCollection di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5b142-108">The **Msvm\_VirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="5b142-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b142-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b142-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b142-110">Properties</span></span>

<span data-ttu-id="5b142-111">La **classe \_ VirtualSystemCollection di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b142-111">The **Msvm\_VirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b142-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="5b142-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b142-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5b142-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b142-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b142-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b142-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5b142-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b142-116">Identificazione univoca dell'oggetto raccolta.</span><span class="sxs-lookup"><span data-stu-id="5b142-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="5b142-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5b142-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b142-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5b142-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b142-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b142-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b142-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="5b142-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="5b142-121">Nome definito dall'utente per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="5b142-121">An user-defined name for the collection.</span></span> <span data-ttu-id="5b142-122">Si noti che non è garantito che sia univoco.</span><span class="sxs-lookup"><span data-stu-id="5b142-122">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="5b142-123">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="5b142-123">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b142-124">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b142-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b142-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b142-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b142-126">Tipo di failover eseguito per la raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="5b142-126">Type of failover that was performed for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="5b142-127">Aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="5b142-127">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="5b142-128">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="5b142-128">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="5b142-129">**Normale** (1)</span><span class="sxs-lookup"><span data-stu-id="5b142-129">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="5b142-130">**Pianificato** (2)</span><span class="sxs-lookup"><span data-stu-id="5b142-130">**Planned** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b142-131">**LastApplyConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="5b142-131">**LastApplyConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b142-132">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b142-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b142-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b142-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b142-134">Livello di coerenza dell'ultimo Delta applicato.</span><span class="sxs-lookup"><span data-stu-id="5b142-134">Consistency level of the last applied delta.</span></span>

> [!Note]  
> <span data-ttu-id="5b142-135">Aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="5b142-135">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5b142-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5b142-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="5b142-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coerente** con l'applicazione (1)</span><span class="sxs-lookup"><span data-stu-id="5b142-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5b142-138">L'ultimo Delta applicato indica un punto nel tempo in cui il sistema virtuale era in uno stato coerente con l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5b142-138">The last applied delta indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="5b142-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coerente con l'arresto anomalo** (2)</span><span class="sxs-lookup"><span data-stu-id="5b142-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5b142-140">L'ultimo Delta applicato indica un punto nel tempo in cui il sistema virtuale si trova in uno stato di arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="5b142-140">The last applied delta indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>

<span data-ttu-id="5b142-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Coerente con l'arresto anomalo del gruppo** (3)</span><span class="sxs-lookup"><span data-stu-id="5b142-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Group Crash Consistent** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5b142-142">L'ultimo Delta applicato indica un momento in cui il gruppo si trova in uno stato di arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="5b142-142">The last applied delta indicates a point in time when the group was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5b142-143">**LastApplyTime**</span><span class="sxs-lookup"><span data-stu-id="5b142-143">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b142-144">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5b142-144">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="5b142-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b142-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b142-146">Ora in cui viene applicata l'ultima replica al recupero per la raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="5b142-146">The time at which the last replication is applied on recovery for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="5b142-147">Aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="5b142-147">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="5b142-148">**LastApplyVirtualMachineIds**</span><span class="sxs-lookup"><span data-stu-id="5b142-148">**LastApplyVirtualMachineIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b142-149">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5b142-149">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="5b142-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b142-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b142-151">Matrice di ID di macchina virtuale che sono stati applicati correttamente nell'ultimo ciclo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="5b142-151">Array of Virtual Machine Ids which were successfully applied in last apply cycle.</span></span>

> [!Note]  
> <span data-ttu-id="5b142-152">Aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="5b142-152">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="5b142-153">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="5b142-153">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b142-154">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b142-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b142-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b142-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b142-156">Tipo di replica per la raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="5b142-156">Replication type for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="5b142-157">Aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="5b142-157">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="5b142-158">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="5b142-158">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="5b142-159">**Primario** (1)</span><span class="sxs-lookup"><span data-stu-id="5b142-159">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="5b142-160">**Replica** (2)</span><span class="sxs-lookup"><span data-stu-id="5b142-160">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="5b142-161">**Replica di test** (3)</span><span class="sxs-lookup"><span data-stu-id="5b142-161">**Test Replica** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b142-162">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="5b142-162">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b142-163">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b142-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b142-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b142-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b142-165">Stato di replica per la raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="5b142-165">Replication state for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="5b142-166">Aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="5b142-166">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5b142-167">**Disabilitato** (0)</span><span class="sxs-lookup"><span data-stu-id="5b142-167">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="5b142-168">**Pronto per la replica** (1)</span><span class="sxs-lookup"><span data-stu-id="5b142-168">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="5b142-169">**In attesa del completamento della replica iniziale** (2)</span><span class="sxs-lookup"><span data-stu-id="5b142-169">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="5b142-170">**Replica** in corso (3)</span><span class="sxs-lookup"><span data-stu-id="5b142-170">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_initiated"></span><span id="failover_initiated"></span><span id="FAILOVER_INITIATED"></span>

<span data-ttu-id="5b142-171">**Failover avviato** (4)</span><span class="sxs-lookup"><span data-stu-id="5b142-171">**Failover initiated** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="5b142-172">**Ripristino** (5)</span><span class="sxs-lookup"><span data-stu-id="5b142-172">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="5b142-173">**Commit eseguito** (6)</span><span class="sxs-lookup"><span data-stu-id="5b142-173">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="5b142-174">**Sospeso** (7)</span><span class="sxs-lookup"><span data-stu-id="5b142-174">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="5b142-175">**Critico** (8)</span><span class="sxs-lookup"><span data-stu-id="5b142-175">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="5b142-176">**In attesa dell'avvio della risincronizzazione** (9)</span><span class="sxs-lookup"><span data-stu-id="5b142-176">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="5b142-177">**Risincronizzazione** (10)</span><span class="sxs-lookup"><span data-stu-id="5b142-177">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned_failover_initiatedRepurpose_initiatedTest_failover_initiatedPartially_enabled"></span><span id="planned_failover_initiatedrepurpose_initiatedtest_failover_initiatedpartially_enabled"></span><span id="PLANNED_FAILOVER_INITIATEDREPURPOSE_INITIATEDTEST_FAILOVER_INITIATEDPARTIALLY_ENABLED"></span>

<span data-ttu-id="5b142-178">**Failover pianificato InitiatedRepurpose initiatedTest failover initiatedPartially abilitato** (11)</span><span class="sxs-lookup"><span data-stu-id="5b142-178">**Planned failover initiatedRepurpose initiatedTest failover initiatedPartially enabled** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_disabled"></span><span id="partially_disabled"></span><span id="PARTIALLY_DISABLED"></span>

<span data-ttu-id="5b142-179">**Parzialmente disabilitato** (12)</span><span class="sxs-lookup"><span data-stu-id="5b142-179">**Partially disabled** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_recovered"></span><span id="partially_recovered"></span><span id="PARTIALLY_RECOVERED"></span>

<span data-ttu-id="5b142-180">**Parzialmente recuperato** (13)</span><span class="sxs-lookup"><span data-stu-id="5b142-180">**Partially recovered** (13)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5b142-181">(14)</span><span class="sxs-lookup"><span data-stu-id="5b142-181">(14)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5b142-182">(15)</span><span class="sxs-lookup"><span data-stu-id="5b142-182">(15)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5b142-183">(16)</span><span class="sxs-lookup"><span data-stu-id="5b142-183">(16)</span></span>


<span data-ttu-id="5b142-184"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5b142-184"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5b142-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b142-185">Requirements</span></span>



| <span data-ttu-id="5b142-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b142-186">Requirement</span></span> | <span data-ttu-id="5b142-187">Valore</span><span class="sxs-lookup"><span data-stu-id="5b142-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b142-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b142-188">Minimum supported client</span></span><br/> | <span data-ttu-id="5b142-189">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5b142-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5b142-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b142-190">Minimum supported server</span></span><br/> | <span data-ttu-id="5b142-191">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5b142-191">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5b142-192">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5b142-192">Namespace</span></span><br/>                | <span data-ttu-id="5b142-193">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5b142-193">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5b142-194">MOF</span><span class="sxs-lookup"><span data-stu-id="5b142-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b142-195"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b142-195"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b142-196">DLL</span><span class="sxs-lookup"><span data-stu-id="5b142-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b142-197"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b142-197"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5b142-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b142-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b142-199">**\_COLLECTIONOFMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="5b142-199">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

