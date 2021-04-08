---
description: Rappresenta l'associazione tra le estensioni Ethernet e le rispettive funzionalità.
ms.assetid: 6b32235a-175d-48f9-af3a-2d40f748a518
title: Classe Msvm_EthernetSwitchExtensionCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtensionCapabilities
- Msvm_EthernetSwitchExtensionCapabilities.ManagedElement
- Msvm_EthernetSwitchExtensionCapabilities.Capabilities
- Msvm_EthernetSwitchExtensionCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 950a8a0288487bf557e9dd201100b2a894417641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760856"
---
# <a name="msvm_ethernetswitchextensioncapabilities-class"></a>\_Classe MSVM EthernetSwitchExtensionCapabilities

Rappresenta l'associazione tra le estensioni Ethernet e le rispettive funzionalità.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtensionCapabilities : CIM_ElementCapabilities
{
  Msvm_InstalledEthernetSwitchExtension  REF ManagedElement;
  Msvm_EthernetSwitchFeatureCapabilities REF Capabilities;
  uint16                                     Characteristics[];
};
```

## <a name="members"></a>Members

La **classe \_ EthernetSwitchExtensionCapabilities di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ EthernetSwitchExtensionCapabilities di MSVM** dispone di queste proprietà.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("funzionalità")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) che rappresenta l'oggetto funzionalità associato all'opzione. Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> <dt>

**Caratteristiche**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni descrittive sulle funzionalità. Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).



| Valore                                                                                                                                                                                                                       | Significato                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Impostazione predefinita**</dt> <dt>2</dt> </dl> | Le funzionalità associate rappresentano le funzionalità predefinite dell'elemento gestito.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Corrente**</dt> <dt>3</dt> </dl> | Le funzionalità associate rappresentano le funzionalità correnti dell'elemento gestito.<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Managed")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) che rappresenta l'estensione installata. Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

