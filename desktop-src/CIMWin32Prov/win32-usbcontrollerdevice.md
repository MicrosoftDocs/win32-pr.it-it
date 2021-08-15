---
description: La classe WMI di associazione USBControllerDevice Win32 mette in relazione un \_ controller USB (Universal Serial Bus) e l'istanza CIM \_ LogicalDevice connessa.
ms.assetid: a0c64984-9116-4cb8-86e0-38c897cb7119
ms.tgt_platform: multiple
title: Win32_USBControllerDevice classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_USBControllerDevice
- Win32_USBControllerDevice.NegotiatedDataWidth
- Win32_USBControllerDevice.NegotiatedSpeed
- Win32_USBControllerDevice.AccessState
- Win32_USBControllerDevice.NumberOfHardResets
- Win32_USBControllerDevice.NumberOfSoftResets
- Win32_USBControllerDevice.Antecedent
- Win32_USBControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a7627426a094d8c335032363b3213aeca19e400d5761d23ede8b7cecf0dcab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118007261"
---
# <a name="win32_usbcontrollerdevice-class"></a>Classe USBControllerDevice Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) di associazione **\_ USBControllerDevice Win32** mette in relazione un controller USB (Universal Serial Bus) e l'istanza [**CIM \_ LogicalDevice**](cim-logicaldevice.md) connessa.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{DE57D792-A032-11D2-90F0-0060081A46FD}"), AMENDMENT]
class Win32_USBControllerDevice : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBController REF Antecedent;
  CIM_LogicalDevice REF Dependent;
};
```

## <a name="members"></a>Members

La **classe WIN32 \_ USBControllerDevice** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe WIN32 \_ USBControllerDevice** ha queste proprietà.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il controller sta attivando o accedendo al dispositivo. Queste informazioni sono necessarie quando un dispositivo logico può essere eseguito da più controller o accedervi.

Questa proprietà viene ereditata da [**CIM \_ ControlledBy.**](cim-controlledby.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Attivo** (1)


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**Inattivo** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ USBController**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) \| ("CIM CIM \_ USBController")
</dt> </dl>

[**USBController \_ CIM**](cim-usbcontroller.md) che rappresenta il controller USB (Universal Serial Bus) associato a questo dispositivo.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) \| ("CIM CIM \_ LogicalDevice")
</dt> </dl>

Oggetto [**CIM \_ LogicalDevice che**](cim-logicaldevice.md) descrive il dispositivo logico connesso al controller USB (Universal Serial Bus).

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit")
</dt> </dl>

Quando sono possibili diverse larghezze di bus o dati di connessione, questa proprietà definisce quella in uso tra i dispositivi. La larghezza dei dati è specificata in bit. Se la larghezza dei dati non viene negoziata o se queste informazioni non sono disponibili o importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection.**](cim-deviceconnection.md)

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit al secondo")
</dt> </dl>

Quando sono possibili diverse velocità del bus o della connessione, questa proprietà definisce quella usata tra i dispositivi. La velocità è specificata in bit al secondo. Se la velocità di connessione o bus non viene negoziata o se queste informazioni non sono disponibili o importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection.**](cim-deviceconnection.md)

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di hard reset emessi dal controller. Un hard reset riporta il dispositivo allo stato di inizializzazione o avvio. Tutte le informazioni e i dati interni sullo stato del dispositivo andranno persi.

Questa proprietà viene ereditata da [**CIM \_ ControlledBy.**](cim-controlledby.md)

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di soft reset emessi dal controller. Un soft reset non cancella completamente lo stato e i dati correnti del dispositivo. La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.

Questa proprietà viene ereditata da [**CIM \_ ControlledBy.**](cim-controlledby.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe WIN32 \_ USBControllerDevice** è derivata da [**CIM \_ ControlledBy.**](cim-controlledby.md)

Per una discussione sull'uso, vedere [l'articolo del](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) blog Displaying USB Devices using WMI (Visualizzazione di dispositivi USB con WMI). Per una descrizione dell'uso delle classi di associazione, vedere [l'articolo Get-USB - Uso delle classi di associazione WMI in PowerShell.](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/)

## <a name="examples"></a>Esempio

Nell'esempio di PowerShell seguente viene recuperato il dispositivo logico dipendente e vengono visualizzate le informazioni pertinenti.


```PowerShell
gwmi Win32_USBControllerDevice |%{[wmi]($_.Dependent)} | Sort Manufacturer,Description,DeviceID | Ft -GroupBy Manufacturer Description,Service,DeviceID
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

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

 
