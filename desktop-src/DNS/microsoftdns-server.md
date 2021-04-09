---
title: Classe MicrosoftDNS_Server
description: La \_ classe server MicrosoftDNS descrive un server DNS. Ogni istanza di questa classe può essere associata a un'istanza della \_ cache MicrosoftDNS, a un'istanza di MicrosoftDNS \_ RootHints e a più istanze di MicrosoftDNS \_ zone.
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- DNS della classe MicrosoftDNS_Server
- MicrosoftDNS_Server della classe DNS, descritta
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
ms.openlocfilehash: 854a90f5b0fa4d331bd0478d104e50dd70b0cd65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963829"
---
# <a name="microsoftdns_server-class"></a>\_Classe server MicrosoftDNS

La **classe \_ Server MicrosoftDNS** descrive un server DNS. Ogni istanza di questa classe può essere associata a un'istanza della [**\_ cache MicrosoftDNS**](microsoftdns-cache.md), a un'istanza di [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)e a più istanze di [**MicrosoftDNS \_ zone**](microsoftdns-zone.md).

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

La **classe \_ Server MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ Server MicrosoftDNS** dispone di questi metodi.



| Metodo                   | Descrizione                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| **Getdistinguishname** | Recupera il nome distinto DNS per la zona.<br/>                        |
| **StartScavenging**      | Avvia lo scavenging dei record non aggiornati nelle zone soggette allo scavenging.<br/> |
| **StartService**         | Avvia il server DNS.<br/>                                                |
| **StopService**          | Arresta il server DNS.<br/>                                                 |



 

### <a name="properties"></a>Proprietà

La **classe \_ Server MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**AddressAnswerLimit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Numero massimo di record host restituiti in risposta a una richiesta di indirizzo. I valori compresi tra 5 e 28 sono validi.

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se il server DNS accetta richieste di aggiornamento dinamico. I valori validi sono riportati nella tabella seguente.



| Valore                                                                                                | Significato                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nessuna restrizione.<br/>                                                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Non consente aggiornamenti dinamici dei record SOA.<br/>                                             |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Non consente aggiornamenti dinamici di record NS nella radice della zona.<br/>                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Non consente aggiornamenti dinamici di record NS non nella radice della zona (record NS di delega).<br/> |



 

Sommare questi valori per determinare il valore dell'impostazione.

</dd> <dt>

**AutoCacheUpdate**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il server DNS tenta di aggiornare le voci della cache utilizzando i dati dei server radice. All'avvio di un server DNS, è necessario un elenco di NS "hint" del server radice e di record A per i server che storicamente chiamano il file di cache. I server DNS Microsoft dispongono di una funzionalità che consente di provare a eseguire il writeback di un nuovo file di cache in base alle risposte dei server radice.

</dd> <dt>

**AutoConfigFileZones**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica quali zone primarie standard autorevoli per il nome del server DNS devono essere aggiornate quando il server dei nomi viene modificato. I valori validi sono i seguenti:



| Valore                                                                                                | Significato                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nessuna.<br/>                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Solo i server che consentono aggiornamenti dinamici.<br/>        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Solo i server che non consentono aggiornamenti dinamici.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Tutti i server.<br/>                                    |



 

Il valore predefinito è 1.

* * Windows Server 2003: * *

Il numero 3 rappresenta tutti i server.

</dd> <dt>

**BindSecondaries**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Determina il formato del messaggio AXFR durante l'invio a database secondari del server DNS non Microsoft. Se impostato su TRUE, il server DNS invia i trasferimenti a database secondari del server DNS non Microsoft nel formato non compresso. Se FALSE, tutti i trasferimenti vengono inviati nel formato Fast.

</dd> <dt>

**Metodo avvio**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Metodo di inizializzazione per il server DNS. Nella tabella che segue sono riportati i valori validi.



| Valore                                                                                                | Significato                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Non inizializzato.<br/>                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Avvio dal file.<br/>                   |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Avvio dal registro di sistema.<br/>               |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Avvio da directory e registro di sistema.<br/> |



 

</dd> <dt>

**DefaultAgingState**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Valore predefinito di **ScavengingInterval** impostato per tutte le zone integrate Active Directory create in questo server DNS. Il valore predefinito è zero, che indica che lo scavenging è disabilitato.

</dd> <dt>

**DefaultNoRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Nessun intervallo di aggiornamento, in ore, impostato per tutte le zone integrate Active Directory create in questo server DNS. Il valore predefinito è 168 ore (sette giorni).

</dd> <dt>

**DefaultRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Intervallo di aggiornamento, in ore, impostato per tutte le zone integrate Active Directory create in questo server DNS. Il valore predefinito è 168 ore (sette giorni).

