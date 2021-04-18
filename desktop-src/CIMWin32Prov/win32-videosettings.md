---
description: La \_ classe WMI dell'associazione VideoSettings Win32 mette in correlazione un controller video e le impostazioni video a cui è possibile applicare.
ms.assetid: 0cc42352-0a89-434d-a8b6-230c677de49c
ms.tgt_platform: multiple
title: Classe Win32_VideoSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoSettings
- Win32_VideoSettings.Setting
- Win32_VideoSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38e949b6b6501dc51b39448d72e6bf61f37fbecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304571"
---
# <a name="win32_videosettings-class"></a>Win32 \_ VideoSettings (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ VideoSettings Win32** mette in correlazione un controller video e le impostazioni video a cui è possibile applicare.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEE-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoSettings : CIM_VideoSetting
{
  CIM_VideoControllerResolution REF Setting;
  Win32_VideoController         REF Element;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ VideoSettings** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ VideoSettings** dispone di queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ VideoController**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ VideoController")
</dt> </dl>

[**\_ VideoController Win32**](win32-videocontroller.md) che contiene le proprietà del controller video in cui è possibile utilizzare un'impostazione video.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ VideoControllerResolution**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("impostazione"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ VideoControllerResolution")
</dt> </dl>

Un [**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) contenente le impostazioni che possono essere applicate al controller video.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ VideoSettings** è derivata da [**CIM \_ VideoSetting**](cim-videosetting.md).

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

[**\_VIDEOSETTING CIM**](cim-videosetting.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
