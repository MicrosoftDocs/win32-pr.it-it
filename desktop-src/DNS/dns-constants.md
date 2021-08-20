---
title: Costanti DNS
description: Le costanti seguenti sono definite per DNS nell'ordine dei byte dell'host.
ms.assetid: 95bc9193-7962-498a-9abd-c4718ac35f0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61da11c9d8f5af28e2152bad5fe9c7b5eb6eb7d83fdb7f94c11e8c2f3c04d9f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118164157"
---
# <a name="dns-constants"></a>Costanti DNS

Le costanti seguenti sono definite per DNS nell'ordine dei byte dell'host.

## <a name="dns-record-types"></a>Tipi di record DNS



| Costante           | Valore            |
|--------------------|------------------|
| TIPO DI DNS \_ \_ A       | 0x0001           |
| NS \_ DI TIPO DNS \_      | 0x0002           |
| TIPO DNS \_ \_ MD      | 0x0003           |
| MF DI TIPO DNS \_ \_      | 0x0004           |
| DNS \_ TYPE \_ CNAME   | 0x0005           |
| SOA \_ DI \_ TIPO DNS     | 0x0006           |
| TIPO DI \_ \_ DNS MB      | 0x0007           |
| MG \_ DI TIPO \_ DNS      | 0x0008           |
| TIPO \_ DNS \_ MR      | 0x0009           |
| TIPO DNS \_ \_ NULL    | 0x000a           |
| WKS DI TIPO DNS \_ \_     | 0x000b           |
| TIPO DNS \_ \_ PTR     | 0x000c           |
| HINFO \_ DI TIPO DNS \_   | 0x000d           |
| MINFO \_ DI TIPO DNS \_   | 0x000e           |
| DNS \_ TYPE \_ MX      | 0x000f           |
| TESTO \_ DEL TIPO \_ DNS    | 0x0010           |
| RP \_ DI \_ TIPO DNS      | 0x0011           |
| TIPO DNS \_ \_ AFSDB   | 0x0012           |
| TIPO \_ DI DNS \_ X25     | 0x0013           |
| \_ \_ ISDN DI TIPO DNS    | 0x0014           |
| TIPO DI \_ \_ DNS RT      | 0x0015           |
| TIPO DNS \_ \_ NSAP    | 0x0016           |
| TIPO DNS \_ \_ NSAPPTR | 0x0017           |
| TIPO DI DNS \_ \_ SIG     | 0x0018           |
| CHIAVE \_ DI TIPO \_ DNS     | 0x0019           |
| TIPO \_ DNS \_ PX      | 0x001a           |
| GPOS \_ DI \_ TIPO DNS    | 0x001b           |
| TIPO \_ DNS \_ AAAA    | 0x001c           |
| LOC \_ DI TIPO DNS \_     | 0x001d           |
| TIPO DNS \_ \_ NXT     | 0x001e           |
| EID DI TIPO DNS \_ \_     | 0x001f           |
| TIPO DNS \_ \_ NIMLOC  | 0x0020           |
| TIPO DNS \_ \_ SRV     | 0x0021           |
| TIPO DNS \_ \_ ATMA    | 0x0022           |
| TIPO DNS \_ \_ NAPTR   | 0x0023           |
| TIPO DNS \_ \_ KX      | 0x0024           |
| CERTIFICATO \_ DI TIPO \_ DNS    | 0x0025           |
| TIPO \_ DI DNS \_ A6      | 0x0026           |
| TIPO DNS \_ \_ DNAME   | 0x0027           |
| SINK \_ DI TIPO \_ DNS    | 0x0028           |
| OPT \_ PER IL TIPO \_ DNS     | 0x0029           |
| DNS \_ TYPE \_ DS      | 0x002B           |
| \_RRSIG DI TIPO DNS \_   | 0x002E           |
| NSEC \_ DI TIPO DNS \_    | 0x002F           |
| DNS \_ TYPE \_ DNSKEY  | 0x0030           |
| \_ \_ DHCID DI TIPO DNS   | 0x0031           |
| UINFO \_ DI TIPO DNS \_   | 0x0064           |
| UID TIPO DNS \_ \_     | 0x0065           |
| GID \_ DI TIPO DNS \_     | 0x0066           |
| TIPO DNS \_ \_ UNSPEC  | 0x0067           |
| ADDRS \_ DI \_ TIPO DNS   | 0x00f8           |
| TKEY \_ DI TIPO DNS \_    | 0x00f9           |
| TIPO DNS \_ \_ TSIG    | 0x00fa           |
| TIPO \_ DNS \_ IXFR    | 0x00fb           |
| TIPO DNS \_ \_ AXFR    | 0x00fc           |
| TIPO DNS \_ \_ MAILB   | 0x00fd           |
| TIPO DNS \_ \_ MAILA   | 0x00fe           |
| TIPO \_ DNS \_ ALL     | 0x00ff           |
| TIPO \_ DNS \_ ANY     | 0x00ff           |
| WINS \_ DEL TIPO \_ DNS    | 0xff01           |
| WINSR \_ DI TIPO DNS \_   | 0xff02           |
| TIPO \_ DNS \_ NBSTAT  | WINSR \_ DI TIPO DNS \_ |



 

