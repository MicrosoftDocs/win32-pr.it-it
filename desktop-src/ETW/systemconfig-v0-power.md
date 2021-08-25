---
description: "SystemConfig_V0_Power classe: questa classe è la classe del tipo di evento per gli eventi di configurazione dell'alimentazione. La sintassi seguente è semplificata dal codice MOF."
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: SystemConfig_V0_Power classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 588622fb010cf9ca43f7253adc269e86b1755e5e459cbd6320a28d1d5416706a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914341"
---
# <a name="systemconfig_v0_power-class"></a>Classe SystemConfig \_ V0 \_ Power

Questa classe è la classe del tipo di evento per gli eventi di configurazione dell'alimentazione.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a>Members

La **classe SystemConfig \_ V0 \_ Power** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SystemConfig \_ V0 \_ Power** ha queste proprietà.

<dl> <dt>

Pad1
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(6)
</dt> </dl>

Riservato.

</dd> <dt>

Pad2
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(7)
</dt> </dl>

Riservato.

</dd> <dt>

Pad3
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(8)
</dt> </dl>

Riservato.

</dd> <dt>

s1
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1)
</dt> </dl>

True indica che il sistema supporta lo stato di sospensione S1.

</dd> <dt>

s2
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2)
</dt> </dl>

True indica che il sistema supporta lo stato di sospensione S2.

</dd> <dt>

s3
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3)
</dt> </dl>

True indica che il sistema supporta lo stato di sospensione S3.

</dd> <dt>

s4
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4)
</dt> </dl>

True indica che il sistema supporta lo stato di sospensione S4.

</dd> <dt>

s5
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(5)
</dt> </dl>

True indica che il sistema supporta lo stato di sospensione S5.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




