---
description: La classe WMI di associazione Win32 POTSModemToSerialPort mette in relazione un modem con la porta \_ seriale utilizzata dal modem.
ms.assetid: 4dbde5ae-f785-4d2d-80d9-508effd72cf2
ms.tgt_platform: multiple
title: Win32_POTSModemToSerialPort classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModemToSerialPort
- Win32_POTSModemToSerialPort.NegotiatedDataWidth
- Win32_POTSModemToSerialPort.NegotiatedSpeed
- Win32_POTSModemToSerialPort.AccessState
- Win32_POTSModemToSerialPort.NumberOfHardResets
- Win32_POTSModemToSerialPort.NumberOfSoftResets
- Win32_POTSModemToSerialPort.Dependent
- Win32_POTSModemToSerialPort.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9188b456f31f81164ab27966e652c87ad06a80aa5115769d119c8f90dc268f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064431"
---
# <a name="win32_potsmodemtoserialport-class"></a>Classe Win32 \_ POTSModemToSerialPort

La classe [WMI](../wmisdk/retrieving-a-class.md) **di associazione Win32 \_ POTSModemToSerialPort** mette in relazione un modem con la porta seriale utilizzata dal modem.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModemToSerialPort : CIM_ControlledBy
{
  uint32               NegotiatedDataWidth;
  uint64               NegotiatedSpeed;
  uint16               AccessState;
  uint32               NumberOfHardResets;
  uint32               NumberOfSoftResets;
  Win32_POTSModem  REF Dependent;
  Win32_SerialPort REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ POTSModemToSerialPort** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ POTSModemToSerialPort** ha queste proprietà.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il controller sta attivamente per eseguire comandi o accedere al dispositivo. Queste informazioni sono necessarie quando un dispositivo logico può essere utilizzato o accessibile tramite più controller.

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

Tipo di dati: **Win32 \_ SerialPort**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")
</dt> </dl>

SerialPort [**Win32 \_**](win32-serialport.md) che rappresenta la porta seriale utilizzata dal modem.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ POTSModem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ POTSModem")
</dt> </dl>

Oggetto [**\_ POTSModem Win32 che**](win32-potsmodem.md) rappresenta il modem POTS che usa la porta seriale.

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

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](../wmisdk/creating-a-wmi-script.md)

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection.**](cim-deviceconnection.md)

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di reimpostazioni hard reset rilasciate dal controller. Un ripristino a livello di disco riporta il dispositivo allo stato di inizializzazione o avvio. Tutte le informazioni sullo stato interno del dispositivo e i dati vengono persi.

Questa proprietà viene ereditata da [**CIM \_ ControlledBy.**](cim-controlledby.md)

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di reimpostazioni soft-reset rilasciate dal controller. Una reimpostazione soft non cancella completamente lo stato e i dati correnti del dispositivo. La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.

Questa proprietà viene ereditata da [**CIM \_ ControlledBy.**](cim-controlledby.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe WIN32 \_ POTSModemToSerialPort** è derivata da [**CIM \_ ControlledBy.**](cim-controlledby.md)

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

 

 
