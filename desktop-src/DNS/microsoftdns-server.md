---
title: MicrosoftDNS_Server classe
description: La classe Server MicrosoftDNS \_ descrive un server DNS. Ogni istanza di questa classe può essere associata a un'istanza di Cache MicrosoftDNS, a un'istanza di MicrosoftDNS RootHints e a più istanze di \_ \_ MicrosoftDNS \_ Zone.
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- MicrosoftDNS_Server DNS della classe
- MicrosoftDNS_Server classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c4a42432a11b5cde0df657ba2a9725a68d76a055fce3787bce56c10dfd227ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539271"
---
# <a name="microsoftdns_server-class"></a>Classe server \_ MicrosoftDNS

La **classe \_ Server MicrosoftDNS** descrive un server DNS. Ogni istanza di questa classe può essere associata a un'istanza di [**\_ Cache MicrosoftDNS,**](microsoftdns-cache.md)a un'istanza di [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)e a più istanze di [**MicrosoftDNS \_ Zone**](microsoftdns-zone.md).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a>Members

La **classe \_ Server MicrosoftDNS** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ Server MicrosoftDNS** dispone di questi metodi.



| Metodo                   | Descrizione                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| **GetDistinguishedName** | Recupera il nome distinto DNS per la zona.<br/>                        |
| **Avvioscavenging**      | Avvia lo scavenging dei record non aggiornati nelle zone sottoposte a scavenging.<br/> |
| **Startservice**         | Avvia il server DNS.<br/>                                                |
| **StopService**          | Arresta il server DNS.<br/>                                                 |



 

### <a name="properties"></a>Proprietà

La **classe \_ Server MicrosoftDNS** ha queste proprietà.

<dl> <dt>

**AddressAnswerLimit**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Numero massimo di record host restituiti in risposta a una richiesta di indirizzo. I valori compresi tra 5 e 28 sono validi.

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica se il server DNS accetta richieste di aggiornamento dinamico. I valori validi sono come illustrato nella tabella seguente.



| Valore                                                                                                | Significato                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nessuna restrizione.<br/>                                                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Non consente aggiornamenti dinamici dei record SOA.<br/>                                             |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Non consente aggiornamenti dinamici dei record NS nella radice della zona.<br/>                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Non consente aggiornamenti dinamici dei record NS non nella radice della zona (delega dei record NS).<br/> |



 

Sommare questi valori per determinare il valore dell'impostazione.

</dd> <dt>

**AutoCacheUpdate**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se il server DNS tenta di aggiornare le voci della cache usando i dati dei server radice. Quando un server DNS viene avviato, è necessario un elenco di record NS e A del server radice denominati file di cache. I server DNS Microsoft dispongono di una funzionalità che consente di tentare di eseguire il write back di un nuovo file di cache in base alle risposte dei server radice.

</dd> <dt>

**AutoConfigFileZones**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica quali zone primarie standard autorevoli per il nome del server DNS devono essere aggiornate quando il server dei nomi cambia. I valori validi sono i seguenti:



| Valore                                                                                                | Significato                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nessuno.<br/>                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Solo i server che consentono gli aggiornamenti dinamici.<br/>        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Solo i server che non consentono gli aggiornamenti dinamici.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Tutti i server.<br/>                                    |



 

Il valore predefinito è 1.

**Windows Server 2003: **

Il numero 3 rappresenta Tutti i server.

</dd> <dt>

**BindSecondaries**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Determina il formato del messaggio AXFR durante l'invio a database secondari del server DNS non Microsoft. Se impostato su TRUE, il server DNS invia i trasferimenti ai database secondari del server DNS non Microsoft nel formato non compresso. Se FALSE, tutti i trasferimenti vengono inviati nel formato rapido.

</dd> <dt>

**BootMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Metodo di inizializzazione per il server DNS. Nella tabella che segue sono riportati i valori validi.



| Valore                                                                                                | Significato                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Inizializzato.<br/>                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Avviare dal file.<br/>                   |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Avvio dal Registro di sistema.<br/>               |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Avviare dalla directory e dal Registro di sistema.<br/> |



 

</dd> <dt>

**DefaultAgingState**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Valore **scavengingInterval** predefinito impostato per tutte le zone integrate in Active Directory create in questo server DNS. Il valore predefinito è zero, a indicare che lo scavenging è disabilitato.

</dd> <dt>

**DefaultNoRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Intervallo di nessun aggiornamento, in ore, impostato per tutte le zone integrate in Active Directory create in questo server DNS. Il valore predefinito è 168 ore (sette giorni).

</dd> <dt>

**DefaultRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Intervallo di aggiornamento, in ore, impostato per tutte le zone integrate in Active Directory create in questo server DNS. Il valore predefinito è 168 ore (sette giorni).

</dd> <dt>

**DisableAutoReverseZones**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se il server DNS crea automaticamente zone di ricerca inversa standard.

</dd> <dt>

**DisjointNets**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se è possibile eseguire l'override dell'associazione di porta predefinita per un socket usato per inviare query ai server DNS remoti.

</dd> <dt>

**DsAvailable**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se è disponibile un DS nel server DNS.

</dd> <dt>

**DsPollingInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Intervallo, in secondi, per eseguire il polling delle zone integrate in DS.

</dd> <dt>

**DsTombstoneInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Durata dei record contrassegnati per la rimozione definitiva nelle zone integrate del servizio directory, espressa in secondi.

</dd> <dt>

**EDnsCacheTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Durata, in secondi, delle informazioni memorizzate nella cache che descrivono la versione EDNS supportata da altri server DNS.

</dd> <dt>

**EnableDirectoryPartitions**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica se il supporto per le partizioni di directory applicative è abilitato nel server DNS.

**Windows Server 2003: **

Questo metodo è denominato EnableDirectoryPartitionSupport.

</dd> <dt>

**EnableDnsSec**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica se il server DNS include RR, KEY, SIG e NXT specifici di DNSSEC in una risposta, in base alla tabella seguente:



| Valore                                                                                                | Significato                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nessun record DNSSEC viene incluso nella risposta, a meno che la query non ha richiesto un set di record di risorse del tipo di record DNSSEC.<br/>          |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | I record DNSSEC sono inclusi nella risposta in base a RFC 2535.<br/>                                                                  |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | I record DNSSEC vengono inclusi in una risposta solo se la query client originale conteneva il record di risorse OPT in base a RFC 2671<br/> |



 

Se una query richiede un set di record di risorse di tipo DNSSEC, il server DNS risponde sempre con tali record, se disponibile.

</dd> <dt>

**EnableEDnsProbes**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica il comportamento del server DNS. Se TRUE, il server DNS risponde sempre con i record di risorse OPT in base a RFC 2671, a meno che il server remoto non abbia indicato che non supporta EDNS in uno scambio precedente. Se FALSE, il server DNS risponde alle query con opt solo se i opt vengono inviati nella query originale.

</dd> <dt>

**EventLogLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica gli eventi dei record del server DNS nel Visualizzatore eventi di sistema. Vengono usati i valori seguenti.



| Valore                                                                                                | Significato                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nessuno.<br/>                         |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Registrare solo gli errori.<br/>              |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Registrare solo avvisi ed errori.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Registrare tutti gli eventi.<br/>               |



 

</dd> <dt>

**ForwardDelegations**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica se le query alle zone secondarie delegate vengono inoltrate.

</dd> <dt>

**Server d'inoltro**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Enumera l'elenco di indirizzi IP dei server d'inoltro a cui il server DNS inoltra le query.

</dd> <dt>

**ForwardingTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Tempo, in secondi, un server DNS che inoltra una query attenderà la risoluzione dal [*server d'inoltro*](f-gly.md) prima di tentare di risolvere la query stessa.

Questo valore non ha significato se il server di inoltro non è impostato per l'uso della ricorsione. Per determinare questo problema, controllare la proprietà booleana IsSlave.

</dd> <dt>

**IsSlave**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

**TRUE** se il server DNS non usa la ricorsione quando la risoluzione dei nomi tramite server d'inoltro ha esito negativo.

</dd> <dt>

**ListenAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Enumera l'elenco di indirizzi IP in cui il server DNS può ricevere query.

</dd> <dt>

**LocalNetPriority**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se il server DNS assegna la priorità all'indirizzo net locale quando restituiscono record A.

</dd> <dt>

**LogFileMaxSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Dimensioni del log di debug del server DNS, in byte.

</dd> <dt>

**LogFilePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome file e percorso del log di debug del server DNS. Il valore predefinito è %system32% \\ \\ dns dns.log. I percorsi relativi sono relativi a %Systemroot% \\ System32. È possibile usare percorsi assoluti, ma i percorsi UNC non sono supportati.

</dd> <dt>

**LogIPFilterList**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Elenco di indirizzi IP usati per filtrare gli eventi DNS scritti nel log di debug.

</dd> <dt>

**LogLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica i criteri attivati nel registro Visualizzatore eventi sistema.

Deve essere impostato su valori specifici in base all'algoritmo seguente: a ogni criterio (da attivare nel registro Visualizzatore eventi di sistema) viene assegnato un valore specifico.



| Valore                                                                                                                  | Significato                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>                   | Query.<br/>                                   |
| <span id="16"></span><dl> <dt>**16**</dt> </dl>                 | Notificare.<br/>                                  |
| <span id="32"></span><dl> <dt>**32**</dt> </dl>                 | Aggiornamento.<br/>                                  |
| <span id="254"></span><dl> <dt>**254**</dt> </dl>               | Transazioni nonquery.<br/>                   |
| <span id="256"></span><dl> <dt>**256**</dt> </dl>               | Domande.<br/>                               |
| <span id="512"></span><dl> <dt>**512**</dt> </dl>               | Risposte.<br/>                                 |
| <span id="4096"></span><dl> <dt>**4096**</dt> </dl>             | Trasmissione.<br/>                                    |
| <span id="8192"></span><dl> <dt>**8192**</dt> </dl>             | Ricezione.<br/>                                 |
| <span id="16384"></span><dl> <dt>**16384**</dt> </dl>           | Udp.<br/>                                     |
| <span id="32768"></span><dl> <dt>**32768**</dt> </dl>           | TCP.<br/>                                     |
| <span id="65535"></span><dl> <dt>**65535**</dt> </dl>           | Tutti i pacchetti.<br/>                             |
| <span id="65536"></span><dl> <dt>**65536**</dt> </dl>           | Transazione di scrittura del servizio directory NT.<br/>  |
| <span id="131072"></span><dl> <dt>**131072**</dt> </dl>         | Transazione di aggiornamento del servizio directory NT.<br/> |
| <span id="16777216"></span><dl> <dt>**16777216**</dt> </dl>     | Pacchetti completi.<br/>                            |
| <span id="2147483648"></span><dl> <dt>**2147483648**</dt> </dl> | Write-through.<br/>                           |



 

La somma dei valori corrispondenti a tutti i criteri da attivare è indicata in questa proprietà.

</dd> <dt>

**LooseWildcarding**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se il server DNS esegue caratteri jolly loose. Se non definito o zero, il server segue il comportamento dei caratteri jolly specificato nella RFC DNS. In questo caso, è consigliabile che un amministratore includa record MX per tutti gli host che non sono in grado di ricevere messaggi di posta elettronica. Se diverso da zero, il server cerca il nodo con caratteri jolly più vicino; In questo caso, un amministratore deve inserire i record MX nella radice della zona e in un nodo con caratteri jolly (' ') direttamente \* sotto la radice della zona. Inoltre, gli amministratori devono inserire record MX autoreferenziati sugli host che ricevono i propri messaggi di posta elettronica.

</dd> <dt>

**MaxCacheTTL**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Tempo massimo, in secondi, in cui il record di una query di nome ricorsiva può rimanere nella cache del server DNS. Il server DNS elimina i record dalla cache alla scadenza del valore di questa voce, anche se il valore del campo TTL nel record è maggiore.

Il valore predefinito di questa proprietà è 86.400 secondi (1 giorno).

</dd> <dt>

**MaxNegativeCacheTTL**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Tempo massimo, in secondi, in cui un errore di nome generato da una query ricorsiva può rimanere nella cache del server DNS. IL DNS elimina i record dalla cache alla scadenza del timer, anche se il campo TTL è maggiore. Il valore predefinito è 86.400 (un giorno).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome di dominio completo (FQDN) o indirizzo IP del server DNS.

</dd> <dt>

**NameCheckFlag**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica il set di caratteri idonei da usare nei nomi DNS. Vengono utilizzati i valori seguenti.



| Valore                                                                                                | Significato                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | RFC strict (ANSI)<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Non RFC (ANSI)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Multibyte (UTF8)<br/>  |



 

**Windows Server 2003: **

Il valore "2" indica "Qualsiasi".

</dd> <dt>

**NoRecursion**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se il server DNS esegue la ricerca ricorsiva. TRUE indica che le operazioni di ricerca ricorsive non vengono eseguite.

</dd> <dt>

**RecursionRetry**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Secondi trascorsi prima di riprovare a eseguire una ricerca ricorsiva. Se la proprietà non è definita o è zero, vengono esecuti tentativi dopo tre secondi. Gli utenti sono sconsigliati di modificare questa proprietà. Esistono alcune situazioni in cui la proprietà deve essere modificata. ad esempio quando il server DNS contatta i server remoti tramite un collegamento lento e il server DNS riprova prima di ricevere una risposta dal DNS remoto. In questo caso, aumentare il timeout in modo che sia leggermente più lungo del tempo di risposta osservato dal DNS remoto sarebbe ragionevole.

</dd> <dt>

**RecursionTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Secondi trascorsi prima che il server DNS ceda la query ricorsiva. Se la proprietà non è definita o è zero, il server DNS si disdeziona dopo 15 secondi. In generale, il timeout di 15 secondi è sufficiente per consentire a qualsiasi risposta in sospeso di tornare al server DNS.

Gli utenti sono sconsigliati di modificare questa proprietà. Uno scenario in cui la proprietà deve essere modificata è quando il server DNS contatta i server remoti tramite un collegamento lento e si osserva che il server DNS rifiuta le query (con ERRORE DEL SERVER) prima della ricezione delle \_ risposte.

Anche i resolver client ritentano le query, pertanto è necessaria un'attenta analisi per determinare se le risposte remote sono effettivamente associate alla query che ha timeout. In questo caso, aumentare il valore di timeout in modo che sia leggermente più lungo del tempo di risposta osservato dal DNS remoto sarebbe ragionevole.

</dd> <dt>

**Roundrobin**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se il server DNS round robin ha più record A.

</dd> <dt>

**Rpcprotocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Protocollo RPC o protocolli su cui viene eseguito rpc amministrativo. L'algoritmo seguente viene usato per assegnare un valore specifico:



| Valore                                                                                                | Significato                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nessuno<br/>        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | TCP<br/>         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Named Pipe<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Lpc<br/>         |



 

La somma dei valori indica i protocolli usati.

</dd> <dt>

**ScavengingInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Intervallo, in ore, tra due operazioni di scavenging consecutive eseguite dal server DNS. Zero indica che lo scavenging è disabilitato. Il valore predefinito è 168 ore (sette giorni).

</dd> <dt>

**Risposte protette**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se il server DNS salva in modo esclusivo i record di nomi nello stesso sottoalbero del server che li ha forniti.

</dd> <dt>

**SendPort**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Porta su cui il server DNS invia query UDP ad altri server. Per impostazione predefinita, il server DNS invia query su un socket associato alla porta DNS.

In determinate situazioni, questa non è la configurazione migliore. Un caso ovvio è quando un amministratore blocca la porta DNS con un firewall per impedire l'accesso esterno al server DNS, ma vuole comunque che il server sia in grado di contattare i server DNS Internet per fornire la risoluzione dei nomi per i client interni. Un altro caso è quando il server DNS supporta le reti non contigue (la proprietà **DisjointNets** impostata su TRUE identifica questo scenario). In questi casi, l'impostazione della proprietà **SendOnNonDnsPort** su un valore diverso da zero indica al server DNS di eseguire il binding a una porta arbitraria per l'invio ai server DNS remoti.

Se il **valore di SendOnNonDnsPort** è maggiore di 1024, il server DNS esegue l'associazione in modo esplicito al valore di porta specificato. Questa opzione di configurazione è utile quando un amministratore deve correggere la porta di query DNS ai fini del firewall.

**Windows Server 2003: **

Se si imposta la proprietà SendPort su un valore diverso da zero, il server DNS viene associato a una porta arbitraria per l'invio a server DNS remoti.

</dd> <dt>

**ServerAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Enumera l'elenco di indirizzi IP per il server DNS.

</dd> <dt>

**StrictFileParsing**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se il server DNS analizza rigorosamente [*i file*](z-gly.md) di zona. Se non è definito o zero, il server registra e ignora i dati non validi nel file di zona e continua a caricarsi. Se diverso da zero, il server registra e non riesce in caso di errori del file di zona.

</dd> <dt>

**Updateoptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Limita il tipo di record che possono essere aggiornati dinamicamente nel server, utilizzati in aggiunta alle impostazioni **AllowUpdate** negli oggetti Server e Zone.

**Windows Server 2003: **

0: nessuna restrizione.

1: non consentire gli aggiornamenti dinamici dei record SOA.

2: non consentire gli aggiornamenti dinamici dei record NS nella radice della zona.

4: non consentire gli aggiornamenti dinamici dei record NS non nella radice della zona (record NS di delega).

Sommare questi valori per determinare il valore dell'impostazione.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del server DNS.

</dd> <dt>

**Writeauthorityns**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica se il server DNS scrive i record NS e SOA nella sezione dell'autorità al completamento della risposta.

</dd> <dt>

**XfrConnectTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Tempo, in secondi, in cui il server DNS attende una connessione TCP riuscita a un server remoto durante il tentativo di trasferimento di una zona.

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

[**Metodo StartService della classe server \_ MicrosoftDNS**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Metodo StopService della classe server \_ MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Metodo StartScavenging della classe server \_ MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Metodo GetDistinguishedName della classe server \_ MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





