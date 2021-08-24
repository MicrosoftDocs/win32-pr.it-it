---
description: Rappresenta lo stato di replica per una relazione di replica.
ms.assetid: F11EFF86-5CC9-4310-8254-B310C54B561D
title: Msvm_ReplicationRelationship classe
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
ms.openlocfilehash: c8ff905475863df11c6fb6529f030f73a4f1b785792be4c5fe8c7ce1142096c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068481"
---
# <a name="msvm_replicationrelationship-class"></a>Classe Msvm \_ ReplicationRelationship

Rappresenta lo stato di replica per una relazione di replica. Poiché è possibile avere più repliche per ogni macchina virtuale di replica, è possibile usare questa classe per identificare ogni relazione di replica.

La sintassi seguente è semplificata dal codice MOF e include queste proprietà ereditate.

## <a name="syntax"></a>Sintassi

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

## <a name="members"></a>Members

La **classe Msvm \_ ReplicationRelationship** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ReplicationRelationship** ha queste proprietà.

<dl> <dt>

**FailedOverReplicationType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di failover eseguito per la relazione di replica.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normale** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Coerente con l'applicazione** (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Pianificato** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica la relazione di replica. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

Questa proprietà ha il formato seguente:

**Microsoft: <vmid> \\ HVR \\<0/1>**

0 indica la replica primaria e 1 indica [la replica estesa.](#extended-replication)

</dd> <dt>

**LastApplicationConsistentReplicationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora in cui l'ultima replica coerente dell'applicazione viene ricevuta al ripristino per la relazione di replica.

</dd> <dt>

**LastApplyTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora in cui viene applicata l'ultima replica al ripristino per la relazione di replica.

</dd> <dt>

**LastReplicationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora in cui viene ricevuta l'ultima replica al momento del ripristino per la relazione di replica.

</dd> <dt>

**LastReplicationType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo dell'ultima replica ricevuta per la relazione di replica.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normale** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Coerente con l'applicazione** (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Pianificato** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Replicationhealth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integrità della replica per la relazione di replica.

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**Ok** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Avviso** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critico** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato della replica per la relazione di replica.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Pronto per la replica** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**In attesa del completamento della replica iniziale** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replica** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replica sincronizzata completata** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recuperato** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Commit** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Sospeso** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**In attesa di avviare la risincronizzazione** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Risincronizzazione** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Risincronizzazione sospesa** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in corso** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in corso** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback completato** (14)


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Aggiornamento del disco in corso** (15)


</dt> <dd>

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 versione 1703.

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Aggiornamento del disco critico** (16)


</dt> <dd>

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 versione 1703.

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (17)


</dt> <dd>

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 versione 1703.

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Riuso della replica in corso** (18)


</dt> <dd>

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 versione 1703.

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Preparato per la replica di sincronizzazione** (19)


</dt> <dd>

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 versione 1703.

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Preparato per la replica inversa di** gruppo (20)


</dt> <dd>

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 versione 1703.

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in corso** (21)


</dt> <dd>

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 versione 1703.

 

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

### <a name="extended-replication"></a>Replica estesa

La funzionalità di replica Hyper-V in Windows 8 consente alle macchine virtuali eseguite in un server Hyper-V nel sito primario di essere replicate in modo efficiente in un altro server Hyper-V nel sito secondario.

La funzionalità di replica Hyper-V in Windows 8.1 consente a un utente di estendere la relazione di replica dal sito secondario in poi a un terzo sito. Il terzo sito può essere un host Hyper-V di cui è stato eseguito il pre-provisioning come server di ripristino o provider di replica esterno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dt>

[**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

