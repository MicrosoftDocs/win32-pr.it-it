---
description: Recupera le statistiche di replica associate alla relazione di replica specificata della macchina virtuale.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: Msvm_ReplicationService::GetReplicationStatisticsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d4386692dcaf86527e28b82c91415bf858b47cd19bbc4693af6bff12255138c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253701"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a>Metodo Msvm \_ ReplicationService::GetReplicationStatisticsEx

Recupera le statistiche di replica associate alla relazione di replica specificata della macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Riferimento a [**un'istanza CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui recuperare le statistiche di replica.

</dd> <dt>

*ReplicaRelationship* \[ Pollici\]
</dt> <dd>

Rappresentazione di stringa di un'istanza incorporata della [**classe Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) che definisce la relazione di replica per cui recuperare le statistiche di replica.

</dd> <dt>

*ReplicationStatistics* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, riceve un'istanza incorporata della [**classe Msvm \_ ReplicationStatistics**](msvm-replicationstatistics.md) che contiene le statistiche di replica per la relazione di replica richiesta.

</dd> <dt>

*ReplicationHealthIssues* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, riceve una matrice di istanze incorporate della [**classe Msvm \_ Error**](msvm-error.md) che indicano eventuali avvisi o errori di replica per la macchina virtuale richiesta.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)). Questo riferimento può essere **NULL se** l'attività è stata completata.

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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\Virtualizzazione \\ radice \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> <dt>

[**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

