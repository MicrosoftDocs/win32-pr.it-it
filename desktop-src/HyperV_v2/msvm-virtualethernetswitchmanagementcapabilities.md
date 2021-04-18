---
description: Descrive le funzionalità del VirtualEthernetSwitchManagementService MSVM associato \_ .
ms.assetid: daed7a02-bae8-4bda-abc6-0657df7dc4f8
title: Classe Msvm_VirtualEthernetSwitchManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementCapabilities
- Msvm_VirtualEthernetSwitchManagementCapabilities.InstanceID
- Msvm_VirtualEthernetSwitchManagementCapabilities.Caption
- Msvm_VirtualEthernetSwitchManagementCapabilities.Description
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementName
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.MaxElementNameLen
- Msvm_VirtualEthernetSwitchManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameMask
- Msvm_VirtualEthernetSwitchManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IndicationsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupport
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d66d73773b956ecbbbf4ca102b18bb6f8ece4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313844"
---
# <a name="msvm_virtualethernetswitchmanagementcapabilities-class"></a>\_Classe MSVM VirtualEthernetSwitchManagementCapabilities

Descrive le funzionalità del [**\_ VirtualEthernetSwitchManagementService MSVM**](msvm-virtualethernetswitchmanagementservice.md)associato.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  string  Description = "Defines Virtual Ethernet Switch Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a>Members

La **classe \_ VirtualEthernetSwitchManagementCapabilities di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualEthernetSwitchManagementCapabilities di MSVM** dispone di queste proprietà.

<dl> <dt>

**AsynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported")
</dt> </dl>

Matrice di identificatori di metodi, ognuno dei quali identifica un metodo della classe [**\_ VirtualEthernetSwitchManagementService MSVM**](msvm-virtualethernetswitchmanagementservice.md) supportata in modo asincrono dall'implementazione. Questa proprietà viene ereditata da **CIM \_ VirtualSystemManagementCapabilities**.

<dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>

**DefineSystem** (2)


</dt> <dd></dd> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>

**DestroySystem** (3)


</dt> <dd></dd> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>

**DestroySystemConfiguration** (4)


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>

**ModifyResourceSettings** (5)


</dt> <dd></dd> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>

**ModifySystemSettings** (6)


</dt> <dd></dd> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>

**RemoveResources** (7)


</dt> <dd></dd> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>

**SelectSystemConfiguration** (8)


</dt> <dd></dd> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>

**SnapshotSystem** (9)


</dt> <dd></dd> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>

**AddResources** (10)


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

**AddFeatureSettingsSupported** (32779)


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

**ModifyFeatureSettingsSupported** (32780)


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

**RemoveFeatureSettingsSupported** (32781)


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

**AddFeatureSettingsSupported** (32779)


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

**ModifyFeatureSettingsSupported** (32780)


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

**RemoveFeatureSettingsSupported** (32781)


</dt> <dd></dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Virtual Ethernet Switch Management Service Capabilities".

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "definisce le funzionalità del servizio di gestione del comcambio Ethernet virtuale".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Virtual Ethernet Switch Management Service Capabilities".

</dd> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **ElementName** può essere modificata. Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le restrizioni per **ElementName**, espresse come espressione regolare. Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.

</dd> <dt>

**IndicationsSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di identificatori di indicazione, ciascuno dei quali identifica un'indicazione supportata dall'implementazione. Questa proprietà viene ereditata da **CIM \_ VirtualSystemManagementCapabilities**.



| Valore                                                                                                                                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span><dl> <dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt> </dl> | Indica se l'implementazione supporta la notifica sulle modifiche di stato delle istanze [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) che rappresentano le risorse dei sistemi virtuali.<br/> |
| <span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt> </dl>                 | Indica se l'implementazione supporta la notifica sulle modifiche dello stato delle istanze di [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)) .<br/>                                                      |
| <span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt> </dl>         | Indica se l'implementazione supporta la notifica sulle modifiche di stato delle istanze [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresentano i sistemi virtuali.<br/>            |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF riservato**</dt> <dt>..</dt> </dl>                                                                                                                                    |                                                                                                                                                                                                       |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> 32767 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt> </dl>                                                                                                             |                                                                                                                                                                                                       |



 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**IOVSupport**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore booleano che indica se la virtualizzazione di I/O (IOV) è supportata dalla piattaforma. Se il valore è **true**, IOV è supportato dalla piattaforma e **IOVSupportReasons** sarà vuoto. In caso contrario, la proprietà **IOVSupportReasons** avrà i motivi per cui non è possibile supportare IOV.

</dd> <dt>

**IOVSupportReasons**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che indica i possibili motivi per cui IOV non è supportato. Se il valore di **IOVSupport** è **true**, questa matrice sarà vuota.

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo di dati: **unit16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxValue** (256)
</dt> </dl>

Specifica la lunghezza massima supportata della proprietà **ElementName** . Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **unit16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica gli stati possibili che è possibile richiedere quando si utilizza il metodo **RequestStateChange** sull'elemento logico Enabled. Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities** ed è sempre **null**.

</dd> <dt>

**SynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di identificatori di metodi, ognuno dei quali identifica un metodo della classe [**\_ VirtualEthernetSwitchManagementService MSVM**](msvm-virtualethernetswitchmanagementservice.md) supportata in modo sincrono dall'implementazione di. Questa proprietà viene ereditata da **CIM \_ VirtualSystemManagementCapabilities**.

<dl> <dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)
</dt> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)
</dt> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)
</dt> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)
</dt> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)
</dt> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)
</dt> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)
</dt> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)
</dt> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)
</dt> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)
</dt> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)
</dt> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781)
</dt> </dl>

</dd> <dt>

**VirtualSystemTypesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe, ognuna delle quali designa un tipo di sistema virtuale supportato dall'implementazione di. Il valore di ogni elemento di matrice non **null** deve essere conforme al formato definito per la proprietà **VirtualSystemType** della [**classe \_ VirtualSystemSettingData di MSVM**](msvm-virtualsystemsettingdata.md) . Questa proprietà viene ereditata da **CIM \_ VirtualSystemManagementCapabilities**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

