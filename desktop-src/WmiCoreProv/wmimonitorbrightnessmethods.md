---
description: Contiene metodi che gestiscono la luminosità del monitoraggio.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: Classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 255cfa75ab892739ce211432ef81d32da4e1cbb3205e5467045e2d81f156d102
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321363"
---
# <a name="wmimonitorbrightnessmethods-class"></a>Classe WmiMonitorBrightnessMethods

La **classe WMI WmiMonitorBrightnessMethods** contiene metodi che gestiscono la luminosità del monitoraggio.

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Members

La **classe WmiMonitorBrightnessMethods** ha questi tipi di membri:

-   [Metodi](#wmimonitorbrightnessmethods-class)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe WmiMonitorBrightnessMethods** include questi metodi.



| Metodo                                                                                                         | Descrizione                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | Imposta nuovamente la luminosità sull'impostazione dei criteri.<br/>     |
| [**WmiSetALSBrightness**](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | Imposta il valore di luminosità del sensore di luce ambientale.<br/>     |
| [**WmiSetALSBrightnessState**](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | Controlla lo stato di luminosità del sensore di luce ambientale.<br/> |
| [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | Imposta la luminosità del monitor.<br/>                        |



 

### <a name="properties"></a>Proprietà

La **classe WmiMonitorBrightnessMethods** ha queste proprietà.

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

 

 




