---
description: La relazione CIM ControlledBy indica i dispositivi a cui viene eseguito il comando o l'accesso tramite il dispositivo logico \_ controller.
ms.assetid: 6aa4e088-32a0-4c88-bb82-341b6ab53b4c
ms.tgt_platform: multiple
title: CIM_ControlledBy classe (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.NegotiatedDataWidth
- CIM_ControlledBy.NegotiatedSpeed
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: efaf4d0d9312e929fa79d689490bd9e5b6a3e164dfdecafaf7cd9fe87b16990d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080815"
---
# <a name="cim_controlledby-class-cimwin32-wmi-providers"></a>CIM_ControlledBy classe (provider WMI CIMWin32)

La **relazione CIM \_ ControlledBy** indica i dispositivi a cui viene eseguito il comando o l'accesso tramite il dispositivo logico del controller.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8502C53D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  CIM_LogicalDevice REF Dependent;
  CIM_Controller    REF Antecedent;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
};
```

## <a name="members"></a>Members

La **classe CIM \_ ControlledBy** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ ControlledBy** ha queste proprietà.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il controller sta attivando o accedendo al dispositivo. Queste informazioni sono necessarie quando un dispositivo logico può essere eseguito da più controller o accedervi.

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

Tipo di dati: **Controller CIM \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Controller [**CIM \_ che**](cim-controller.md) rappresenta il controller.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Oggetto [**CIM \_ LogicalDevice**](cim-logicaldevice.md) che rappresenta il dispositivo controllato.

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

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection.**](cim-deviceconnection.md)

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di hard reset emessi dal controller. Un hard reset riporta il dispositivo allo stato di inizializzazione o avvio. Tutte le informazioni e i dati interni sullo stato del dispositivo andranno persi.

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di soft reset emessi dal controller. Un soft reset non cancella completamente lo stato e i dati correnti del dispositivo. La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ ControlledBy** è derivata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).

WMI non implementa questa classe. Per altre informazioni sulle classi derivate **da CIM \_ ControlledBy,** vedere [Classi Win32](win32-provider.md).

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[**CIM \_ DeviceConnection**](cim-deviceconnection.md)
</dt> </dl>

 

