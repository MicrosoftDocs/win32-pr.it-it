---
title: MDM_Policy_User_Config01_CredentialsUI02 classe
description: La classe Mdm \_ Policy \_ User \_ Config01 \_ CredentialsUI02 rappresenta i criteri delle credenziali disponibili.
ms.assetid: b0a45070-c25b-4a4d-9fbc-cd107fd0fa2f
keywords:
- MDM_Policy_User_Config01_CredentialsUI02 classe
- MDM_Policy_User_Config01_CredentialsUI02 classe , descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_CredentialsUI02
- MDM_Policy_User_Config01_CredentialsUI02.InstanceID
- MDM_Policy_User_Config01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac752d6564d0fa2d8c40403c148d6fc09bbc0db7785535ecf943cf1b7ad6940e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694161"
---
# <a name="mdm_policy_user_config01_credentialsui02-class"></a>Classe \_ Mdm Policy User \_ \_ Config01 \_ CredentialsUI02

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe Mdm \_ Policy \_ User \_ Config01 \_ CredentialsUI02 rappresenta i criteri delle credenziali disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
};
```

## <a name="members"></a>Members

La **classe Mdm Policy User \_ \_ \_ Config01 \_ CredentialsUI02** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Mdm Policy User \_ \_ \_ Config01 \_ CredentialsUI02** ha queste proprietà.

<dl> <dt>

[DisablePasswordReveal](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

