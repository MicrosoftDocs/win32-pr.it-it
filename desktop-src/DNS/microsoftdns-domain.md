---
title: Classe MicrosoftDNS_Domain
description: La \_ classe di dominio MicrosoftDNS rappresenta un dominio in una gerarchia DNS.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- DNS della classe MicrosoftDNS_Domain
- MicrosoftDNS_Domain della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119790"
---
# <a name="microsoftdns_domain-class"></a>\_Classe di dominio MicrosoftDNS

La classe di **\_ dominio MicrosoftDNS** rappresenta un dominio in una gerarchia DNS.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a>Members

La classe di **\_ dominio MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe di **\_ dominio MicrosoftDNS** dispone di questi metodi.



| Metodo                   | Descrizione                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| **Getdistinguishname** | Ottiene il nome distinto DS per la zona. <br/> Qualificatori: implementato<br/> |



 

### <a name="properties"></a>Proprietà

La classe di **\_ dominio MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del contenitore del dominio, che può essere una zona, una cache o un RootHints.

Nei casi in cui il contenitore è una zona (un'istanza della classe di [**\_ zona MicrosoftDNS**](microsoftdns-zone.md) ), questa proprietà contiene il nome di dominio completo della zona.

Quando il contenitore è la zona radice, la stringa \\ \\ deve essere utilizzata.

Nei casi in cui il contenitore è la cache DNS dei record di risorse (un'istanza della classe della [**\_ cache MicrosoftDNS**](microsoftdns-cache.md) ), questa proprietà viene impostata sulla stringa \\ .. Cache \\ .

Se il contenitore è RootHints (un'istanza della classe [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md) ), questa proprietà deve essere impostata su \\ . RootHints \\ .

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN o indirizzo IP del server DNS che contiene il dominio.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN del dominio.

Per le istanze della cache DNS o RootHints, le stringhe \\ .. Memorizza nella cache \\ e \\ .. \\ È necessario usare RootHints, rispettivamente.

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

[**Metodo getdistinguishname della classe di \_ dominio MicrosoftDNS**](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





