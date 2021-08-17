---
description: Crea un nuovo sistema di computer pianificato in base alla definizione di macchina virtuale specificata.
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
ms.openlocfilehash: ee8dd5bb7d17684216b747717c0adf32011dafa543f05c91a0c1264da89caf2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149737"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo ImportSystemDefinition della classe Msvm \_ VirtualSystemManagementService

Crea un nuovo sistema di computer pianificato in base alla definizione di macchina virtuale specificata.

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

*SystemDefinitionFile* \[ Pollici\]
</dt> <dd>

Percorso completo del file di definizione del sistema (.xml o exp) che rappresenta la macchina virtuale da importare. Il file di definizione non deve essere già in uso dal sistema host o dalla piattaforma di virtualizzazione.

</dd> <dt>

*SnapshotFolder* \[ Pollici\]
</dt> <dd>

Percorso completo della cartella in cui sono disponibili le configurazioni snapshot per questa macchina virtuale. Questa cartella verrà cercata per individuare gli snapshot a cui fa riferimento la definizione della macchina virtuale. Gli snapshot di riferimento non trovati in questa posizione devono essere eliminati usando il [**metodo DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) o importati usando il [**metodo ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) prima di realizzare il sistema del computer pianificato.

</dd> <dt>

*GenerateNewSystemIdentifier* \[ Pollici\]
</dt> <dd>

Indica se riutilizzare l'identificatore univoco per la macchina virtuale. Se questo parametro è **True,** viene generato un nuovo identificatore di sistema. Se questo parametro è **False,** viene usato l'identificatore di sistema esistente.

</dd> <dt>

*ImportedSystem* \[ Cambio\]
</dt> <dd>

Se l'operazione viene completata in modo sincrono, un riferimento a un [**oggetto Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) che rappresenta la macchina virtuale importata.

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

**File in uso** (32779)
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

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

