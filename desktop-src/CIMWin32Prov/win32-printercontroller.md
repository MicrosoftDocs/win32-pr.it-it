---
description: La \_ classe WMI dell'associazione PrinterController Win32 mette in relazione una stampante e il dispositivo locale a cui è connessa la stampante. Si noti che questa classe restituisce solo le istanze per le stampanti locali.
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Classe Win32_PrinterController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877822"
---
# <a name="win32_printercontroller-class"></a>Win32 \_ PrinterController (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PrinterController Win32** mette in relazione una stampante e il dispositivo locale a cui è connessa la stampante. Si noti che questa classe restituisce solo le istanze per le stampanti locali.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ PrinterController** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PrinterController** dispone di queste proprietà.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato dell'accesso del controller al dispositivo. Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.

Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Sconosciuto

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Attivo

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Inattivo

</dd> </dl>

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ controller CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Riferimento all'istanza [**del \_ controller CIM**](cim-controller.md) che rappresenta il dispositivo locale associato a questa stampante.

Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ stampante Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Riferimento all'istanza [**della \_ stampante Win32**](win32-printer.md) che rappresenta la stampante associata alla periferica locale.

Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza dei dati in uso tra dispositivi (se sono possibili più larghezze di dati del bus o della connessione). La larghezza dei dati è specificata in bit. Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Velocità di utilizzo tra i dispositivi (quando sono possibili più velocità del bus o di connessione). La velocità è specificata in bit al secondo. Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di reimpostazioni rigide rilasciate dal controller.

Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di reimpostazioni software rilasciate dal controller.

Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ PrinterController** è derivata da [**CIM \_ ControlledBy**](cim-controlledby.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
