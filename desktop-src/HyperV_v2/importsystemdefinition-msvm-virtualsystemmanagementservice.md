---
description: Crea un nuovo sistema di computer pianificato in base alla definizione della macchina virtuale specificata.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Metodo ImportSystemDefinition della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb38ab343a3d92fabd1dc44ed100d2d2f7f7bf01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309511"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo ImportSystemDefinition della classe MSVM \_ VirtualSystemManagementService

Crea un nuovo sistema di computer pianificato in base alla definizione della macchina virtuale specificata.

## <a name="syntax"></a>Sintassi


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SystemDefinitionFile* \[ in\]
</dt> <dd>

Percorso completo del file di definizione del sistema (con estensione XML o EXP) che rappresenta la macchina virtuale da importare. Il file di definizione non deve essere già utilizzato dal sistema host o dalla piattaforma di virtualizzazione.

</dd> <dt>

*SnapshotFolder* \[ in\]
</dt> <dd>

Percorso completo della cartella in cui è possibile trovare le configurazioni dello snapshot per questa macchina virtuale. Verrà eseguita una ricerca nella cartella per individuare gli snapshot a cui fa riferimento la definizione della macchina virtuale. Gli snapshot a cui viene fatto riferimento non trovati in questo percorso devono essere eliminati usando il metodo [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) o importati usando il metodo [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) prima di realizzare il computer pianificato.

</dd> <dt>

*GenerateNewSystemIdentifier* \[ in\]
</dt> <dd>

Indica se riutilizzare l'identificatore univoco per la macchina virtuale. Se questo parametro è **true**, viene generato un nuovo identificatore di sistema. Se questo parametro è **false**, viene utilizzato l'identificatore di sistema esistente.

</dd> <dt>

*ImportedSystem* \[ out\]
</dt> <dd>

Se l'operazione viene completata in modo sincrono, un riferimento a un oggetto [**\_ PlannedComputerSystem MSVM**](msvm-plannedcomputersystem.md) che rappresenta la macchina virtuale importata.

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

**File in uso** (32779)
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

[**\_VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

