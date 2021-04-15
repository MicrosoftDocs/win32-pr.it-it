---
title: Classe MDM_Policy_Config01_CredentialProviders02
description: La \_ \_ classe Config01 CredentialProviders02 dei criteri MDM \_ Configura i criteri del provider di credenziali disponibili.
ms.assetid: 84a44fef-1481-4d1d-9531-f2ff6f3b36e6
keywords:
- Classe MDM_Policy_Config01_CredentialProviders02
- Classe MDM_Policy_Config01_CredentialProviders02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialProviders02
- MDM_Policy_Config01_CredentialProviders02.InstanceID
- MDM_Policy_Config01_CredentialProviders02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f77a4ec63a37c71353be43836dd307d5f5293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476025"
---
# <a name="mdm_policy_config01_credentialproviders02-class"></a>\_ \_ Classe Config01 CredentialProviders02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La \_ \_ classe Config01 CredentialProviders02 dei criteri MDM \_ Configura i criteri del provider di credenziali disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialProviders02
{
  string InstanceID;
  string ParentID;
  string AllowPINLogon;
  string BlockPicturePassword;
  sint32 DisableAutomaticReDeploymentCredentials;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Config01 \_ CredentialProviders02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ CredentialProviders02 dei criteri MDM Config01** ha queste proprietà.

<dl> <dt>

[AllowPINLogon](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-allowpinlogon)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[BlockPicturePassword](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-blockpicturepassword)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DisableAutomaticReDeploymentCredentials](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-disableautomaticredeploymentcredentials)
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

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