## <a name="dns-class-types"></a>Tipi di classi DNS



| Costante             | Valore  |
|----------------------|--------|
| CLASSE DNS \_ \_ INTERNET | 0x0001 |
| CLASSE DNS \_ \_ CSNET    | 0x0002 |
| CLASSE DNS \_ \_ CHAOS    | 0x0003 |
| CLASSE \_ \_ DNS HESIOD   | 0x0004 |
| CLASSE DNS \_ \_ NONE     | 0x00fe |
| CLASSE DNS \_ \_ ALL      | 0x00ff |
| CLASSE DNS \_ \_ ANY      | 0x00ff |



 

## <a name="dns-query-types"></a>Tipi di query DNS



| Costante                    | Valore  |
|-----------------------------|--------|
| DNS \_ OPCODE \_ QUERY          | 0x0000 |
| DNS \_ OPCODE \_ IQUERY         | 0x0001 |
| STATO DEL SERVER DNS \_ OPCODE \_ \_ | 0x0002 |
| CODICE OPERATIVO DNS \_ \_ SCONOSCIUTO        | 0x0003 |
| NOTIFICA \_ DEL CODICE OPERATIVO \_ DNS         | 0x0004 |
| AGGIORNAMENTO \_ DEL CODICE OPERATIVO \_ DNS         | 0x0005 |



 

## <a name="dns-record-flags"></a>Flag di record DNS

I flag seguenti fanno riferimento alla sezione di un record di risorse all'interno di un messaggio DNS:



| Costante           | Valore      | Significato                         |
|--------------------|------------|---------------------------------|
| DOMANDA \_ DNSREC   | 0x00000000 | RR si trova nella sezione della domanda   |
| RISPOSTA \_ DNSREC     | 0x00000001 | RR si trova nella sezione delle risposte     |
| AUTORITÀ \_ DNSREC  | 0x00000002 | RR si trova nella sezione authority  |
| DNSREC \_ ADDITIONAL | 0x00000003 | RR si trova nella sezione aggiuntiva |



 

I flag seguenti fanno riferimento a una sezione di RR all'interno di un messaggio DNS di aggiornamento per [RFC 2136:](https://www.ietf.org/rfc/rfc2136.txt)



| Costante       | Valore      | Significato                           |
|----------------|------------|-----------------------------------|
| ZONA \_ DNSREC   | 0x00000000 | RR si trova nella sezione zone         |
| DNSREC \_ PREREQ | 0x00000001 | RR si trova nella sezione dei prerequisiti |
| DNSREC \_ UPDATE | 0x00000002 | RR si trova nella sezione update       |



 

I flag seguenti si escludono a vicenda:



| Costante        | Valore      | Significato                                                    |
|-----------------|------------|------------------------------------------------------------|
| DNSREC \_ DELETE  | 0x00000004 | Eliminare un RR. Usato in combinazione con DNSREC \_ UPDATE       |
| DNSREC \_ NOEXIST | 0x00000004 | RR non esiste. Usato in combinazione con DNSREC \_ PREREQ |



 

## <a name="dns-query-options"></a>Opzioni di query DNS



