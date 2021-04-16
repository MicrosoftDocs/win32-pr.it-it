---
description: La \_ classe WMI dell'associazione SCSIControllerDevice Win32 mette in correlazione un controller small computer System Interface (SCSI) e il dispositivo logico (unità disco) connesso.
ms.assetid: 0334829c-3625-4acf-8ef3-da934c51e9bf
ms.tgt_platform: multiple
title: Classe Win32_SCSIControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIControllerDevice
- Win32_SCSIControllerDevice.NegotiatedDataWidth
- Win32_SCSIControllerDevice.NegotiatedSpeed
- Win32_SCSIControllerDevice.AccessState
- Win32_SCSIControllerDevice.NumberOfHardResets
- Win32_SCSIControllerDevice.NumberOfSoftResets
- Win32_SCSIControllerDevice.Antecedent
- Win32_SCSIControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a3189f9d9b75321df7c69214e68779864953f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524258"
---
# <a name="win32_scsicontrollerdevice-class"></a>Win32 \_ SCSIControllerDevice (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SCSIControllerDevice Win32** mette in correlazione un controller small computer System Interface (SCSI) e il dispositivo logico (unità disco) connesso.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{CC0F48D2-C847-11d2-911E-0060081A46FD}"), AMENDMENT]
class Win32_SCSIControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_SCSIController REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SCSIControllerDevice** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SCSIControllerDevice** dispone di queste proprietà.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il controller sta attivando o accedendo attivamente al dispositivo. Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.

Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).

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

Tipo di dati: **Win32 \_ controller SCSI**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| CIM \_ Win32 controller SCSI")
</dt> </dl>

Il riferimento all'attività precedente [**Win32 \_ controller SCSI**](win32-scsicontroller.md) rappresenta il controller SCSI associato a questo dispositivo.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("dipendente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Il riferimento dipendente [**CIM \_ LogicalDevice**](cim-logicaldevice.md) rappresenta il dispositivo logico connesso al controller SCSI.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bits")
</dt> </dl>

Quando sono possibili più larghezze di dati del bus o della connessione, questa proprietà definisce quella in uso tra i dispositivi. La larghezza dei dati è specificata in bit. Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit al secondo")
</dt> </dl>

Quando sono possibili più velocità di connessione o bus, questa proprietà definisce quella usata tra i dispositivi. La velocità è specificata in bit al secondo. Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di reimpostazioni rigide rilasciate dal controller. Una reimpostazione hardware restituisce il dispositivo alla relativa inizializzazione o allo stato di avvio. Tutte le informazioni sullo stato del dispositivo interno e i dati vengono persi.

Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di reimpostazioni software rilasciate dal controller. Un ripristino soft non cancella completamente i dati e lo stato corrente del dispositivo. La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.

Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ SCSIControllerDevice** è derivata da [**CIM \_ ControlledBy**](cim-controlledby.md).

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

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
