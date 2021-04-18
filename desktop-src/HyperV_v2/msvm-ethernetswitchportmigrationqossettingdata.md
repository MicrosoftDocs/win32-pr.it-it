---
description: Rappresenta le impostazioni QOS VFP.
ms.assetid: e58a7a8d-0301-43ea-9338-18bc8c458e2d
title: Classe Msvm_EthernetSwitchPortMigrationQosSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortMigrationQosSettingData
- Msvm_EthernetSwitchPortMigrationQosSettingData.QueueId
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_ReservationMode
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_LinkSpeedPercentage
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_DefaultReservation
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareLimits
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableSoftwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundReservedValue
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundMaximumMbps
- Msvm_EthernetSwitchPortMigrationQosSettingData.InboundMaximumMbps
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e279b24178c33c760477995ff744a0699cea1aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313855"
---
# <a name="msvm_ethernetswitchportmigrationqossettingdata-class"></a>\_Classe MSVM EthernetSwitchPortMigrationQosSettingData

Rappresenta le impostazioni QOS VFP.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, UUID("FD2A5DE3-DC6C-4320-82A5-234D3AF55297"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("E9B59CFA-2BE1-4B21-828F-B6FBDBDDC017"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VFP QOS Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortMigrationQosSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  QueueId = "";
  uint8   Switch_ReservationMode = 0;
  uint8   Switch_LinkSpeedPercentage = 0;
  uint64  Switch_DefaultReservation = 0;
  boolean Switch_EnableHardwareLimits = FALSE;
  boolean Switch_EnableHardwareReservations = FALSE;
  boolean Switch_EnableSoftwareReservations = TRUE;
  uint64  OutboundReservedValue = 0;
  uint64  OutboundMaximumMbps = 0;
  uint64  InboundMaximumMbps = 0;
};
```

## <a name="members"></a>Members

La **classe \_ EthernetSwitchPortMigrationQosSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ EthernetSwitchPortMigrationQosSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**InboundMaximumMbps**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Valore del limite della larghezza di banda per il traffico in ingresso.

</dd> <dt>

**OutboundMaximumMbps**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Valore del limite della larghezza di banda per il traffico in uscita.

</dd> <dt>

**OutboundReservedValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Valore di prenotazione della larghezza di banda.

</dd> <dt>

**QueueId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

ID della coda QOS.

</dd> <dt>

**Cambia \_ DefaultReservation**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Valore di prenotazione predefinito.

</dd> <dt>

**Cambia \_ EnableHardwareLimits**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (5), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Indica se vengono tentati gli offload hardware per i limiti, se disponibili.

</dd> <dt>

**Cambia \_ EnableHardwareReservations**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (6), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Indica se vengono tentati gli offload hardware per le prenotazioni se disponibili.

</dd> <dt>

**Cambia \_ EnableSoftwareReservations**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica se è disponibile la prenotazione basata su software.

</dd> <dt>

**Cambia \_ LinkSpeedPercentage**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Percentuale di velocità del collegamento da usare per la prenotazione.

</dd> <dt>

**Cambia \_ ReservationMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Modalità di prenotazione QOS sull'opzione.

<dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

**Absolute** (0)


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

**Peso** (1)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EthernetSwitchPortFeatureSettingData MSVM**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

