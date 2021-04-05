---
title: Classe MDM_VPNv2_RouteList02_01
description: La \_ classe MDM VPNv2 \_ RouteList02 \_ 01 contiene un elenco facoltativo di route da aggiungere alla tabella di routing per l'interfaccia VPN.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- Classe MDM_VPNv2_RouteList02_01
- Classe MDM_VPNv2_RouteList02_01, descritta
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
ms.openlocfilehash: 3ebc274bb3efd2bc78850dd37c95b25db35c4cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048583"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a>\_Classe MDM VPNv2 \_ RouteList02 \_ 01

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** contiene un elenco facoltativo di route da aggiungere alla tabella di routing per l'interfaccia VPN.

Questa operazione è necessaria per i casi di split tunneling in cui il sito del server VPN ha più subnet che la subnet predefinita in base all'indirizzo IP assegnato all'interfaccia.

Ogni computer su cui è in esecuzione TCP/IP prende decisioni di routing. Queste decisioni sono controllate dalla tabella di routing IP. L'aggiunta di valori in questo nodo aggiorna la tabella di routing con le route per l'interfaccia VPN post-connessione. I valori in questo nodo rappresentano il prefisso di destinazione delle route IP. Un prefisso di destinazione è costituito da un prefisso di indirizzo IP e da una lunghezza del prefisso.

L'aggiunta di una route consente allo stack di rete di identificare il traffico che deve superare l'interfaccia VPN per la VPN con split tunneling. Alcuni server VPN possono configurarla durante la negoziazione della connessione e non necessitano di queste informazioni nel profilo VPN. Rivolgersi all'amministratore del server VPN per determinare se sono necessarie queste informazioni nel profilo VPN.

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

La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** presenta queste proprietà.

<dl> <dt>

[Indirizzo](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
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

Identifica il nome del nodo padre.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"

</dd> <dt>

[PrefixSize](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilizzo di script di PowerShell con il provider del Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

