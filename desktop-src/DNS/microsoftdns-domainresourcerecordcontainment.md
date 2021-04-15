---
title: Classe MicrosoftDNS_DomainResourceRecordContainment
description: La \_ classe MicrosoftDNS DomainResourceRecordContainment viene usata per il contenimento del record RR. ogni istanza del \_ dominio MicrosoftDNS può contenere più istanze della \_ classe MicrosoftDNS ResourceRecord.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- DNS della classe MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment della classe DNS, descritta
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
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476756"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a>\_Classe MicrosoftDNS DomainResourceRecordContainment

La classe **MicrosoftDNS \_ DomainResourceRecordContainment** viene usata per il contenimento del record RR. ogni istanza del [**\_ dominio MicrosoftDNS**](microsoftdns-domain.md) può contenere più istanze della classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) . Ogni istanza della classe **MicrosoftDNS \_ ResourceRecord** appartiene a una singola istanza della classe di **\_ dominio MicrosoftDNS** e viene definita debole per tale istanza.

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

La **classe \_ DomainResourceRecordContainment di MicrosoftDNS** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ DomainResourceRecordContainment di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ dominio MicrosoftDNS**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: chiave, override ("GroupComponent")

Descrizione: la zona, la cache, RootHints o il dominio contenente direttamente il record di risorse.

Ereditato dal \_ componente CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **MicrosoftDNS \_ ResourceRecord**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: chiave, override ("PartComponent")

Descrizione: il record di risorse contenuto in un dominio, una zona, una cache o un RootHints.

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

[**\_ServerDomainContainment MicrosoftDNS**](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[**\_DomainDomainContainment MicrosoftDNS**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





