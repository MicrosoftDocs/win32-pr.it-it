---
description: Reimposta le statistiche di replica per una macchina virtuale e agisce sulla relazione di replica primaria della macchina virtuale.
ms.assetid: da4b60f8-6964-45af-8412-935234c7c0ff
title: Metodo ResetReplicationStatistics della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8407e20cb38c9aecac26ab0bcee99ce0c8a6be2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312331"
---
# <a name="resetreplicationstatistics-method-of-the-msvm_replicationservice-class"></a>Metodo ResetReplicationStatistics della classe MSVM \_ ReplicationService

Reimposta le statistiche di replica per una macchina virtuale e agisce sulla relazione di replica primaria della macchina virtuale.

> [!Note]  
> A partire da Windows 8.1, è consigliabile non usare più **ResetReplicationStatistics** per reimpostare le statistiche di replica. Usare invece [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).

 

## <a name="syntax"></a>Sintassi


```mof
uint32 ResetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ in\]
</dt> <dd>

Riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per la quale reimpostare le statistiche di replica.

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

**Sistema in uso** (32774)
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

[**GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[**\_ReplicationService MSVM**](msvm-replicationservice.md)
</dt> </dl>

 

