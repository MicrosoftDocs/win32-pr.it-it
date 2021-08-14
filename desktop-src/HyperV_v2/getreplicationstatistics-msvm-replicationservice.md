---
description: Recupera le statistiche di replica per una macchina virtuale e agisce sulla relazione di replica primaria della macchina virtuale.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Metodo GetReplicationStatistics della Msvm_ReplicationService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 767ea873b725523e3d430708dc5485d3d24c62e07e5cebac001b020ee996bd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392917"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a>Metodo GetReplicationStatistics della classe Msvm \_ ReplicationService

Recupera le statistiche di replica per una macchina virtuale e agisce sulla relazione di replica primaria della macchina virtuale.

> [!Note]  
> A partire Windows 8.1, è consigliabile non usare **più GetReplicationStatistics** per recuperare le statistiche di replica. Usare invece [**GetReplicationStatisticsEx.**](getreplicationstatisticsex-msvm-replicationservice.md)

 

## <a name="syntax"></a>Sintassi


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Riferimento a [**un'istanza \_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui recuperare le statistiche di replica.

</dd> <dt>

*ReplicationStatistics* \[ Cambio\]
</dt> <dd>

Se ha esito positivo, riceve un'istanza incorporata della [**classe Msvm \_ ReplicationStatistics**](msvm-replicationstatistics.md) che contiene le statistiche di replica per la macchina virtuale richiesta.

</dd> <dt>

*ReplicationHealthIssues* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, riceve una matrice di istanze incorporate della [**classe Msvm \_ Error**](msvm-error.md) che indicano eventuali avvisi o errori di replica per la macchina virtuale richiesta.

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
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

