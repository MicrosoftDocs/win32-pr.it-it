---
description: 'Altre informazioni su: InstanceParameters Properties'
title: Proprietà di InstanceParameters
TOCTitle: InstanceParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55103291
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0ac2b8aa959b8fa07f06e2de86dcfc173bab15ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559776"
---
# <a name="instanceparameters-properties"></a>Proprietà di InstanceParameters

Includi membri protetti  
Includi membri ereditati  

Il tipo [InstanceParameters](./instanceparameters-class.md) espone i membri seguenti.

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
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></td>
<td>Ottiene o imposta il percorso di file system relativo o assoluto di una cartella in cui il ripristino dell'arresto anomalo o un'operazione di ripristino è in grado di individuare i database a cui si fa riferimento nel log delle transazioni nella cartella specificata.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350972(v=exchg.10).md">BaseName</a></td>
<td>Ottiene o imposta il prefisso di tre lettere utilizzato per molti dei file utilizzati dal motore di database. Il file del checkpoint, ad esempio, è denominato EDB. CHK per impostazione predefinita, perché EDB è il nome di base predefinito.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></td>
<td>Ottiene o imposta un valore che indica il numero di risorse dell'albero B + memorizzato nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione. I valori di grandi dimensioni per questo parametro comportano l'utilizzo di una maggiore quantità di memoria da parte del motore di database, ma aumentano la velocità con cui l'applicazione può aprire in modo casuale un numero elevato di tabelle. Questa operazione è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle. Supportato in Windows Vista e in alto. Ignorato in Windows XP e Windows Server 2003.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350974(v=exchg.10).md">CachePriority</a></td>
<td>Ottiene o imposta la proprietà per istanza per le priorità della cache relativa (impostazione predefinita = 100).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></td>
<td>Ottiene o imposta la soglia in byte per informazioni sul numero di file di log delle transazioni che dovranno essere riprodotti dopo un arresto anomalo del sistema. Se la registrazione circolare è abilitata usando CircularLog, questo parametro controllerà anche la quantità approssimativa di file di log delle transazioni che verranno conservati su disco.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350977(v=exchg.10).md">CircularLog</a></td>
<td>Ottiene o imposta un valore che indica se la registrazione circolare è attiva. Quando la registrazione circolare è disattivata, tutti i file di log delle transazioni generati vengono conservati su disco fino a quando non sono più necessari perché è stato eseguito un backup completo del database. Quando la registrazione circolare è attiva, solo i file di log delle transazioni più piccoli rispetto al checkpoint corrente vengono conservati su disco. Il vantaggio di questa modalità è che non è necessario che i backup ritirino i vecchi file di log delle transazioni.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></td>
<td>Ottiene o imposta un valore che indica se JetInit ha esito negativo quando il motore di database è configurato per iniziare a utilizzare i file di log delle transazioni su disco con dimensioni diverse da quelle configurate. In genere, <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> recupererà correttamente i database, ma avrà esito negativo con <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> per indicare che le dimensioni del file di log non sono configurate correttamente. Tuttavia, quando questo parametro è impostato su true, il motore di database eliminerà automaticamente tutti i vecchi file di log, avviando un nuovo set di file di log delle transazioni usando le dimensioni del file di log configurate. Questo parametro è utile quando l'applicazione desidera modificare in modo trasparente le dimensioni del file del log delle transazioni, ma continua a funzionare in modo trasparente negli scenari di aggiornamento e ripristino.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></td>
<td>Ottiene o imposta un valore che indica se ESENT creerà automaticamente le cartelle mancanti nei percorsi del file System.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></td>
<td>Ottiene o imposta il numero di pagine aggiunte a un file di database ogni volta che è necessario aumentare per contenere più dati.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></td>
<td>Ottiene o imposta l'intervallo massimo consentito per il completamento dell'analisi del database, in secondi.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></td>
<td>Ottiene o imposta l'intervallo minimo per la ripetizione dell'analisi del database, in secondi.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></td>
<td>Ottiene o imposta la limitazione dell'analisi del database, in millisecondi.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></td>
<td>Ottiene o imposta un valore che indica se è necessario eseguire la manutenzione del database durante il ripristino.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></td>
<td>Ottiene o imposta un valore che indica se la serializzazione della manutenzione del database è abilitata per i database che condividono lo stesso disco.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></td>
<td>Ottiene o imposta un valore che indica se <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a> verificherà la presenza di indici compilati utilizzando una versione precedente della libreria NLS nel sistema operativo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></td>
<td>Ottiene o imposta un valore che indica se la deframmentazione in linea è abilitata.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350988(v=exchg.10).md">EventSource</a></td>
<td>Ottiene o imposta una stringa specifica dell'applicazione che verrà aggiunta a qualsiasi messaggio del registro eventi emesso dal motore di database. In questo modo è possibile correlare facilmente i messaggi del log eventi con l'applicazione di origine. Per impostazione predefinita, verrà usato il nome dell'eseguibile dell'applicazione host.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350966(v=exchg.10).md">EventSourceKey</a></td>
<td>Ottiene o imposta il nome del registro eventi utilizzato dal motore di database per i messaggi del log eventi. Per impostazione predefinita, tutti i messaggi del registro eventi vengono inviati al registro eventi dell'applicazione. Se viene configurato il nome della chiave del registro di sistema per un altro log eventi, i messaggi del registro eventi verranno invece inseriti.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350968(v=exchg.10).md">LogBuffers</a></td>
<td>Ottiene o imposta la quantità di memoria utilizzata per memorizzare nella cache i record del log prima che vengano scritti nel file di log delle transazioni. L'unità per questo parametro è la dimensione settoriale del volume che include i file di log delle transazioni. La dimensione del settore è quasi sempre di 512 byte, quindi è sicuro presupporre che le dimensioni dell'unità. Questo parametro ha un effetto sulle prestazioni. Quando il motore di database è sottoposto a un carico di aggiornamento intenso, questo buffer può essere pieno molto rapidamente. Una dimensione della cache maggiore per il file di log delle transazioni è essenziale per le prestazioni di aggiornamento ottimali in una condizione di carico elevato. Il valore predefinito è troppo piccolo per questo caso. Non impostare questo parametro su un numero di buffer maggiore (in byte) della metà delle dimensioni di un file di log delle transazioni.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></td>
<td>Ottiene o imposta il percorso di file system relativo o assoluto della cartella che conterrà i log delle transazioni per l'istanza.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350969(v=exchg.10).md">LogFileSize</a></td>
<td>Ottiene o imposta le dimensioni dei file di log delle transazioni. Questo parametro deve essere impostato in unità di 1024 byte (ad esempio, un'impostazione di 2048 fornirà 2MB di logfile).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350993(v=exchg.10).md">MaxCursors</a></td>
<td>Ottiene o imposta il numero di risorse del cursore riservate per l'istanza. Una risorsa di cursore corrisponde direttamente a una JET_TABLEID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></td>
<td>Ottiene o imposta il numero di risorse dell'albero B + riservate per l'istanza.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350994(v=exchg.10).md">MaxSessions</a></td>
<td>Ottiene o imposta il numero di risorse delle sessioni riservate per questa istanza. Una risorsa di sessione corrisponde direttamente a una JET_SESID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></td>
<td>Ottiene o imposta il numero di risorse della tabella temporanea utilizzate da un'istanza di. Questa impostazione influirà sul numero di tabelle temporanee che possono essere usate contemporaneamente. Se questo parametro di sistema è impostato su zero, non verrà creato alcun database temporaneo e le attività che richiedono l'utilizzo del database temporaneo avranno esito negativo. Questa impostazione può essere utile per evitare l'i/O necessario per creare il database temporaneo se è noto che non verrà utilizzato.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></td>
<td>Ottiene o imposta la percentuale di archivio versioni che può essere utilizzata dalla transazione meno recente prima di <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (impostazione predefinita = 100).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350975(v=exchg.10).md">MaxVerPages</a></td>
<td>Ottiene o imposta il numero massimo di pagine dell'archivio versioni riservate per questa istanza.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></td>
<td>Ottiene o imposta un valore che indica se i messaggi di registro eventi informativi che verrebbero normalmente generati dal motore di database verranno eliminati.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></td>
<td>Ottiene o imposta un valore che indica se è consentito l'apertura di un solo database tramite JetOpenDatabase da una sessione specificata. Il database temporaneo è escluso da questa restrizione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></td>
<td>Ottiene o imposta le dimensioni iniziali del database temporaneo. Le dimensioni sono le pagine del database. Una dimensione pari a zero indica che devono essere utilizzate le dimensioni predefinite di un database normale. È spesso consigliabile che le piccole applicazioni configurino il database temporaneo in modo che sia il più piccolo possibile. L'impostazione di questo parametro su <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> consente di ottenere il database temporaneo più piccolo possibile.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></td>
<td>Ottiene o imposta il numero preferito di pagine dell'archivio versioni riservate per questa istanza. Se la dimensione dell'archivio versioni supera questa soglia, le informazioni utilizzate solo per le attività in background facoltative, ad esempio il ripristino dello spazio eliminato nel database, vengono invece sacrificate per mantenere la stanza per le informazioni transazionali.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></td>
<td>Ottiene o imposta il numero massimo di operazioni di I/O inviate per uno scopo specifico.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350981(v=exchg.10).md">Ripristino</a></td>
<td>Ottiene o imposta un valore che indica se il ripristino dell'arresto anomalo è impostato su on.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351007(v=exchg.10).md">SystemDirectory</a></td>
<td>Ottiene o imposta il percorso file system relativo o assoluto della cartella che conterrà il file del checkpoint per l'istanza.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350983(v=exchg.10).md">TempDirectory</a></td>
<td>Ottiene o imposta il percorso di file system relativo o assoluto della cartella che conterrà il database temporaneo per l'istanza di.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></td>
<td>Ottiene o imposta il numero di elementi di lavoro di pulitura in background che possono essere accodati al pool di thread del motore di database in un momento specifico.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350985(v=exchg.10).md">WaypointLatency</a></td>
<td>Ottiene o imposta il numero di registri per i quali ESENT rinvia gli scaricamenti del database. Questa operazione può essere utilizzata per aumentare la recuperabilità del database se gli errori determinano la perdita di file di registro. Supportato su Windows 7 e su. Ignorato in Windows XP, Windows Server 2003, Windows Vista e Windows Server 2008.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
