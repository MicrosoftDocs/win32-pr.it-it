---
title: MDM_Policy_Config01_RemoteProcedureCall02 classe
description: La classe MDM \_ Policy \_ Config01 \_ RemoteProcedureCall02 configura i criteri di chiamata di procedura remota.
ms.assetid: d844c59d-c71e-4a8f-ad1e-955a918a36b8
keywords:
- MDM_Policy_Config01_RemoteProcedureCall02 classe
- MDM_Policy_Config01_RemoteProcedureCall02 classe, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteProcedureCall02
- MDM_Policy_Config01_RemoteProcedureCall02.InstanceID
- MDM_Policy_Config01_RemoteProcedureCall02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4194e426a3293cefbce1d64fb7e267b0b65fdc7a6f26188e11c96d25d8adc00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118165257"
---
# <a name="mdm_policy_config01_remoteprocedurecall02-class"></a>Classe \_ \_ \_ RemoteProcedureCall02 di Mdm Policy Config01

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe MDM \_ Policy \_ Config01 \_ RemoteProcedureCall02 configura i criteri di chiamata di procedura remota.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteProcedureCall02
{
  string InstanceID;
  string ParentID;
  string RestrictUnauthenticatedRPCClients;
  string RPCEndpointMapperClientAuthentication;
};
```

## <a name="members"></a>Members

La **classe Mdm Policy \_ \_ Config01 \_ RemoteProcedureCall02** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Mdm Policy \_ \_ Config01 \_ RemoteProcedureCall02** ha queste proprietà.

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

[RestrictUnauthenticatedRPCClients](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-restrictunauthenticatedrpcclients)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[RPCEndpointMapperClientAuthentication](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-rpcendpointmapperclientauthentication)
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



 

