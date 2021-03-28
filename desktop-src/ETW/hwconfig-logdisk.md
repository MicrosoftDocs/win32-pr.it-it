---
description: La \_ classe HWConfig LogDisk è la classe del tipo di evento per gli eventi di configurazione del disco logico. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: Classe HWConfig_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529886"
---
# <a name="hwconfig_logdisk-class"></a>\_Classe HWConfig LogDisk

La classe **HWConfig \_ LogDisk** è la classe del tipo di evento per gli eventi di configurazione del disco logico.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a>Members

La **classe \_ LogDisk di HWConfig** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ LogDisk di HWConfig** dispone di queste proprietà.

<dl> <dt>

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

Pad
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2)
</dt> </dl>

Riservato.

</dd> <dt>

PartitionSize
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4)
</dt> </dl>

Dimensioni totali, in byte, della partizione.

</dd> <dt>

StartOffset
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Offset iniziale (in byte) della partizione dall'inizio del disco.

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

 

 




