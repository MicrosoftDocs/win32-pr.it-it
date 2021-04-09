---
title: Classe MicrosoftDNS_ResourceRecord
description: La \_ classe MicrosoftDNS ResourceRecord rappresenta le proprietà generali di un RR DNS. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- DNS della classe MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe546ceabb5590ccd4907448af5efd5e2d4fe2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964374"
---
# <a name="microsoftdns_resourcerecord-class"></a>\_Classe MicrosoftDNS ResourceRecord

La classe **MicrosoftDNS \_ ResourceRecord** rappresenta le proprietà generali di un RR DNS.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a>Members

La **classe \_ ResourceRecord di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ ResourceRecord di MicrosoftDNS** dispone di questi metodi.



| Metodo                                   | Descrizione                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromTextRepresentation** | Analizza l'RR nella stringa TextRepresentation e con i nomi del server e del contenitore DNS di input, definisce e crea un'istanza di un oggetto ResourceRecord. Il metodo restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: nessuno<br/> |
| **GetObjectByTextRepresentation**        | Recupera un'istanza esistente della \_ sottoclasse MicrosoftDns ResourceRecord, rappresentata dalla stringa TextRepresentation insieme al server DNS e al nome del contenitore. <br/> Qualificatori: nessuno<br/>                                                        |



 

### <a name="properties"></a>Proprietà

La **classe \_ ResourceRecord di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene l'RR.

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il nome di dominio completo o l'indirizzo IP del server DNS che contiene l'RR.

</dd> <dt>

**NomeDominio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Rappresenta il nome FQDN del dominio che contiene l'RR. Questa proprietà può contenere le stringhe \\ . Cache \\ o \\ .. RootHints \\ se la cache interna o RootHints contengono rispettivamente l'RR.

</dd> <dt>

**OwnerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del proprietario per l'RR.

</dd> <dt>

**RecordClass = 1**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

* * Windows Server 2003: * *

Questa stringa rappresenta la classe del record di risorse. I valori validi includono:

1: IN (Internet)

2: CS (CSNET)

3: CH (CHAOS)

4: HS (Esiodo)

</dd> <dt>

**RecordData**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati del record di risorse.

</dd> <dt>

**TextRepresentation**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Rappresentazione testuale dell'intero RR.

</dd> <dt>

**TimeStamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora dell'ultimo aggiornamento dell'RR, espressa in ore trascorse dal 1 gennaio 1601, ora di Greenwich (GMT).

</dd> <dt>

**TTL**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo, in secondi, che l'RR può memorizzare nella cache da un [*resolver*](r-gly.md)DNS.

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

[**Metodo CreateInstanceFromTextRepresentation della classe MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[**Metodo GetObjectByTextRepresentation della classe MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





