---
description: Rappresenta i dati dell'impostazione del dominio di routing.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Classe Msvm_EthernetSwitchPortRoutingDomainSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885863"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a>\_Classe MSVM EthernetSwitchPortRoutingDomainSettingData

Rappresenta i dati dell'impostazione del dominio di routing.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a>Members

La **classe \_ EthernetSwitchPortRoutingDomainSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ EthernetSwitchPortRoutingDomainSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**IsolationIdList**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (3), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

ID VirtualSubnetId o VLAN per i domini di routing.

</dd> <dt>

**IsolationIdNameList**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (4), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Matrice di nomi descrittivi VirtualSubnetId o VLAN.

</dd> <dt>

**RoutingDomainGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

GUID del dominio di routing.

</dd> <dt>

**RoutingDomainName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Nome descrittivo del dominio di routing.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EthernetSwitchPortFeatureSettingData MSVM**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

