---
description: Rappresenta i dati dell'impostazione della funzionalità RDMA della porta.
ms.assetid: a9b8c98f-194e-4eec-8d4a-961b1a439e62
title: Classe Msvm_EthernetSwitchPortRdmaSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRdmaSettingData
- Msvm_EthernetSwitchPortRdmaSettingData.RdmaOffloadWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98d4f06923bfcfa16d564b296e3b544d9aad6275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885864"
---
# <a name="msvm_ethernetswitchportrdmasettingdata-class"></a>\_Classe MSVM EthernetSwitchPortRdmaSettingData

Rappresenta i dati dell'impostazione della funzionalità RDMA della porta.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("7A498FC4-8572-4FDC-92AB-7A6FC7042D53"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Rdma Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRdmaSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32 RdmaOffloadWeight = 0;
};
```

## <a name="members"></a>Members

La **classe \_ EthernetSwitchPortRdmaSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ EthernetSwitchPortRdmaSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**RdmaOffloadWeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Il peso assegnato a questa porta per RDMA Guest. Il peso è l'importanza relativa durante l'assegnazione delle risorse RDMA. L'impostazione della proprietà **RdmaOffloadWeight** su 0 Disabilita RDMA sulla porta. Il valore predefinito è 0.

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

 

 




