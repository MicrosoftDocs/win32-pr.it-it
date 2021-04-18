---
description: Rappresenta le impostazioni per il servizio migrazione del sistema virtuale in un host.
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Classe Msvm_VirtualSystemMigrationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c8685e468d60983408c52a985169c61be91f632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305988"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a>\_Classe MSVM VirtualSystemMigrationServiceSettingData

Rappresenta le impostazioni per il servizio migrazione del sistema virtuale in un host. Non è possibile modificare direttamente le proprietà di questa classe. Il client deve chiamare il metodo **MSVM \_ VirtualSystemMigrationService. ModifyServiceSettings** per modificare una di queste proprietà.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a>Members

La **classe \_ VirtualSystemMigrationServiceSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualSystemMigrationServiceSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il meccanismo di autenticazione utilizzato per le connessioni di rete di migrazione del sistema virtuale. Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

**CredSSP** (0)


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

**Kerberos** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata dalla classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se la compressione del traffico della migrazione in tempo reale è abilitata o disabilitata. True indica Enabled.

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**EnableSmbTransport**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se l'utilizzo di SMB come tipo di trasporto per il trasferimento dello stato della macchina virtuale tra gli host Hyper-V durante la migrazione del sistema virtuale è abilitato o disabilitato. **True** indica Enabled. Se le NIC RDMA sono configurate per il trasporto SMB durante la migrazione in tempo reale della macchina virtuale, si ottengono prestazioni migliori. Se il valore di **EnableSmbTransport** è true, il valore di **EnableCompression** viene ignorato.

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**EnableVirtualSystemMigration**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se la migrazione del sistema virtuale è abilitata o disabilitata. La migrazione dell'archiviazione è sempre abilitata. Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .

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

**MaximumActiveStorageMigration**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il numero massimo di migrazioni di archiviazione attive consentite. Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .

</dd> <dt>

**MaximumActiveVirtualSystemMigration**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il numero massimo di migrazioni attive del sistema virtuale consentite. Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

