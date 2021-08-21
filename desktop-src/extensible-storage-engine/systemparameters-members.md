---
description: 'Altre informazioni su: Membri systemParameters'
title: Membri di SystemParameters
TOCTitle: SystemParameters members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_members(v=EXCHG.10)
ms:contentKeyID: 55104101
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d2ad43871c768955f98c0e372adde37cd731f8f4689bcb05b21f7e169bed715c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118070998"
---
# <a name="systemparameters-members"></a>Membri di SystemParameters

Includere membri protetti  
Includi membri ereditati  

Costanti per l'API ESENT. Non è necessario cercarlo tramite i parametri di sistema. Questa classe fornisce proprietà statiche per impostare e ottenere parametri di sistema ESENT globali. Questa classe fornisce proprietà statiche per impostare e ottenere parametri di sistema ESENT globali.

Il [tipo SystemParameters](./systemparameters-class.md) espone i membri seguenti.

## <a name="properties"></a>Proprietà

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351215(v=exchg.10).md">BookmarkMost</a></td>
<td>Ottiene le dimensioni massime di un segnalibro. <a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351214(v=exchg.10).md">CacheSize</a></td>
<td>Ottiene o imposta le dimensioni della cache del database in pagine. Per impostazione predefinita, la cache del database ne ottimizza automaticamente le dimensioni. Impostando questa proprietà su un valore diverso da zero, la cache si adatta automaticamente alle dimensioni di destinazione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></td>
<td>Ottiene o imposta le dimensioni massime della cache delle pagine del database. Le dimensioni sono in pagine di database. Se questo parametro viene lasciato al valore predefinito, le dimensioni massime della cache verranno impostate sulla dimensione della memoria fisica quando viene chiamato JetInit.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></td>
<td>Ottiene o imposta le dimensioni minime della cache delle pagine del database, in pagine di database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></td>
<td>Ottiene il numero massimo di componenti in una chiave di ordinamento o di indice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351218(v=exchg.10).md">Configuration</a></td>
<td>Ottiene o imposta un valore che specifica i valori predefiniti per l'intero set di parametri di sistema. Quando questo parametro è impostato su una configurazione specifica, tutti i valori dei parametri di sistema vengono reimpostati sui valori predefiniti per tale configurazione. Se la configurazione è impostata per un'istanza specifica, i parametri di sistema globali non verranno reimpostati sui valori predefiniti. Configurazione piccola (0): il motore di database è ottimizzato per l'uso della memoria. Configurazione legacy (1): il motore di database ha le impostazioni predefinite tradizionali. Supportato in Windows Vista e versioni seguenti. Ignorato in Windows XP e Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></td>
<td>Ottiene o imposta le dimensioni in byte delle pagine del database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></td>
<td>Ottiene o imposta un valore che indica se il motore di database accetta o rifiuta le modifiche apportate a un subset dei parametri di sistema. Questo parametro viene usato insieme a <a href="dn351218(v=exchg.10).md">Configuration per</a> impedire che alcuni parametri di sistema vengano impostati in base alle impostazioni predefinite della configurazione selezionata. Supportato in Windows Vista e versioni seguenti. Ignorato in Windows XP e Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351152(v=exchg.10).md">EnableFileCache</a></td>
<td>Ottiene o imposta un valore che indica se il motore di database deve utilizzare la cache dei file del sistema operativo per tutti i file gestiti.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351220(v=exchg.10).md">EnableViewCache</a></td>
<td>Ottiene o imposta un valore che indica se il motore di database deve utilizzare l'I/O dei file mappati alla memoria per i file di database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></td>
<td>Ottiene o imposta il livello di dettaglio dei messaggi eventlog generati nel registro eventi dal motore di database. Numeri più elevati comportano messaggi di log eventi più dettagliati.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351154(v=exchg.10).md">ExceptionAction</a></td>
<td>Ottiene o imposta la codifica del valore da eseguire con le eccezioni generate all'interno di JET.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351227(v=exchg.10).md">Oggetti HungIOActions</a></td>
<td>Ottiene o imposta il set di azioni da eseguire sugli I/O che appaiono bloccata.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></td>
<td>Ottiene o imposta la soglia per ciò che viene considerato un I/O bloccato su cui intervenire.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351156(v=exchg.10).md">KeyMost</a></td>
<td>Ottiene la dimensione massima della chiave. Dipende dalla versione di Esent e dalle dimensioni della pagina del database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></td>
<td>Ottiene o imposta la compatibilità con le versioni precedenti delle convenzioni di denominazione dei file delle versioni precedenti del motore di database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></td>
<td>Ottiene le dimensioni dei blocchi lv. Dipende dalle dimensioni della pagina del database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351230(v=exchg.10).md">MaxInstances</a></td>
<td>Ottiene o imposta il numero massimo di istanze che è possibile creare.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></td>
<td>Ottiene o imposta la quantità minima di dati che devono essere compressi con la compressione xpress.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></td>
<td>Questo parametro controlla il numero di I/O di file di database che possono essere accodati per disco nel sistema operativo host contemporaneamente. Un valore maggiore per questo parametro può contribuire in modo significativo alle prestazioni di un'applicazione di database di grandi dimensioni.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></td>
<td>Ottiene o imposta il nome descrittivo per questa istanza del processo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></td>
<td>Ottiene o imposta la soglia alla quale la cache delle pagine del database inizia a rimuovere le pagine dalla cache per fare spazio alle pagine non memorizzate nella cache. Quando il numero di buffer di pagina nella cache scende al di sotto di questa soglia, verrà avviato un processo in background per riempire il pool di buffer disponibili. Questa soglia è sempre relativa alla dimensione massima della cache impostata da JET_paramCacheSizeMax. Questa soglia deve essere sempre inferiore alla soglia di arresto impostata da JET_paramStopFlushThreshold. L'altezza della distanza della soglia iniziale determinerà il tempo di risposta che la cache delle pagine del database deve avere per produrre buffer disponibili prima che l'applicazione ne abbia bisogno. Una soglia di avvio elevata offrirà al processo in background più tempo per reagire. Tuttavia, una soglia di avvio elevata implica una soglia di arresto più elevata che ridurrà le dimensioni effettive della cache delle pagine del database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></td>
<td>Ottiene o imposta la soglia alla quale la cache delle pagine del database termina di rimuovere le pagine dalla cache per fare spazio alle pagine non memorizzate nella cache. Quando il numero di buffer di pagina nella cache supera questa soglia, il processo in background avviato per riempire il pool di buffer disponibili viene arrestato. Questa soglia è sempre relativa alla dimensione massima della cache impostata da JET_paramCacheSizeMax. Anche questa soglia deve essere sempre maggiore della soglia iniziale impostata da JET_paramStartFlushThreshold. La distanza tra la soglia di inizio e la soglia di arresto influisce sull'efficienza con cui le pagine del database vengono scaricate dal processo in background. Un gap maggiore rende più probabile che le scritture nelle pagine adiacenti possano essere combinate. Tuttavia, una soglia di arresto elevata ridurrà le dimensioni effettive della cache delle pagine del database.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="fields"></a>Campi

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351208(v=exchg.10).md">BaseNameLength</a></td>
<td>Lunghezza del prefisso utilizzato per assegnare un nome ai file usati dal motore di database.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351146(v=exchg.10).md">ColumnMost</a></td>
<td>Dimensioni massime per le colonne non JET_coltyp. LongBinary o JET_coltyp. LongText.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351210(v=exchg.10).md">ColumnsFixedMost</a></td>
<td>Numero massimo di colonne fisse consentite in una tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351140(v=exchg.10).md">ColonneMost</a></td>
<td>Numero massimo di colonne consentite in una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351148(v=exchg.10).md">ColumnsTaggedMost</a></td>
<td>Numero massimo di colonne con tag consentite in una tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351212(v=exchg.10).md">ColumnsVarMost</a></td>
<td>Numero massimo di colonne a lunghezza variabile consentite in una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351141(v=exchg.10).md">LocaleNameMaxLength</a></td>
<td>Lunghezza massima di un nome delle impostazioni locali (LOCALE_NAME_MAX_LENGTH da winnt.h).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351213(v=exchg.10).md">NameMost</a></td>
<td>Dimensioni massime di un nome di tabella/colonna/indice.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a></td>
<td>Numero di pagine che fornisce il database temporaneo più piccolo possibile.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[SystemParameters (classe)](./systemparameters-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
