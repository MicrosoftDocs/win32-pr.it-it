---
title: Classe MDM_VPNv2_Manual03
description: MDM \_ VPNv2 \_ Manual03class è un nodo facoltativo contenente le impostazioni manuali del server.
ms.assetid: c294c5a2-35e2-46ca-b7d8-9c63f9d3cdd6
keywords:
- Classe MDM_VPNv2_Manual03
- Classe MDM_VPNv2_Manual03, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_Manual03
- MDM_VPNv2_Manual03.InstanceID
- MDM_VPNv2_Manual03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e36d9a048e3a5a523770b9a3987a346fe2283
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964783"
---
# <a name="mdm_vpnv2_manual03-class"></a>\_Classe MDM VPNv2 \_ Manual03

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe **MDM \_ VPNv2 \_ Manual03** è un nodo facoltativo contenente le impostazioni manuali del server.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Manual03
{
  string InstanceID;
  string ParentID;
  string Server;
};
```

## <a name="members"></a>Members

La classe **MDM \_ VPNv2 \_ Manual03** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **MDM \_ VPNv2 \_ Manual03** dispone di queste proprietà.

<dl> <dt>

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

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/proxy/"

</dd> <dt>

[Server](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-manual-server)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
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

 

