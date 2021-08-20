---
description: Modifica le impostazioni di replica per una macchina virtuale. Quando un client chiama questo metodo per una macchina virtuale di replica, modifica le impostazioni di replica della relazione di replica con la replica estesa.
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Metodo ModifyReplicationSettings della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyReplicationSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ed9e490ecc0eec1dcb4f6549281631f0b43e855ad4fb825b6c07517abe26a6c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149534"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a>Metodo ModifyReplicationSettings della classe Msvm \_ ReplicationService

Modifica le impostazioni di replica per una macchina virtuale. Quando un client chiama questo metodo per una macchina virtuale di replica, modifica le impostazioni di replica della relazione di replica con la replica estesa.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifyReplicationSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Riferimento a [**un'istanza \_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui devono essere modificate le impostazioni di replica.

</dd> <dt>

*ReplicationSettingData* \[ Pollici\]
</dt> <dd>

Rappresentazione di stringa della [**classe Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) che definisce le nuove impostazioni di replica.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
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

**Il sistema è in uso** (32774)
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

**ModifyReplicationSettings** accetta [**un'istanza \_ msvm ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) come input. Il frsd associato per la macchina virtuale come provider da host a host è la scelta predefinita. Il file FRSD di input viene convalidato per verificare la validità delle impostazioni per ogni proprietà per il provider predefinito. In questa tabella vengono riepilogate le differenze di convalida rispetto al provider esterno.



| Proprietà                                             | Provider esterni                                 |
|------------------------------------------------------|----------------------------------------------------|
| Provider di replica                                  | Uguale al provider predefinito                           |
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
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

