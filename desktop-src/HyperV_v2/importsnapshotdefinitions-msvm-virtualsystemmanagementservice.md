---
description: Cerca nella cartella specificata tutti i file di definizione dello snapshot associati al sistema di computer pianificato specificato e crea un nuovo snapshot nel sistema di computer pianificato per ogni file di definizione associato in questo percorso.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Metodo ImportSnapshotDefinitions della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cfa20eb845546f58201bdc167cfbe38bd4a3bd0ad327a04e009db4504ce0966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694591"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo ImportSnapshotDefinitions della classe Msvm \_ VirtualSystemManagementService

Cerca nella cartella specificata tutti i file di definizione dello snapshot associati al sistema di computer pianificato specificato e crea un nuovo snapshot nel sistema di computer pianificato per ogni file di definizione associato in questo percorso.

## <a name="syntax"></a>Sintassi


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PlannedSystem* \[ Pollici\]
</dt> <dd>

Riferimento a un [**oggetto Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) che rappresenta la macchina virtuale pianificata che fa riferimento agli snapshot da importare.

</dd> <dt>

*SnapshotFolder* \[ Pollici\]
</dt> <dd>

Percorso completo della cartella in cui sono disponibili le configurazioni snapshot per questa macchina virtuale.

</dd> <dt>

*ImportedSnapshots* \[ Cambio\]
</dt> <dd>

Se l'operazione viene completata in modo sincrono, matrice di riferimenti alle istanze [**di Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresentano gli snapshot importati correttamente.

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

 

