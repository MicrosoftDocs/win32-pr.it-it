---
title: MicrosoftDNS_DomainDomainContainment classe
description: La classe MicrosoftDNS \_ DomainDomainContainment viene usata per il contenimento del dominio. I domini DNS possono contenere altri domini DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- MicrosoftDNS_DomainDomainContainment DNS di classe
- MicrosoftDNS_DomainDomainContainment classe DNS , descritto
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
ms.openlocfilehash: f8f96d03f007af463fb4c4f672eb0d1374867636f4a4224469589563b9c5882e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084751"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a>Classe MicrosoftDNS \_ DomainDomainContainment

La **classe MicrosoftDNS \_ DomainDomainContainment** viene usata per il contenimento del dominio. I domini DNS possono contenere altri domini DNS. Ogni istanza della [**classe \_ di dominio MicrosoftDNS**](microsoftdns-domain.md) può contenere più altre istanze del **dominio \_ MicrosoftDNS.** Un'istanza di **un oggetto \_ Dominio MicrosoftDNS** è direttamente contenuta in non più di un dominio **MicrosoftDNS di \_ livello superiore.**

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

La **classe MicrosoftDNS \_ DomainDomainContainment** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ DomainDomainContainment** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Dominio MicrosoftDNS \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: Key, Max(1), Override("GroupComponent")

Descrizione: Dominio, zona, cache o RootHints di livello superiore.

Ereditato dal componente \_ CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Dominio MicrosoftDNS \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: Key, Override("PartComponent")

Descrizione: dominio contenuto in un dominio, una zona, una cache o rootHints di livello superiore.

Ereditato dal componente \_ CIM.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





