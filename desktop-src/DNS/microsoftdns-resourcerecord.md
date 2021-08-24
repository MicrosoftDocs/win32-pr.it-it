---
title: MicrosoftDNS_ResourceRecord classe
description: La classe MicrosoftDNS \_ ResourceRecord rappresenta le proprietà generali di un dns RR. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- MicrosoftDNS_ResourceRecord DNS della classe
- MicrosoftDNS_ResourceRecord classe DNS , descritto
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
ms.openlocfilehash: 8b54d23ae522291a2a38ad5d3f046fc444efdefd4d270519fbc3a2ee5739ba47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874801"
---
# <a name="microsoftdns_resourcerecord-class"></a>Classe \_ ResourceRecord MicrosoftDNS

La **classe MicrosoftDNS \_ ResourceRecord** rappresenta le proprietà generali di un dns RR.

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

La **classe MicrosoftDNS \_ ResourceRecord** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MicrosoftDNS \_ ResourceRecord** include questi metodi.



| Metodo                                   | Descrizione                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromTextRepresentation** | Analizza il RR nella stringa TextRepresentation e con i nomi dei server e dei contenitori DNS di input definisce e crea un'istanza di un oggetto ResourceRecord. Il metodo restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: nessuno<br/> |
| **GetObjectByTextRepresentation**        | Recupera un'istanza esistente della sottoclasse MicrosoftDns ResourceRecord, rappresentata dalla stringa TextRepresentation insieme al server DNS e al nome \_ del contenitore. <br/> Qualificatori: nessuno<br/>                                                        |



 

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ ResourceRecord** ha queste proprietà.

<dl> <dt>

**Containername**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il nome del contenitore per l'istanza di Zona, Cache o RootHints che contiene il RR.

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica l'FQDN o l'indirizzo IP del server DNS che contiene il RR.

</dd> <dt>

**Domainname**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Rappresenta il nome di dominio completo del dominio che contiene il RR. Questa proprietà può contenere le stringhe \\ . Cache \\ o \\ . RootHints \\ se la cache interna o RootHints contengono rispettivamente il RR.

</dd> <dt>

**OwnerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del proprietario per il RR.

</dd> <dt>

**RecordClass=1**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**Windows Server 2003: **

Questa stringa rappresenta la classe del record di risorse. I valori validi includono:

1: IN (Internet)

2: CS (CSNET)

3: CH (CHAOS)

4: HS (Hesiod)

</dd> <dt>

**RecordData**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati del record di risorse.

</dd> <dt>

**TextRepresentation**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Rappresentazione testuale dell'intero RR.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora dell'ultimo aggiornamento del RR, espresso in ore trascorse dal 1° gennaio 1601, ora media di Greenwich (GMT).

</dd> <dt>

**TTL**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un [*resolver*](r-gly.md)DNS.

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

[**Metodo CreateInstanceFromTextRepresentation della classe ResourceRecord MicrosoftDNS \_**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[**Metodo GetObjectByTextRepresentation della classe ResourceRecord MicrosoftDNS \_**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





