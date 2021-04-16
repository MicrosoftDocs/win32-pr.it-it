---
description: 'Altre informazioni su: membri SystemParameters'
title: Membri SystemParameters
TOCTitle: SystemParameters members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_members(v=EXCHG.10)
ms:contentKeyID: 55104101
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e317ef4e63a33951dc55e030718d226ae3eaeec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550095"
---
# <a name="systemparameters-members"></a>Membri SystemParameters

Includi membri protetti  
Includi membri ereditati  

Costanti per l'API ESENT. Questi non devono essere cercati tramite i parametri di sistema. Questa classe fornisce proprietà statiche per impostare e ottenere i parametri di sistema ESENT globali. Questa classe fornisce proprietà statiche per impostare e ottenere i parametri di sistema ESENT globali.

Il tipo [SystemParameters](./systemparameters-class.md) espone i membri seguenti.

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
<td>Ottiene la dimensione massima di un segnalibro. <a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351214(v=exchg.10).md">CacheSize</a></td>
<td>Ottiene o imposta le dimensioni della cache del database in pagine. Per impostazione predefinita, le dimensioni della cache del database vengono ottimizzate automaticamente, impostando questa proprietà su un valore diverso da zero, la cache verrà adattata alle dimensioni di destinazione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></td>
<td>Ottiene o imposta la dimensione massima della cache delle pagine del database. Le dimensioni sono le pagine del database. Se questo parametro viene lasciato al valore predefinito, le dimensioni massime della cache verranno impostate sulle dimensioni della memoria fisica quando viene chiamato JetInit.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></td>
<td>Ottiene o imposta le dimensioni minime della cache delle pagine del database, nelle pagine del database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></td>
<td>Ottiene il numero massimo di componenti in una chiave di ordinamento o di indice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351218(v=exchg.10).md">Configuration</a></td>
<td>Ottiene o imposta un valore che specifica i valori predefiniti per l'intero set di parametri di sistema. Quando questo parametro è impostato su una configurazione specifica, tutti i valori dei parametri di sistema vengono reimpostati sui valori predefiniti per tale configurazione. Se la configurazione è impostata per un'istanza specifica, i parametri di sistema globali non verranno reimpostati sui valori predefiniti. Small Configuration (0): il motore di database è ottimizzato per l'uso della memoria. Configurazione legacy (1): il motore di database presenta le impostazioni predefinite tradizionali. Supportato in Windows Vista e in alto. Ignorato in Windows XP e Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></td>
<td>Ottiene o imposta le dimensioni in byte delle pagine del database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></td>
<td>Ottiene o imposta un valore che indica se il motore di database accetta o rifiuta le modifiche apportate a un subset dei parametri di sistema. Questo parametro viene usato in combinazione con la <a href="dn351218(v=exchg.10).md">configurazione</a> per impedire che alcuni parametri di sistema vengano impostati dalle impostazioni predefinite della configurazione selezionata. Supportato in Windows Vista e in alto. Ignorato in Windows XP e Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351152(v=exchg.10).md">EnableFileCache</a></td>
<td>Ottiene o imposta un valore che indica se il motore di database deve utilizzare la cache dei file del sistema operativo per tutti i file gestiti.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351220(v=exchg.10).md">EnableViewCache</a></td>
<td>Ottiene o imposta un valore che indica se il motore di database deve utilizzare l'I/O di file mappato alla memoria per i file di database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></td>
<td>Ottiene o imposta il livello di dettaglio dei messaggi EventLog emessi al log eventi dal motore di database. I numeri più alti comporteranno messaggi EventLog più dettagliati.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351154(v=exchg.10).md">ExceptionAction</a></td>
<td>Ottiene o imposta la codifica dei valori da eseguire con le eccezioni generate all'interno di JET.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351227(v=exchg.10).md">HungIOActions</a></td>
<td>Ottiene o imposta il set di azioni da intraprendere su IOs che appaiono sospese.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></td>
<td>Ottiene o imposta la soglia per le operazioni di i/o sospese su cui si deve agire.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351156(v=exchg.10).md">Per la maggior parte</a></td>
<td>Ottiene le dimensioni massime della chiave. Questo dipende dalla versione di ESENT e dalle dimensioni della pagina del database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></td>
<td>Ottiene o imposta la compatibilità con le versioni precedenti con le convenzioni di denominazione dei file delle versioni precedenti del motore di database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></td>
<td>Ottiene le dimensioni dei blocchi LV. Dipende dalle dimensioni della pagina del database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351230(v=exchg.10).md">MaxInstances</a></td>
<td>Ottiene o imposta il numero massimo di istanze che è possibile creare.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></td>
<td>Ottiene o imposta la quantità minima di dati che devono essere compressi con la compressione Xpress.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></td>
<td>Questo parametro controlla il numero di I/o di file di database che possono essere accodati per singolo disco nel sistema operativo host alla volta. Un valore più elevato per questo parametro può migliorare significativamente le prestazioni di un'applicazione di database di grandi dimensioni.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></td>
<td>Ottiene o imposta il nome descrittivo per questa istanza del processo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></td>
<td>Ottiene o imposta la soglia in corrispondenza della quale la cache delle pagine del database inizia a rimuovere le pagine dalla cache per creare spazio per le pagine che non sono memorizzate nella cache. Quando il numero di buffer di pagina nella cache scende al di sotto di questa soglia, viene avviato un processo in background per ripristinare il pool di buffer disponibili. Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal JET_paramCacheSizeMax. Anche questa soglia deve essere sempre inferiore alla soglia di arresto impostata dal JET_paramStopFlushThreshold. L'altezza della distanza della soglia iniziale determina il tempo di risposta che la cache delle pagine del database deve avere per produrre i buffer disponibili prima che siano necessari per l'applicazione. Una soglia di inizio elevata offrirà al processo in background più tempo per rispondere. Tuttavia, una soglia di avvio elevata implica una soglia di arresto superiore e che ridurrà le dimensioni effettive della cache delle pagine del database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></td>
<td>Ottiene o imposta la soglia in corrispondenza della quale la cache delle pagine del database smette di rimuovere le pagine dalla cache per creare spazio per le pagine non memorizzate nella cache. Quando il numero di buffer di pagina nella cache supera questa soglia, il processo in background che è stato avviato per ripristinare il pool di buffer disponibili viene arrestato. Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal JET_paramCacheSizeMax. Anche questa soglia deve essere sempre maggiore della soglia iniziale impostata da JET_paramStartFlushThreshold. La distanza tra la soglia iniziale e la soglia di arresto influiscono sull'efficienza con cui le pagine del database vengono scaricate dal processo in background. Un gap maggiore renderà più probabile che le Scritture nelle pagine adiacenti vengano combinate. Tuttavia, una soglia di arresto elevata ridurrà le dimensioni effettive della cache delle pagine del database.</td>
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
<td>Lunghezza del prefisso utilizzato per denominare i file utilizzati dal motore di database.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351146(v=exchg.10).md">ColumnMost</a></td>
<td>Dimensioni massime per le colonne che non sono JET_coltyp. LongBinary o JET_coltyp. LONGTEXT.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351210(v=exchg.10).md">ColumnsFixedMost</a></td>
<td>Numero massimo di colonne fisse consentite in una tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351140(v=exchg.10).md">ColumnsMost</a></td>
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
<td>Lunghezza massima del nome delle impostazioni locali (LOCALE_NAME_MAX_LENGTH da Winnt. h).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351213(v=exchg.10).md">NameMost</a></td>
<td>Dimensione massima di un nome di tabella/colonna/indice.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a></td>
<td>Il numero di pagine che fornisce il database temporaneo più piccolo possibile.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[SystemParameters (classe)](./systemparameters-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
