---
description: Verifica la compatibilità delle informazioni di compatibilità con il sistema del computer host.
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: Metodo CheckSystemCompatibilityInfo della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7492d3f7dcdc20abca5cd574d1006b5e2090d02d28f7446dd94ec7b777541b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041981"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Metodo CheckSystemCompatibilityInfo della classe Msvm \_ VirtualSystemMigrationService

Verifica la compatibilità delle informazioni di compatibilità con il sistema del computer host.

## <a name="syntax"></a>Sintassi


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CompatibilityInfo* \[ Pollici\]
</dt> <dd>

BLOB di dati ottenuto chiamando il [**metodo GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) nel sistema del computer host.

</dd> <dt>

*Motivi* \[ Cambio\]
</dt> <dd>

Matrice di stringhe che riceve le istanze incorporate della [**classe Msvm \_ Error**](msvm-error.md) che rappresentano eventuali avvisi o errori.

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

**Non compatibile** (32784)
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

 

 