</dd> <dt>

**DisableAutoReverseZones**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il server DNS crea automaticamente le zone di ricerca inversa standard.

</dd> <dt>

**DisjointNets**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se è possibile eseguire l'override del binding di porta predefinito per un socket utilizzato per inviare query a server DNS remoti.

</dd> <dt>

**DsAvailable**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se esiste un DS disponibile nel server DNS.

</dd> <dt>

**DsPollingInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Intervallo, in secondi, per il polling delle zone integrate in DS.

</dd> <dt>

**DsTombstoneInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Durata dei record contrassegnati per la rimozione definitiva nelle zone integrate del servizio directory, espressa in secondi.

</dd> <dt>

**EDnsCacheTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Durata, in secondi, delle informazioni memorizzate nella cache che descrivono la versione di EDNS supportata da altri server DNS.

</dd> <dt>

**EnableDirectoryPartitions**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se il supporto per le partizioni di directory applicative è abilitato nel server DNS.

* * Windows Server 2003: * *

Questo metodo è denominato EnableDirectoryPartitionSupport.

</dd> <dt>

**EnableDnsSec**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se il server DNS include RRs, KEY, SIG e NXT specifici per DNSSEC in una risposta, nella tabella seguente:



| Valore                                                                                                | Significato                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nessun record DNSSEC viene incluso nella risposta a meno che la query non abbia richiesto un set di record di risorse del tipo di record DNSSEC.<br/>          |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | I record DNSSEC sono inclusi nella risposta in base allo standard RFC 2535.<br/>                                                                  |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | I record DNSSEC sono inclusi in una risposta solo se la query client originale conteneva il record di risorse OPT in base allo standard RFC 2671<br/> |



 

Se una query richiede un set di record di risorse del tipo DNSSEC, il server DNS risponde sempre con tali record, se disponibili.

</dd> <dt>

**EnableEDnsProbes**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica il comportamento del server DNS. Se il valore è TRUE, il server DNS risponde sempre con i record di risorse OPT in base allo standard RFC 2671, a meno che il server remoto non abbia indicato che non supporta EDNS in uno scambio precedente. Se FALSE, il server DNS risponde alle query con opz solo se le opz vengono inviate nella query originale.

</dd> <dt>

**EventLogLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica gli eventi registrati dal server DNS nel registro di sistema Visualizzatore eventi. Vengono utilizzati i valori seguenti.



| Valore                                                                                                | Significato                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nessuna.<br/>                         |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Registra solo gli errori.<br/>              |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Registra solo avvisi ed errori.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Registra tutti gli eventi.<br/>               |



 

</dd> <dt>

**ForwardDelegations**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se le query nelle sottozone delegate vengono trasmesse.

</dd> <dt>

**Server d'inoltro**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Enumera l'elenco di indirizzi IP dei server d'indirizzamento a cui il server DNS esegue l'inoltri.

</dd> <dt>

**ForwardingTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Tempo, in secondi, in cui un server DNS che invia una query attenderà la risoluzione dal server d' [*avvio prima di*](f-gly.md) tentare di risolvere la query stessa.

Questo valore non è significativo se il server di inoltri non è impostato per utilizzare la ricorsione. Per determinare questo problema, controllare la proprietà booleana slave.

</dd> <dt>

**Slave**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

**True** se il server DNS non utilizza la ricorsione quando la risoluzione dei nomi tramite i server d'avanzamento ha esito negativo.

</dd> <dt>

**ListenAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Enumera l'elenco di indirizzi IP su cui il server DNS può ricevere le query.

</dd> <dt>

**LocalNetPriority**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il server DNS assegna la priorità all'indirizzo di rete locale quando viene restituito un record.

</dd> <dt>

**LogFileMaxSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Dimensioni in byte del log di debug del server DNS.

</dd> <dt>

**LogFilePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Nome file e percorso del log di debug del server DNS. Il valore predefinito è% system32% \\ DNS \\ . log. I percorsi relativi sono relativi a% SystemRoot% \\ system32. È possibile utilizzare i percorsi assoluti, ma i percorsi UNC non sono supportati.

</dd> <dt>

**LogIPFilterList**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Elenco di indirizzi IP utilizzati per filtrare gli eventi DNS scritti nel log di debug.

</dd> <dt>

**LogLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica i criteri attivati nel registro di sistema Visualizzatore eventi.

Deve essere impostato su valori specifici in base all'algoritmo seguente: ogni criterio (da attivare nel registro di sistema Visualizzatore eventi) viene assegnato a un valore specifico.



