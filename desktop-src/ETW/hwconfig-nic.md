---
description: La \_ classe NIC HWConfig è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: Classe HWConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: df3897c67ed65eeec5ace49dac1088ca35223a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058118"
---
# <a name="hwconfig_nic-class"></a>\_Classe NIC HWConfig

La **classe \_ NIC HWConfig** è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a>Members

La **classe \_ NIC HWConfig** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ NIC HWConfig** dispone di queste proprietà.

<dl> <dt>

NICName
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Nome della scheda di interfaccia di rete.

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

 

 




