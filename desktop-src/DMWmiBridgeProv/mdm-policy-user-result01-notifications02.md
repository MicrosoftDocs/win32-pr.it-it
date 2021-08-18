---
title: MDM_Policy_User_Result01_Notifications02 classe
description: La classe MDM \_ Policy \_ User \_ Result01 \_ Notifications02 rappresenta i criteri di notifica disponibili.
ms.assetid: a2da74f3-2585-4c8c-abab-751ba4c708a1
keywords:
- MDM_Policy_User_Result01_Notifications02 classe
- MDM_Policy_User_Result01_Notifications02 classe , descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Notifications02
- MDM_Policy_User_Result01_Notifications02.InstanceID
- MDM_Policy_User_Result01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91143ffaba94abb42acf84f20e537ce81148bb15ab073f5f5318a6b7524633d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077015"
---
# <a name="mdm_policy_user_result01_notifications02-class"></a>Classe MDM \_ Policy \_ User \_ Result01 \_ Notifications02

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM Policy User \_ \_ \_ Result01 \_ Notifications02** rappresenta i criteri di notifica disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a>Members

La **classe MDM Policy User \_ \_ \_ Result01 \_ Notifications02** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM Policy User \_ \_ \_ Result01 \_ Notifications02** ha queste proprietà.

<dl> <dt>

[DisallowNotificationMirroring](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
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

Identifica il nome del nodo padre. Per questa classe, la stringa è "Notifications".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./User/Vendor/MSFT/Policy/Result"

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Spazio dei nomi<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>File mofs \\DMWmiBridgeProv.dll</dt> </dl> |



 

