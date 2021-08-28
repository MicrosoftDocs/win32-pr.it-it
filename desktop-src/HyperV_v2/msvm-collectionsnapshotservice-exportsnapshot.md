---
description: Esporta una raccolta snapshot di sistemi di computer virtuali in un file. La raccolta snapshot, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.
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
ms.openlocfilehash: ec61899e92da562250bf392077468adef14a35eda72d89d28ad9b3ddc3da2f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426841"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Metodo ExportSnapshot della classe Msvm \_ CollectionSnapshotService

Esporta una raccolta snapshot di sistemi di computer virtuali in un file. La raccolta snapshot, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.

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

*SnapshotCollection* \[ Pollici\]
</dt> <dd>

Riferimento a una raccolta [**CIM \_ che**](cim-collection.md) rappresenta la raccolta snapshot da esportare.

</dd> <dt>

*ExportDirectory* \[ Pollici\]
</dt> <dd>

Percorso completo della directory in cui deve essere esportata la raccolta di sistemi virtuali. Se la proprietà **CreateVmExportSubdirectory** nel parametro *ExportSettingData* è impostata su **True,** questa directory può essere riutilizzata per l'esportazione di più raccolte di sistemi virtuali e questo metodo inserisce ogni definizione di raccolta di sistemi virtuali in una sottodirectory separata in questo percorso.

</dd> <dt>

*ExportSettingData* \[ Pollici\]
</dt> <dd>

Istanza di [**Msvm \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) che rappresenta le impostazioni per l'operazione di esportazione.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Riferimento facoltativo restituito se l'operazione viene eseguita in modo asincrono. Se presente, il riferimento restituito a un'istanza di [**CIM \_ ConcreteJob**](cim-concretejob.md) può essere usato per monitorare lo stato di avanzamento e ottenere il risultato del metodo .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo viene eseguito in modo sincrono, restituisce 0 se ha esito positivo. Se questo metodo viene eseguito in modo asincrono, restituisce 4096 e il parametro di output Job può essere usato per tenere traccia dello stato di avanzamento dell'operazione asincrona. Qualsiasi altro valore restituito indica un errore.

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

 

 




