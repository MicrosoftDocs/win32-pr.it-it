---
title: MDM_VPNv2_AppTriggerList02_App04 classe
description: La classe MDM \_ VPNv2AppTriggerList02 App04 descrive un elenco di applicazioni impostate per \_ attivare la VPN.
ms.assetid: d17ec7b9-8a66-47da-8373-81b56168b495
keywords:
- MDM_VPNv2_AppTriggerList02_App04 classe
- MDM_VPNv2_AppTriggerList02_App04 classe, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_AppTriggerList02_App04
- MDM_VPNv2_AppTriggerList02_App04.InstanceID
- MDM_VPNv2_AppTriggerList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067e23f747ff5fdc6b3e9c848a5d8f4b8463b716c14cadd5cac9d89bfe2ab746
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109241"
---
# <a name="mdm_vpnv2_apptriggerlist02_app04-class"></a>Classe \_ \_ AppTriggerList02 App04 MDM VPNv2 \_

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM \_ VPNv2AppTriggerList02 \_ App04** descrive un elenco di applicazioni impostate per attivare la VPN.

Se una di queste app viene avviata e il profilo VPN è attualmente il profilo attivo, questo profilo VPN verrà attivato per la connessione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_AppTriggerList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a>Members

La **classe MDM \_ VPNv2 \_ AppTriggerList02 \_ App04** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM \_ VPNv2 \_ AppTriggerList02 \_ App04** ha queste proprietà.

<dl> <dt>

[Id](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
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

Nodo app sotto l'ID riga.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"

</dd> <dt>

[Tipo](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
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
| Spazio dei nomi<br/>                | DMMap \\ MDM CIMv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

