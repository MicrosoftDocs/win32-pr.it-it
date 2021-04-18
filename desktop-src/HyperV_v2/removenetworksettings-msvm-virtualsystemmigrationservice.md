---
description: Rimuove le subnet della rete di migrazione dal servizio di migrazione del sistema virtuale.
ms.assetid: 6ae8de07-552b-4525-8806-bfb9da73bd42
title: Metodo RemoveNetworkSettings della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.RemoveNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66b7a9fd1ce29d9dd645242ec7cda346f79a6f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307871"
---
# <a name="removenetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Metodo RemoveNetworkSettings della classe MSVM \_ VirtualSystemMigrationService

Rimuove le subnet della rete di migrazione dal servizio di migrazione del sistema virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveNetworkSettings(
  [in]  Msvm_VirtualSystemMigrationNetworkSettingData REF NetworkSettings[],
  [out] CIM_ConcreteJob                               REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NetworkSettings* \[ in\]
</dt> <dd>

Matrice di istanze incorporate della classe [**\_ VirtualSystemMigrationNetworkSettingData MSVM**](msvm-virtualsystemmigrationnetworksettingdata.md) che rappresentano le subnet di rete da rimuovere.

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

[**AddNetworkSettings**](addnetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**ModifyNetworkSettings**](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**\_VirtualSystemMigrationService MSVM**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

