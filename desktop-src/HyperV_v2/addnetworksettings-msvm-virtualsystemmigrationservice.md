---
description: Aggiunge le subnet della rete di migrazione per il servizio migrazione del sistema virtuale.
ms.assetid: b0e0f187-beeb-4fdf-a91c-f6c5500f0f6d
title: Metodo AddNetworkSettings della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.AddNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 75d168b1a49d8ac44ab66ba9da13d1e598c647b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312342"
---
# <a name="addnetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Metodo AddNetworkSettings della classe MSVM \_ VirtualSystemMigrationService

Aggiunge le subnet della rete di migrazione per il servizio migrazione del sistema virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddNetworkSettings(
  [in]  string              NetworkSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NetworkSettings* \[ in\]
</dt> <dd>

Matrice di istanze incorporate della classe [**\_ VirtualSystemMigrationNetworkSettingData MSVM**](msvm-virtualsystemmigrationnetworksettingdata.md) che contengono le impostazioni della rete di migrazione.

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

[**ModifyNetworkSettings**](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**RemoveNetworkSettings**](removenetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**\_VirtualSystemMigrationService MSVM**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

