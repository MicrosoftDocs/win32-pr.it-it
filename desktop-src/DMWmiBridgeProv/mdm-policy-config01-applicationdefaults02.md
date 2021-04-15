---
title: Classe MDM_Policy_Config01_ApplicationDefaults02
description: La \_ \_ \_ classe Config01 APPLICATIONDEFAULTS02 di criteri MDM consente a un amministratore di impostare il tipo di file e le associazioni di protocollo predefiniti. Se impostato, le associazioni predefinite verranno applicate all'accesso al PC.
ms.assetid: 01a45151-bce3-47a7-bffe-1a3f5a1348ff
keywords:
- Classe MDM_Policy_Config01_ApplicationDefaults02
- Classe MDM_Policy_Config01_ApplicationDefaults02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02.InstanceID
- MDM_Policy_Config01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246278b1e4185337ebb63d9d23f74e2ff8753615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476036"
---
# <a name="mdm_policy_config01_applicationdefaults02-class"></a>\_ \_ Classe Config01 ApplicationDefaults02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La \_ \_ \_ classe Config01 APPLICATIONDEFAULTS02 di criteri MDM consente a un amministratore di impostare il tipo di file e le associazioni di protocollo predefiniti. Se impostato, le associazioni predefinite verranno applicate all'accesso al PC.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Config01 \_ ApplicationDefaults02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ ApplicationDefaults02 dei criteri MDM Config01** ha queste proprietà.

<dl> <dt>

[DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
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



 

