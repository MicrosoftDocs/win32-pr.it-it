---
description: Rappresenta le impostazioni ACL della porta estesa.
ms.assetid: 357dd891-6692-4ffc-b8a8-4ece40d4af28
title: Msvm_EthernetSwitchPortExtendedAclSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortExtendedAclSettingData
- Msvm_EthernetSwitchPortExtendedAclSettingData.Name
- Msvm_EthernetSwitchPortExtendedAclSettingData.Direction
- Msvm_EthernetSwitchPortExtendedAclSettingData.Action
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemoteIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalPort
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemotePort
- Msvm_EthernetSwitchPortExtendedAclSettingData.Protocol
- Msvm_EthernetSwitchPortExtendedAclSettingData.Weight
- Msvm_EthernetSwitchPortExtendedAclSettingData.Stateful
- Msvm_EthernetSwitchPortExtendedAclSettingData.IdleSessionTimeout
- Msvm_EthernetSwitchPortExtendedAclSettingData.IsolationID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27f94de089df73c246de887268d34c187bef2507391ceeb33dd7c8cc8068bc43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148320"
---
# <a name="msvm_ethernetswitchportextendedaclsettingdata-class"></a>Classe Msvm \_ EthernetSwitchPortExtendedAclSettingData

Rappresenta le impostazioni ACL della porta estesa.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, UUID("CD168FF0-A16D-4514-B7B5-8BBBA791A928"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Extended ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortExtendedAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  Name = "";
  uint8   Direction = 0;
  uint8   Action = 0;
  string  LocalIPAddress = "ANY";
  string  RemoteIPAddress = "ANY";
  string  LocalPort = "ANY";
  string  RemotePort = "ANY";
  string  Protocol = "ANY";
  Uint16  Weight = 0;
  Boolean Stateful = FALSE;
  Uint16  IdleSessionTimeout = 255;
  Uint32  IsolationID = 0;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ EthernetSwitchPortExtendedAclSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ EthernetSwitchPortExtendedAclSettingData** dispone di queste proprietà.

<dl> <dt>

**Azione**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Azione dell'elenco di controllo di accesso esteso.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

**Consenti** (1)


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

**Deny** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Direzione**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica se l'elenco di controllo di accesso esteso si applica alla direzione in ingresso o in uscita.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

**In** ingresso (1)


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

**In uscita** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IdleSessionTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint16**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Valore di timeout della sessione inattiva (in secondi) per l'ACL con stato.

</dd> <dt>

**IsolationID**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)
</dt> </dl>

ID di isolamento per il quale deve essere applicato l'elenco di controllo di accesso esteso.

</dd> <dt>

**LocalIPAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indirizzo IP locale.

</dd> <dt>

**Localport**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Intervallo di porte locale.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Nome descrittivo dell'elenco di controllo di accesso esteso.

</dd> <dt>

**Protocollo**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Stringa del protocollo.

</dd> <dt>

**RemoteIPAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indirizzo IP remoto.

</dd> <dt>

**Remoteport**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Intervallo di porte remote.

</dd> <dt>

**Stateful**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica se l'elenco di controllo di accesso esteso è con stato o senza stato.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint16**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Peso applicato all'elenco di controllo di accesso esteso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

