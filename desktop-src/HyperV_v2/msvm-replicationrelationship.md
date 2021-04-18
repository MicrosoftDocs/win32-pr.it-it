---
description: Rappresenta lo stato della replica per una relazione di replica.
ms.assetid: F11EFF86-5CC9-4310-8254-B310C54B561D
title: Classe Msvm_ReplicationRelationship
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationRelationship
- Msvm_ReplicationRelationship.InstanceID
- Msvm_ReplicationRelationship.ReplicationState
- Msvm_ReplicationRelationship.ReplicationHealth
- Msvm_ReplicationRelationship.FailedOverReplicationType
- Msvm_ReplicationRelationship.LastReplicationType
- Msvm_ReplicationRelationship.LastApplicationConsistentReplicationTime
- Msvm_ReplicationRelationship.LastReplicationTime
- Msvm_ReplicationRelationship.LastApplyTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04665f96f4ec77501ee0b161d816c84943ca2c98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312894"
---
# <a name="msvm_replicationrelationship-class"></a><span data-ttu-id="3665a-103">\_Classe MSVM ReplicationRelationship</span><span class="sxs-lookup"><span data-stu-id="3665a-103">Msvm\_ReplicationRelationship class</span></span>

<span data-ttu-id="3665a-104">Rappresenta lo stato della replica per una relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="3665a-104">Represents replication status for a replication relationship.</span></span> <span data-ttu-id="3665a-105">Poiché è possibile avere più repliche per ogni macchina virtuale di replica, è possibile usare questa classe per identificare ogni relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="3665a-105">Because you can have multiple replications for each replica virtual machine, you can use this class to identify each replication relationship.</span></span>

