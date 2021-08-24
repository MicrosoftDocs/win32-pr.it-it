---
title: MDM_Policy_Config01_NetworkIsolation02 classe
description: La classe Mdm \_ Policy \_ Config01 \_ NetworkIsolation02 rappresenta i criteri del browser disponibili.
ms.assetid: f25ecbef-d232-4731-bac8-38a7d597db00
keywords:
- MDM_Policy_Config01_NetworkIsolation02 classe
- MDM_Policy_Config01_NetworkIsolation02 classe , descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_NetworkIsolation02
- MDM_Policy_Config01_NetworkIsolation02.InstanceID
- MDM_Policy_Config01_NetworkIsolation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759b6a3abbf27e2e074cea2482bec881546c179c88ef45b9a153c21222e153ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750541"
---
# <a name="mdm_policy_config01_networkisolation02-class"></a>Classe \_ \_ \_ NetworkIsolation02 di MDM Policy Config01

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe Mdm Policy \_ \_ Config01 \_ NetworkIsolation02** rappresenta i criteri del browser disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_NetworkIsolation02
{
  string InstanceID;
  string ParentID;
  string EnterpriseIPRange;
  sint32 EnterpriseIPRangesAreAuthoritative;
  string EnterpriseNetworkDomainNames;
  string EnterpriseProxyServers;
  sint32 EnterpriseProxyServersAreAuthoritative;
  string NeutralResources;
  string EnterpriseCloudResources;
  string EnterpriseInternalProxyServers;
};
```

## <a name="members"></a>Members

La **classe MDM Policy \_ \_ Config01 \_ NetworkIsolation02** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Mdm Policy \_ \_ Config01 \_ NetworkIsolation02** ha queste proprietà.

<dl> <dt>

[EnterpriseCloudResources](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisecloudresources)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[EnterpriseInternalProxyServers](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseinternalproxyservers)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[EnterpriseIPRange](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprange)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[EnterpriseIPRangesAreAuthoritative](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprangesareauthoritative)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[EnterpriseNetworkDomainNames](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisenetworkdomainnames)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[EnterpriseProxyServers](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyservers)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[EnterpriseProxyServersAreAuthoritative](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyserversareauthoritative)
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

Identifica il nome del nodo padre. Per questa classe, la stringa è "NetworkIsolation".

</dd> <dt>

[Risorse neutre](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-neutralresources)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
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

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/Policy/Config"

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

