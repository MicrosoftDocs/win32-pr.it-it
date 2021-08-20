---
description: Crea una nuova relazione di replica per una macchina virtuale. Quando un client chiama questo metodo per una macchina virtuale di replica, estende la relazione di replica al provider specificato.
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
ms.openlocfilehash: d9b61c2339a426314d5c62fe5481b51ba3960c2650ccbdc40b9b9ebd4761cfc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150084"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a>Metodo CreateReplicationRelationship della classe Msvm \_ ReplicationService

Crea una nuova relazione di replica per una macchina virtuale. Quando un client chiama questo metodo per una macchina virtuale di replica, estende la relazione di replica al provider specificato.

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

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Riferimento a [**un'istanza di CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui deve essere abilitata la replica.

</dd> <dt>

*ReplicationSettingData* \[ Pollici\]
</dt> <dd>

Rappresentazione di stringa di un'istanza della [**classe Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) che definisce le impostazioni di replica per la nuova relazione di replica da creare per la macchina virtuale.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Operazione non** riuscita (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Lo stato è sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non** valido (32773)
</dt> <dt>

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> <dt>

**File non trovato** (32779)
</dt> </dl>

## <a name="remarks"></a>Commenti

**CreateReplicationRelationship** accetta [**un'istanza \_ msvm ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) come input. Il file FRSD associato per la macchina virtuale come provider da host a host è la scelta predefinita. Il file FRSD di input viene convalidato per le impostazioni valide per ogni proprietà per il provider predefinito. Questa tabella riepiloga le differenze di convalida rispetto al provider esterno.



| Proprietà                                             | Provider esterni                                 |
|------------------------------------------------------|----------------------------------------------------|
| ReplicationProvider                                  | Uguale al provider predefinito                           |
| AuthenticationType                                   | Ignorato                                            |
| CertificateThumbPrint                                | Ignorato                                            |
| RootCertificateThumbPrint (RO)                       | Ignorato                                            |
| CompressionEnabled                                   | Uguale al provider predefinito                           |
| BypassProxyServer                                    | Uguale al provider predefinito                           |
| RecoveryConnectionPoint                              | Ignorato \* (può cambiare se il provider ha un requisito) |
| RecoveryHostSystem (RO)                              | Ignorato                                            |
| PrimaryConnectionPoint (RO)                          | Uguale al provider predefinito                           |
| PrimaryHostSystem (RO)                               | Uguale al provider predefinito                           |
| RecoveryServerPortNumber                             | Ignorato \* (può cambiare se il provider ha un requisito) |
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
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> <dt>

[**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

