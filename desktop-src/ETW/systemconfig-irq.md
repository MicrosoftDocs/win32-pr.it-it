---
description: Questa classe è la classe del tipo di evento per gli eventi di richiesta di interrupt (IRQ). La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: Classe SystemConfig_IRQ
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
ms.openlocfilehash: e1dd674c34c06259bc343615c17d165be3f57d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977591"
---
# <a name="systemconfig_irq-class"></a>\_Classe IRQ SystemConfig

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

La **classe \_ IRQ SystemConfig** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ IRQ SystemConfig** ha queste proprietà.

<dl> <dt>

**DeviceDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Descrizione del dispositivo o del software che effettua la richiesta.

</dd> <dt>

**DeviceDescriptionLen**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Lunghezza, in caratteri, della stringa in **DeviceDescription**.

</dd> <dt>

**IRQAffinity**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), Format ("x")
</dt> </dl>

Maschera di affinità IRQ. Affinity mask identifica i processori o i gruppi di processori specifici che possono ricevere l'IRQ.

</dd> <dt>

**IRQNum**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2)
</dt> </dl>

Numero di riga della richiesta di interrupt.

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

 

 