| Costante                                | Valore      | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DNS \_ QUERY \_ STANDARD                    | 0x00000000 | Query standard.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| RISPOSTA \_ \_ \_ TRONCATA ALLA QUERY DNS \_ | 0x00000001 | Restituisce risultati troncati. Non esegue nuovi tentativi in TCP.                                                                                                                                                                                                                                                                                                                                                                                                   |
| LA QUERY DNS \_ \_ USA SOLO \_ \_ TCP              | 0x00000002 | Usa tcp solo per la query.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| QUERY DNS \_ \_ SENZA \_ RICORSIONE               | 0x00000004 | Indica al server DNS di eseguire una query iterativa, in particolare indica al server DNS di non eseguire la risoluzione ricorsiva per risolvere la query.                                                                                                                                                                                                                                                                                                   |
| DNS \_ QUERY \_ BYPASS \_ CACHE               | 0x00000008 | Ignora la cache [*del resolver*](r-gly.md) nella ricerca.                                                                                                                                                                                                                                                                                                                                                                            |
| QUERY DNS \_ \_ SENZA QUERY IN \_ \_ TRANSITO             | 0x00000010 | Indica a DNS di eseguire una query solo nella cache locale. **Windows 2000 Server e Windows 2000 Professional:** Questo valore non è supportato. Per una funzionalità simile, usare **DNS \_ QUERY CACHE \_ \_ ONLY.**<br/>                                                                                                                                                                                                                                      |
| QUERY DNS \_ \_ SENZA NOME \_ \_ LOCALE             | 0x00000020 | Indica a DNS di ignorare il nome locale. **Windows 2000 Server e Windows 2000 Professional:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                    |
| QUERY DNS \_ \_ SENZA \_ FILE HOSTS \_             | 0x00000040 | Impedisce alla query DNS di consultare il file HOSTS. **Windows 2000 Server e Windows 2000 Professional:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                   |
| DNS \_ QUERY \_ NO \_ NETBT                   | 0x00000080 | Impedisce alla query DNS di usare NetBT per la risoluzione. **Windows 2000 Server e Windows 2000 Professional:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                  |
| SOLO \_ WIRE DI QUERY \_ \_ DNS                  | 0x00000100 | Indica a DNS di eseguire una query solo tramite la rete, ignorando le informazioni locali. **Windows 2000 Server e Windows 2000 Professional:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                      |
| MESSAGGIO \_ RESTITUITO DELLA QUERY \_ \_ DNS             | 0x00000200 | Indica a DNS di restituire l'intero messaggio di risposta DNS. **Windows 2000 Server e Windows 2000 Professional:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                   |
| SOLO \_ \_ MULTICAST DI QUERY \_ DNS             | 0x00000400 | Impedisce l'uso di DNS da parte della query e usa solo LLMNR (Local Link Multicast Name Resolution). **Windows Vista e Windows Server 2008 o versioni successive:** Questo valore è supportato.<br/>                                                                                                                                                                                                                                                                  |
| DNS \_ QUERY \_ NO \_ MULTICAST               | 0x00000800 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| QUERY DNS \_ \_ - CONSIDERA COME \_ \_ FQDN             | 0x00001000 | Impedisce alla risposta DNS di collegare suffissi al nome inviato in un processo di risoluzione dei nomi.                                                                                                                                                                                                                                                                                                                                                  |
| DNS \_ QUERY \_ ADDRCONFIG                  | 0x00002000 | Windows 7: non inviare query di tipo [**A**](/windows/win32/api/windns/ns-windns-dns_a_data) se gli indirizzi IPv4 non sono disponibili in un'interfaccia e non inviare query di tipo [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) se gli indirizzi IPv6 non sono disponibili.                                                                                                                                                                                                                                   |
| DNS \_ QUERY \_ DUAL \_ ADDR                  | 0x00004000 | Windows solo 7: eseguire query su record di tipo [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) e [**A**](/windows/win32/api/windns/ns-windns-dns_a_data) e restituire i risultati per ognuno. I risultati **per i** record di tipo A vengono mappati nel **tipo AAAA.**                                                                                                                                                                                                                                                           |
| ATTESA \_ \_ MULTICAST QUERY DNS \_             | 0x00020000 | Attende un timeout completo per raccogliere tutte le risposte dal collegamento locale. Se non è impostato, il comportamento predefinito è restituire con la prima risposta. **Windows Vista e Windows Server 2008 o versione successiva:** Questo valore è supportato.<br/>                                                                                                                                                                                                              |
| VERIFICA \_ \_ MULTICAST QUERY DNS \_           | 0x00040000 | Indirizza un test usando il nome host del computer locale per verificare l'univocità dei nomi nello stesso collegamento locale. Raccoglie tutte le risposte anche se il normale comportamento del mittente LLMNR non è abilitato. **Windows Vista e Windows Server 2008 o versioni successive:** Questo valore è supportato.<br/>                                                                                                                                                                                  |
| QUERY DNS \_ NON REIMPOSTA I VALORI \_ \_ \_ TTL \_    | 0x00100000 | Se impostato e se la risposta contiene più record, i record vengono archiviati con la durata (TTL) corrispondente al valore minimo TTL tra tutti i record. Quando questa opzione è impostata, il valore "Non modificare la durata (TTL) dei singoli record" nel set di record restituito non viene modificato.                                                                                                                                                                               |
| QUERY DNS \_ \_ - DISABILITARE LA CODIFICA \_ \_ IDN      | 0x00200000 | Disabilita il supporto della codifica IDN (International Domain Name) nelle API [**DnsQuery,**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) [**DnsQueryEx,**](/windows/desktop/api/Windns/nf-windns-dnsqueryex) [**DnsModifyRecordsInSet**](/windows/desktop/api/Windns/nf-windns-dnsmodifyrecordsinset_a)e [**DnsReplaceRecordSet.**](/windows/desktop/api/Windns/nf-windns-dnsreplacerecordseta) Tutti i nomi punycode vengono trattati come ASCII e saranno codificati ASCII in rete. Tutti i nomi non ASCII vengono codificati in UTF8 in transito. **Windows 8 o versioni successive:** Questo valore è supportato.<br/> |
| AGGIUNTA \_ \_ MULTIETICHETTA QUERY DNS \_          | 0x00800000 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| QUERY DNS \_ \_ RISERVATE                    | 0xf0000000 | Riservato.                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="dns-update-options"></a>Opzioni di aggiornamento DNS



