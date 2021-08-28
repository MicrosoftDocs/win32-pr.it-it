---
description: Rappresenta le impostazioni della larghezza di banda della porta.
ms.assetid: 62a42c4c-8ea1-47c6-8ae6-e9252f2ed0e4
title: Msvm_EthernetSwitchPortBandwidthSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthSettingData
- Msvm_EthernetSwitchPortBandwidthSettingData.InstanceID
- Msvm_EthernetSwitchPortBandwidthSettingData.Caption
- Msvm_EthernetSwitchPortBandwidthSettingData.Description
- Msvm_EthernetSwitchPortBandwidthSettingData.ElementName
- Msvm_EthernetSwitchPortBandwidthSettingData.Reservation
- Msvm_EthernetSwitchPortBandwidthSettingData.Weight
- Msvm_EthernetSwitchPortBandwidthSettingData.Limit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstLimit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c47a1f9b7f6697a58a24b4a5878d1977521a5073cca9d60e0bb3c45594f71496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531351"
---
# <a name="msvm_ethernetswitchportbandwidthsettingdata-class"></a>Classe Msvm \_ EthernetSwitchPortBandwidthSettingData

Rappresenta le impostazioni della larghezza di banda della porta.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Settings";
  string Description = "Represents the port bandwidth settings.";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  uint64 Reservation = 0;
  uint64 Weight = 0;
  uint64 Limit = 0;
  uint64 BurstLimit = 0;
  uint64 BurstSize = 0;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ EthernetSwitchPortBandwidthSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ EthernetSwitchPortBandwidthSettingData** ha queste proprietà.

<dl> <dt>

**BurstLimit**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Larghezza di banda massima consentita dalla porta durante i picchi.

</dd> <dt>

**BurstSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Dimensioni massime di burst consentite.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Bandwidth Impostazioni".

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Rappresenta le impostazioni della larghezza di banda della porta".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Bandwidth Impostazioni".

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Limite**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Limite di larghezza di banda consentito per la porta.

</dd> <dt>

**Prenotazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Larghezza di banda minima assoluta garantita per la porta.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Larghezza di banda minima in peso garantita per la porta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

