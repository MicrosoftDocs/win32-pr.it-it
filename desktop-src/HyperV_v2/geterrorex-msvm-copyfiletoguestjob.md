---
description: 'Msvm_CopyFileToGuestJob::GetErrorEx : recupera gli oggetti errore per il processo, se presenti.'
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: Msvm_CopyFileToGuestJob::GetErrorEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 69dd440df079379d8e4bd9cee6e1cad23e684cb80a11e7e48d39752ccea82426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149814"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a>Metodo \_ Msvm CopyFileToGuestJob::GetErrorEx

Recupera gli oggetti errore per il processo, se presenti. Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna [**istanza msvm \_ Error.**](msvm-error.md) Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, vengono restituite una o più istanze **di Errore \_ Msvm.**

## <a name="syntax"></a>Sintassi


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Errori* \[ Cambio\]
</dt> <dd>

Se lo stato operativo del processo non è 2 (OK), questo metodo restituisce una o più istanze incorporate della classe [**Msvm \_ Error,**](msvm-error.md) in formato CIM-XML, che rappresentano gli errori rilevati nel processo. Se lo stato operativo del processo è 2 (OK), viene **restituito Null.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completata senza errori** (0)
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
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