| Valore                                                                                                                  | Significato                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>                   | Query.<br/>                                   |
| <span id="16"></span><dl> <dt>**16**</dt> </dl>                 | Comunica.<br/>                                  |
| <span id="32"></span><dl> <dt>**32**</dt> </dl>                 | Aggiornamento.<br/>                                  |
| <span id="254"></span><dl> <dt>**254**</dt> </dl>               | Transazioni non query.<br/>                   |
| <span id="256"></span><dl> <dt>**256**</dt> </dl>               | Domande.<br/>                               |
| <span id="512"></span><dl> <dt>**512**</dt> </dl>               | Risposte.<br/>                                 |
| <span id="4096"></span><dl> <dt>**4096**</dt> </dl>             | Trasmissione.<br/>                                    |
| <span id="8192"></span><dl> <dt>**8192**</dt> </dl>             | Ricezione.<br/>                                 |
| <span id="16384"></span><dl> <dt>**16384**</dt> </dl>           | UDP.<br/>                                     |
| <span id="32768"></span><dl> <dt>**32768**</dt> </dl>           | TCP.<br/>                                     |
| <span id="65535"></span><dl> <dt>**65535**</dt> </dl>           | Tutti i pacchetti.<br/>                             |
| <span id="65536"></span><dl> <dt>**65536**</dt> </dl>           | Transazione di scrittura del servizio directory NT.<br/>  |
| <span id="131072"></span><dl> <dt>**131072**</dt> </dl>         | Transazione di aggiornamento del servizio directory NT.<br/> |
| <span id="16777216"></span><dl> <dt>**16777216**</dt> </dl>     | Pacchetti completi.<br/>                            |
| <span id="2147483648"></span><dl> <dt>**2147483648**</dt> </dl> | Scrivere.<br/>                           |



 

La somma dei valori corrispondenti a tutti i criteri da attivare è indicata in questa proprietà.

</dd> <dt>

**LooseWildcarding**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il server DNS esegue caratteri jolly separati. Se non è definito o zero, il server segue il comportamento dei caratteri jolly specificato nella RFC DNS. In questo caso, è consigliabile che un amministratore includa i record MX per tutti gli host che non sono in grado di ricevere messaggi di posta elettronica. Se è diverso da zero, il server cerca il nodo con caratteri jolly più vicino; in questo caso, un amministratore deve inserire i record MX nella radice della zona e in un nodo con caratteri jolly (' \* ') direttamente sotto la radice della zona. Inoltre, gli amministratori devono inserire record MX autoreferenziali negli host che ricevono la propria posta elettronica.

</dd> <dt>

**MaxCacheTTL**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Tempo massimo, in secondi, per cui il record di una query con nome ricorsivo può rimanere nella cache del server DNS. Il server DNS elimina i record dalla cache quando il valore di questa voce scade, anche se il valore del campo TTL nel record è maggiore.

Il valore predefinito di questa proprietà è 86.400 secondi (1 giorno).

</dd> <dt>

**MaxNegativeCacheTTL**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Tempo massimo, in secondi, in cui un errore di nome deriva da una query ricorsiva può rimanere nella cache del server DNS. DNS elimina i record dalla cache quando questo timer scade, anche se il campo TTL è maggiore. Il valore predefinito è 86.400 (un giorno).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome di dominio completo (FQDN) o indirizzo IP del server DNS.

</dd> <dt>

**NameCheckFlag**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica il set di caratteri idonei da usare nei nomi DNS. Vengono utilizzati i valori seguenti.



| Valore                                                                                                | Significato                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | RFC rigoroso (ANSI)<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Non RFC (ANSI)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Multibyte (UTF8)<br/>  |



 

* * Windows Server 2003: * *

Il valore "2" indica "any".

</dd> <dt>

**NoRecursion**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il server DNS esegue ricerche ricorsive. TRUE indica che le ricerche ricorsive non vengono eseguite.

</dd> <dt>

**RecursionRetry**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Secondi trascorsi prima di riprovare a eseguire una ricerca ricorsiva. Se la proprietà è undefined o zero, i tentativi vengono eseguiti dopo tre secondi. Gli utenti sono sconsigliati di modificare questa proprietà. In alcune situazioni la proprietà deve essere modificata. un esempio è quando il server DNS Contatta i server remoti tramite un collegamento lento e il server DNS viene ritentato prima di ricevere la risposta dal DNS remoto. In questo caso, l'aumento del timeout per un tempo leggermente superiore rispetto al tempo di risposta osservato dal DNS remoto sarebbe ragionevole.

</dd> <dt>

**RecursionTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Secondi trascorsi i quali il server DNS assegna una query ricorsiva. Se la proprietà è indefinita o zero, il server DNS si concede dopo 15 secondi. In generale, il timeout di 15 secondi è sufficiente per consentire a qualsiasi risposta in attesa di tornare al server DNS.

Gli utenti sono sconsigliati di modificare questa proprietà. Uno scenario in cui la proprietà deve essere modificata è quando il server DNS Contatta i server remoti tramite un collegamento lento e il server DNS rileva il rifiuto delle query (con errore del SERVER \_ ) prima della ricezione delle risposte.

I resolver client ritentano anche le query, quindi è necessaria un'attenta analisi per determinare se le risposte remote sono effettivamente associate alla query che ha raggiunto il timeout. In questo caso, l'aumento del valore di timeout leggermente superiore al tempo di risposta osservato dal DNS remoto sarebbe ragionevole.

</dd> <dt>

**RoundRobin**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il server DNS round robin ha più record A.

</dd> <dt>

**RpcProtocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Protocollo o protocolli RPC su cui viene eseguita la RPC amministrativa. Per assegnare un valore specifico, viene usato l'algoritmo seguente:



| Valore                                                                                                | Significato                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | nessuno<br/>        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | TCP<br/>         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Named Pipe<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | LPC<br/>         |



 

La somma dei valori indica i protocolli utilizzati.

</dd> <dt>

**ScavengingInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Intervallo, in ore, tra due operazioni di scavenging consecutive eseguite dal server DNS. Zero indica che lo scavenging è disabilitato. Il valore predefinito è 168 ore (sette giorni).

</dd> <dt>

**SecureResponses**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il server DNS Salva esclusivamente i record di nomi nello stesso sottoalbero del server in cui sono stati forniti.

</dd> <dt>

**SendPort**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Porta su cui il server DNS invia query UDP ad altri server. Per impostazione predefinita, il server DNS invia query su un socket associato alla porta DNS.

In determinate situazioni, questa non è la configurazione migliore. Un caso ovvio è quando un amministratore blocca la porta DNS con un firewall per impedire l'accesso esterno al server DNS, ma vuole comunque che il server sia in grado di contattare i server DNS Internet per fornire la risoluzione dei nomi per i client interni. Un altro caso è quello in cui il server DNS supporta le reti non contigue (la proprietà **DisjointNets** impostata su true identifica questo scenario). In questi casi, l'impostazione della proprietà **SendOnNonDnsPort** su un valore diverso da zero indica al server DNS di eseguire l'associazione a una porta arbitraria per l'invio a server DNS remoti.

Se il valore di **SendOnNonDnsPort** è maggiore di 1024, il server DNS viene associato in modo esplicito al valore della porta specificato. Questa opzione di configurazione è utile quando un amministratore deve correggere la porta di query DNS per finalità del firewall.

* * Windows Server 2003: * *

Se si imposta la proprietà SendPort su un valore diverso da zero, il server DNS eseguirà l'associazione a una porta arbitraria per l'invio a server DNS remoti.

</dd> <dt>

**ServerAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Enumera l'elenco di indirizzi IP per il server DNS.

</dd> <dt>

**StrictFileParsing**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il server DNS analizza rigorosamente [*i file di zona*](z-gly.md) . Se non è definito o zero, il server registrerà e ignorerà i dati non validi nel file di zona e continuerà a essere caricato. Se è diverso da zero, il server registrerà e non riuscirà in caso di errori nel file di zona.

</dd> <dt>

**UpdateOptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Limita il tipo di record che possono essere aggiornati dinamicamente sul server, usati in aggiunta alle impostazioni di **AllowUpdate** negli oggetti server e zona.

* * Windows Server 2003: * *

0: nessuna restrizione.

1: non consente aggiornamenti dinamici di record SOA.

2: non consentire aggiornamenti dinamici di record NS nella radice della zona.

4: non consentire aggiornamenti dinamici di record NS non nella radice della zona (record NS di delega).

Sommare questi valori per determinare il valore dell'impostazione.

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del server DNS.

</dd> <dt>

**WriteAuthorityNS**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se il server DNS scrive i record NS e SOA nella sezione Authority in seguito alla risposta corretta.

</dd> <dt>

**XfrConnectTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Tempo, in secondi, in cui il server DNS attende una connessione TCP riuscita a un server remoto durante il tentativo di trasferimento di zona.

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

[**Metodo StartService della \_ classe server MicrosoftDNS**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Metodo StopService della \_ classe server MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Metodo StartScavenging della \_ classe server MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Metodo getdistinguishname della \_ classe server MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





