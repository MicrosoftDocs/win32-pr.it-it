---
title: MDM_Policy_User_Config01_Printers02 classe
description: La classe MDM \_ Policy \_ User \_ Config01 \_ Printers02 rappresenta i criteri di stampa disponibili.
ms.assetid: 9faeaa04-92b4-43b0-be17-0f85f2eb493c
keywords:
- MDM_Policy_User_Config01_Printers02 classe
- MDM_Policy_User_Config01_Printers02 classe , descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Printers02
- MDM_Policy_User_Config01_Printers02.InstanceID
- MDM_Policy_User_Config01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 656bdd78586f250b4988de23adc4cbe825e14cd2d37c1cbc3c602367eb157443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694011"
---
# <a name="mdm_policy_user_config01_printers02-class"></a>Classe \_ Mdm Policy User \_ \_ Config01 \_ Printers02

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe MDM \_ Policy \_ User \_ Config01 \_ Printers02 rappresenta i criteri di stampa disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions_User;
};
```

## <a name="members"></a>Members

La **classe MDM Policy User \_ \_ \_ Config01 \_ Printers02** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Mdm Policy User \_ \_ \_ Config01 \_ Printers02** ha queste proprietà.

<dl> <dt>

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

</dd> <dt>

[Utente PointAndPrintRestrictions \_](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions-user)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

