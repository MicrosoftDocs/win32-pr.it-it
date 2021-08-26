---
description: Questa classe è la classe del tipo di evento per gli eventi del canale IDE. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: SystemConfig_IDEChannel classe
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
ms.openlocfilehash: 8cf764d266d98199e27b40c8690b36183aa82aa2cfb8ded006087ab55f3ddfca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041601"
---
# <a name="systemconfig_idechannel-class"></a>Classe \_ SYSTEMConfig IDEChannel

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

La **classe \_ SYSTEMConfig IDEChannel** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SYSTEMConfig IDEChannel** ha queste proprietà.

<dl> <dt>

**DeviceTimingMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3), Format("x")
</dt> </dl>

Modalità in cui l'IDE potrebbe funzionare. Di seguito sono indicati i valori possibili:

-   PIO \_ MODE0 (0x1)
-   PIO \_ MODE1 (0x2)
-   PIO \_ MODE2 (0x4)
-   PIO \_ MODE3 (0x8)
-   PIO \_ MODE4 (0x10)
-   SWDMA \_ MODE0 (0x20)
-   SWDMA \_ MODE1 (0x40)
-   SWDMA \_ MODE2 (0x80)
-   MWDMA \_ MODE0 (0x100)
-   MWDMA \_ MODE2 (0x200)
-   MWDMA \_ MODE3 (0x400)
-   UDMA \_ MODE0 (0x800)
-   UDMA \_ MODE1 (0x1000)
-   UDMA \_ MODE2 (0x2000)
-   UDMA \_ MODE3 (0x4000)
-   UDMA \_ MODE4 (0x8000)
-   UDMA \_ MODE5 (0x10000)

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Format("x")
</dt> </dl>

Tipo di dispositivo. Di seguito sono indicati i valori possibili:

-   ATA (1)
-   ATAPI (2)

</dd> <dt>

**LocationInformation**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(5), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Canale IDE (ad esempio, Canale primario, Canale secondario e così via).

</dd> <dt>

**LocationInformationLen**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4)
</dt> </dl>

Lunghezza della stringa **LocationInformation.**

</dd> <dt>

**TargetId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1)
</dt> </dl>

Identificatore del disco.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




