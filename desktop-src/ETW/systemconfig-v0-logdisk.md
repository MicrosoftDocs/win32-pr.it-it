---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco logico.
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: Classe SystemConfig_V0_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: dbc1ee189bae1fe71f42267f38bd40763764dea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980546"
---
# <a name="systemconfig_v0_logdisk-class"></a>\_Classe SystemConfig V0 \_ LogDisk

Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco logico.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a>Members

La classe **SystemConfig \_ V0 \_ LogDisk** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **SystemConfig \_ V0 \_ LogDisk** ha queste proprietà.

<dl> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (10)
</dt> </dl>

Numero di byte in ogni settore per l'unità disco fisica.

</dd> <dt>

**Numerodisco**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (3)
</dt> </dl>

Numero di indice del disco contenente questa partizione.

</dd> <dt>

**DriveLetterString**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (6), **Max** (4)
</dt> </dl>

Lettera di unità del disco nel formato " <letter> :".

</dd> <dt>

**DriveType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (5)
</dt> </dl>

Tipo di unità disco. I valori possibili sono:



| Valore                                                                        | Significato                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>1</dt> </dl> | Partition<br/>                            |
| <dl> <dt>2</dt> </dl> | Volume<br/>                               |
| <dl> <dt>3</dt> </dl> | Partizione estesa su più dischi<br/> |



 

</dd> <dt>

**FileSystem**
</dt> <dd> <dl> <dt>

Tipo di dati: **Char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (13), **Max** (16)
</dt> </dl>

File System sul disco logico, ad esempio NTFS.

</dd> <dt>

**NumberOfFreeClusters**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (11)
</dt> </dl>

Numero di cluster liberi nel volume specificato.

</dd> <dt>

**Pad**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (7)
</dt> </dl>

Riservato.

</dd> <dt>

**PartitionNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (8)
</dt> </dl>

Numero di indice della partizione.

</dd> <dt>

**PartitionSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (2)
</dt> </dl>

Dimensioni totali, in byte, della partizione.

</dd> <dt>

**SectorsPerCluster**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (9)
</dt> </dl>

Numero di settori nel volume.

</dd> <dt>

**Dimensioni**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (4)
</dt> </dl>

Dimensioni, in byte, dell'unità disco.

</dd> <dt>

**StartOffset**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (1)
</dt> </dl>

Offset iniziale (in byte) della partizione dall'inizio del disco.

</dd> <dt>

**TotalNumberOfClusters**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (12)
</dt> </dl>

Numero di cluster usati e disponibili nel volume.

</dd> <dt>

**VolumeExt**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (14)
</dt> </dl>

Riservato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




