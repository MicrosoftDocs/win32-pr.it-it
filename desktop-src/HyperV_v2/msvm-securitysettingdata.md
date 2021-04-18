---
description: Rappresenta lo stato configurato delle impostazioni di sicurezza per.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Classe Msvm_SecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312885"
---
# <a name="msvm_securitysettingdata-class"></a>\_Classe MSVM SecuritySettingData

Rappresenta lo stato configurato delle impostazioni di sicurezza per una macchina virtuale.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a>Members

La **classe \_ SecuritySettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SecuritySettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**DataProtectionRequested**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** per richiedere la protezione dei dati per una macchina virtuale. in caso contrario, **false**. Il valore predefinito è **false**.

</dd> <dt>

**EncryptStateAndVmMigrationTraffic**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** per avere lo stato e il traffico di migrazione di una macchina virtuale crittografata; in caso contrario, **false**. Il valore predefinito per una VM appena creata è **false**.

</dd> <dt>

**KsdEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** per abilitare un dispositivo di archiviazione chiavi (KSD) per la macchina virtuale. in caso contrario, **false**. Una macchina virtuale appena creata ha un KSD Disable.

</dd> <dt>

**ShieldingRequested**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** per richiedere la schermatura per una macchina virtuale. in caso contrario, **false**. Una macchina virtuale appena creata ha uno stato richiesto per la schermatura iniziale di **false**.

</dd> <dt>

**TpmEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** per abilitare un modulo TPM (Trusted Platform nodul) per questa macchina virtuale. in caso contrario, **false**. Una macchina virtuale appena creata dispone di un TPM disabilitato.

</dd> <dt>

**VirtualizationBasedSecurityOptOut**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** per non offrire una protezione basata sulla virtualizzazione delle macchine virtuali; in caso contrario, **false**. L'impostazione predefinita per lo stato di rifiuto esplicito di una macchina virtuale appena creata è **false**.

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

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

