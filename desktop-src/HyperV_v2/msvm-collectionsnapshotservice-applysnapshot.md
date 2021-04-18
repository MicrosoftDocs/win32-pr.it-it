---
description: Applica una raccolta snapshot alla raccolta del sistema di computer virtuale.
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Metodo ApplySnapshot della classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1fa5b664b39541b9d697dfbbfd0493f7a6f7cf96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306635"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Metodo ApplySnapshot della classe MSVM \_ CollectionSnapshotService

Applica una raccolta snapshot alla raccolta del sistema di computer virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Snapshotcollection* \[ in\]
</dt> <dd>

Riferimento a una [**\_ raccolta CIM**](cim-collection.md) che rappresenta la raccolta di snapshot da applicare.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Riferimento facoltativo restituito se l'operazione viene eseguita in modo asincrono. Se presente, il riferimento restituito a un'istanza di [**CIM \_ ConcreteJob**](cim-concretejob.md) può essere usato per monitorare lo stato di avanzamento e per ottenere il risultato del metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0. in caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Non riuscito** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Tipo non valido** (6)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097.. 32767)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CollectionSnapshotService MSVM**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




