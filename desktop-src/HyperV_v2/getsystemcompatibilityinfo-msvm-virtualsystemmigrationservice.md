---
description: Genera un BLOB opaco di dati che contiene informazioni sulla compatibilità per il sistema specificato.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Metodo GetSystemCompatibilityInfo della Msvm_VirtualSystemMigrationService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4866b54bb6f5d5b90d4221b81e8a847e910e4486edc55eb4f932684397072504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392815"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Metodo GetSystemCompatibilityInfo della classe Msvm \_ VirtualSystemMigrationService

Genera un BLOB opaco di dati che contiene informazioni sulla compatibilità per il sistema specificato. Questo metodo viene usato insieme al metodo [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) per determinare se è possibile eseguire una migrazione rapida o in tempo reale di una macchina virtuale a un altro computer host senza tentare effettivamente la migrazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Riferimento a una classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale per cui recuperare le informazioni di compatibilità. Se questo parametro fa riferimento al sistema del computer host, i dati restituiti nel parametro *CompatibilityInfo* possono essere usati per determinare se è possibile eseguire rapidamente la migrazione di una delle macchine virtuali nel computer host a un altro computer host.

</dd> <dt>

*CompatibilityInfo* \[ Cambio\]
</dt> <dd>

BLOB opaco di dati che può essere passato al metodo [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) in un altro computer host per verificare la compatibilità.

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

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




