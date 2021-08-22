---
description: Crea uno snapshot di un sistema virtuale.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Metodo CreateSnapshot della classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ee1a2e66745ceac50cc00ba6e625a171f18c7d2b54d4e51af2c86f6711675ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532751"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>Metodo CreateSnapshot della classe CIM \_ VirtualSystemSnapshotService

Crea uno snapshot di un sistema virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedSystem* \[ Pollici\]
</dt> <dd>

Riferimento [**CIM \_ ComputerSystem**](cim-computersystem.md) al sistema virtuale interessato.

</dd> <dt>

*SnapshotSettings* \[ Pollici\]
</dt> <dd>

Impostazioni dei parametri.

</dd> <dt>

*SnapshotType* \[ Pollici\]
</dt> <dd>

Tipo di snapshot richiesto:

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Snapshot completo** (2)


</dt> <dd>

Snapshot completo del sistema virtuale.

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Snapshot del disco** (3)


</dt> <dd>

Snapshot dei dischi del sistema virtuale.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Specifico del** fornitore (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshot* \[ in, out\]
</dt> <dd>

Riferimento [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) per lo snapshot del sistema virtuale risultante.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione è a esecuzione lunga, è possibile che venga restituito un processo. In questo caso, l'istanza della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta il nuovo snapshot del sistema virtuale viene presentata tramite l'associazione [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) con il valore della **proprietà AffectedElement** che fa riferimento alla nuova istanza della classe **CIM \_ VirtualSystemSettingData** che rappresenta lo snapshot del sistema virtuale e il valore di **ElementEffects** impostato su 5 (Create).

> [!Note]  
> Questo parametro era di lettura/scrittura Windows 8.1.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0. In caso contrario, restituisce un errore.

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

**DmTF riservato** (..)
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
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ VirtualSystemSnapshotService**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




