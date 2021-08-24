---
description: Oggetto SystemConfigurationChangeEvent Win32 \_&\# 8194; La classe WMI indica che l'elenco di dispositivi nel sistema è stato aggiornato (un dispositivo è stato aggiunto o rimosso o la configurazione è stata modificata).
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Win32_SystemConfigurationChangeEvent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 63a0708f2e081ffc8c5fb359be1e57aacd1cd62bd1db1daee2063e66e2fb55c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751301"
---
# <a name="win32_systemconfigurationchangeevent-class"></a>Classe \_ SystemConfigurationChangeEvent Win32

La classe  [WMI](../wmisdk/retrieving-a-class.md) **\_ Win32 SystemConfigurationChangeEvent** indica che l'elenco di dispositivi nel sistema è stato aggiornato (un dispositivo è stato aggiunto o rimosso o la configurazione è stata modificata). Viene generato un evento e viene creata un'istanza di questa classe quando viene inviato il messaggio "DevMgrRefreshOn<*ComputerName*>". La modifica esatta all'elenco dei dispositivi non è contenuta nel messaggio, pertanto è necessario un aggiornamento del dispositivo per ottenere le impostazioni di sistema correnti. Esempi di modifiche alla configurazione interessate sono le impostazioni IRQ, le porte COM e le versioni del BIOS.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a>Members

La **classe \_ SystemConfigurationChangeEvent Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SystemConfigurationChangeEvent Win32** ha queste proprietà.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management \| Messages WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management Messages \| WM \_ SETTINGCHANGE")
</dt> </dl>

Tipo di notifica di modifica dell'evento che si è verificata.

Questa proprietà viene ereditata da [**Win32 \_ DeviceChangeEvent.**](win32-devicechangeevent.md)

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

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](../wmisdk/--event.md). Per altre informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere [Costanti di sicurezza WMI.](../wmisdk/wmi-security-constants.md)

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Times).

Questa proprietà viene ereditata [**\_ \_ dall'evento**](../wmisdk/--event.md).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](../wmisdk/creating-a-wmi-script.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ SystemConfigurationChangeEvent Win32** è derivata da [**\_ Win32 DeviceChangeEvent.**](win32-devicechangeevent.md)

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

[**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
