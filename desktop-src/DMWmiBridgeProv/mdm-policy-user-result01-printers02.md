---
title: MDM_Policy_User_Result01_Printers02 classe
description: La classe Mdm \_ Policy \_ User \_ Result01 \_ Printers02 rappresenta i criteri di stampa disponibili.
ms.assetid: c9555ba3-589c-4b9f-8fad-86fcda031555
keywords:
- MDM_Policy_User_Result01_Printers02 classe
- MDM_Policy_User_Result01_Printers02 classe, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Printers02
- MDM_Policy_User_Result01_Printers02.InstanceID
- MDM_Policy_User_Result01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a220a7d5fddd96ff8202813f42a9c4d765f4fcc134300e18e92139980dadec00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131847"
---
# <a name="mdm_policy_user_result01_printers02-class"></a>Classe \_ Mdm Policy User \_ \_ Result01 \_ Printers02

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe Mdm \_ Policy \_ User \_ Result01 \_ Printers02 rappresenta i criteri di stampa disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions_User;
};
```

## <a name="members"></a>Members

La **classe Mdm Policy User \_ \_ \_ Result01 \_ Printers02** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Mdm Policy User \_ \_ \_ Result01 \_ Printers02** ha queste proprietà.

<dl> <dt>

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

</dd> <dt>

[Utente PointAndPrintRestrictions \_](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions-user)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
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



 

