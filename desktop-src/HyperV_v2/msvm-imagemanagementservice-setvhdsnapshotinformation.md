---
description: Modifica una voce di snapshot VHD all'interno di un file di set VHD. Se l'ID dello snapshot in questione esiste già, la voce di snapshot esistente verrà sovrascritta con la nuova voce. In caso contrario, la nuova voce verrà aggiunta al file di set VHD.
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
ms.openlocfilehash: 54f5ac23cdf8f49532a05eee3fd23293715cd02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307888"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>Metodo SetVHDSnapshotInformation della classe MSVM \_ servizio

Modifica una voce di snapshot VHD all'interno di un file di set VHD. Se l'ID dello snapshot in questione esiste già, la voce di snapshot esistente verrà sovrascritta con la nuova voce. In caso contrario, la nuova voce verrà aggiunta al file di set VHD.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Informazioni* \[ su in\]
</dt> <dd>

Informazioni snapshot VHD da modificare o aggiungere nel file di set VHD. La stringa è un'istanza incorporata di [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Riferimento al processo (può essere null se l'attività è stata completata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

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
</dt> <dt>

**File non trovato** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio MSVM**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




