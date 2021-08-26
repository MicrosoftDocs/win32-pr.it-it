---
description: La classe WMI di associazione NetworkAdapterSetting Win32 \_ mette in relazione una scheda di rete e le relative impostazioni di configurazione.
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Win32_NetworkAdapterSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f7330e5b6a2b86508528bb1136acd58b308ca4b9c44b31b9b6e0777f4eccd19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972672"
---
# <a name="win32_networkadaptersetting-class"></a>Classe NetworkAdapterSetting Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) **di associazione \_ NetworkAdapterSetting Win32** mette in relazione una scheda di rete e le relative impostazioni di configurazione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a>Members

La **classe \_ NetworkAdapterSetting Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ NetworkAdapterSetting Win32** dispone di queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ NetworkAdapter Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("NetworkAdapter \| WMI Win32") \_
</dt> </dl>

Oggetto [**\_ NetworkAdapter Win32**](win32-networkadapter.md) che descrive le proprietà della scheda di rete che utilizza una particolare impostazione della scheda di rete.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ NetworkAdapterConfiguration Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration")
</dt> </dl>

Oggetto [**\_ NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md) che descrive le impostazioni di configurazione usate nella scheda di rete.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ NetworkAdapterSetting Win32** deriva da [**Win32 \_ DeviceSettings.**](win32-devicesettings.md)

Per informazioni su come usare le classi di associazione, vedere [AssociatoRS OF Statement](../wmisdk/associators-of-statement.md).

## <a name="examples"></a>Esempio

Nell'esempio VBScript seguente viene **utilizzato \_ NetworkAdapterSetting Win32** per identificare l'indirizzo IP nella connessione alla rete locale.


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
Next
```



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

[**Impostazioni dispositivo \_ Win32**](win32-devicesettings.md)
</dt> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> <dt>

[Attività WMI: Rete](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