<span data-ttu-id="3665a-106">La sintassi seguente è semplificata dal codice MOF e include queste proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3665a-106">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3665a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3665a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationRelationship : CIM_ManagedSystemElement
{
  string   InstanceID;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  datetime LastApplicationConsistentReplicationTime;
  datetime LastReplicationTime;
  datetime LastApplyTime;
};
```

## <a name="members"></a><span data-ttu-id="3665a-108">Members</span><span class="sxs-lookup"><span data-stu-id="3665a-108">Members</span></span>

<span data-ttu-id="3665a-109">La **classe \_ ReplicationRelationship di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3665a-109">The **Msvm\_ReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="3665a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3665a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3665a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3665a-111">Properties</span></span>

<span data-ttu-id="3665a-112">La **classe \_ ReplicationRelationship di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3665a-112">The **Msvm\_ReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3665a-113">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="3665a-113">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3665a-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3665a-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3665a-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3665a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3665a-116">Tipo di failover eseguito per la relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="3665a-116">The type of failover that was performed for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="3665a-117">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="3665a-117">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="3665a-118">**Normale** (1)</span><span class="sxs-lookup"><span data-stu-id="3665a-118">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="3665a-119">**Coerente** con l'applicazione (2)</span><span class="sxs-lookup"><span data-stu-id="3665a-119">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="3665a-120">**Pianificato** (3)</span><span class="sxs-lookup"><span data-stu-id="3665a-120">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3665a-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3665a-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3665a-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3665a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3665a-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3665a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3665a-124">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="3665a-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="3665a-125">Identifica la relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="3665a-125">Identifies replication relationship.</span></span> <span data-ttu-id="3665a-126">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3665a-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="3665a-127">Il formato di questa proprietà è il seguente:</span><span class="sxs-lookup"><span data-stu-id="3665a-127">This property has this format:</span></span>

<span data-ttu-id="3665a-128">**Microsoft: <vmid> \\ HVR \\<0/1>**</span><span class="sxs-lookup"><span data-stu-id="3665a-128">**Microsoft:<vmid>\\HVR\\<0/1>**</span></span>

<span data-ttu-id="3665a-129">0 indica primario e 1 indica la [replica estesa](#extended-replication).</span><span class="sxs-lookup"><span data-stu-id="3665a-129">0 indicates primary and 1 indicates [extended replication](#extended-replication).</span></span>

</dd> <dt>

<span data-ttu-id="3665a-130">**LastApplicationConsistentReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="3665a-130">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3665a-131">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3665a-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3665a-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3665a-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3665a-133">Data e ora in cui l'ultima replica coerente con l'applicazione viene ricevuta durante il ripristino per la relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="3665a-133">The date and time at which the last application consistent replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="3665a-134">**LastApplyTime**</span><span class="sxs-lookup"><span data-stu-id="3665a-134">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3665a-135">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3665a-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3665a-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3665a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3665a-137">Data e ora in cui l'ultima replica viene applicata al recupero per la relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="3665a-137">The date and time at which the last replication is applied on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="3665a-138">**LastReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="3665a-138">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3665a-139">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3665a-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3665a-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3665a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3665a-141">Data e ora in cui l'ultima replica viene ricevuta durante il ripristino per la relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="3665a-141">The date and time at which the last replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="3665a-142">**LastReplicationType**</span><span class="sxs-lookup"><span data-stu-id="3665a-142">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3665a-143">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3665a-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3665a-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3665a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3665a-145">Tipo dell'ultima replica ricevuta per la relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="3665a-145">The type of the last replication that was received for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="3665a-146">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="3665a-146">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="3665a-147">**Normale** (1)</span><span class="sxs-lookup"><span data-stu-id="3665a-147">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="3665a-148">**Coerente** con l'applicazione (2)</span><span class="sxs-lookup"><span data-stu-id="3665a-148">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="3665a-149">**Pianificato** (3)</span><span class="sxs-lookup"><span data-stu-id="3665a-149">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3665a-150">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="3665a-150">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3665a-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3665a-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3665a-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3665a-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3665a-153">Integrità della replica per la relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="3665a-153">Replication health for the replication relationship.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3665a-154">**Non applicabile** (0)</span><span class="sxs-lookup"><span data-stu-id="3665a-154">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="3665a-155">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="3665a-155">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="3665a-156">**Avviso** (2)</span><span class="sxs-lookup"><span data-stu-id="3665a-156">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="3665a-157">**Critico** (3)</span><span class="sxs-lookup"><span data-stu-id="3665a-157">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3665a-158">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="3665a-158">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3665a-159">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3665a-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3665a-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3665a-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3665a-161">Stato di replica per la relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="3665a-161">Replication state for the replication relationship.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3665a-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (0)</span><span class="sxs-lookup"><span data-stu-id="3665a-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="3665a-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Pronto per la replica** (1)</span><span class="sxs-lookup"><span data-stu-id="3665a-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="3665a-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**In attesa del completamento della replica iniziale** (2)</span><span class="sxs-lookup"><span data-stu-id="3665a-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="3665a-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replica** in corso (3)</span><span class="sxs-lookup"><span data-stu-id="3665a-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="3665a-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replica sincronizzata completata** (4)</span><span class="sxs-lookup"><span data-stu-id="3665a-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="3665a-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Ripristino** (5)</span><span class="sxs-lookup"><span data-stu-id="3665a-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="3665a-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Commit eseguito** (6)</span><span class="sxs-lookup"><span data-stu-id="3665a-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="3665a-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Sospeso** (7)</span><span class="sxs-lookup"><span data-stu-id="3665a-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="3665a-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (8)</span><span class="sxs-lookup"><span data-stu-id="3665a-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="3665a-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**In attesa dell'avvio della risincronizzazione** (9)</span><span class="sxs-lookup"><span data-stu-id="3665a-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="3665a-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Risincronizzazione** (10)</span><span class="sxs-lookup"><span data-stu-id="3665a-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="3665a-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Risincronizzazione sospesa** (11)</span><span class="sxs-lookup"><span data-stu-id="3665a-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="3665a-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in corso** (12)</span><span class="sxs-lookup"><span data-stu-id="3665a-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="3665a-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in corso** (13)</span><span class="sxs-lookup"><span data-stu-id="3665a-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="3665a-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback completato** (14)</span><span class="sxs-lookup"><span data-stu-id="3665a-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="3665a-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Aggiornamento del disco in corso** (15)</span><span class="sxs-lookup"><span data-stu-id="3665a-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="3665a-178">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="3665a-178">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="3665a-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Aggiornamento del disco critico** (16)</span><span class="sxs-lookup"><span data-stu-id="3665a-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="3665a-180">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="3665a-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3665a-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (17)</span><span class="sxs-lookup"><span data-stu-id="3665a-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="3665a-182">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="3665a-182">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="3665a-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Riutilizzo della replica in corso** (18)</span><span class="sxs-lookup"><span data-stu-id="3665a-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="3665a-184">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="3665a-184">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="3665a-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Preparato per la replica di sincronizzazione** (19)</span><span class="sxs-lookup"><span data-stu-id="3665a-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="3665a-186">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="3665a-186">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="3665a-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Preparato per la replica inversa del gruppo** (20)</span><span class="sxs-lookup"><span data-stu-id="3665a-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="3665a-188">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="3665a-188">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="3665a-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**FireDrill in corso** (21)</span><span class="sxs-lookup"><span data-stu-id="3665a-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="3665a-190">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="3665a-190">This property was added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3665a-191">Commenti</span><span class="sxs-lookup"><span data-stu-id="3665a-191">Remarks</span></span>

### <a name="extended-replication"></a><span data-ttu-id="3665a-192">Replica estesa</span><span class="sxs-lookup"><span data-stu-id="3665a-192">Extended replication</span></span>

<span data-ttu-id="3665a-193">La funzionalità di replica Hyper-V in Windows 8 consente la replica efficiente delle macchine virtuali in esecuzione in un server Hyper-V nel sito primario in un altro server Hyper-V nel sito secondario.</span><span class="sxs-lookup"><span data-stu-id="3665a-193">The Hyper-V replication feature in Windows 8 allows virtual machines that run on a Hyper-V server at the primary site to be efficiently replicated to another Hyper-V server at the secondary site.</span></span>

<span data-ttu-id="3665a-194">La funzionalità di replica Hyper-V in Windows 8.1 consente a un utente di estendere la relazione di replica dal sito secondario a un terzo sito.</span><span class="sxs-lookup"><span data-stu-id="3665a-194">The Hyper-V replication feature in Windows 8.1 enables a user to extend the replication relationship from the secondary site onwards to a third site.</span></span> <span data-ttu-id="3665a-195">Il terzo sito può essere un host Hyper-V di cui è stato eseguito il pre-provisioning come un server di ripristino o un provider di replica esterno.</span><span class="sxs-lookup"><span data-stu-id="3665a-195">The third site can be a Hyper-V host pre-provisioned as a recovery server or external replication provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="3665a-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3665a-196">Requirements</span></span>



| <span data-ttu-id="3665a-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="3665a-197">Requirement</span></span> | <span data-ttu-id="3665a-198">Valore</span><span class="sxs-lookup"><span data-stu-id="3665a-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3665a-199">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3665a-199">Minimum supported client</span></span><br/> | <span data-ttu-id="3665a-200">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3665a-200">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3665a-201">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3665a-201">Minimum supported server</span></span><br/> | <span data-ttu-id="3665a-202">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3665a-202">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3665a-203">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3665a-203">Namespace</span></span><br/>                | <span data-ttu-id="3665a-204">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3665a-204">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3665a-205">MOF</span><span class="sxs-lookup"><span data-stu-id="3665a-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3665a-206"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3665a-206"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3665a-207">DLL</span><span class="sxs-lookup"><span data-stu-id="3665a-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3665a-208"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3665a-208"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3665a-209">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3665a-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3665a-210">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3665a-210">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="3665a-211">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3665a-211">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

