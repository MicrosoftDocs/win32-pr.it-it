---
description: Recupera l'oggetto errore per il processo, se disponibile.
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: 'Metodo Msvm_CopyFileToGuestJob:: GetError'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a0a89feab4e78ba3703e117972598c4de5f70310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307745"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a>\_Metodo MSVM CopyFileToGuestJob:: GetError

Recupera l'oggetto errore per il processo, se disponibile. Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce un oggetto [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)) . Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, viene restituita un'istanza di **\_ errore CIM** .

## <a name="syntax"></a>Sintassi


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Errore* \[ out\]
</dt> <dd>

Se lo stato operativo del processo non è 2 (OK), questo metodo restituisce un'istanza incorporata della classe [**di \_ errore MSVM**](msvm-error.md) in formato CIM-XML. Se lo stato operativo del processo è 2 (OK), viene restituito **null** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
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

**Sistema in uso** (32774)
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
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\\\Virtualizzazione radice \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CopyFileToGuestJob MSVM**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

