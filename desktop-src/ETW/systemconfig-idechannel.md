---
description: Questa classe è la classe del tipo di evento per gli eventi del canale IDE. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: Classe SystemConfig_IDEChannel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60cdfcec8f62e6fb96dcedc895d874f01a209430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526382"
---
# <a name="systemconfig_idechannel-class"></a>\_Classe SystemConfig IDEChannel

Questa classe è la classe del tipo di evento per gli eventi del canale IDE.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a>Members

La **classe \_ IDEChannel di SystemConfig** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ IDEChannel di SystemConfig** dispone di queste proprietà.

<dl> <dt>

**DeviceTimingMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3), Format ("x")
</dt> </dl>

Modalità di funzionamento dell'IDE. Di seguito sono indicati i valori possibili:

-   PIO \_ MODE0 (0x1)
-   PIO \_ Mode1 (0x2)
-   PIO \_ Mode2 (0x4)
-   PIO \_ Mode3 (0x8)
-   PIO \_ MODE4 (0x10)
-   SWDMA \_ MODE0 (0x20)
-   SWDMA \_ Mode1 (0x40)
-   SWDMA \_ Mode2 (0x80)
-   MWDMA \_ MODE0 (0x100)
-   MWDMA \_ Mode2 (0x200)
-   MWDMA \_ Mode3 (0x400)
-   \_MODE0 UDMA (0x800)
-   \_Mode1 UDMA (0x1000)
-   \_Mode2 UDMA (0x2000)
-   \_Mode3 UDMA (0x4000)
-   \_MODE4 UDMA (0x8000)
-   \_Mode5 UDMA (0x10000)

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), Format ("x")
</dt> </dl>

Tipo di dispositivo. Di seguito sono indicati i valori possibili:

-   ATA (1)
-   ATAPI (2)

</dd> <dt>

**LocationInformation**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Il canale IDE, ad esempio canale primario, canale secondario e così via.

</dd> <dt>

**LocationInformationLen**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4)
</dt> </dl>

Lunghezza della stringa **LocationInformation** .

</dd> <dt>

**TargetId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1)
</dt> </dl>

Identificatore del disco.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




