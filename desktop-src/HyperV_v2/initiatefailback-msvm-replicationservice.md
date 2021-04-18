---
description: Avvia il failback per una macchina virtuale di ripristino.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: 'Metodo Msvm_ReplicationService:: InitiateFailback'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b356982296427212287ea11b528a7878dc166245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309512"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a>\_Metodo MSVM ReplicationService:: InitiateFailback

Avvia il failback per una macchina virtuale di ripristino.

## <a name="syntax"></a>Sintassi


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ in\]
</dt> <dd>

Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui avviare un failback.

</dd> <dt>

*ReplicationSettingData* \[ in\]
</dt> <dd>

Rappresentazione di stringa di un'istanza incorporata della classe [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) che definisce le impostazioni di replica per il failback.

</dd> <dt>

*RecoveryPointIdentifier* \[ in\]
</dt> <dd>

Input facoltativo che identifica il punto di ripristino a cui viene richiesto il failback.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)). Questo riferimento può essere usato per monitorare lo stato di avanzamento e per ottenere il risultato del metodo.

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

**InitiateFailback** funziona in una macchina virtuale di ripristino e porta la macchina virtuale allo stato *WaitingForFailback* . **InitiateFailback** consente di eseguire il reverse della richiesta di failback al provider corrispondente, che consente di risincronizzare il punto di ripristino dal lato nuovo-primario. Al termine del failback del punto di ripristino richiesto, lo stato di replica passa allo stato *FailbackCompleted* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\\\Virtualizzazione radice \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ReplicationService MSVM**](msvm-replicationservice.md)
</dt> </dl>

 

