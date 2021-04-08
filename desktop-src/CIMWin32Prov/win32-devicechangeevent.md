---
description: La \_ classe WMI astratta Win32 DeviceChangeEvent rappresenta gli eventi di modifica del dispositivo risultanti dall'aggiunta, dalla rimozione o dalla modifica dei dispositivi nel computer.
ms.assetid: 78155357-4231-4ded-980e-89feeb864ef2
ms.tgt_platform: multiple
title: Classe Win32_DeviceChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceChangeEvent
- Win32_DeviceChangeEvent.SECURITY_DESCRIPTOR
- Win32_DeviceChangeEvent.TIME_CREATED
- Win32_DeviceChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f97ab262d95b70a69b06e15202a78d5c1364f90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749031"
---
# <a name="win32_devicechangeevent-class"></a>Win32 \_ DeviceChangeEvent (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) astratta **Win32 \_ DeviceChangeEvent** rappresenta gli eventi di modifica del dispositivo risultanti dall'aggiunta, dalla rimozione o dalla modifica dei dispositivi nel computer. Sono incluse le modifiche apportate alla configurazione hardware (ancoraggio e disancoraggio), lo stato dell'hardware o i dispositivi appena mappati (mapping di un'unità di rete). Ad esempio, un dispositivo è stato modificato quando \_ viene inviato un messaggio WM DEVICECHANGE.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("0DE6AAF8-49F1-4868-B3D4-61CB69BA4322"), AMENDMENT]
class Win32_DeviceChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ DeviceChangeEvent** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ DeviceChangeEvent** dispone di queste proprietà.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management Messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management Messages \| WM \_ SETTINGCHANGE")
</dt> </dl>

Tipo di notifica di modifica dell'evento che si è verificato.

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

**Configurazione modificata** (1)


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

**Arrivo del dispositivo** (2)


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

**Rimozione del dispositivo** (3)


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

**Ancoraggio** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event). Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**ORA di \_ creazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Time).

Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Commenti

**Win32 \_ DeviceChangeEvent** è una classe astratta derivata da [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).

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

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

