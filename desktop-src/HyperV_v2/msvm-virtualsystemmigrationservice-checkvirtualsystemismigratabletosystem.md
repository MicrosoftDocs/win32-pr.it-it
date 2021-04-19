---
description: Determina se è possibile eseguire la migrazione del sistema virtuale specificato a un sistema di destinazione.
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: Metodo CheckVirtualSystemIsMigratableToSystem della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305993"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Metodo CheckVirtualSystemIsMigratableToSystem della classe MSVM \_ VirtualSystemMigrationService

Determina se è possibile eseguire la migrazione del sistema virtuale specificato a un sistema di destinazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ in\]
</dt> <dd>

Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale di cui verificare la capacità di migrazione.

</dd> <dt>

*DestinationSystem* \[ in\]
</dt> <dd>

Riferimento a un'istanza della classe [**\_ ComputerSystem di MSVM**](msvm-computersystem.md) che rappresenta la macchina virtuale per cui verificare la capacità di migrazione.

</dd> <dt>

*MigrationSettingData* \[ in\]
</dt> <dd>

Istanza incorporata della classe [**\_ VirtualSystemMigrationSettingData MSVM**](msvm-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni per l'operazione di migrazione.

</dd> <dt>

*NewSystemSettingData* \[ in\]
</dt> <dd>

Istanza incorporata della classe [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.

</dd> <dt>

*NewResourceSettingData* \[ in\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata della classe [**\_ ResourceAllocationSettingData MSVM**](msvm-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali del sistema virtuale dopo la migrazione.

</dd> <dt>

*IsMigratable* \[ out\]
</dt> <dd>

Riceve il risultato del controllo della migrazione che indica se è possibile eseguire correttamente la migrazione del sistema virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Non riuscito** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Parametri incompatibili** (6)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Metodo riservato** (4097.. 32767)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualSystemMigrationService MSVM**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




