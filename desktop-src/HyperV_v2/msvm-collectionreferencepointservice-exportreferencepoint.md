---
description: Esporta una raccolta di punti di riferimento in un file. La raccolta di punti di riferimento, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Metodo ExportReferencePoint della classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49517da44cc7955d825792afcc475c56e37fad37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319509"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Metodo ExportReferencePoint della classe MSVM \_ CollectionReferencePointService

Esporta una raccolta di punti di riferimento in un file. La raccolta di punti di riferimento, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.

## <a name="syntax"></a>Sintassi


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ReferencePointCollection* \[ in\]
</dt> <dd>

Riferimento a una [**\_ raccolta CIM**](cim-collection.md) che rappresenta la raccolta di punti di riferimento da esportare.

</dd> <dt>

*ExportDirectory* \[ in\]
</dt> <dd>

Percorso completo della directory in cui deve essere esportata la raccolta di punti di riferimento.

</dd> <dt>

*ExportSettingData* \[ in\]
</dt> <dd>

Istanza di [**MSVM \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) che rappresenta le impostazioni per l'operazione di esportazione.

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

[**\_CollectionReferencePointService MSVM**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




