---
title: Classe MicrosoftDNS_ServerDomainContainment
description: Ogni istanza della \_ classe WMI dell'associazione al server MicrosoftDNS può contenere più istanze della \_ classe di dominio MicrosoftDNS.
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- DNS della classe MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740266"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a>\_Classe MicrosoftDNS ServerDomainContainment

Ogni istanza della classe WMI dell'associazione al [**\_ Server MicrosoftDNS**](microsoftdns-server.md) può contenere più istanze della classe di [**\_ dominio MicrosoftDNS**](microsoftdns-domain.md) . Ogni istanza della classe **di \_ dominio MicrosoftDNS** appartiene a una singola istanza della classe **\_ Server MicrosoftDNS** e viene definita debole per tale server.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe \_ ServerDomainContainment di MicrosoftDNS** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ServerDomainContainment di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **MicrosoftDNS \_ Server**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: chiave, override ("GroupComponent"), min (1), Max (1)

Descrizione: il server DNS.

Ereditato dal **\_ componente CIM**.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ dominio MicrosoftDNS**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: chiave, override ("PartComponent")

Descrizione: dominio, zona, cache o RootHints gestito dal server DNS.

Ereditato dal **\_ componente CIM**.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **MicrosoftDNS \_ ServerDomainContainment** è derivata dalla classe **del \_ componente CIM** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_DomainDomainContainment MicrosoftDNS**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**\_DomainResourceRecordContainment MicrosoftDNS**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





