---
title: Costanti DNS
description: Le costanti seguenti sono definite per DNS nell'ordine dei byte dell'host.
ms.assetid: 95bc9193-7962-498a-9abd-c4718ac35f0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64497e14d6c4ae11f4a6ed68200614aa4f602270
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046364"
---
# <a name="dns-constants"></a>Costanti DNS

Le costanti seguenti sono definite per DNS nell'ordine dei byte dell'host.

## <a name="dns-record-types"></a>Tipi di record DNS



| Costante           | Valore            |
|--------------------|------------------|
| \_tipo DNS \_ A       | 0x0001           |
| \_NS di tipo DNS \_      | 0x0002           |
| \_MD di tipo DNS \_      | 0x0003           |
| \_tipo DNS \_ MF      | 0x0004           |
| \_tipo DNS \_ CNAME   | 0x0005           |
| tipo di DNS \_ \_ SOA     | 0x0006           |
| tipo di DNS \_ \_ MB      | 0x0007           |
| tipo di DNS \_ \_ mg      | 0x0008           |
| \_tipo DNS \_ Mr      | 0x0009           |
| \_tipo DNS \_ null    | 0x000a           |
| tipo di DNS \_ \_ wks     | 0x000b           |
| \_tipo DNS \_ ptr     | 0x000c           |
| \_HINFO di tipo DNS \_   | 0x000d           |
| \_mInfo di tipo DNS \_   | 0x000e           |
| \_tipo DNS \_ MX      | 0x000F           |
| \_testo del tipo DNS \_    | 0x0010           |
| tipo di DNS \_ \_ RP      | 0x0011           |
| \_AFSDB di tipo DNS \_   | 0x0012           |
| \_X25 di tipo DNS \_     | 0x0013           |
| tipo di DNS \_ \_ ISDN    | 0x0014           |
| tipo di DNS \_ \_ RT      | 0x0015           |
| \_NSAP di tipo DNS \_    | 0x0016           |
| \_NSAPPTR di tipo DNS \_ | 0x0017           |
| tipo di DNS \_ \_ sig     | 0x0018           |
| \_chiave di tipo DNS \_     | 0x0019           |
| \_tipo DNS \_ px      | 0x001a           |
| \_oggetti Criteri di gruppo di tipo DNS \_    | 0x001b           |
| tipo di DNS \_ \_ aaaa    | 0x001c           |
| \_loc di tipo DNS \_     | 0x001d           |
| tipo di DNS \_ \_ NXT     | 0x001e           |
| tipo di DNS \_ \_ Eid     | 0x001F           |
| \_NIMLOC di tipo DNS \_  | 0x0020           |
| \_SRV di tipo DNS \_     | 0x0021           |
| \_tipo DNS \_ Atma    | 0x0022           |
| \_NAPTR di tipo DNS \_   | 0x0023           |
| tipo di DNS \_ \_ Kx      | 0x0024           |
| \_certificato di tipo DNS \_    | 0x0025           |
| \_Tipo DNS \_ a6      | 0x0026           |
| \_DNAME di tipo DNS \_   | 0x0027           |
| \_sink di tipo DNS \_    | 0x0028           |
| tipo di DNS \_ \_ opz     | 0x0029           |
| \_DS di tipo DNS \_      | 0x002B           |
| \_RRSIG di tipo DNS \_   | 0x002E           |
| \_nsec di tipo DNS \_    | 0x002F           |
| \_DNSKEY di tipo DNS \_  | 0x0030           |
| \_DHCID di tipo DNS \_   | 0x0031           |
| \_UINFO di tipo DNS \_   | 0x0064           |
| \_UID del tipo DNS \_     | 0x0065           |
| \_GID di tipo DNS \_     | 0x0066           |
| UNSPEC del \_ tipo DNS \_  | 0x0067           |
| \_indirizzi di tipo DNS \_   | 0x00f8           |
| \_tipo DNS \_ TKey    | 0x00f9           |
| \_TSIG di tipo DNS \_    | 0x00fa           |
| \_IXFR di tipo DNS \_    | 0x00fb           |
| \_AXFR di tipo DNS \_    | 0x00fc           |
| \_MAILB di tipo DNS \_   | 0x00fd           |
| \_tipo DNS \_ maila   | 0x00fe           |
| \_tipo DNS \_ All     | 0x00ff           |
| \_tipo DNS \_ any     | 0x00ff           |
| \_WINS del tipo DNS \_    | 0xff01           |
| \_WINSR del tipo DNS \_   | 0xff02           |
| \_NBSTAT di tipo DNS \_  | \_WINSR del tipo DNS \_ |



 

