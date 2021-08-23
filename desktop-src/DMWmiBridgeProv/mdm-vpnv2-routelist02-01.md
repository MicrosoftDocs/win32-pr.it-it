---
title: MDM_VPNv2_RouteList02_01 classe
description: La classe MDM \_ VPNv2 RouteList02 01 contiene un elenco facoltativo di route da aggiungere alla tabella \_ di routing per \_ l'interfaccia VPN.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- MDM_VPNv2_RouteList02_01 classe
- MDM_VPNv2_RouteList02_01 classe, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ea9725d70d3acfe4e6831d1d386aedecfd9374728b103d50b67aa15cb61ec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750271"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a>Classe Mdm \_ VPNv2 \_ RouteList02 \_ 01

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM \_ VPNv2 \_ RouteList02 \_ 01** contiene un elenco facoltativo di route da aggiungere alla tabella di routing per l'interfaccia VPN.

Questa operazione è necessaria per il caso di split tunneling in cui il sito del server VPN dispone di più subnet che la subnet predefinita in base all'INDIRIZZO IP assegnato all'interfaccia.

Ogni computer che esegue TCP/IP prende decisioni di routing. Queste decisioni sono controllate dalla tabella di routing IP. L'aggiunta di valori in questo nodo aggiorna la tabella di routing con route per l'interfaccia VPN dopo la connessione. I valori in questo nodo rappresentano il prefisso di destinazione delle route IP. Un prefisso di destinazione è costituito da un prefisso di indirizzo IP e una lunghezza del prefisso.

L'aggiunta di una route consente all'stack di rete di identificare il traffico che deve passare attraverso l'interfaccia VPN per la VPN a tunnel diviso. Alcuni server VPN possono configurarlo durante la negoziazione della connessione e non necessitano di queste informazioni nel profilo VPN. Rivolgersi all'amministratore del server VPN per determinare se sono necessarie queste informazioni nel profilo VPN.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a>Members

La **classe MDM \_ VPNv2 \_ RouteList02 \_ 01** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM \_ VPNv2 \_ RouteList02 \_ 01** ha queste proprietà.

<dl> <dt>

[Indirizzo](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
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

Identifica il nome del nodo padre.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"

</dd> <dt>

[PrefixSize](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

