---
title: Classe MDM_Policy_Config01_Security02
description: La \_ \_ classe Config01 Security02 dei criteri MDM \_ rappresenta i criteri di sicurezza disponibili.
ms.assetid: 8db74f3f-a7a5-4e93-8aeb-111dcf2111fa
keywords:
- Classe MDM_Policy_Config01_Security02
- Classe MDM_Policy_Config01_Security02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Security02
- MDM_Policy_Config01_Security02.InstanceID
- MDM_Policy_Config01_Security02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268e1e01cddb72ddd85e3c18369bdb998bb315aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048417"
---
# <a name="mdm_policy_config01_security02-class"></a>\_ \_ Classe Config01 Security02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ \_ Config01 \_ Security02 dei criteri MDM** rappresenta i criteri di sicurezza disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Security02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddProvisioningPackage;
  sint32 AllowRemoveProvisioningPackage;
  sint32 ClearTPMIfNotReady;
  sint32 PreventAutomaticDeviceEncryptionForAzureADJoinedDevices;
  sint32 RequireDeviceEncryption;
  sint32 RequireProvisioningPackageSignature;
  sint32 RequireRetrieveHealthCertificateOnBoot;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Config01 \_ Security02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ Security02 dei criteri MDM Config01** ha queste proprietà.

<dl> <dt>

[AllowAddProvisioningPackage](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowRemoveProvisioningPackage](/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ClearTPMIfNotReady](/windows/client-management/mdm/policy-csp-security#security-cleartpmifnotready)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe la stringa è "Security".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"

</dd> <dt>

[PreventAutomaticDeviceEncryptionForAzureADJoinedDevices](/windows/client-management/mdm/policy-csp-security#security-preventautomaticdeviceencryptionforazureadjoineddevices)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[RequireDeviceEncryption](/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[RequireProvisioningPackageSignature](/windows/client-management/mdm/policy-csp-security#security-requireprovisioningpackagesignature)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[RequireRetrieveHealthCertificateOnBoot](/windows/client-management/mdm/policy-csp-security#security-requireretrievehealthcertificateonboot)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | \\ \\ DMMap MDM CIMv2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilizzo di script di PowerShell con il provider del Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

