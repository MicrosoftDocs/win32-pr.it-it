---
description: Rappresenta le impostazioni per il servizio di migrazione del sistema virtuale in un host.
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Msvm_VirtualSystemMigrationServiceSettingData classe
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
ms.openlocfilehash: 9ab3feab1f34d0f44ce5cd0618915d8575af9e463a9ec772961c185e946ac094
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963501"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a>Classe Msvm \_ VirtualSystemMigrationServiceSettingData

Rappresenta le impostazioni per il servizio di migrazione del sistema virtuale in un host. Le proprietà per questa classe non possono essere modificate direttamente. Il client deve chiamare il **metodo Msvm \_ VirtualSystemMigrationService.ModifyServiceSettings** per modificare una di queste proprietà.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe Msvm \_ VirtualSystemMigrationServiceSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VirtualSystemMigrationServiceSettingData** ha queste proprietà.

<dl> <dt>

**Authenticationtype**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il meccanismo di autenticazione usato per le connessioni di rete di migrazione del sistema virtuale. Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della [**classe Msvm \_ VirtualSystemMigrationService.**](msvm-virtualsystemmigrationservice.md)

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

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata dalla [**classe \_ CIM ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se la compressione del traffico di migrazione in tempo reale è abilitata o disabilitata. True indica abilitato.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**EnableSmbTransport**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se l'uso di SMB come tipo di trasporto per il trasferimento dello stato della macchina virtuale tra gli host Hyper-V durante la migrazione del sistema virtuale è abilitato o disabilitato. **True** indica abilitato. Si ottiene un miglioramento delle prestazioni se le schede di interfaccia di rete RDMA sono configurate per il trasporto SMB durante la migrazione in tempo reale delle macchine virtuali. Se **il valore di EnableSmbTransport** è true, il valore di **EnableCompression** viene ignorato.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**EnableVirtualSystemMigration**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se la migrazione del sistema virtuale è abilitata o disabilitata. Archiviazione migrazione è sempre abilitata. Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della [**classe Msvm \_ VirtualSystemMigrationService.**](msvm-virtualsystemmigrationservice.md)

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

**MaximumActiveStorageMigration**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il numero massimo di migrazioni di archiviazione attive consentite. Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della [**classe Msvm \_ VirtualSystemMigrationService.**](msvm-virtualsystemmigrationservice.md)

</dd> <dt>

**MaximumActiveVirtualSystemMigration**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il numero massimo di migrazioni del sistema virtuale attive consentite. Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della [**classe Msvm \_ VirtualSystemMigrationService.**](msvm-virtualsystemmigrationservice.md)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

