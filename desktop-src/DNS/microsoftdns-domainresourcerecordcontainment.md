---
title: MicrosoftDNS_DomainResourceRecordContainment classe
description: La classe MicrosoftDNS DomainResourceRecordContainment viene usata per il contenimento di RR. Ogni istanza del dominio MicrosoftDNS può contenere più istanze della \_ \_ classe ResourceRecord MicrosoftDNS. \_
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- MicrosoftDNS_DomainResourceRecordContainment DNS della classe
- MicrosoftDNS_DomainResourceRecordContainment classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 498d9b953895ebece94dc77edb587045d1cfdd45c29f04c202756bd1080dc9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795611"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a>Classe \_ DomainResourceRecordContainment MicrosoftDNS

La **classe MicrosoftDNS \_ DomainResourceRecordContainment** viene usata per il contenimento di RR. Ogni istanza del dominio [**MicrosoftDNS \_**](microsoftdns-domain.md) può contenere più istanze della [**classe \_ ResourceRecord MicrosoftDNS.**](microsoftdns-resourcerecord.md) Ogni istanza della **classe \_ MicrosoftDNS ResourceRecord** appartiene a una singola istanza della classe Di dominio **MicrosoftDNS \_** ed è definita come debole per tale istanza.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe MicrosoftDNS \_ DomainResourceRecordContainment** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ DomainResourceRecordContainment** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Dominio \_ MicrosoftDNS**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: Key, Override("GroupComponent")

Descrizione: zona, cache, RootHints o dominio che contiene direttamente il record di risorse.

Ereditato dal componente \_ CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **MicrosoftDNS \_ ResourceRecord**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: Key, Override("PartComponent")

Descrizione: record di risorse contenuto in un dominio, una zona, una cache o un roothints.

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

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





