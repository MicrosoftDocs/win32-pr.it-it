---
description: La classe CIM SerialInterface rappresenta una relazione CIM ControlledBy che indica i dispositivi a cui si accede tramite il controller seriale e le \_ \_ caratteristiche dell'accesso.
ms.assetid: bebc304a-c2b7-41c7-b24a-8f450ee3c4bb
ms.tgt_platform: multiple
title: CIM_SerialInterface classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialInterface
- CIM_SerialInterface.NegotiatedDataWidth
- CIM_SerialInterface.NegotiatedSpeed
- CIM_SerialInterface.AccessState
- CIM_SerialInterface.NumberOfHardResets
- CIM_SerialInterface.NumberOfSoftResets
- CIM_SerialInterface.Dependent
- CIM_SerialInterface.Antecedent
- CIM_SerialInterface.FlowControlInfo
- CIM_SerialInterface.NumberOfStopBits
- CIM_SerialInterface.ParityInfo
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c6b704c8af9e6907150ed4d09caacaafb0229902005fdbc63453dc315a3401a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919831"
---
# <a name="cim_serialinterface-class"></a>Classe \_ CiM SerialInterface

La **classe \_ CIM SerialInterface** rappresenta una relazione [**CIM \_ ControlledBy**](cim-controlledby.md) che indica i dispositivi a cui si accede tramite il controller seriale e le caratteristiche dell'accesso.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8B309BDA-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SerialInterface : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  CIM_LogicalDevice    REF Dependent;
  CIM_SerialController REF Antecedent;
  uint16                   FlowControlInfo;
  uint16                   NumberOfStopBits;
  uint16                   ParityInfo;
};
```

## <a name="members"></a>Members

La **classe \_ CiM SerialInterface** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CiM SerialInterface** ha queste proprietà.

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

Tipo di dati: **CIM \_ SerialController**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**SerialController \_ CIM**](cim-serialcontroller.md) che descrive il controller seriale.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

[**LogicalDevice \_ CIM**](cim-logicaldevice.md) che descrive il dispositivo logico.

</dd> <dt>

**FlowControlInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il controllo di flusso per i dati trasmessi.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (2)


</dt> <dd></dd> <dt>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XonXoff** (3)


</dt> <dd></dd> <dt>

<span id="RTS_CTS"></span><span id="rts_cts"></span>

<span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)


</dt> <dd></dd> <dt>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**XonXoff e RTS/CTS** (5)


</dt> <dd>

XonXoff e RTS/CTS

</dd> </dl>

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit")
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

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")
</dt> </dl>

Quando sono possibili diverse velocità del bus o della connessione, questa proprietà definisce quella usata tra i dispositivi. La velocità è specificata in bit al secondo. Se la velocità di connessione o bus non viene negoziata o se queste informazioni non sono disponibili o importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

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

</dd> <dt>

**NumberOfStopBits**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit")
</dt> </dl>

Numero di bit di arresto da trasmettere.

</dd> <dt>

**ParityInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Informazioni sull'impostazione di parità per i dati trasmessi.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (1)


</dt> <dd></dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

**Even** (2)


</dt> <dd></dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

**Dispari** (3)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ CIM SerialInterface** è derivata da [**CIM \_ ControlledBy.**](cim-controlledby.md)

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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
</dt> </dl>

 

