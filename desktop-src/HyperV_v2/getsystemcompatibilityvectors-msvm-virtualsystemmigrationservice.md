---
description: Ottiene un elenco di istanze di Msvm CompatibilityVector che possono essere usate per verificare la compatibilità tra macchine virtuali \_ e host.
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: Msvm_VirtualSystemMigrationService::GetSystemCompatibilityVectors
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
ms.openlocfilehash: 19eb9fe54c9a20e635d706eff9b22eb0e78cb8347b27fcdcaff0f419e60a6112
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427661"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a>Metodo Msvm \_ VirtualSystemMigrationService::GetSystemCompatibilityVectors

Ottiene un elenco di [**istanze di Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) che possono essere usate per verificare la compatibilità tra macchine virtuali e host.

## <a name="syntax"></a>Sintassi


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Riferimento a una classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale per cui recuperare i vettori di compatibilità. Se questo parametro fa riferimento al sistema del computer di hosting, i dati restituiti nel parametro *CompatibilityVectors* possono essere usati per determinare se è possibile eseguire rapidamente la migrazione di una delle macchine virtuali nel sistema del computer host a un altro sistema di computer host.

</dd> <dt>

*CompatibilityVectors* \[ Cambio\]
</dt> <dd>

Matrice di istanze [**di Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) che contengono le informazioni di compatibilità per le macchine virtuali o il sistema del computer di hosting.

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
</dt> </dl>

## <a name="remarks"></a>Commenti

**GetSystemCompatibilityVectors** ottiene informazioni di compatibilità per una macchina virtuale (VM) (se eseguita in un sistema di computer vm) o un host (quando viene eseguita in un sistema di computer host). Le informazioni di compatibilità rimangono opache rispetto al client, mentre le informazioni forniscono un modo per confrontare le informazioni di compatibilità dell'host con quella della macchina virtuale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\Virtualizzazione \\ radice \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




