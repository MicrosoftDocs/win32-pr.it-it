---
description: Avvia la replica di una macchina virtuale.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Metodo StartReplication della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f774192cf5c65f6fff0d9a1a17df51483984b49efd6be437f0348547eed5082c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050491"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a>Metodo StartReplication della classe Msvm \_ ReplicationService

Avvia la replica di una macchina virtuale. Quando un client chiama questo metodo per una macchina virtuale di replica, avvia la replica con la replica estesa.

## <a name="syntax"></a>Sintassi


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Riferimento a [**un'istanza CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui deve essere avviata la replica.

</dd> <dt>

*InitialReplicationType* \[ Pollici\]
</dt> <dd>

Tipo di trasferimento da utilizzare per eseguire la replica iniziale.

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Trasferimento di** rete (1)


</dt> <dd>

Trasferimento di rete.

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Esportazione** (2)


</dt> <dd>

Esportazione.

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Seeded Network Transfer** (3)


</dt> <dd>

Trasferimento di rete con seed.

</dd> </dl> </dd> <dt>

*InitialReplicationExportLocation* \[ Pollici\]
</dt> <dd>

Se *InitialReplicationType* è 2 (Esportazione), questo parametro contiene il percorso completo della directory in cui deve essere esportata la replica iniziale. Questo parametro non viene usato per altri valori *di InitialReplicationType* e può essere **Null.** Questa directory può essere riutilizzata per l'esportazione di più repliche di macchine virtuali. Questo metodo inserisce ogni replica di macchine virtuali in una sottodirectory separata in questo percorso.

</dd> <dt>

*StartTime* \[ Pollici\]
</dt> <dd>

Ora di inizio pianificata per la replica iniziale tramite la connessione di rete al server di ripristino. Questo parametro viene ignorato *quando InitialReplicationType* è 2 (Esportazione). Se questo parametro è **Null,** la replica iniziale viene avviata immediatamente.

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
</dt> </dl>

 

