---
description: La classe WMI di associazione \_ WIN32 COMApplicationSettings mette in relazione un'applicazione DCOM e le relative impostazioni di configurazione.
ms.assetid: b08eaff1-b42a-42f3-abf7-3664b6195acd
ms.tgt_platform: multiple
title: Win32_COMApplicationSettings classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationSettings
- Win32_COMApplicationSettings.Setting
- Win32_COMApplicationSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a1126563b00861ab8b8168832f72189c3a3828378f5d89c4b74e49f68b09bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417911"
---
# <a name="win32_comapplicationsettings-class"></a>Classe COMApplicationSettings Win32 \_

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) di **associazione WIN32 \_ COMApplicationSettings** mette in relazione un'applicazione DCOM e le relative impostazioni di configurazione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A563-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationSettings : CIM_ElementSetting
{
  Win32_DCOMApplicationSetting REF Setting;
  Win32_DCOMApplication        REF Element;
};
```

## <a name="members"></a>Members

La **classe \_ WIN32 COMApplicationSettings** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ WIN32 COMApplicationSettings** ha queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ DCOMApplication**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")
</dt> </dl>

Oggetto [**\_ DCOMApplication Win32**](win32-dcomapplication.md) che rappresenta l'applicazione DCOM in cui vengono applicate le impostazioni.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ DCOMApplicationSetting**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplicationSetting")
</dt> </dl>

Oggetto [**\_ DCOMApplicationSetting Win32**](win32-dcomapplicationsetting.md) che rappresenta le impostazioni di configurazione associate all'applicazione DCOM.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ WIN32 COMApplicationSettings** è derivata da [**CIM \_ ElementSetting.**](cim-elementsetting.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento \_ CIMSetting**](cim-elementsetting.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

