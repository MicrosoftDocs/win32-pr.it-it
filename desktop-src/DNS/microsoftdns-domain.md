---
title: MicrosoftDNS_Domain classe
description: La classe Di dominio MicrosoftDNS \_ rappresenta un dominio in una gerarchia DNS.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- MicrosoftDNS_Domain DNS della classe
- MicrosoftDNS_Domain classe DNS , descritto
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
ms.openlocfilehash: a30b171777e6c8a99ddadcfb39c8cdfdd90b09a43ae255c9bbcc026db09bdb1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163319"
---
# <a name="microsoftdns_domain-class"></a>Classe di dominio \_ MicrosoftDNS

La **classe \_ Di dominio MicrosoftDNS** rappresenta un dominio in una gerarchia DNS.

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

La **classe \_ di dominio MicrosoftDNS** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ di dominio MicrosoftDNS** include questi metodi.



| Metodo                   | Descrizione                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| **GetDistinguishedName** | Ottiene il nome distinto DS per la zona. <br/> Qualificatori: implementati<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ Di dominio MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**Containername**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del contenitore del dominio, che può essere una zona, una cache o rootHints.

Nei casi in cui il contenitore è una zona (un'istanza della [**classe MicrosoftDNS \_ Zone),**](microsoftdns-zone.md) questa proprietà contiene il nome di dominio completo della zona.

Quando il contenitore è la zona radice, è necessario \\ \\ usare la stringa .

Nei casi in cui il contenitore è la cache DNS dei record di risorse (un'istanza della [**classe \_ Cache MicrosoftDNS),**](microsoftdns-cache.md) questa proprietà è impostata sulla stringa \\ . Memorizzare nella cache \\ .

Se il contenitore è RootHints (un'istanza della [**classe \_ MicrosoftDNS RootHints),**](microsoftdns-roothints.md) questa proprietà deve essere impostata su \\ . RootHints \\ .

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN o indirizzo IP del server DNS che contiene il dominio.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN del dominio.

Per le istanze di Cache DNS o RootHints, le stringhe \\ .. Memorizzare \\ nella cache \\ e . È necessario \\ usare rispettivamente RootHints.

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

[**Metodo GetDistinguishedName della classe di dominio \_ MicrosoftDNS**](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





