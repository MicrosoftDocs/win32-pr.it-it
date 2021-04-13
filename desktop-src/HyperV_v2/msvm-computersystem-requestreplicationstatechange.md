---
description: Richiede che lo stato di replica della macchina virtuale venga modificato in base al valore specificato e agisca sulla relazione di replica primaria della macchina virtuale.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Metodo RequestReplicationStateChange della classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528531"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a>Metodo RequestReplicationStateChange della classe MSVM \_ ComputerSystem

Richiede che lo stato di replica della macchina virtuale venga modificato in base al valore specificato e agisca sulla relazione di replica primaria della macchina virtuale. Mentre è in corso la modifica dello stato, la proprietà **ReplicationState** viene modificata nel valore del parametro *RequestedState* . Questo metodo è supportato solo per le istanze della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresentano una macchina virtuale.

> [!Note]  
> A partire da Windows 8.1, è consigliabile non usare più **RequestReplicationStateChange** per richiedere la modifica dello stato di replica. Usare invece [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).

 

## <a name="syntax"></a>Sintassi


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RequestedState* \[ in\]
</dt> <dd>

Nuovo stato di replica. Deve essere uno dei valori seguenti.

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Pronto per l'avvio della replica iniziale** (1)


</dt> <dd>

Pronto per avviare la replica iniziale.

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**In attesa del completamento della replica iniziale** (2)


</dt> <dd>

In attesa del completamento della replica iniziale.

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replica** in corso (3)


</dt> <dd>

replica in corso.

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replica sincronizzata completata** (4)


</dt> <dd>

Replica sincronizzata completata.

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (7)


</dt> <dd>

Sospendere la replica.

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Annulla risincronizzazione** (9)


</dt> <dd>

Annulla la risincronizzazione.

</dd> </dl> </dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Riferimento facoltativo a un oggetto [**MSVM \_ ConcreteJob**](msvm-concretejob.md) restituito se l'operazione viene eseguita in modo asincrono. Se presente, il riferimento restituito può essere usato per monitorare lo stato di avanzamento e ottenere il risultato del metodo.

</dd> <dt>

*TimeoutPeriod* \[ in\]
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                                                | Descrizione                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completato senza errori**</dt> <dt>0</dt> </dl>                    | Operazione riuscita<br/>                                                                                                          |
| <dl> <dt>**Parametri del metodo controllati-processo avviato**</dt> <dt>4096</dt> </dl> | La transizione è asincrona.<br/>                                                                                  |
| <dl> <dt>**Errore**</dt> <dt>32768</dt> </dl>                                 |                                                                                                                             |
| <dl> <dt>**Accesso negato**</dt> <dt>32769</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Non supportato**</dt> <dt>32770</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Stato sconosciuto**</dt> <dt>32771</dt> </dl>                      |                                                                                                                             |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                |                                                                                                                             |
| <dl> <dt>**Parametro non valido**</dt> <dt>32773</dt> </dl>                      | Il valore specificato in uno dei parametri non è supportato.<br/>                                                   |
| <dl> Il <dt>**sistema è in uso**</dt> <dt>32774</dt> </dl>                       |                                                                                                                             |
| <dl> <dt>**Stato non valido per l'operazione**</dt> <dt>32775</dt> </dl>       | Il valore specificato nel parametro *RequestedState* non è supportato nella modalità o nello stato di replica corrente.<br/> |
| <dl> <dt>**Tipo di dati non corretto**</dt> <dt>32776</dt> </dl>                    |                                                                                                                             |
| <dl> Il <dt>**sistema non è disponibile**</dt> <dt>32777</dt> </dl>                |                                                                                                                             |
| <dl> <dt>**Memoria insufficiente**</dt> <dt>32778</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**File non trovato**</dt> <dt>32779</dt> </dl>                         |                                                                                                                             |



 

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

[**\_ComputerSystem MSVM**](msvm-computersystem.md)
</dt> </dl>

 

 




