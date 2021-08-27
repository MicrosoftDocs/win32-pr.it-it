---
title: MDM_Policy_Result01_DeviceGuard02 classe
description: La classe \_ \_ \_ DeviceGuard02 di Mdm Policy Result01 configura i criteri di Device Guard.
ms.assetid: ba21d324-85dc-4cb5-8123-196413e457eb
keywords:
- MDM_Policy_Result01_DeviceGuard02 classe
- MDM_Policy_Result01_DeviceGuard02 classe, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceGuard02
- MDM_Policy_Result01_DeviceGuard02.InstanceID
- MDM_Policy_Result01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b210ef96f9c094ce21e12526523922804dc442150d2c3259caa72415ab436d3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131981"
---
# <a name="mdm_policy_result01_deviceguard02-class"></a>Classe \_ \_ \_ DeviceGuard02 di Mdm Policy Result01

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe \_ \_ \_ DeviceGuard02 di Mdm Policy Result01 configura i criteri di Device Guard.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a>Members

La **classe \_ \_ \_ DeviceGuard02 di Mdm Policy Result01** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ DeviceGuard02 di Mdm Policy Result01** ha queste proprietà.

<dl> <dt>

[EnableVirtualizationBasedSecurity](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
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

[LsaCfgFlags](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
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

[RequirePlatformSecurityFeatures](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
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



 

