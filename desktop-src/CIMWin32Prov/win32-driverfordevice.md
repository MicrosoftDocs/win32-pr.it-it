---
description: La classe WMI di associazione \_ Win32 DriverForDevice correla un'istanza della stampante a un'istanza del driver della stampante.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Win32_DriverForDevice classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f55025c84b8ab7e7114f5a1746d84f8fbdb6b0a7dfe952abfe84efb980430881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546321"
---
# <a name="win32_driverfordevice-class"></a>Classe \_ Win32 DriverForDevice

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **di associazione \_ Win32 DriverForDevice** correla un'istanza della stampante a un'istanza del driver della stampante.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 DriverForDevice** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ DriverForDevice** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Stampante Win32 \_**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Riferimento [**all'istanza \_ della stampante Win32**](win32-printer.md) che rappresenta la stampante.

Questa proprietà viene ereditata dalla [**dipendenza CIM \_**](cim-dependency.md).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ PrinterDriver**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento [**all'istanza \_ di PrinterDriver Win32**](win32-printerdriver.md) che rappresenta il driver della stampante.

Questa proprietà viene ereditata dalla [**dipendenza CIM \_**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe Win32 \_ DriverForDevice** è derivata dalla [**dipendenza \_ CIM**](cim-dependency.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

