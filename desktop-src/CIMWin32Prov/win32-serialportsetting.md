---
description: La \_ classe WMI dell'associazione SerialPortSetting Win32 mette in correlazione una porta seriale e le relative impostazioni di configurazione.
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Classe Win32_SerialPortSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965951"
---
# <a name="win32_serialportsetting-class"></a>Win32 \_ SerialPortSetting (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SerialPortSetting Win32** mette in correlazione una porta seriale e le relative impostazioni di configurazione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SerialPortSetting** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SerialPortSetting** dispone di queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ SerialPort Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| SerialPort Win32 WMI \_ ")
</dt> </dl>

[**\_ SerialPort Win32**](win32-serialport.md) che contiene le proprietà di una porta seriale nel computer.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ SerialPortConfiguration**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPortConfiguration")
</dt> </dl>

[**\_ SerialPortConfiguration Win32**](win32-serialportconfiguration.md) che contiene l'impostazione di configurazione per la porta seriale.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ SerialPortSetting** è derivata da [**Win32 \_ DeviceSettings**](win32-devicesettings.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_DeviceSettings Win32**](win32-devicesettings.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
