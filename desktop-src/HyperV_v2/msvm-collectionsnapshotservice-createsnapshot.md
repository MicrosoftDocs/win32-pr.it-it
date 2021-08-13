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
ms.openlocfilehash: 251213d0ff7a98d922a4dec761252479f911e66e2304596a97858fe0b7dc5fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426911"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Metodo CreateSnapshot della classe Msvm \_ CollectionSnapshotService

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

*Raccolta* \[ Pollici\]
</dt> <dd>

Riferimento a un [**oggetto CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) che descrive la raccolta di sistemi virtuali interessata.

</dd> <dt>

*SnapshotSettings* \[ Pollici\]
</dt> <dd>

Contiene le impostazioni dei parametri.

</dd> <dt>

*SnapshotType* \[ Pollici\]
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

Snapshot per scenari di ripristino, tra cui replica di failover e backup.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Specifico del** fornitore (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshotCollection* \[ in, out\]
</dt> <dd>

In caso di esito positivo, restituisce [**un riferimento alla raccolta CIM \_**](cim-collection.md) contenente lo snapshot del sistema virtuale.

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

 

 




