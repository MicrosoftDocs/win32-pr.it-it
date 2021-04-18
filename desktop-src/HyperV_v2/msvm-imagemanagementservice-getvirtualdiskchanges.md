---
description: Recupera un elenco di modifiche nell'area specificata di un disco virtuale a partire dall'ID di Rilevamento modifiche resiliente fornito o dall'ID dello snapshot VHDSet.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Metodo GetVirtualDiskChanges della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307893"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a>Metodo GetVirtualDiskChanges della classe MSVM \_ servizio

Recupera un elenco di modifiche nell'area specificata di un disco virtuale a partire dall'ID di Rilevamento modifiche resiliente fornito o dall'ID dello snapshot VHDSet.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso* \[ in\]
</dt> <dd>

Percorso completo che specifica il percorso del file del disco rigido virtuale.

</dd> <dt>

*LimitId* \[ in\]
</dt> <dd>

Un ID di Rilevamento modifiche resiliente o un ID dello snapshot del set VHD che indica la linea di base per le modifiche nel disco virtuale.

</dd> <dt>

*TargetSnapshotId* \[ in\]
</dt> <dd>

ID dello snapshot VHDSet che indica lo snapshot da confrontare con la linea di base quando si denominano le modifiche nel disco rigido virtuale. Questo parametro è valido solo per i file di set VHD.

</dd> <dt>

*ByteOffset* \[ in\]
</dt> <dd>

Offset di byte dell'area del disco virtuale per la quale eseguire una query sulle modifiche.

</dd> <dt>

*ByteLength* \[ in\]
</dt> <dd>

Lunghezza in byte dell'area del disco virtuale per la quale eseguire una query sulle modifiche. Il numero deve essere inferiore a quello del disco virtuale.

</dd> <dt>

*ProcessedByteLength* \[ out\]
</dt> <dd>

Lunghezza totale in byte elaborata. Potrebbe essere uguale a ByteLength o less.

</dd> <dt>

*ChangedByteOffsets* \[ out\]
</dt> <dd>

Elenco di offset di byte nel disco virtuale che indica l'inizio di ogni intervallo modificato.

</dd> <dt>

*ChangedByteLengths* \[ out\]
</dt> <dd>

Elenco di lunghezze in byte degli intervalli modificati nel disco virtuale.

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

 

 




