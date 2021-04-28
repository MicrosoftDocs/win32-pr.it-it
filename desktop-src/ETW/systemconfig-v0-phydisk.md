---
description: 'SystemConfig_V0_PhyDisk classe: questa classe è la classe del tipo di evento per gli eventi di configurazione del disco fisico.'
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: SystemConfig_V0_PhyDisk classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_PhyDisk
- SystemConfig_V0_PhyDisk.DiskNumber
- SystemConfig_V0_PhyDisk.BytesPerSector
- SystemConfig_V0_PhyDisk.SectorsPerTrack
- SystemConfig_V0_PhyDisk.TracksPerCylinder
- SystemConfig_V0_PhyDisk.Cylinders
- SystemConfig_V0_PhyDisk.SCSIPort
- SystemConfig_V0_PhyDisk.SCSIPath
- SystemConfig_V0_PhyDisk.SCSITarget
- SystemConfig_V0_PhyDisk.SCSILun
- SystemConfig_V0_PhyDisk.Manufacturer
- SystemConfig_V0_PhyDisk.PartitionCount
- SystemConfig_V0_PhyDisk.WriteCacheEnabled
- SystemConfig_V0_PhyDisk.BootDriveLetter
api_type:
- NA
api_location: ''
ms.openlocfilehash: fdb12fac8b2b902f21258fd4c7cfe9846d0456eb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105959"
---
# <a name="systemconfig_v0_phydisk-class"></a>Classe SystemConfig \_ V0 \_ PhyDisk

Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco fisico.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_V0_PhyDisk : SystemConfig_V0
{
  uint32  DiskNumber;
  uint32  BytesPerSector;
  uint32  SectorsPerTrack;
  uint32  TracksPerCylinder;
  uint64  Cylinders;
  uint32  SCSIPort;
  uint32  SCSIPath;
  uint32  SCSITarget;
  uint32  SCSILun;
  char16  Manufacturer[];
  uint32  PartitionCount;
  boolean WriteCacheEnabled;
  char16  BootDriveLetter[];
};
```

## <a name="members"></a>Members

La **classe SystemConfig \_ V0 \_ PhyDisk** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SystemConfig \_ V0 \_ PhyDisk** ha queste proprietà.

<dl> <dt>

**BootDriveLetter**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (13), **Max** (3)
</dt> </dl>

Lettera di unità dell'unità di avvio nel formato " <letter> :".

</dd> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (2)
</dt> </dl>

Numero di byte in ogni settore per l'unità disco fisico.

</dd> <dt>

**Cilindri**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (5)
</dt> </dl>

Numero totale di cilindri nell'unità disco fisico. Nota: il valore di questa proprietà viene ottenuto tramite funzioni estese dell'interrupt BIOS 13 ore. Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata. Per specifiche di unità accurate, rivolgersi al produttore.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (1)
</dt> </dl>

Numero di indice del disco contenente la partizione.

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (10), **Max** (256)
</dt> </dl>

Nome del produttore dell'unità disco.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (11)
</dt> </dl>

Numero di partizioni in questa unità disco fisica riconosciute dal sistema operativo.

</dd> <dt>

**SCSILun**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (9)
</dt> </dl>

Numero di unità logica SCSI (LUN) della scheda SCSI.

</dd> <dt>

**SCSIPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (7)
</dt> </dl>

Numero di bus SCSI della scheda SCSI.

</dd> <dt>

**SCSIPort**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (6)
</dt> </dl>

Numero SCSI della scheda SCSI.

</dd> <dt>

**SCSITarget**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (8)
</dt> </dl>

Contiene il numero del dispositivo di destinazione.

</dd> <dt>

**SectorsPerTrack**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (3)
</dt> </dl>

Numero di settori in ogni traccia per questa unità disco fisico.

</dd> <dt>

**TracksPerCylinder**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (4)
</dt> </dl>

Numero di tracce in ogni cilindro nell'unità disco fisico. Nota: il valore di questa proprietà viene ottenuto tramite funzioni estese dell'interrupt BIOS 13 ore. Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata. Per specifiche di unità accurate, rivolgersi al produttore.

</dd> <dt>

**WriteCacheEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (12)
</dt> </dl>

True se la cache di scrittura è abilitata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                            |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