## <a name="dns-class-types"></a>Tipi di classe DNS



| Costante             | Valore  |
|----------------------|--------|
| \_classe DNS \_ Internet | 0x0001 |
| \_classe DNS \_ CSNET    | 0x0002 |
| \_classe DNS \_ Chaos    | 0x0003 |
| \_classe DNS \_ Esiodo   | 0x0004 |
| \_classe DNS \_ None     | 0x00fe |
| \_classe DNS \_ All      | 0x00ff |
| \_classe DNS \_ any      | 0x00ff |



 

## <a name="dns-query-types"></a>Tipi di query DNS



| Costante                    | Valore  |
|-----------------------------|--------|
| \_query OPCODE \_ DNS          | 0x0000 |
| OPCODE di DNS \_ \_         | 0x0001 |
| \_stato del \_ server \_ OPCODE DNS | 0x0002 |
| \_codice operativo DNS \_ sconosciuto        | 0x0003 |
| \_notifica OPCODE \_ DNS         | 0x0004 |
| \_aggiornamento OPCODE \_ DNS         | 0x0005 |



 

## <a name="dns-record-flags"></a>Flag di record DNS

I flag seguenti fanno riferimento a una sezione di record di risorse (RR) in un messaggio DNS:



| Costante           | Valore      | Significato                         |
|--------------------|------------|---------------------------------|
| \_domanda DNSREC   | 0x00000000 | RR si trova nella sezione Question   |
| \_risposta DNSREC     | 0x00000001 | Il record RR si trova nella sezione risposta     |
| \_autorità DNSREC  | 0x00000002 | RR si trova nella sezione Authority  |
| DNSREC \_ aggiuntive | 0x00000003 | RR si trova nella sezione aggiuntiva |



 

