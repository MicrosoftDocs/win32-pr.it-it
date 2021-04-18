---
description: La \_ classe WMI dell'associazione DriverForDevice Win32 mette in correlazione un'istanza di stampante a un'istanza di driver della stampante.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Classe Win32_DriverForDevice
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
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305092"
---
# <a name="win32_driverfordevice-class"></a>Win32 \_ DriverForDevice (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ DriverForDevice Win32** mette in correlazione un'istanza di stampante a un'istanza di driver della stampante.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ DriverForDevice** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ DriverForDevice** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ stampante Win32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Riferimento all'istanza [**della \_ stampante Win32**](win32-printer.md) che rappresenta la stampante.

Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ PrinterDriver**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'istanza [**Win32 \_ PrinterDriver**](win32-printerdriver.md) che rappresenta il driver della stampante per la stampante.

Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ DriverForDevice** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

