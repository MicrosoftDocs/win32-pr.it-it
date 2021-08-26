---
title: MDM_Policy_Result01_Messaging02 classe
description: La classe MDM \_ Policy \_ Result01 \_ Messaging02 rappresenta l'SMS di backup e ripristino e la messaggistica ovunque.
ms.assetid: cdc92999-3a2b-4653-b64f-79e19abe5559
keywords:
- MDM_Policy_Result01_Messaging02 classe
- MDM_Policy_Result01_Messaging02 classe, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Messaging02
- MDM_Policy_Result01_Messaging02.InstanceID
- MDM_Policy_Result01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2b16379a6d7fa9c58469c2a047f4d3bf5753fab78f5cc980acc258bf3ee849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045691"
---
# <a name="mdm_policy_result01_messaging02-class"></a>Classe \_ Messaging02 di Mdm Policy \_ \_ Result01 Messaging02

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe MDM \_ Policy \_ Result01 \_ Messaging02 rappresenta l'SMS di backup e ripristino e la messaggistica ovunque.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a>Members

La **classe Mdm Policy \_ \_ Result01 \_ Messaging02** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM Policy \_ \_ Result01 \_ Messaging02** ha queste proprietà.

<dl> <dt>

[AllowMessageSync](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
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

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
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



 

