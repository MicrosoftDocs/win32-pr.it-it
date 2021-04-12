---
description: Avvia un failover per una macchina virtuale in un'immagine dell'applicazione o del punto di replica standard.
ms.assetid: cd7e9398-c234-4637-906d-69b46ebf3f51
title: Metodo InitiateFailover della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f05a9b126028b741782d253ac12b79f9f88e1e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344541"
---
# <a name="initiatefailover-method-of-the-msvm_replicationservice-class"></a>Metodo InitiateFailover della classe MSVM \_ ReplicationService

Avvia un failover per una macchina virtuale in un'immagine dell'applicazione o del punto di replica standard.

## <a name="syntax"></a>Sintassi


```mof
uint32 InitiateFailover(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ in\]
</dt> <dd>

Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui avviare un failover.

</dd> <dt>

*SnapshotSettingData* \[ in\]
</dt> <dd>

Riferimento a un'istanza [**di \_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) che rappresenta lo snapshot utilizzato per il failover. Se questo parametro è **null**, il failover deve essere eseguito fino al momento più recente.

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

[**RevertFailover**](revertfailover-msvm-replicationservice.md)
</dt> <dt>

[**SetFailoverNetworkAdapterSettings**](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

