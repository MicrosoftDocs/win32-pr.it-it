---
description: La classe WMI di associazione PrinterSetting Win32 \_ mette in relazione una stampante e le relative impostazioni di configurazione.
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Win32_PrinterSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: be39a9f614ab172c75e5ddc857254cdd91ea20d1352a33071cd6fa3627132d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759381"
---
# <a name="win32_printersetting-class"></a>Classe PrinterSetting Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) di **associazione \_ PrinterSetting Win32** mette in relazione una stampante e le relative impostazioni di configurazione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a>Members

La **classe \_ PrinterSetting Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ PrinterSetting Win32** ha queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) \| ("CIM CIM \_ LogicalDevice")
</dt> </dl>

Oggetto [**CIM \_ LogicalDevice**](cim-logicaldevice.md) che rappresenta le proprietà del dispositivo logico a cui è possibile applicare le impostazioni.

Questa proprietà viene ereditata da [**\_ DeviceSettings Win32.**](win32-devicesettings.md)

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **impostazione \_ CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](../wmisdk/key-qualifier.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) \| ("CIM CIM \_ Setting")
</dt> </dl>

Impostazione [**CIM \_ che**](cim-setting.md) rappresenta le impostazioni che possono essere applicate al dispositivo logico.

Questa proprietà viene ereditata da [**\_ DeviceSettings Win32.**](win32-devicesettings.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ PrinterSetting Win32** deriva da [**\_ DeviceSettings Win32.**](win32-devicesettings.md)

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

[**Win32 \_ DeviceSettings**](win32-devicesettings.md)
</dt> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

 
