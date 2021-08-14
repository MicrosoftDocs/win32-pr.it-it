---
description: La classe NIC HWConfig \_ è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: HWConfig_NIC classe
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
ms.openlocfilehash: 1d9b82f8a97c1ca47734b5bb0a1db09167510978c53f86870df01f2acc59b2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394725"
---
# <a name="hwconfig_nic-class"></a>Classe NIC \_ HWConfig

La **classe NIC HWConfig \_ è** la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete.

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

La **classe \_ NIC HWConfig** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ NIC HWConfig** ha queste proprietà.

<dl> <dt>

NICName
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Nome della scheda di interfaccia di rete.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




