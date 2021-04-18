---
description: Contiene i metodi che ottengono il contenuto non elaborato della definizione del video di input dei dati di identificazione (VESA) Enhanced Extended Display Data (E-EDID) v. 1. x blocchi di dati standard a 128 byte.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: Classe WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315740"
---
# <a name="wmimonitordescriptormethods-class"></a>Classe WmiMonitorDescriptorMethods

La classe WMI **WmiMonitorDescriptorMethods** contiene i metodi che ottengono il contenuto non elaborato della definizione di input video di video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v. 1. x blocchi di dati Standard a 128 byte.

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Members

La classe **WmiMonitorDescriptorMethods** dispone di questi tipi di membri:

-   [Metodi](#wmimonitordescriptormethods-class)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **WmiMonitorDescriptorMethods** dispone di questi metodi.



| Metodo                                                                                           | Descrizione                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | Accede ai dati non elaborati per un blocco descrittore EDID v. 1. x specificato.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **WmiMonitorDescriptorMethods** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nome dell'istanza di monitoraggio specifica.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




