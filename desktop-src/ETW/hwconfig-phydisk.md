---
description: La \_ classe HWConfig PhyDisk è la classe del tipo di evento per gli eventi di configurazione del disco fisico. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: Classe HWConfig_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: 453f06ae11bb8b1e11c9efddd6f63bffd38540e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977655"
---
# <a name="hwconfig_phydisk-class"></a>\_Classe HWConfig PhyDisk

La classe **HWConfig \_ PhyDisk** è la classe del tipo di evento per gli eventi di configurazione del disco fisico.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  string Manufacturer;
};
```

## <a name="members"></a>Members

La **classe \_ PhyDisk di HWConfig** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ PhyDisk di HWConfig** dispone di queste proprietà.

<dl> <dt>

BytesPerSector
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2)
</dt> </dl>

Numero di byte in ogni settore per l'unità disco fisica.

</dd> <dt>

Cilindri
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5)
</dt> </dl>

Numero totale di cilindri sull'unità disco fisica. Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h. Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata. Consultare il produttore per le specifiche di unità accurate.

</dd> <dt>

Numerodisco
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1)
</dt> </dl>

Numero di indice del disco contenente questa partizione.

</dd> <dt>

Produttore
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (10), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Nome del produttore dell'unità disco.

</dd> <dt>

SCSILun
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (9)
</dt> </dl>

Numero di unità logica (LUN) SCSI della scheda SCSI.

</dd> <dt>

SCSIPath
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (7)
</dt> </dl>

Numero del bus SCSI della scheda SCSI.

</dd> <dt>

SCSIPort
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (6)
</dt> </dl>

Numero SCSI della scheda SCSI.

</dd> <dt>

SCSITarget
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (8)
</dt> </dl>

Contiene il numero del dispositivo di destinazione.

</dd> <dt>

SectorsPerTrack
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Numero di settori in ogni traccia per questa unità disco fisica.

</dd> <dt>

TracksPerCylinder
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4)
</dt> </dl>

Numero di tracce in ogni cilindro sull'unità disco fisica. Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h. Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata. Consultare il produttore per le specifiche di unità accurate.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




