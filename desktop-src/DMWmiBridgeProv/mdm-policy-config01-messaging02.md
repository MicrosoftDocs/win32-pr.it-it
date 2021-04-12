---
title: Classe MDM_Policy_Config01_Messaging02
description: La \_ classe Messaging02 dei criteri MDM \_ Config01 \_ consente di eseguire il backup e il ripristino di messaggi di testo e la messaggistica ovunque. Questo criterio consente a un'organizzazione di disabilitare queste funzionalità per evitare che le informazioni vengano archiviate nei server all'esterno del controllo.
ms.assetid: 179ece8a-d3f4-449c-8392-ca8a35e44a31
keywords:
- Classe MDM_Policy_Config01_Messaging02
- Classe MDM_Policy_Config01_Messaging02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Messaging02
- MDM_Policy_Config01_Messaging02.InstanceID
- MDM_Policy_Config01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137d9c36a822cd93d6cfd0c7cd83197204fb8f97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517734"
---
# <a name="mdm_policy_config01_messaging02-class"></a>\_ \_ Classe Config01 Messaging02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La \_ classe Messaging02 dei criteri MDM \_ Config01 \_ consente di eseguire il backup e il ripristino di messaggi di testo e la messaggistica ovunque. Questo criterio consente a un'organizzazione di disabilitare queste funzionalità per evitare che le informazioni vengano archiviate nei server all'esterno del controllo.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Config01 \_ Messaging02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ Messaging02 dei criteri MDM Config01** ha queste proprietà.

<dl> <dt>

[AllowMessageSync](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
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



 

