---
description: 'Altre informazioni su: Extensible Archiviazione Engine Files'
title: Extensible Archiviazione Engine Files
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: 1e6d0988966d1eb58a21668cad559308eadbd3eb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469998"
---
# <a name="extensible-storage-engine-files"></a>Extensible Archiviazione Engine Files


_**Si applica a:** Windows | Windows Server_

## <a name="extensible-storage-engine-files"></a>Extensible Archiviazione Engine Files

Extensible Archiviazione Engine usa i tipi di file seguenti:

- [File di log delle transazioni](#transaction-log-files)

- [File di log delle transazioni temporanei](#temporary-transaction-log-files)

- [File di log delle transazioni riservati](#reserved-transaction-log-files)

- [File di checkpoint](#checkpoint-files)

- [File di database](#database-files)

- [Database temporanei](#temporary-databases)

- [Scaricare i file di mappa](#flush-map-files)

Questa tabella contiene una panoramica dei nomi dei file di dati gestiti da ESE. Per Windows Vista e versioni successive, l'JET_paramLegacyNames predefinita influisce sui nomi di file usati.


| | |  | 



### <a name="transaction-log-files"></a>File di log delle transazioni

I file di log delle transazioni contengono operazioni sui file di database. Contengono informazioni sufficienti per portare un database a uno stato coerente logicamente dopo una chiusura imprevista del processo o l'arresto del sistema.

I nomi dei file di log dipendono da un nome di base di tre lettere, che può essere impostato con [JET_paramBaseName](./transaction-log-parameters.md). Negli esempi seguenti viene utilizzato il nome di base "edb", perché si tratta del nome di base predefinito. L'estensione per i file di log delle transazioni sarà log o jtx a seconda che il JET_bitESE98FileNames sia impostato nel parametro JET_paramLegacyFileNames. Per altre informazioni, vedere [Extensible Archiviazione Engine System Parameters](./extensible-storage-engine-system-parameters.md).

I file di log delle transazioni \<base\> \<generation-number\> sono denominati log, a partire da 1. Il numero di generazione del log è in formato esadecimale. Ad esempio, edb00001.log è il primo log e edb000ff.log è il 255° log. I file di log hanno cinque cifre esadecimali nel nome del file di log, fino al 1048576° file di log, a quel punto i file di log iniziano a essere denominati in un formato 11.3 (ad esempio, edb00100000.log). \<base\>.log è sempre il file di log attualmente in uso. Se il motore di database non è attivo, la generazione di edb.log può essere identificata usando il comando **seguente:esentutl.exe -ml edb.log**.

Anche se i file di log delle transazioni hanno . Estensione LOG comunemente associata a file di testo, i file di log delle transazioni sono in formato binario e non devono mai essere modificati da un utente. Le operazioni di database vengono prima scritte nel log. I dati possono essere scritti nel file di database in un secondo momento. probabilmente immediatamente, potenzialmente molto più avanti. In caso di terminazione imprevista del processo o del sistema, le operazioni sono ancora presenti nei file di log ed è possibile eseguire il rollback delle transazioni incomplete. L'azione di riproduzione dei file di log delle transazioni è detta recupero a riesecuzione automatica e viene eseguita automaticamente quando viene chiamato [JetInit](./jetinit-function.md) o [JetInit2.](./jetinit2-function.md) Il ripristino software può essere eseguito anche manualmente con l'opzione "-r" del Esentutl.exe software. L'azione di riproduzione dei file di log delle transazioni in un database ripristinato da un backup è detta *recupero a hard recovery.*

I file di log hanno dimensioni fisse, personalizzabili [con JET_paramLogFileSize](./transaction-log-parameters.md). Quando il file di log corrente, ovvero edb.log, viene riempito, viene rinominato in log ed è necessario un nuovo file di log delle transazioni nel flusso del \<base\> \<generation-number\> log delle transazioni.

A ogni istanza del database è associata una singola sequenza di file di log. Windows Xp ha [introdotto JetCreateInstance,](./jetcreateinstance-function.md)consentendo l'uso di più sequenze di file di log delle transazioni da parte di un singolo processo. Nella stessa directory, tuttavia, non possono esistere più sequenze di file di log delle transazioni.

I file di log delle transazioni non devono quasi mai essere manipolati, rinominati, spostati o eliminati manualmente perché può verificarsi un danneggiamento dei dati.

I file di log delle transazioni verranno eliminati dal motore di database durante un backup completo (vedere [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)) o durante le normali operazioni, se la registrazione circolare è abilitata.

Dopo aver compilato un file di log delle transazioni, il motore di database deve creare un nuovo file di log. La registrazione circolare è uno strumento che consente di pulire automaticamente i file di log dal motore di database quando non sono più necessari per il ripristino con arresto anomalo del sistema. Questo processo è un'alternativa alla rimozione dei file di log come prodotto per l'esecuzione di un backup. La registrazione circolare può essere controllata con il [JET_paramCircularLog](./transaction-log-parameters.md) di sistema. I file di log delle transazioni non devono essere eliminati con altri metodi.

### <a name="temporary-transaction-log-files"></a>File di log delle transazioni temporanei

Quando edb.log si riempie, ESE deve creare un nuovo file. Il nuovo file di transazione del log è noto come file di log delle transazioni temporaneo prima di essere utilizzato da ESE.

Mentre viene creato un nuovo file di log con dimensioni estese, verrà chiamato \<base\> tmp.log. La creazione di un nuovo file può essere un'operazione potenzialmente disserente, quindi ESE creerà il file di log successivo in modo proattivo come attività in background.

Poiché il file di log delle transazioni temporaneo viene creato in previsione della necessità di un nuovo file di log delle transazioni, non contiene informazioni utili.

### <a name="reserved-transaction-log-files"></a>File di log delle transazioni riservati

I file di log delle transazioni riservati vengono creati all'avvio del motore per consentire la registrazione di operazioni importanti per ottenere un arresto pulito.

**Windows Vista:** In Windows Vista e versioni successive, i file di log delle transazioni riservati sono denominati \<base\> RESXXXXX.js.

**Windows Server 2003:** In Windows Server 2003 e versioni precedenti, i file di log delle transazioni riservati sono denominati res1.log e res2.log.

Quando lo spazio su disco del motore di database è insufficiente, non è possibile creare un nuovo file di log. La cosa più sicura da fare è arrestarsi in modo pulito, ma alcune operazioni, ad esempio le operazioni di rollback, devono comunque essere registrate. La maggior parte delle operazioni di database avrà esito negativo durante questa fase.

Poiché i file di log delle transazioni riservati vengono creati in previsione della necessità di file di log delle transazioni in uno scenario di disco insufficiente, non contengono informazioni utili.

### <a name="checkpoint-files"></a>file del checkpoint

Il file del checkpoint archivia il checkpoint per una sequenza di file di log delle transazioni specifica. Il file del checkpoint è denominato \<base\> .chk o \<base\> .jcp, a seconda che il JET_bitESE98FileNames sia impostato [](./transaction-log-parameters.md)nel parametro JET_paramLegacyFileNames e che il relativo percorso sia specificato da JET_paramSystemPath .

Le operazioni di database vengono prima scritte nei file di log e quindi memorizzate nella cache. In un secondo momento, le operazioni vengono scritte nel file di database, ma per motivi di prestazioni, l'ordine in cui le operazioni vengono scritte nel file di database potrebbe non corrispondere all'ordine in cui sono state registrate in origine. Le operazioni scritte nel file di log delle transazioni saranno in uno dei due stati seguenti:

  - Scritto nel file di log delle transazioni e nel file di database.

  - Scritto nel file di log delle transazioni e non ancora scritto nel file di database.

Molte operazioni di database possono essere archiviate in un singolo file di log delle transazioni. Un determinato file di log può essere costituito da quanto segue:

  - Tutte le operazioni scritte nel file di database.

  - Nessuna operazione scritta nel file di database

  - Combinazione di operazioni scritte nel file di database e operazioni non ancora scritte nel file di database.

Il checkpoint fa riferimento al punto nel tempo nel flusso del log delle transazioni in cui tutte le operazioni precedenti al checkpoint sono state scritte nel file di database. Non esiste alcuna garanzia sulle operazioni che si verificano dopo il checkpoint. alcuni potrebbero essere in memoria e altri potrebbero essere scritti nel database.

Poiché tutte le operazioni nei file di log precedenti al checkpoint sono rappresentate nel file di database, solo i file di log delle transazioni dopo il checkpoint sono necessari per il recupero a tempo determinato per portare un determinato database in uno stato pulito.

### <a name="database-files"></a>File di database

Il file di database contiene lo schema per tutte le tabelle del database, i record per tutte le tabelle nel database e gli indici delle tabelle. La posizione viene specificata usando [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md)o [JetAttachDatabase2](./jetattachdatabase2-function.md).

Un database viene chiuso correttamente solo dopo una chiamata riuscita a [JetTerm](./jetterm-function.md) o [JetTerm2.](./jetterm2-function.md)

Il Esentutl.exe può rilevare se un database viene chiuso in modo pulito con l'opzione "-mh". Ad esempio, "esentutl.exe -mh sample.edb" leggerà l'intestazione del database di un database denominato sample.edb e stamperà lo stato di sample.edb. Può stampare "State: Clean Shutdown" o "State: Dirty Shutdown".

Un database che non è stato chiuso in modo pulito si trova in uno stato di arresto dirty. Prima di Windows XP, questo stato era denominato *incoerente.* Un database dirty (incoerente) può essere portato a uno stato pulito con il ripristino soft. Un database danneggiato non corrisponde a un database dirty ("incoerente").

Un database danneggiato si riferisce a un danneggiamento fisico o logico e non può essere risolto con il ripristino soft. I danneggiamenti fisici possono essere capovolgimenti di bit, che vengono spesso intercettati dai checksum nelle pagine del database. Un checksum non riuscito in un file di database si manifesta come JET_errReadVerifyFailure errore.

Solo i database arrestati in modo pulito possono essere spostati o rinominati in modo sicuro. Se un database non è stato chiuso in modo pulito, non può essere spostato o rinominato automaticamente.

È possibile associare più database a una singola sequenza di file di log delle transazioni.

### <a name="temporary-databases"></a>Database temporanei

Il database temporaneo viene usato come archivio di backup per le tabelle temporanee e viene usato anche durante la creazione di indici.

Il nome e il percorso sono configurati [con JET_paramTempPath](./temporary-database-parameters.md).

Le tabelle temporanee vengono create [con JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md). Vengono inoltre creati da alcune chiamate API e usati per restituire informazioni sullo schema ( ad esempio [JetGetIndexInfo](./jetgetindexinfo-function.md)).

## <a name="flush-map-files"></a>Scaricare i file di mappa

A partire da Windows 10 Anniversary Update (client) e Windows Server 2016 (server), ESE ha aggiunto un ulteriore livello di protezione da scritture perse (o scaricamenti persi) 1, consentendo di rilevare tali eventi tra processi di nuova inizializzazione2. Questa funzionalità richiede la persistenza dei metadati in un file separato denominato file "flush map".

Viene creato un file della mappa di scaricamento per ogni file di database e si trova nella stessa directory. Il nome del file è simile al file di database, ma con un'estensione diversa. Ad esempio, se l'applicazione client crea un database con il percorso completo C: MyDirectory MyDabatase.edb, il file della mappa di scaricamento corrispondente \\ \\ è C: \\ MyDirectory \\ MyDabatase.jfm.

Questo miglioramento introduce due requisiti per la modalità di nome dei file di database:

  - Due database nella stessa directory non devono avere lo stesso nome file con estensioni diverse. Ad esempio: C: \\ MyDirectory \\ MyDabatase.db1 e C: \\ MyDirectory \\ MyDabatase.db2.

  - 2\. Un database non deve avere un'estensione jfm.

Quando si copia o si sposta manualmente un file di database, anche il file corrispondente della mappa di scaricamento deve essere copiato o spostato nella stessa directory di destinazione. Se un file della mappa di scaricamento non è presente al momento di un nuovo allegato di database (tramite [JetAttachDatabase,](./jetattachdatabase-function.md)ne verrà creato uno nuovo e popolato nuovamente su richiesta quando le pagine vengono lette dal database. La combinazione di file di mapping di database e scaricamento non corrispondenti viene gestita da ESE e forza l'eliminazione e la ri-creazione della mappa di scaricamento non corrispondente da zero.

Le dimensioni di un file della mappa di scaricamento sono direttamente proporzionali al file di database associato e approssimativamente uguali a (tutte le dimensioni in byte, risultato deve essere arrotondato al multiplo successivo di 8.192):

`8,192 + ((<database file size> / <database page size>) / 4)`

Ad esempio: per un database da 1,5 GB con dimensioni di pagina di 32 KB, le dimensioni approssimative della mappa di scaricamento sono 24.576 byte (o 24 KB).

Il file della mappa di scaricamento deve essere aggiornato quando le pagine del database vengono scaricate. Se la registrazione transazionale è abilitata(ad esempio, [JET_paramRecovery](./transaction-log-parameters.md) è impostata su "on", il valore predefinito), l'aggiornamento della mappa di scaricamento viene eseguito quando l'applicazione client apporta modifiche al database. In media, l'intera mappa di scaricamento viene scritta nei supporti non volatili una sola volta per ogni 20% JET_paramCheckpointDepthMax valore (in byte) dei log transazionali generati. [](./database-cache-parameters.md) Il numero di operazioni di scrittura dipende dalla distribuzione nel database delle modifiche. Ma è al massimo, approssimativamente (tutte le dimensioni in byte):

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

Se la registrazione transazionale è disabilitata ,ad esempio [JET_paramRecovery](./transaction-log-parameters.md) impostata su "off", la mappa di scaricamento viene aggiornata una sola volta quando il database viene scollegato in modo esplicito (tramite [JetDetachDatabase](./jetdetachdatabase-function.md)o scollegato in modo implicito in modo pulito terminando l'istanza ESE associata tramite una qualsiasi delle funzioni [JetTerm,](./jetterm-function.md) purché non venga passato [JET_bitTermDirty).](./jetterm2-function.md)

1 Un'operazione di scrittura persa (o scaricamento persa) viene definita come operazione di scrittura che restituisce correttamente dal sistema operativo al motore di database ESE, ma i dati effettivi non vengono mai resi persistenti nel file di database nel supporto non volatile. In genere è causato da un malfunzionamento o da uno stack di archiviazione non configurato correttamente (software o hardware). Le applicazioni client [](./extensible-storage-engine-error-codes.md) possono ricevere un JET_errReadLostFlushVerifyFailure errore dalle funzioni ESE che richiedono la lettura dei dati dal database se i dati si trovano in un'area che ha subito un evento di scrittura perso.

2 La possibilità di rilevare le scritture perse all'interno della durata di un processo è presente Windows 8 (client) e Windows Server 2012 (server).
