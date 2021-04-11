---
description: Esporta in un file una raccolta snapshot di sistemi di computer virtuali. La raccolta di snapshot, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Metodo ExportSnapshot della classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226871"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Metodo ExportSnapshot della classe MSVM \_ CollectionSnapshotService

Esporta in un file una raccolta snapshot di sistemi di computer virtuali. La raccolta di snapshot, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.

## <a name="syntax"></a>Sintassi


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Snapshotcollection* \[ in\]
</dt> <dd>

Riferimento a una [**\_ raccolta CIM**](cim-collection.md) che rappresenta la raccolta di snapshot da esportare.

</dd> <dt>

*ExportDirectory* \[ in\]
</dt> <dd>

Percorso completo della directory in cui deve essere esportata la raccolta di sistemi virtuali. Se la proprietà **CreateVmExportSubdirectory** nel parametro *ExportSettingData* è impostata su **true** , è possibile riutilizzare questa directory per esportare più raccolte di sistemi virtuali e questo metodo inserisce ogni definizione di raccolta di sistema virtuale in una sottodirectory separata in questo percorso.

</dd> <dt>

*ExportSettingData* \[ in\]
</dt> <dd>

Istanza di [**MSVM \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) che rappresenta le impostazioni per l'operazione di esportazione.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Riferimento facoltativo restituito se l'operazione viene eseguita in modo asincrono. Se presente, il riferimento restituito a un'istanza di [**CIM \_ ConcreteJob**](cim-concretejob.md) può essere usato per monitorare lo stato di avanzamento e per ottenere il risultato del metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo viene eseguito in modo sincrono, restituisce 0 se ha esito positivo. Se questo metodo viene eseguito in modo asincrono, restituisce 4096 e il parametro di output del processo può essere usato per tenere traccia dello stato di avanzamento dell'operazione asincrona. Qualsiasi altro valore restituito indica un errore.

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

[**\_CollectionSnapshotService MSVM**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




