---
title: MicrosoftDNS_ServerDomainContainment classe
description: Ogni istanza della classe WMI di associazione del server MicrosoftDNS \_ può contenere più istanze della classe di dominio MicrosoftDNS. \_
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- MicrosoftDNS_ServerDomainContainment DNS della classe
- MicrosoftDNS_ServerDomainContainment classe DNS , descritto
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
ms.openlocfilehash: bdc747cae72ac4733ad9bec7288858731b6250312d43476a000d2f99a989267d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527251"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a>Classe ServerDomainContainment di MicrosoftDNS \_

Ogni istanza della classe WMI di associazione [**\_ del server MicrosoftDNS**](microsoftdns-server.md) può contenere più istanze della [**classe di dominio MicrosoftDNS. \_**](microsoftdns-domain.md) Ogni istanza della **classe \_ Di dominio MicrosoftDNS** appartiene a una singola istanza della classe **\_ Server MicrosoftDNS** ed è definita come debole per tale server.

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

La **classe MicrosoftDNS \_ ServerDomainContainment** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ ServerDomainContainment** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Server MicrosoftDNS \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: Key, Override ("GroupComponent"), Min (1), Max (1)

Descrizione: server DNS.

Ereditato dal **componente CIM \_**.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Dominio MicrosoftDNS \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatori: Key, Override("PartComponent")

Descrizione: Dominio, zona, cache o RootHints gestito dal server DNS.

Ereditato dal **componente CIM \_**.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe MicrosoftDNS \_ ServerDomainContainment** è derivata dalla **classe Component CIM. \_**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





