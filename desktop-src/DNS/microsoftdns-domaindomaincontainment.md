---
title: Classe MicrosoftDNS_DomainDomainContainment
description: La \_ classe MicrosoftDNS DomainDomainContainment viene usata per l'indipendenza del dominio; I domini DNS possono contenere altri domini DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- DNS della classe MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048609"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a>\_Classe MicrosoftDNS DomainDomainContainment

La classe **MicrosoftDNS \_ DomainDomainContainment** viene usata per l'indipendenza del dominio; I domini DNS possono contenere altri domini DNS. Ogni istanza della classe [**di \_ dominio MicrosoftDNS**](microsoftdns-domain.md) può contenere più istanze del **\_ dominio MicrosoftDNS**. Un'istanza di un oggetto di **\_ dominio MicrosoftDNS** è contenuta direttamente in non più di un **\_ dominio MicrosoftDNS** di livello superiore.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe \_ DomainDomainContainment di MicrosoftDNS** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ DomainDomainContainment di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ dominio MicrosoftDNS**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: chiave, Max (1), override ("GroupComponent")

Descrizione: un dominio di livello superiore, una zona, una cache o un RootHints.

Ereditato dal \_ componente CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ dominio MicrosoftDNS**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: chiave, override ("PartComponent")

Descrizione: dominio contenuto da un dominio di livello superiore, una zona, una cache o un RootHints.

Ereditato dal \_ componente CIM.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_DomainResourceRecordContainment MicrosoftDNS**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**\_ServerDomainContainment MicrosoftDNS**](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





