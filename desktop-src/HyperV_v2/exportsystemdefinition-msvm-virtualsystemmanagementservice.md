---
description: Esporta in un file una macchina virtuale o uno snapshot di una macchina virtuale.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Metodo ExportSystemDefinition della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749639"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo ExportSystemDefinition della classe MSVM \_ VirtualSystemManagementService

Esporta in un file una macchina virtuale o uno snapshot di una macchina virtuale. Lo stato della macchina virtuale deve essere "spento" o "salvato" per l'esportazione. La macchina virtuale, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.

## <a name="syntax"></a>Sintassi


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ in\]
</dt> <dd>

Riferimento a un [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale da esportare.

</dd> <dt>

*ExportDirectory* \[ in\]
</dt> <dd>

Percorso completo della directory in cui deve essere esportata la macchina virtuale. Se la proprietà **CreateVmExportSubdirectory** della classe [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) nel parametro *ExportSettingData* è impostata su **true**, questa directory può essere riutilizzata per l'esportazione di più macchine virtuali e questo metodo inserisce ogni definizione di macchina virtuale in una sottodirectory separata in questo percorso.

</dd> <dt>

*ExportSettingData* \[ in\]
</dt> <dd>

Istanza incorporata della classe [**\_ VirtualSystemExportSettingData MSVM**](msvm-virtualsystemexportsettingdata.md) che rappresenta le impostazioni per l'operazione di esportazione.

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

 

