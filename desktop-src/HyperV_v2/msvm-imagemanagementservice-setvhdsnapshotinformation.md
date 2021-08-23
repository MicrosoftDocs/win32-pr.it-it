---
description: Modifica una voce di snapshot del disco rigido virtuale all'interno di un file di set di dischi rigidi virtuali. Se l'ID snapshot in questione esiste già, la voce snapshot esistente verrà sovrascritta con la nuova voce. In caso contrario, la nuova voce verrà aggiunta al file del set di dischi rigidi virtuali.
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: Metodo SetVHDSnapshotInformation della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: af4adddb2b59da303f558cfffac61003e70e5767c77e381b13ba6089228d6643
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522451"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>Metodo SetVHDSnapshotInformation della classe Msvm \_ ImageManagementService

Modifica una voce di snapshot del disco rigido virtuale all'interno di un file di set di dischi rigidi virtuali. Se l'ID snapshot in questione esiste già, la voce snapshot esistente verrà sovrascritta con la nuova voce. In caso contrario, la nuova voce verrà aggiunta al file del set di dischi rigidi virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Informazioni* \[ Pollici\]
</dt> <dd>

Informazioni sullo snapshot del disco rigido virtuale da modificare o aggiungere nel file del set di dischi rigidi virtuali. La stringa è un'istanza incorporata [**di Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Riferimento al processo (può essere Null se l'attività viene completata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

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

**File non trovato** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




