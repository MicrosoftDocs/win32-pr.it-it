---
description: Altre informazioni sulle proprietà InstanceParameters
title: Proprietà di InstanceParameters
TOCTitle: InstanceParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55103291
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1db9933e6e0a14b770e4250fc7e1faf564d3266ee258bfa71671093dceee763a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721161"
---
# <a name="instanceparameters-properties"></a>Proprietà di InstanceParameters

Includere membri protetti  
Includere i membri ereditati  

Il [tipo InstanceParameters](./instanceparameters-class.md) espone i membri seguenti.

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
<td>Ottiene o imposta il percorso file system assoluto di una cartella in cui il ripristino anomalo del sistema o un'operazione di ripristino può trovare i database a cui si fa riferimento nel log delle transazioni nella cartella specificata.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350972(v=exchg.10).md">Basename</a></td>
<td>Ottiene o imposta il prefisso di tre lettere utilizzato per molti dei file utilizzati dal motore di database. Ad esempio, il file del checkpoint è denominato EDB. CHK per impostazione predefinita perché EDB è il nome di base predefinito.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></td>
<td>Ottiene o imposta un valore che specifica il numero di risorse dell'albero B+ memorizzate nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione. I valori di grandi dimensioni per questo parametro determinano l'uso di una maggiore quantità di memoria da parte del motore di database, ma aumentano la velocità con cui un numero elevato di tabelle può essere aperto in modo casuale dall'applicazione. Ciò è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle. Supportato in Windows Vista e versioni seguenti. Ignorato Windows XP e Windows Server 2003.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350974(v=exchg.10).md">CachePriority</a></td>
<td>Ottiene o imposta la proprietà per istanza per le priorità relative della cache (impostazione predefinita = 100).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></td>
<td>Ottiene o imposta la soglia in byte per il numero di file di log delle transazioni che dovranno essere riprodotti dopo un arresto anomalo. Se la registrazione circolare è abilitata tramite CircularLog, questo parametro controlla anche la quantità approssimativa di file di log delle transazioni che verranno conservati su disco.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350977(v=exchg.10).md">CircularLog</a></td>
<td>Ottiene o imposta un valore che indica se la registrazione circolare è attivata. Quando la registrazione circolare è disattivata, tutti i file di log delle transazioni generati vengono mantenuti su disco fino a quando non sono più necessari perché è stato eseguito un backup completo del database. Quando la registrazione circolare è attivata, vengono conservati su disco solo i file di log delle transazioni più piccoli rispetto al checkpoint corrente. Il vantaggio di questa modalità è che i backup non sono necessari per ritirare i file di log delle transazioni meno recente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></td>
<td>Ottiene o imposta un valore che indica se JetInit ha esito negativo quando il motore di database è configurato per iniziare a usare file di log delle transazioni su disco di dimensioni diverse da quelle configurate. In genere, <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> recupererà correttamente i database, ma avrà esito negativo con <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> per indicare che le dimensioni del file di log non sono configurate correttamente. Tuttavia, quando questo parametro è impostato su true, il motore di database eliminerà automaticamente tutti i file di log vecchi, avviando un nuovo set di file di log delle transazioni usando le dimensioni del file di log configurate. Questo parametro è utile quando l'applicazione vuole modificare in modo trasparente le dimensioni del file di log delle transazioni, ma funziona ancora in modo trasparente negli scenari di aggiornamento e ripristino.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></td>
<td>Ottiene o imposta un valore che indica se ESENT creerà automaticamente le cartelle mancanti nei percorsi del file system.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></td>
<td>Ottiene o imposta il numero di pagine aggiunte a un file di database ogni volta che è necessario aumentare per contenere più dati.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></td>
<td>Ottiene o imposta l'intervallo massimo, espresso in secondi, per consentire il completamento dell'analisi del database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></td>
<td>Ottiene o imposta l'intervallo minimo di ripetizione dell'analisi del database, espresso in secondi.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></td>
<td>Ottiene o imposta la limitazione dell'analisi del database, in millisecondi.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></td>
<td>Ottiene o imposta un valore che indica se Manutenzione database deve essere eseguito durante il ripristino.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></td>
<td>Ottiene o imposta un valore che indica se la serializzazione di Manutenzione database è abilitata per i database che condividono lo stesso disco.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></td>
<td>Ottiene o imposta un valore che indica se <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a> verifica la presenza di indici compilati usando una versione precedente della libreria NLS nel sistema operativo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></td>
<td>Ottiene o imposta un valore che indica se la deframmentazione online è abilitata.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350988(v=exchg.10).md">Eventsource</a></td>
<td>Ottiene o imposta una stringa specifica dell'applicazione che verrà aggiunta a tutti i messaggi del log eventi generati dal motore di database. In questo modo è possibile correlare facilmente i messaggi del log eventi con l'applicazione di origine. Per impostazione predefinita, verrà usato il nome eseguibile dell'applicazione host.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350966(v=exchg.10).md">EventSourceKey</a></td>
<td>Ottiene o imposta il nome del log eventi utilizzato dal motore di database per i messaggi del log eventi. Per impostazione predefinita, tutti i messaggi del registro eventi verranno inviati al registro eventi dell'applicazione. Se il nome della chiave del Registro di sistema per un altro registro eventi è configurato, i messaggi del registro eventi verranno visualizzati.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350968(v=exchg.10).md">LogBuffer</a></td>
<td>Ottiene o imposta la quantità di memoria utilizzata per memorizzare nella cache i record del log prima che siano scritti nel file di log delle transazioni. L'unità per questo parametro è la dimensione del settore del volume che contiene i file di log delle transazioni. La dimensione del settore è quasi sempre di 512 byte, quindi è sicuro presupporre che le dimensioni per l'unità. Questo parametro influisce sulle prestazioni. Quando il motore di database è in un carico di aggiornamento elevato, questo buffer può diventare pieno molto rapidamente. Una dimensione della cache maggiore per il file di log delle transazioni è fondamentale per prestazioni di aggiornamento ottimali in una condizione di carico elevato. Il valore predefinito è noto per essere troppo piccolo per questo caso. Non impostare questo parametro su un numero di buffer maggiore (in byte) della metà delle dimensioni di un file di log delle transazioni.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></td>
<td>Ottiene o imposta il percorso relativo o file system assoluto della cartella che conterrà i log delle transazioni per l'istanza.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350969(v=exchg.10).md">LogFileSize</a></td>
<td>Ottiene o imposta le dimensioni dei file di log delle transazioni. Questo parametro deve essere impostato in unità di 1024 byte (ad esempio, un'impostazione di 2048 offrirà 2 MB di file di log).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350993(v=exchg.10).md">MaxCursors</a></td>
<td>Ottiene o imposta il numero di risorse cursore riservate per questa istanza. Una risorsa cursore corrisponde direttamente a un JET_TABLEID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></td>
<td>Ottiene o imposta il numero di risorse dell'albero B+ riservate per questa istanza.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350994(v=exchg.10).md">MaxSessions</a></td>
<td>Ottiene o imposta il numero di risorse di sessioni riservate per questa istanza. Una risorsa di sessione corrisponde direttamente a un JET_SESID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></td>
<td>Ottiene o imposta il numero di risorse tabella temporanee per l'uso da parte di un'istanza di . Questa impostazione influisce sul numero di tabelle temporanee che possono essere usate contemporaneamente. Se questo parametro di sistema è impostato su zero, non verrà creato alcun database temporaneo e qualsiasi attività che richiede l'uso del database temporaneo avrà esito negativo. Questa impostazione può essere utile per evitare l'I/O necessario per creare il database temporaneo se è noto che non verrà usato.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></td>
<td>Ottiene o imposta la percentuale di archivio versioni che può essere utilizzata dalla transazione meno recente prima <a href="hh564840(v=exchg.10).md">di VersionStoreOutOfMemory</a> (impostazione predefinita = 100).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350975(v=exchg.10).md">MaxVerPages</a></td>
<td>Ottiene o imposta il numero massimo di pagine dell'archivio versioni riservate per questa istanza.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></td>
<td>Ottiene o imposta un valore che indica se i messaggi del log eventi informativi che normalmente verrebbero generati dal motore di database verranno eliminati.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></td>
<td>Ottiene o imposta un valore che indica se un solo database può essere aperto con JetOpenDatabase da una determinata sessione contemporaneamente. Il database temporaneo è escluso da questa restrizione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></td>
<td>Ottiene o imposta le dimensioni iniziali del database temporaneo. Le dimensioni sono in pagine di database. Una dimensione pari a zero indica che devono essere usate le dimensioni predefinite di un database comune. È spesso consigliabile per le applicazioni di piccole dimensioni configurare il database temporaneo in modo che sia il più piccolo possibile. L'impostazione di questo <a href="dn351211(v=exchg.10).md">parametro su PageTempDBSmallest</a> consente di ottenere il database temporaneo più piccolo possibile.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></td>
<td>Ottiene o imposta il numero preferito di pagine dell'archivio versioni riservate per questa istanza. Se le dimensioni dell'archivio versioni superano questa soglia, tutte le informazioni usate solo per le attività in background facoltative, ad esempio il recupero dello spazio eliminato nel database, vengono invece sacrificate per mantenere spazio per le informazioni transazionali.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></td>
<td>Ottiene o imposta il numero massimo di operazioni di I/O inviati per un determinato scopo.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350981(v=exchg.10).md">Ripristino</a></td>
<td>Ottiene o imposta un valore che indica se il ripristino dell'arresto anomalo del sistema è in esecuzione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351007(v=exchg.10).md">SystemDirectory</a></td>
<td>Ottiene o imposta il percorso file system assoluto della cartella che conterrà il file del checkpoint per l'istanza.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350983(v=exchg.10).md">TempDirectory</a></td>
<td>Ottiene o imposta il percorso file system assoluto della cartella che conterrà il database temporaneo per l'istanza.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></td>
<td>Ottiene o imposta il numero di elementi di lavoro di pulizia in background che possono essere accodati al pool di thread del motore di database in qualsiasi momento.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn350985(v=exchg.10).md">WaypointLatency</a></td>
<td>Ottiene o imposta il numero di log per cui esent rinviare gli scaricamenti del database. Può essere usato per aumentare la recuperabilità del database se gli errori causano la perdita dei file di log. Supportato in Windows 7 e versioni seguenti. Ignorato in Windows XP, Windows Server 2003, Windows Vista e Windows Server 2008.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
