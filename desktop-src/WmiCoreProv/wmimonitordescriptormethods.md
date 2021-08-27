---
description: Contiene i metodi che ottengono il contenuto non elaborato dei blocchi di dati standard VESA (Video Electronics Standard Association) Enhanced Extended Display Identification Data (E-EDID) v.1.x standard a 128 byte.
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
ms.openlocfilehash: 7e8fe02540cd68047e3e74c052a8ea833a67d829228979da31bb12e13e84d9f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120961"
---
# <a name="wmimonitordescriptormethods-class"></a>Classe WmiMonitorDescriptorMethods

La classe **WMI WmiMonitorDescriptorMethods** contiene metodi che ottengono il contenuto non elaborato dei blocchi di dati standard VESA (Video Electronics Standard Association) v.1.x standard a 128 byte.

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Members

La **classe WmiMonitorDescriptorMethods** ha questi tipi di membri:

-   [Metodi](#wmimonitordescriptormethods-class)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe WmiMonitorDescriptorMethods** include questi metodi.



| Metodo                                                                                           | Descrizione                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | Accede ai dati non elaborati per un blocco descrittore EDID v.1.x specificato.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe WmiMonitorDescriptorMethods** ha queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nome dell'istanza del monitoraggio specifica.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




