---
description: Elimina definitivamente una raccolta di punti di riferimento esistente. Questo metodo può essere un effetto collaterale per eliminare altri punti di riferimento che dipendono dalla raccolta di punti di riferimento interessata.
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Metodo DestroyReferencePoint della classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d7fb3fd9168778854518022744f1a0c5ba3c5f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132015"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Metodo DestroyReferencePoint della classe MSVM \_ CollectionReferencePointService

Elimina definitivamente una raccolta di punti di riferimento esistente. Questo metodo può essere un effetto collaterale per eliminare altri punti di riferimento che dipendono dalla raccolta di punti di riferimento interessata.

## <a name="syntax"></a>Sintassi


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedReferencePointCollection* \[ in\]
</dt> <dd>

Riferimento alla raccolta di punti di riferimento del sistema virtuale interessata.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, restituisce 0 (nessun errore) o 4096 (processo avviato); in caso contrario, viene restituito un errore.

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

[**\_CollectionReferencePointService MSVM**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




