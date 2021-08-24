---
title: MDM_Policy_User_Config01_Authentication02 classe
description: La classe Mdm \_ Policy \_ User \_ Config01 \_ Authentication02 rappresenta i criteri di gestione dell'autenticazione disponibili.
ms.assetid: 66d94f97-07ea-4025-95f9-d55282df3661
keywords:
- MDM_Policy_User_Config01_Authentication02 classe
- MDM_Policy_User_Config01_Authentication02 classe, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Authentication02
- MDM_Policy_User_Config01_Authentication02.InstanceID
- MDM_Policy_User_Config01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db9b794127f6085c44568b1671607f54dd58dd16a4af0a4756b6e913e39ca493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694211"
---
# <a name="mdm_policy_user_config01_authentication02-class"></a>Classe \_ Mdm Policy User \_ \_ Config01 \_ Authentication02

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe Mdm Policy User \_ \_ \_ Config01 \_ Authentication02** rappresenta i criteri di gestione dell'autenticazione disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEAPCertSSO;
};
```

## <a name="members"></a>Members

La **classe MDM Policy User \_ \_ \_ Config01 \_ Authentication02** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Mdm Policy User \_ \_ \_ Config01 \_ Authentication02** ha queste proprietà.

<dl> <dt>

[AllowEAPCertSSO](/windows/client-management/mdm/policy-csp-authentication#authentication-alloweapcertsso)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe, la stringa è "Authentication".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./User/Vendor/MSFT/Policy/Config"

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