| Costante                                 | Valore      | Significato                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMPOSTAZIONE PREDEFINITA \_ PER \_ L'USO DELLA \_ SICUREZZA DEGLI AGGIORNAMENTI \_ DNS      | 0x00000000 | Usa il comportamento predefinito, specificato nel Registro di sistema, per gli aggiornamenti dns dinamici sicuri.                                                                |
| SICUREZZA AGGIORNAMENTO DNS \_ \_ \_ DISATTIVATA               | 0x00000010 | Non tenta di proteggere gli aggiornamenti dinamici.                                                                                                                      |
| SICUREZZA AGGIORNAMENTO DNS \_ \_ \_ ON                | 0x00000020 | Tenta l'aggiornamento dinamico non sicuro. Se rifiutato, tenta di proteggere l'aggiornamento dinamico.                                                                               |
| SOLO SICUREZZA \_ \_ DEGLI AGGIORNAMENTI \_ DNS              | 0x00000100 | Tenta di proteggere solo gli aggiornamenti dinamici.                                                                                                                         |
| CONTESTO DI \_ SICUREZZA DELLA CACHE DEGLI AGGIORNAMENTI \_ \_ \_ DNS    | 0x00000200 | Memorizza nella cache il contesto di sicurezza da utilizzare nelle transazioni future.                                                                                                   |
| TEST \_ \_ DELL'AGGIORNAMENTO DNS \_ USA ACCOUNT DI \_ SISTEMA \_ \_ LOCALE | 0x00000400 | Usa le credenziali dell'account del computer locale.                                                                                                               |
| AGGIORNAMENTO DNS \_ \_ \_ FORZARE IL \_ NEGO SULLA SICUREZZA       | 0x00000800 | Non usa il contesto di sicurezza memorizzato nella cache.                                                                                                                         |
| PROVA TUTTI I SERVER MASTER PER \_ \_ \_ \_ L'AGGIORNAMENTO DNS \_   | 0x00001000 | Invia gli aggiornamenti DNS a tutti i server DNS multi-master.                                                                                                            |
| \_L'AGGIORNAMENTO DNS NON IGNORA SCHEDE DI \_ \_ \_ \_ AGGIORNAMENTO  | 0x00002000 | Non aggiornare le schede in cui gli aggiornamenti DNS dinamici sono disabilitati. **Windows 2000 Server con SP2 o versione successiva:** Questo valore è supportato.<br/>                 |
| AGGIORNAMENTO \_ DEL SERVER REMOTO \_ \_ DNS              | 0x00004000 | Registrare i record CNAME in un server remoto oltre al server DNS locale. **Windows 2000 Server con SP2 o versione successiva:** Questo valore è supportato.<br/> |
| DNS \_ UPDATE \_ RESERVED                    | 0xffff0000 | Riservato per utilizzi futuri.                                                                                                                                      |



 

## <a name="dns-response-codes"></a>Codici di risposta DNS



| Errore                | Significato                                        |
|----------------------|------------------------------------------------|
| DNS \_ RCODE \_ NOERROR  | Nessun errore                                       |
| DNS \_ RCODE \_ FORMERR  | Errore di formato                                   |
| DNS \_ RCODE \_ SERVFAIL | Errore del server                                 |
| DNS \_ RCODE \_ NXDOMAIN | Errore del nome                                     |
| DNS \_ RCODE \_ NOTIMPL  | Non implementato                                |
| RCODE \_ DNS \_ RIFIUTATO  | Connection refused                             |
| DNS \_ RCODE \_ YXDOMAIN | Il nome di dominio non deve esistere                   |
| DNS \_ RCODE \_ YXRRSET  | Il set di record di risorse (RR) non deve esistere      |
| DNS \_ RCODE \_ NXRRSET  | Set di RR inesistente                          |
| DNS \_ RCODE \_ NOTAUTH  | Non autorevole per la zona                     |
| DNS \_ RCODE \_ NOTZONE  | Nome non presente nella zona                               |
| DNS \_ RCODE \_ BADVERS  | Meccanismo di estensione non valida per la versione DNS (EDNS) |
| DNS \_ RCODE \_ BADSIG   | Firma non valida                                  |
| DNS \_ RCODE \_ BADKEY   | Chiave non chiave                                        |
| DNS \_ RCODE \_ BADTIME  | Timestamp non valido                                  |



 

 

 





