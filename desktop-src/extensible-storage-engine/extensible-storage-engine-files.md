---
description: 'Altre informazioni su: file del motore di archiviazione estendibile'
title: File del motore di archiviazione estendibile
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: c27bb0104c5923496c5dd7962ef4a9bacdc90af4
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321173"
---
# <a name="extensible-storage-engine-files"></a>File del motore di archiviazione estendibile


_**Si applica a:** Windows | Windows Server_

## <a name="extensible-storage-engine-files"></a>File del motore di archiviazione estendibile

Il motore di archiviazione estendibile utilizza i seguenti tipi di file:

- [File di log delle transazioni](#transaction-log-files)

- [File di log delle transazioni temporanei](#temporary-transaction-log-files)

- [File di log delle transazioni riservati](#reserved-transaction-log-files)

- [File di checkpoint](#checkpoint-files)

- [File di database](#database-files)

- [Database temporanei](#temporary-databases)

- [Scarica file mappa](#flush-map-files)

Questa tabella contiene una panoramica dei nomi dei file di dati gestiti da ESE. Per Windows Vista e versioni successive, l'impostazione JET_paramLegacyNames influisca sui nomi file utilizzati.

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p>Sistema operativo</p>
    </th>
    <th>
      <p>Windows Server 2003 e versioni precedenti<br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p>Windows Vista e versioni successive (client) <br />
Windows Server 2008 e versioni successive (Server)
</p>
    </th>
    <th>
      <p>Aggiornamento dell'anniversario di Windows 10 e versioni successive (client) <br />
Windows Server 2016 e versioni successive (Server)
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p>
        <strong>Impostazione JET_paramLegacyNames</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>N/A</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>Nessuna</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>JET_bitESE98FileNames</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>Uguale a Windows Vista/Server 2008</strong>
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <p>Log corrente</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . log</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . jtx</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Log pre-init</p>
    </td>
    <td>
      <p>&lt;Inst &gt; tmp. log</p>
    </td>
    <td>
      <p>&lt;Inst &gt; tmp. jtx</p>
    </td>
    <td>
      <p>&lt;Inst &gt; tmp. log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Log ruotati</p>
    </td>
    <td>
      <p>&lt;Inst &gt; xxxxx. log</p>
    </td>
    <td>
      <p>&lt;Inst &gt; xxxxx. jtx dopo fffff passare a &lt; inst &gt; xxxxxxxx. jtx</p>
    </td>
    <td>
      <p>&lt;Inst &gt; xxxxx. log dopo fffff passare a &lt; inst &gt; xxxxxxxx. log.</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">File del checkpoint</a>
      </p>
    </td>
    <td>
      <p>&lt;Inst &gt; . chk</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . JCP</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . chk</p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Database temporanei</a>
      </p>
    </td>
    <td>
      <p>&lt;nome file database temporaneo &gt; predefinito: tmp. edb</p>
    </td>
    <td>
      <p>&lt;nome file database temporaneo &gt; predefinito: tmp. edb</p>
    </td>
    <td>
      <p>&lt;nome file database temporaneo &gt; predefinito: tmp. edb</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">File di log delle transazioni riservati</a>
      </p>
    </td>
    <td>
      <p>Res1. log &amp; Res2. log</p>
    </td>
    <td>
      <p>&lt;Inst &gt; RESXXXXX. JRS</p>
    </td>
    <td colspan="2">
      <p>&lt;Inst &gt; RESXXXXX. JRS</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">File di database</a>
      </p>
    </td>
    <td>
      <p>&lt;nome file di database&gt;</p>
    </td>
    <td>
      <p>&lt;nome file di database&gt;</p>
    </td>
    <td>
      <p>&lt;nome file di database&gt;</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Scarica file mappa</a>
      </p>
    </td>
    <td>
      <p>N/D</p>
    </td>
    <td>
      <p>N/D</p>
    </td>
    <td>
      <p>N/D</p>
    </td>
    <td>
      <p>&lt;nome del file di database senza estensione &gt; . JFM</p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a>File di log delle transazioni

I file di log delle transazioni contengono operazioni sui file di database. Contengono informazioni sufficienti per portare un database in uno stato coerente logicamente dopo una chiusura imprevista di un processo o l'arresto del sistema.

I nomi dei file di log dipendono da un nome di base di tre lettere, che può essere impostato con [JET_paramBaseName](./transaction-log-parameters.md). Negli esempi seguenti viene usato il nome di base "edb", perché questo è il nome di base predefinito. L'estensione per i file di log delle transazioni sarà. log o. jtx a seconda che il JET_bitESE98FileNames sia impostato nel parametro JET_paramLegacyFileNames. Per ulteriori informazioni, vedere [parametri di sistema Extensible Storage Engine](./extensible-storage-engine-system-parameters.md).

I file di log delle transazioni sono denominati \<base\> \<generation-number\> . log, a partire da 1. Il numero di generazione del log è in formato esadecimale. Ad esempio, Edb00001. log è il primo log e edb000ff. log è il log di 255 io vi. I file di log hanno cinque cifre esadecimali nel nome del file di log, fino al file di log 1048576th, a cui i file di log iniziano con il nome in formato 11,3, ad esempio edb00100000. log. \<base\>. log è sempre il file di log attualmente in uso. Se il motore di database non è attivo, la generazione di edb. log può essere identificata usando il comando seguente: **esentutl.exe-ml edb. log**.

Sebbene i file di log delle transazioni dispongano di. Estensione di LOG comunemente associata a file di testo, i file di log delle transazioni sono in formato binario e non devono mai essere modificati da un utente. Le operazioni di database vengono scritte prima nel log. I dati possono essere scritti nel file di database in un secondo momento; probabilmente immediatamente, potenzialmente molto più tardi. In caso di interruzione imprevista di un processo o di un sistema, le operazioni sono ancora presenti nei file di log e non è possibile eseguire il rollback delle transazioni incomplete. La riproduzione dei file di log delle transazioni è detta *ripristino software* e viene eseguita automaticamente quando si chiama [JetInit](./jetinit-function.md) o [JetInit2](./jetinit2-function.md) . Il ripristino software può essere eseguito anche manualmente con l'opzione "-r" del programma Esentutl.exe. La riproduzione dei file di log delle transazioni in un database ripristinato da un backup è detta ripristino a *freddo*.

I file di log sono di dimensioni fisse, personalizzabili con [JET_paramLogFileSize](./transaction-log-parameters.md). Quando il file di log corrente, ovvero edb. log, viene riempito, viene rinominato in \<base\> \<generation-number\> . log e nel flusso del log delle transazioni è necessario un nuovo file di log delle transazioni.

A ogni istanza di database è associata una singola sequenza di file di log. In Windows XP è stato introdotto [JetCreateInstance](./jetcreateinstance-function.md), consentendo l'utilizzo di più sequenze di file di log delle transazioni da un unico processo. Tuttavia, nella stessa directory non possono esistere più sequenze di file di log delle transazioni.

I file di log delle transazioni non dovrebbero mai essere manipolati, rinominati, spostati o eliminati manualmente perché il danneggiamento dei dati può verificarsi.

I file di log delle transazioni verranno eliminati dal motore di database durante un backup completo (vedere [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)) o durante le normali operazioni, se è abilitata la registrazione circolare.

Al termine del riempimento di un file di log delle transazioni, il motore di database deve creare un nuovo file di log. La registrazione circolare è un mezzo mediante il quale i file di log possono essere puliti automaticamente dal motore di database quando non sono più necessari per il ripristino dell'arresto anomalo del sistema. Questo processo rappresenta un'alternativa alla rimozione dei file di log come prodotto dall'esecuzione di un backup. È possibile controllare la registrazione circolare con il parametro di sistema [JET_paramCircularLog](./transaction-log-parameters.md) . I file di log delle transazioni non devono essere eliminati utilizzando un altro metodo.

### <a name="temporary-transaction-log-files"></a>File di log delle transazioni temporanei

Quando si compila edb. log, ESE deve creare un nuovo file. Il nuovo file di transazione di log è noto come file di log delle transazioni temporaneo prima dell'utilizzo da parte di ESE.

Quando viene creato un nuovo file di log e le relative dimensioni vengono estese, questo viene chiamato \<base\> tmp. log. La creazione di un nuovo file può essere un'operazione potenzialmente costosa, quindi ESE creerà il file di log successivo in modo proattivo come attività in background.

Poiché il file di log delle transazioni temporaneo viene creato in previsione della necessità di un nuovo file di log delle transazioni, non contiene informazioni utili.

### <a name="reserved-transaction-log-files"></a>File di log delle transazioni riservati

I file di log delle transazioni riservati vengono creati quando il motore inizia a consentire la registrazione di operazioni importanti per ottenere una chiusura normale.

**Windows Vista:** In Windows Vista e versioni successive, i file di log delle transazioni riservati sono denominati \<base\> RESXXXXX. JRS.

**Windows Server 2003:** In Windows Server 2003 e versioni precedenti, i file di log delle transazioni riservati sono denominati Res1. log e Res2. log.

Quando il motore di database esaurisce lo spazio su disco, non è possibile creare un nuovo file di log. L'operazione più sicura consiste nell'arrestare in modo corretto, ma è necessario che alcune operazioni, ad esempio le operazioni di rollback, siano ancora registrate. La maggior parte delle operazioni del database avrà esito negativo durante questa fase.

Poiché i file di log delle transazioni riservati vengono creati in previsione della necessità dei file di log delle transazioni in uno scenario fuori disco, non contengono informazioni utili.

### <a name="checkpoint-files"></a>file del checkpoint

Il file del checkpoint archivia il checkpoint per una particolare sequenza di file di log delle transazioni. Il file del checkpoint è denominato \<base\> . chk o \<base\> . JCP, a seconda che il JET_bitESE98FileNames sia impostato nel parametro JET_paramLegacyFileNames e la relativa posizione venga fornita da [JET_paramSystemPath](./transaction-log-parameters.md).

Le operazioni di database vengono innanzitutto scritte nei file di log e quindi memorizzate nella cache. In un secondo momento, le operazioni vengono scritte nel file di database, ma per motivi di prestazioni, l'ordine in cui le operazioni vengono scritte nel file di database potrebbe non corrispondere all'ordine in cui sono state originariamente registrate. Le operazioni scritte nel file di log delle transazioni saranno in uno dei due stati seguenti:

  - Viene scritto nel file di log delle transazioni e nel file di database.

  - Viene scritto nel file di log delle transazioni e non è ancora stato scritto nel file di database.

Molte operazioni di database possono essere archiviate in un singolo file di log delle transazioni. Un file di log specificato può essere costituito dagli elementi seguenti:

  - Tutte le operazioni scritte nel file di database.

  - Nessuna operazione scritta nel file di database

  - Una combinazione di operazioni scritte nel file di database e operazioni non ancora scritte nel file di database.

Il Checkpoint si riferisce al punto nel tempo nel flusso del log delle transazioni in cui tutte le operazioni precedenti al Checkpoint sono state scritte nel file di database. Non esiste alcuna garanzia sulle operazioni che si verificano dopo il checkpoint. alcuni potrebbero essere in memoria e altri potrebbero essere scritti nel database.

Poiché tutte le operazioni nei file di log prima del checkpoint sono rappresentate nel file di database, solo i file di log delle transazioni dopo il Checkpoint sono necessari per il ripristino automatico per portare un determinato database in uno stato pulito.

### <a name="database-files"></a>File di database

Il file di database contiene lo schema per tutte le tabelle del database, i record per tutte le tabelle nel database e gli indici sulle tabelle. Il relativo percorso viene specificato tramite [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md)o [JetAttachDatabase2](./jetattachdatabase2-function.md).

Un database viene arrestato correttamente solo dopo una chiamata riuscita a [JetTerm](./jetterm-function.md) o [JetTerm2](./jetterm2-function.md).

Il programma Esentutl.exe può rilevare se un database è stato arrestato in modo corretto con l'opzione "-MH". Ad esempio, "esentutl.exe-MH Sample. edb" leggerà l'intestazione del database di un database denominato Sample. edb e visualizzerà lo stato di Sample. edb. Potrebbe stampare "stato: arresto normale" o "stato: arresto anomalo".

Un database che non è stato arrestato in modo corretto è in uno stato di arresto anomalo. Prima di Windows XP, questo stato veniva chiamato *incoerente*. Un database Dirty (non coerente) può essere portato a uno stato pulito con ripristino soft. Un database danneggiato non corrisponde a un database Dirty ("non coerente").

Un database danneggiato si riferisce a un danneggiamento fisico o logico e non può essere risolto con il ripristino soft. I danneggiamenti fisici possono essere flip di bit, che verranno spesso intercettati dai checksum nelle pagine del database. Un checksum non riuscito in un file di database si manifesta come errore di JET_errReadVerifyFailure.

Solo i database arrestati correttamente possono essere spostati in modo sicuro o rinominati. Se un database non è stato arrestato correttamente, non può essere spostato o rinominato automaticamente in modo sicuro.

È possibile associare più database a una singola sequenza di file di log delle transazioni.

### <a name="temporary-databases"></a>Database temporanei

Il database temporaneo viene usato come archivio di backup per TempTables e viene usato anche per la creazione di indici.

Il nome e il percorso sono configurati con [JET_paramTempPath](./temporary-database-parameters.md).

TempTables vengono creati con [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md). Vengono inoltre create da alcune chiamate API e utilizzate per restituire informazioni sullo schema, ad esempio [JetGetIndexInfo](./jetgetindexinfo-function.md).

## <a name="flush-map-files"></a>Scarica file mappa

A partire dall'aggiornamento dell'anniversario di Windows 10 (client) e da Windows Server 2016 (Server), ESE ha aggiunto un ulteriore livello di protezione contro le Scritture perse (o gli scaricamenti persi) 1, consentendo di rilevare tali eventi riinitialization2ti tra più processi. Questa funzionalità richiede il salvataggio permanente dei metadati in un file separato denominato file "Flush map".

Viene creato un file di mappa di scaricamento per ogni file di database e si trova nella stessa directory. Il nome del file è simile a quello del file di database, ma con un'estensione diversa. Ad esempio, se l'applicazione client crea un database con il percorso completo C: \\ directory \\ MyDabatase. edb, il file di mappa di scaricamento corrispondente è c: \\ directory \\ MyDabatase. JFM.

Questo miglioramento introduce due requisiti per la modalità di denominazione dei file di database:

  - Due database nella stessa directory non devono avere lo stesso nome di file con estensioni diverse. Ad esempio: C: \\ directory \\ MyDabatase. DB1 e c: \\ directory \\ MyDabatase. DB2.

  - 2 \. Un database non deve avere un'estensione JFM.

Quando si copia o si sposta manualmente un file di database, anche il file di mapping di scaricamento corrispondente deve essere copiato o spostato nella stessa directory di destinazione. Se non è presente un file di mappa di scaricamento al momento di un nuovo allegato del database (tramite [JetAttachDatabase](./jetattachdatabase-function.md), ne verrà creato uno nuovo che verrà ripopolato su richiesta man mano che le pagine vengono lette dal database. La combinazione di file di database e di mapping di scaricamento non corrispondenti viene gestita da ESE e impone l'eliminazione e la ricreazione della mappa di scaricamento non corrispondente da zero.

La dimensione di un file di mappa di scaricamento è direttamente proporzionale al file di database associato e approssimativamente uguale a (tutte le dimensioni in byte, il risultato deve essere arrotondato al multiplo successivo di 8.192):

`8,192 + ((<database file size> / <database page size>) / 4)`

Ad esempio: per un database da 1,5 GB che usa una dimensione di pagina 32 KB, le dimensioni approssimative della mappa di scaricamento sono pari a 24.576 byte (o 24KB).

È necessario aggiornare il file della mappa di scaricamento quando vengono scaricate le pagine del database. Se la registrazione transazionale è abilitata, ad esempio [JET_paramRecovery](./transaction-log-parameters.md) impostata su "on", ovvero l'impostazione predefinita, l'aggiornamento della mappa di scaricamento viene eseguito quando l'applicazione client apporta modifiche al database. In media, l'intera mappa di scaricamento viene scritta nei supporti non volatili una volta per ogni 20% di [JET_paramCheckpointDepthMax](./database-cache-parameters.md) (in byte) dei log delle transazioni generati. Il numero di operazioni di scrittura dipende dal modo in cui le modifiche vengono distribuite in tutto il database. Ma è al massimo approssimativamente (tutte le dimensioni in byte):

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

Se la registrazione transazionale è disabilitata, ad esempio [JET_paramRecovery](./transaction-log-parameters.md) impostata su "off", la mappa di scaricamento viene aggiornata solo una volta quando il database viene scollegato in modo esplicito tramite [JetDetachDatabase](./jetdetachdatabase-function.md)o viene scollegato in modo implicito terminando la relativa istanza ESE associata (tramite una delle funzioni [JetTerm](./jetterm-function.md) , purché [JET_bitTermDirty](./jetterm2-function.md) non venga passato).

1 una scrittura persa (o uno scaricamento perso) viene definita come operazione di scrittura che restituisce correttamente dal sistema operativo al motore di database ESE, ma i dati effettivi non vengono mai resi permanente nel file di database nel supporto non volatile. Il problema è in genere causato da uno stack di archiviazione (software o hardware) malfunzionante o configurato in maniera non configurata. Le applicazioni client possono ricevere un errore di [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) dalle funzioni ESE che richiedono la lettura dei dati dal database se i dati si trovano in un'area che ha subito un evento di scrittura perso.

2 la possibilità di rilevare le Scritture perse entro la durata di un processo è stata apportata a partire da Windows 8 (client) e Windows Server 2012 (Server).
