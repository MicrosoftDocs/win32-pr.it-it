---
description: Elimina uno snapshot esistente della raccolta di sistemi virtuali. Questo metodo può causare l'eliminazione di altri snapshot dipendenti dagli snapshot interessati.
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Metodo DestroySnapshot della classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bacdb760580057516b6663bf53f5cd02a83f76148fa782ab875ca7385c053cb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431496"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Metodo DestroySnapshot della classe Msvm \_ CollectionSnapshotService

Elimina uno snapshot esistente della raccolta di sistemi virtuali. Questo metodo può causare l'eliminazione di altri snapshot dipendenti dagli snapshot interessati.

## <a name="syntax"></a>Sintassi


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedSnapshotCollection* \[ Pollici\]
</dt> <dd>

Riferimento a una [**raccolta CIM \_ che**](cim-collection.md) descrive la raccolta di snapshot del sistema virtuale interessata.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Riferimento facoltativo restituito se l'operazione viene eseguita in modo asincrono. Se presente, il riferimento restituito a un'istanza di [**CIM \_ ConcreteJob**](cim-concretejob.md) può essere usato per monitorare lo stato di avanzamento e ottenere il risultato del metodo .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0 (Completato) o 4096 (Processo avviato). In caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non** valido (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Tipo non valido** (6)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097..32767)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
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

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




