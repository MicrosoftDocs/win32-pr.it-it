---
description: Questa classe è la classe del tipo di evento per gli eventi di richiesta di interrupt (IRQ). La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: SystemConfig_IRQ classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3da720de11aa7dbbd759131a521e44e546b7cad6d2525565c81d0aa6920dd0ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078291"
---
# <a name="systemconfig_irq-class"></a>Classe \_ SystemConfig IRQ

Questa classe è la classe del tipo di evento per gli eventi di richiesta di interrupt (IRQ).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a>Members

La **classe \_ SystemConfig IRQ** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SystemConfig IRQ** ha queste proprietà.

<dl> <dt>

**DeviceDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Descrizione del dispositivo o del software che effettua la richiesta.

</dd> <dt>

**DeviceDescriptionLen**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3)
</dt> </dl>

Lunghezza, in caratteri, della stringa in **DeviceDescription**.

</dd> <dt>

**IRQAffinity**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Format("x")
</dt> </dl>

Maschera di affinità IRQ. La maschera di affinità identifica i processori specifici (o gruppi di processori) che possono ricevere l'IRQ.

</dd> <dt>

**IRQNum**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2)
</dt> </dl>

Numero di riga della richiesta di interruzione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




