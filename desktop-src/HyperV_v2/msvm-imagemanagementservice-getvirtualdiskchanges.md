---
description: Recupera un elenco di modifiche nell'area specificata di un disco virtuale a partire dall'ID Rilevamento modifiche resiliente o dall'ID snapshot VHDSet specificato.
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
ms.openlocfilehash: 8b96c5b4d2bbdff78b6f9f2bc9a1e7547742a553564e0f81547b8d998f86f14f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522561"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a>Metodo GetVirtualDiskChanges della classe Msvm \_ ImageManagementService

Recupera un elenco di modifiche nell'area specificata di un disco virtuale a partire dall'ID Rilevamento modifiche resiliente o dall'ID snapshot VHDSet specificato.

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

*Percorso* \[ Pollici\]
</dt> <dd>

Percorso completo che specifica il percorso del file del disco rigido virtuale.

</dd> <dt>

*LimitId* \[ Pollici\]
</dt> <dd>

ID di Rilevamento modifiche resiliente o ID snapshot del set di dischi rigidi virtuali che indica la linea di base per le modifiche nel disco virtuale.

</dd> <dt>

*TargetSnapshotId* \[ Pollici\]
</dt> <dd>

ID snapshot VHDSet che indica lo snapshot da confrontare con la baseline quando si determinano le modifiche nel disco rigido virtuale. Questo parametro è valido solo per i file del set di dischi rigidi virtuali.

</dd> <dt>

*ByteOffset* \[ Pollici\]
</dt> <dd>

Offset in byte dell'area nel disco virtuale per cui eseguire query relative alle modifiche.

</dd> <dt>

*ByteLength* \[ Pollici\]
</dt> <dd>

Lunghezza in byte dell'area nel disco virtuale per cui eseguire query relative alle modifiche. Deve essere minore delle dimensioni del disco virtuale.

</dd> <dt>

*ProcessedByteLength* \[ Cambio\]
</dt> <dd>

Lunghezza totale in byte elaborata. Può essere uguale o inferiore a ByteLength.

</dd> <dt>

*ChangedByteOffsets* \[ Cambio\]
</dt> <dd>

Elenco di offset di byte nel disco virtuale che indica l'inizio di ogni intervallo modificato.

</dd> <dt>

*ChangedByteLengths* \[ Cambio\]
</dt> <dd>

Elenco di lunghezze in byte degli intervalli modificati nel disco virtuale.

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

 

 