I flag seguenti si riferiscono alla sezione di un RR in un messaggio DNS di aggiornamento per [RFC 2136](https://www.ietf.org/rfc/rfc2136.txt):



| Costante       | Valore      | Significato                           |
|----------------|------------|-----------------------------------|
| \_zona DNSREC   | 0x00000000 | Il record RR si trova nella sezione zone         |
| \_PREREQ DNSREC | 0x00000001 | Il record RR si trova nella sezione dei prerequisiti |
| aggiornamento di DNSREC \_ | 0x00000002 | Il record RR si trova nella sezione Update       |



 

I flag seguenti si escludono a vicenda:



| Costante        | Valore      | Significato                                                    |
|-----------------|------------|------------------------------------------------------------|
| eliminazione di DNSREC \_  | 0x00000004 | Eliminare un record RR. Usato in combinazione con l' \_ aggiornamento di DNSREC       |
| DNSREC \_ NOexist | 0x00000004 | Il record RR non esiste. Usato insieme a DNSREC \_ PREREQ |



 

## <a name="dns-query-options"></a>Opzioni query DNS



| Costante                                | Valore      | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_standard di query DNS \_                    | 0x00000000 | Query standard.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_risposta di \_ Accept \_ troncata della query \_ DNS | 0x00000001 | Restituisce i risultati troncati. Non esegue un nuovo tentativo in TCP.                                                                                                                                                                                                                                                                                                                                                                                                   |
| \_query DNS \_ utilizza \_ \_ solo TCP              | 0x00000002 | USA solo TCP per la query.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_query DNS \_ senza \_ ricorsione               | 0x00000004 | Indica al server DNS di eseguire una query iterativa, indicando in particolare al server DNS di non eseguire la risoluzione ricorsiva per risolvere la query.                                                                                                                                                                                                                                                                                                   |
| \_cache di \_ bypass \_ della query DNS               | 0x00000008 | Ignora la cache del [*resolver*](r-gly.md) nella ricerca.                                                                                                                                                                                                                                                                                                                                                                            |
| query \_ DNS \_ senza \_ \_ query Wire             | 0x00000010 | Indica a DNS di eseguire una query solo nella cache locale. **Windows 2000 Server e windows 2000 Professional:** Questo valore non è supportato. Per una funzionalità simile, **usare \_ \_ \_ solo la cache delle query DNS**.<br/>                                                                                                                                                                                                                                      |
| \_query DNS \_ senza \_ \_ nome locale             | 0x00000020 | Indica a DNS di ignorare il nome locale. **Windows 2000 Server e windows 2000 Professional:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                                    |
| \_query DNS \_ senza \_ \_ file host             | 0x00000040 | Impedisce alla query DNS di consultare il file degli host. **Windows 2000 Server e windows 2000 Professional:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                   |
| \_query DNS \_ senza \_ NetBT                   | 0x00000080 | Impedisce che la query DNS utilizzi NetBT per la risoluzione. **Windows 2000 Server e windows 2000 Professional:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                  |
| \_ \_ solo Wire query \_ DNS                  | 0x00000100 | Indica a DNS di eseguire una query usando solo la rete, ignorando le informazioni locali. **Windows 2000 Server e windows 2000 Professional:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                      |
| \_messaggio di query DNS \_ restituito \_             | 0x00000200 | Indica a DNS di restituire l'intero messaggio di risposta DNS. **Windows 2000 Server e windows 2000 Professional:** Questo valore non è supportato.<br/>                                                                                                                                                                                                                                                                                                   |
| \_ \_ solo multicast query \_ DNS             | 0x00000400 | Impedisce alla query di usare DNS e usa solo la risoluzione dei nomi multicast del collegamento locale (LLMNR). **Windows Vista e Windows Server 2008 o versioni successive:** Questo valore è supportato.<br/>                                                                                                                                                                                                                                                                  |
| \_query DNS \_ senza \_ multicast               | 0x00000800 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_la query DNS \_ considera \_ come \_ FQDN             | 0x00001000 | Impedisce che la risposta DNS alleghi i suffissi al nome inviato in un processo di risoluzione dei nomi.                                                                                                                                                                                                                                                                                                                                                  |
| \_ADDRCONFIG di query DNS \_                  | 0x00002000 | Solo Windows 7: non inviare query [**di**](/windows/win32/api/windns/ns-windns-dns_a_data) tipo se gli indirizzi IPv4 non sono disponibili in un'interfaccia e non inviano query di tipo [**aaaa**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) se gli indirizzi IPv6 non sono disponibili.                                                                                                                                                                                                                                   |
| \_query DNS \_ Dual \_ addr                  | 0x00004000 | Solo Windows 7: eseguire query sia su [**aaaa**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) che su record [**di tipo e**](/windows/win32/api/windns/ns-windns-dns_a_data) restituire i risultati per ogni. I risultati **per i record di tipo** vengono mappati nel tipo **aaaa** .                                                                                                                                                                                                                                                           |
| \_ \_ attesa multicast query \_ DNS             | 0x00020000 | Attende un timeout completo per raccogliere tutte le risposte dal collegamento locale. Se non è impostato, il comportamento predefinito prevede la restituzione con la prima risposta. **Windows Vista e Windows Server 2008 o versioni successive:** Questo valore è supportato.<br/>                                                                                                                                                                                                              |
| \_ \_ Verifica multicast query \_ DNS           | 0x00040000 | Indirizza un test usando il nome host del computer locale per verificare l'univocità del nome nello stesso collegamento locale. Raccoglie tutte le risposte anche se il normale comportamento del mittente LLMNR non è abilitato. **Windows Vista e Windows Server 2008 o versioni successive:** Questo valore è supportato.<br/>                                                                                                                                                                                  |
| la \_ query DNS non \_ \_ Reimposta \_ \_ i valori TTL    | 0x00100000 | Se impostato, e se la risposta contiene più record, i record vengono archiviati con la durata (TTL) corrispondente al valore minimo TTL compreso tra tutti i record. Quando questa opzione è impostata, "non modificare la durata (TTL) dei singoli record" nel set di record restituito non viene modificato.                                                                                                                                                                               |
| \_query DNS \_ disabilitare \_ la \_ codifica IDN      | 0x00200000 | Disabilita il supporto della codifica IDN (International Domain Name) nelle API [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a), [**DnsQueryEx**](/windows/desktop/api/Windns/nf-windns-dnsqueryex), [**DnsModifyRecordsInSet**](/windows/desktop/api/Windns/nf-windns-dnsmodifyrecordsinset_a)e [**DnsReplaceRecordSet**](/windows/desktop/api/Windns/nf-windns-dnsreplacerecordseta) . Tutti i nomi di Punycode vengono considerati ASCII e saranno codificati ASCII in transito. Tutti i nomi non ASCII sono codificati in UTF8 sulla rete. **Windows 8 o versioni successive:** Questo valore è supportato.<br/> |
| Aggiunta di un'etichetta a una \_ query DNS \_ \_          | 0x00800000 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_query DNS \_ riservata                    | 0xF0000000 | Riservato.                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="dns-update-options"></a>Opzioni di aggiornamento DNS



| Costante                                 | Valore      | Significato                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ impostazione predefinita utilizzo sicurezza aggiornamenti DNS \_      | 0x00000000 | Usa il comportamento predefinito, specificato nel registro di sistema, per gli aggiornamenti dinamici del DNS sicuro.                                                                |
| \_protezione aggiornamento \_ DNS \_ disattivato               | 0x00000010 | Non tenta di eseguire aggiornamenti dinamici protetti.                                                                                                                      |
| \_sicurezza degli aggiornamenti DNS \_ \_ in                | 0x00000020 | Tenta l'aggiornamento dinamico non protetto. Se rifiutato, tenta l'aggiornamento dinamico protetto.                                                                               |
| \_ \_ solo sicurezza aggiornamenti \_ DNS              | 0x00000100 | Tenta solo aggiornamenti dinamici protetti.                                                                                                                         |
| \_contesto di \_ sicurezza della cache degli aggiornamenti \_ DNS \_    | 0x00000200 | Memorizza nella cache il contesto di sicurezza da utilizzare nelle transazioni future.                                                                                                   |
| il \_ test di aggiornamento DNS \_ \_ Usa \_ \_ sys \_ Acct locale | 0x00000400 | Usa le credenziali dell'account del computer locale.                                                                                                               |
| \_ \_ \_ nego sicurezza di aggiornamento \_ DNS       | 0x00000800 | Non usa il contesto di sicurezza memorizzato nella cache.                                                                                                                         |
| \_aggiornamento DNS \_ provare \_ tutti \_ i \_ server master   | 0x00001000 | Invia gli aggiornamenti DNS a tutti i server DNS multimaster.                                                                                                            |
| \_aggiornamento DNS \_ ignorare \_ nessun \_ adapter di aggiornamento \_  | 0x00002000 | Non aggiornare gli adapter in cui gli aggiornamenti DNS dinamici sono disabilitati. **Windows 2000 Server con SP2 o versione successiva:** Questo valore è supportato.<br/>                 |
| \_ \_ server remoto aggiornamento \_ DNS              | 0x00004000 | Registrare i record CNAME in un server remoto oltre al server DNS locale. **Windows 2000 Server con SP2 o versione successiva:** Questo valore è supportato.<br/> |
| \_aggiornamento DNS \_ riservato                    | 0xffff0000 | Riservato per utilizzi futuri.                                                                                                                                      |



 

## <a name="dns-response-codes"></a>Codici di risposta DNS



| Errore                | Significato                                        |
|----------------------|------------------------------------------------|
| DNS \_ RCODE \_ NOERROR  | Nessun errore                                       |
| DNS \_ RCODE \_ precedente  | Errore di formato                                   |
| DNS \_ RCODE \_ SERVFAIL | Errore del server                                 |
| DNS \_ RCODE \_ NXDOMAIN | Errore nome                                     |
| DNS \_ RCODE \_ NOTIMPL  | Non implementato                                |
| DNS \_ RCODE \_ rifiutato  | Connection refused                             |
| DNS \_ RCODE \_ YXDOMAIN | Il nome di dominio non deve esistere                   |
| DNS \_ RCODE \_ YXRRSET  | Il set di record di risorse (RR) non deve esistere      |
| DNS \_ RCODE \_ NXRRSET  | Il set RR non esiste                          |
| DNS \_ RCODE \_ NOTAUTH  | Non autorevole per la zona                     |
| DNS \_ RCODE \_ NOTZONE  | Nome non nell'area                               |
| DNS \_ RCODE \_ BADVERS  | Meccanismo di estensione non valido per la versione DNS (EDNS) |
| DNS \_ RCODE \_ BADSIG   | Firma non valida                                  |
| DNS \_ RCODE \_ BADKEY   | Chiave non valida                                        |
| DNS \_ RCODE \_ BADTIME  | Timestamp non valido                                  |



 

 

 





