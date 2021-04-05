---
description: Converte uno snapshot di raccolta esistente in una raccolta di punti di riferimento. La raccolta snapshot viene eliminata come effetto collaterale. Solo gli snapshot di ripristino possono essere convertiti in punti di riferimento.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Metodo ConvertToReferencePoint della classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885729"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a>Metodo ConvertToReferencePoint della classe MSVM \_ CollectionSnapshotService

Converte uno snapshot di raccolta esistente in una raccolta di punti di riferimento. La raccolta snapshot viene eliminata come effetto collaterale. Solo gli snapshot di ripristino possono essere convertiti in punti di riferimento.

## <a name="syntax"></a>Sintassi


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedSnapshotCollection* \[ in\]
</dt> <dd>

Riferimento a un [**MSVM \_ snapshotcollection**](msvm-snapshotcollection.md) che contiene la raccolta di snapshot del sistema virtuale interessata.

</dd> <dt>

*ResultingReferencePointCollection* \[ in uscita\]
</dt> <dd>

Riferimento a un [**\_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) che contiene la raccolta di punti di riferimento del sistema virtuale risultante

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0 (completa) o 4096 (processo avviato); in caso contrario, restituisce un errore.

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
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CollectionSnapshotService MSVM**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




