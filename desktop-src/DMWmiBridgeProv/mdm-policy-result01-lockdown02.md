---
title: MDM_Policy_Result01_LockDown02 classe
description: La classe MDM \_ Policy \_ Result01 \_ Lockdown02 rappresenta i criteri di blocco disponibili.
ms.assetid: 78eab50e-b1a7-4b96-a848-b8a86a3b82c3
keywords:
- MDM_Policy_Result01_LockDown02 classe
- MDM_Policy_Result01_LockDown02 classe , descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LockDown02
- MDM_Policy_Result01_LockDown02.InstanceID
- MDM_Policy_Result01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9473baaf106c607dac7bab3a7f350173f88044564f536bfa2cd4beadca707c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587871"
---
# <a name="mdm_policy_result01_lockdown02-class"></a>Classe \_ Mdm Policy \_ Result01 \_ LockDown02

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM Policy \_ \_ Result01 \_ Lockdown02** rappresenta i criteri di blocco disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a>Members

La **classe MDM Policy \_ \_ Result01 \_ LockDown02** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM Policy \_ \_ Result01 \_ LockDown02** ha queste proprietà.

<dl> <dt>

[AllowEdgeSwipe](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
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

Identifica il nome del nodo padre. Per questa classe, la stringa è "Lockdown".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/Policy/Result"

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>File mofs \\DMWmiBridgeProv.dll</dt> </dl> |



 

