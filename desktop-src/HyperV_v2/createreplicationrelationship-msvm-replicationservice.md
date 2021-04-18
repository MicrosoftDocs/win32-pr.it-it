---
description: Crea una nuova relazione di replica per una macchina virtuale. Quando un client chiama questo metodo per una macchina virtuale di replica, estende la relazione di replica con il provider specificato.
ms.assetid: 44d3b5aa-46c2-4fe9-9a1d-6ee699d3640d
title: Metodo CreateReplicationRelationship della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CreateReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c44628aef9aa278170a1292a74621419bb6256b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314345"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a>Metodo CreateReplicationRelationship della classe MSVM \_ ReplicationService

Crea una nuova relazione di replica per una macchina virtuale. Quando un client chiama questo metodo per una macchina virtuale di replica, estende la relazione di replica con il provider specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ in\]
</dt> <dd>

Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui deve essere abilitata la replica.

</dd> <dt>

*ReplicationSettingData* \[ in\]
</dt> <dd>

Rappresentazione in forma di stringa di un'istanza della classe [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) che definisce le impostazioni di replica per la nuova relazione di replica da creare per la macchina virtuale.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Stato sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

Il **sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> <dt>

**File non trovato** (32779)
</dt> </dl>

## <a name="remarks"></a>Commenti

**CreateReplicationRelationship** accetta un'istanza di [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) come input. Il FRSD associato per la macchina virtuale come provider da host a host è la scelta predefinita. FRSD di input viene convalidato per le impostazioni valide per ogni proprietà del provider predefinito. In questa tabella vengono riepilogate le differenze di convalida rispetto al provider esterno.



| Proprietà                                             | Provider esterni                                 |
|------------------------------------------------------|----------------------------------------------------|
| ReplicationProvider                                  | Uguale al provider predefinito                           |
| AuthenticationType                                   | Ignorato                                            |
| CertificateThumbPrint                                | Ignorato                                            |
| RootCertificateThumbPrint (RO)                       | Ignorato                                            |
| CompressionEnabled                                   | Uguale al provider predefinito                           |
| BypassProxyServer                                    | Uguale al provider predefinito                           |
| RecoveryConnectionPoint                              | Ignorato \* (può cambiare se il provider ha requisito) |
| RecoveryHostSystem (RO)                              | Ignorato                                            |
| PrimaryConnectionPoint (RO)                          | Uguale al provider predefinito                           |
| PrimaryHostSystem (RO)                               | Uguale al provider predefinito                           |
| RecoveryServerPortNumber                             | Ignorato \* (può cambiare se il provider ha requisito) |
| ReplicateHostKvpItems                                | Ignorato                                            |
| ApplicationConsistentSnapshotInterval                | Uguale al provider predefinito                           |
| RecoveryHistory                                      | Uguale al provider predefinito                           |
| IncludedDisks\[\]                                    | Uguale al provider predefinito                           |
| AutoResynchronizeEnabled                             | Uguale al provider predefinito                           |
| AutoResynchronizeIntervalStart                       | Uguale al provider predefinito                           |
| AutoResynchronizeIntervalEnd                         | Uguale al provider predefinito                           |
| EnableWriteOrderPreservationAcrossDisks (deprecato) | Uguale al provider predefinito                           |
| ReplicationInterval                                  | Uguale al provider predefinito                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ReplicationService MSVM**](msvm-replicationservice.md)
</dt> <dt>

[**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

