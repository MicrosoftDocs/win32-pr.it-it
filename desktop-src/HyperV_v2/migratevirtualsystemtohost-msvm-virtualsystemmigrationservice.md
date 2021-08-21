---
description: Esegue la migrazione di un sistema virtuale o dell'archiviazione di un sistema virtuale a un host di destinazione specificato da un nome host.
ms.assetid: 796b043c-5ac9-4c69-9838-0f415be5a63e
title: Metodo MigrateVirtualSystemToHost della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7e6ebff1fabf1ed0b705dcbc4571566a5965b9120463bb009e68196f0c1f9a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149656"
---
# <a name="migratevirtualsystemtohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Metodo MigrateVirtualSystemToHost della classe Msvm \_ VirtualSystemMigrationService

Esegue la migrazione di un sistema virtuale o dell'archiviazione di un sistema virtuale a un host di destinazione specificato da un nome host.

## <a name="syntax"></a>Sintassi


```mof
uint32 MigrateVirtualSystemToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Riferimento a un'istanza della [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il sistema di computer virtuali di cui eseguire la migrazione.

</dd> <dt>

*DestinationHost* \[ Pollici\]
</dt> <dd>

Nome del sistema host per la migrazione. Il formato di questo nome viene specificato dalla **proprietà DestinationHostFormatsSupported** della [**classe Msvm \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) associata a questa classe.

</dd> <dt>

*MigrationSettingData* \[ Pollici\]
</dt> <dd>

Istanza incorporata della [**classe Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni per l'operazione di migrazione.

</dd> <dt>

*NewSystemSettingData* \[ Pollici\]
</dt> <dd>

Istanza incorporata della [**classe Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.

</dd> <dt>

*NewResourceSettingData* \[ Pollici\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata della [**classe Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali del sistema virtuale dopo la migrazione.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

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

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

