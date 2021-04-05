---
description: Crea uno snapshot di una raccolta di sistemi virtuali.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Metodo CreateSnapshot della classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 653dae65cc5fe50416b069da6a66e8c678c1b512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755154"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Metodo CreateSnapshot della classe MSVM \_ CollectionSnapshotService

Crea uno snapshot di una raccolta di sistemi virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Raccolta* \[ di in\]
</dt> <dd>

Riferimento a un [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) che descrive la raccolta di sistemi virtuali interessata.

</dd> <dt>

*SnapshotSettings* \[ in\]
</dt> <dd>

Contiene le impostazioni dei parametri.

</dd> <dt>

*SnapshotType* \[ in\]
</dt> <dd>

Tipo di snapshot richiesto:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Snapshot standard** (1)


</dt> <dd>

Snapshot standard del sistema virtuale.

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Snapshot di ripristino** (2)


</dt> <dd>

Snapshot per gli scenari di ripristino, inclusi backup e replica di failover.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Specifico del fornitore** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshotCollection* \[ in uscita\]
</dt> <dd>

Se l'operazione riesce, restituisce un riferimento alla [**\_ raccolta CIM**](cim-collection.md) contenente lo snapshot del sistema virtuale.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Riferimento facoltativo restituito se l'operazione viene eseguita in modo asincrono. Se presente, il riferimento restituito a un'istanza di [**CIM \_ ConcreteJob**](cim-concretejob.md) può essere usato per monitorare lo stato di avanzamento e per ottenere il risultato del metodo.

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

 

 




