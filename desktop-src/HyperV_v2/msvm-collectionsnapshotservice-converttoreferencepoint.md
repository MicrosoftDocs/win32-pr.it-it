---
description: Convertire uno snapshot di raccolta esistente in una raccolta di punti di riferimento. La raccolta di snapshot viene eliminata come effetto collaterale. Solo gli snapshot di ripristino possono essere convertiti in punti di riferimento.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Metodo ConvertToReferencePoint della Msvm_CollectionSnapshotService classe
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
ms.openlocfilehash: 97faedea1cdb852e26f6b94211586e5539075c0a225bf98f1a10cf45305d7296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148867"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a>Metodo ConvertToReferencePoint della classe Msvm \_ CollectionSnapshotService

Convertire uno snapshot di raccolta esistente in una raccolta di punti di riferimento. La raccolta di snapshot viene eliminata come effetto collaterale. Solo gli snapshot di ripristino possono essere convertiti in punti di riferimento.

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

*AffectedSnapshotCollection* \[ Pollici\]
</dt> <dd>

Riferimento a un [**oggetto Msvm \_ SnapshotCollection contenente**](msvm-snapshotcollection.md) la raccolta di snapshot del sistema virtuale interessata.

</dd> <dt>

*ResultingReferencePointCollection* \[ in, out\]
</dt> <dd>

Riferimento a un [**oggetto \_ ReferencePointCollection msvm contenente**](msvm-referencepointcollection.md) la raccolta di punti di riferimento del sistema virtuale risultante

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione è a esecuzione lunga, facoltativamente può essere restituito un processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0 (Completato) o 4096 (Processo avviato); In caso contrario, restituisce un errore.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Tipo non valido** (6)
</dt> <dt>

**DmTF Reserved** (..)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
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

 

 




