---
description: Esporta una macchina virtuale o uno snapshot di una macchina virtuale in un file.
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
ms.openlocfilehash: 72198055a81ce13a6b38859ed5ba6370faf7de046bc9f2cc3a158548c2679685
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254037"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo ExportSystemDefinition della classe Msvm \_ VirtualSystemManagementService

Esporta una macchina virtuale o uno snapshot di una macchina virtuale in un file. La macchina virtuale deve essere nello stato "spento" o "salvato" per essere esportata. La macchina virtuale, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.

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

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Riferimento a un [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale da esportare.

</dd> <dt>

*ExportDirectory* \[ Pollici\]
</dt> <dd>

Percorso completo della directory in cui deve essere esportata la macchina virtuale. Se la proprietà **CreateVmExportSubdirectory** della classe [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) nel parametro *ExportSettingData* è impostata su **True,** questa directory può essere riutilizzata per l'esportazione di più macchine virtuali e questo metodo inserisce ogni definizione di macchina virtuale in una sottodirectory separata in questo percorso.

</dd> <dt>

*ExportSettingData* \[ Pollici\]
</dt> <dd>

Istanza incorporata della classe [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) che rappresenta le impostazioni per l'operazione di esportazione.

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

**Il sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
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

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

