---
description: La classe \_ WMI Win32 AutochkSetting rappresenta le impostazioni per l'operazione di controllo automatico di un disco.
ms.assetid: 637f4d5d-f2f0-4fe0-bbde-7804156979b7
ms.tgt_platform: multiple
title: Win32_AutochkSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AutochkSetting
- Win32_AutochkSetting.Caption
- Win32_AutochkSetting.Description
- Win32_AutochkSetting.SettingID
- Win32_AutochkSetting.UserInputDelay
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6cccf1877d8812e1fee4816e80189b8404d4090a1ef15f45e840fdd6e58d8ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020329"
---
# <a name="win32_autochksetting-class"></a>Classe \_ AutochkSetting Win32

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ Win32 AutochkSetting** rappresenta le impostazioni per l'operazione di controllo automatico di un disco.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, AMENDMENT]
class Win32_AutochkSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 UserInputDelay;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ AutochkSetting** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ AutochkSetting** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**Chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

ID utilizzato come parte di una chiave per l'oggetto corrente.

</dd> <dt>

**UserInputDelay**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM \\ \\ CurrentControlSet \\ \\ Control Session Manager \\ \\ \| AutoChkTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")
</dt> </dl>

Ritardo di input dell'utente per il controllo automatico.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe Win32 \_ AutochkSetting** è derivata dall'impostazione [**CIM \_**](cim-setting.md).

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

[**Impostazione \_ CIM**](cim-setting.md)
</dt> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> </dl>

 

