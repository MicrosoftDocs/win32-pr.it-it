---
description: Rappresenta i dati delle impostazioni del dominio di routing.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Msvm_EthernetSwitchPortRoutingDomainSettingData classe
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
ms.openlocfilehash: b0bc01c7e771996d46c29b0f6341e3a535860c4c36996562e7e526ca5db59a2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523841"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a>Classe Msvm \_ EthernetSwitchPortRoutingDomainSettingData

Rappresenta i dati delle impostazioni del dominio di routing.

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

La **classe Msvm \_ EthernetSwitchPortRoutingDomainSettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ EthernetSwitchPortRoutingDomainSettingData** dispone di queste proprietà.

<dl> <dt>

**IsolationIdList**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (3), [**Versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

ID VirtualSubnetId o VLAN per i domini di routing.

</dd> <dt>

**IsolationIdNameList**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (4), [**Versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Matrice di nomi descrittivi VirtualSubnetId o VLAN.

</dd> <dt>

**RoutingDomainGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

GUID del dominio di routing.

</dd> <dt>

**RoutingDomainName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Nome descrittivo del dominio di routing.

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

 

