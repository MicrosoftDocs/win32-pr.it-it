---
description: Ottiene un elenco di \_ istanze di CompatibilityVector MSVM che possono essere usate per verificare la compatibilità della macchina virtuale (VM) con l'host.
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: 'Metodo Msvm_VirtualSystemMigrationService:: GetSystemCompatibilityVectors'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966502"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a>\_Metodo MSVM VirtualSystemMigrationService:: GetSystemCompatibilityVectors

Ottiene un elenco di istanze di [**\_ CompatibilityVector MSVM**](msvm-compatibilityvector.md) che possono essere usate per verificare la compatibilità della macchina virtuale (VM) con l'host.

## <a name="syntax"></a>Sintassi


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ in\]
</dt> <dd>

Riferimento a una classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale per cui recuperare i vettori di compatibilità. Se questo parametro fa riferimento al sistema del computer host, i dati restituiti nel parametro *CompatibilityVectors* possono essere usati per determinare se è possibile eseguire rapidamente la migrazione di una o più macchine virtuali nel computer host a un altro computer host.

</dd> <dt>

*CompatibilityVectors* \[ out\]
</dt> <dd>

Matrice di istanze [**di \_ CompatibilityVector MSVM**](msvm-compatibilityvector.md) che contengono le informazioni sulla compatibilità per le macchine virtuali o il computer host.

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

## <a name="remarks"></a>Commenti

**GetSystemCompatibilityVectors** ottiene le informazioni sulla compatibilità per una macchina virtuale (VM) (quando viene eseguita in un computer VM) o un host (quando viene eseguito in un computer host). Le informazioni sulla compatibilità rimangono opache per il client mentre le informazioni consentono di confrontare le informazioni di compatibilità dell'host con quelle della macchina virtuale.

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

[**\_CompatibilityVector MSVM**](msvm-compatibilityvector.md)
</dt> <dt>

[**\_VirtualSystemMigrationService MSVM**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




