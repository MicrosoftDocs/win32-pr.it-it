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
# <a name="instanceparameters-properties"></a><span data-ttu-id="bb169-103">Proprietà di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="bb169-103">InstanceParameters properties</span></span>

<span data-ttu-id="bb169-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="bb169-104">Include protected members</span></span>  
<span data-ttu-id="bb169-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="bb169-105">Include inherited members</span></span>  

<span data-ttu-id="bb169-106">Il tipo [InstanceParameters](./instanceparameters-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="bb169-106">The [InstanceParameters](./instanceparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="bb169-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bb169-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="bb169-108">Nome</span><span class="sxs-lookup"><span data-stu-id="bb169-108">Name</span></span></th>
<th><span data-ttu-id="bb169-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb169-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-111"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span><span class="sxs-lookup"><span data-stu-id="bb169-111"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span></span></td>
<td><span data-ttu-id="bb169-112">Ottiene o imposta il percorso di file system relativo o assoluto di una cartella in cui il ripristino dell'arresto anomalo o un'operazione di ripristino è in grado di individuare i database a cui si fa riferimento nel log delle transazioni nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="bb169-112">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-114"><a href="dn350972(v=exchg.10).md">BaseName</a></span><span class="sxs-lookup"><span data-stu-id="bb169-114"><a href="dn350972(v=exchg.10).md">BaseName</a></span></span></td>
<td><span data-ttu-id="bb169-115">Ottiene o imposta il prefisso di tre lettere utilizzato per molti dei file utilizzati dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="bb169-115">Gets or sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="bb169-116">Il file del checkpoint, ad esempio, è denominato EDB. CHK per impostazione predefinita, perché EDB è il nome di base predefinito.</span><span class="sxs-lookup"><span data-stu-id="bb169-116">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-118"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span><span class="sxs-lookup"><span data-stu-id="bb169-118"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="bb169-119">Ottiene o imposta un valore che indica il numero di risorse dell'albero B + memorizzato nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bb169-119">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="bb169-120">I valori di grandi dimensioni per questo parametro comportano l'utilizzo di una maggiore quantità di memoria da parte del motore di database, ma aumentano la velocità con cui l'applicazione può aprire in modo casuale un numero elevato di tabelle.</span><span class="sxs-lookup"><span data-stu-id="bb169-120">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="bb169-121">Questa operazione è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle.</span><span class="sxs-lookup"><span data-stu-id="bb169-121">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="bb169-122">Supportato in Windows Vista e in alto.</span><span class="sxs-lookup"><span data-stu-id="bb169-122">Supported on Windows Vista and up.</span></span> <span data-ttu-id="bb169-123">Ignorato in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb169-123">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-125"><a href="dn350974(v=exchg.10).md">CachePriority</a></span><span class="sxs-lookup"><span data-stu-id="bb169-125"><a href="dn350974(v=exchg.10).md">CachePriority</a></span></span></td>
<td><span data-ttu-id="bb169-126">Ottiene o imposta la proprietà per istanza per le priorità della cache relativa (impostazione predefinita = 100).</span><span class="sxs-lookup"><span data-stu-id="bb169-126">Gets or sets the per-instance property for relative cache priorities (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-128"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span><span class="sxs-lookup"><span data-stu-id="bb169-128"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span></span></td>
<td><span data-ttu-id="bb169-129">Ottiene o imposta la soglia in byte per informazioni sul numero di file di log delle transazioni che dovranno essere riprodotti dopo un arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="bb169-129">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="bb169-130">Se la registrazione circolare è abilitata usando CircularLog, questo parametro controllerà anche la quantità approssimativa di file di log delle transazioni che verranno conservati su disco.</span><span class="sxs-lookup"><span data-stu-id="bb169-130">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-132"><a href="dn350977(v=exchg.10).md">CircularLog</a></span><span class="sxs-lookup"><span data-stu-id="bb169-132"><a href="dn350977(v=exchg.10).md">CircularLog</a></span></span></td>
<td><span data-ttu-id="bb169-133">Ottiene o imposta un valore che indica se la registrazione circolare è attiva.</span><span class="sxs-lookup"><span data-stu-id="bb169-133">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="bb169-134">Quando la registrazione circolare è disattivata, tutti i file di log delle transazioni generati vengono conservati su disco fino a quando non sono più necessari perché è stato eseguito un backup completo del database.</span><span class="sxs-lookup"><span data-stu-id="bb169-134">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="bb169-135">Quando la registrazione circolare è attiva, solo i file di log delle transazioni più piccoli rispetto al checkpoint corrente vengono conservati su disco.</span><span class="sxs-lookup"><span data-stu-id="bb169-135">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="bb169-136">Il vantaggio di questa modalità è che non è necessario che i backup ritirino i vecchi file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="bb169-136">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-138"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span><span class="sxs-lookup"><span data-stu-id="bb169-138"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span></span></td>
<td><span data-ttu-id="bb169-139">Ottiene o imposta un valore che indica se JetInit ha esito negativo quando il motore di database è configurato per iniziare a utilizzare i file di log delle transazioni su disco con dimensioni diverse da quelle configurate.</span><span class="sxs-lookup"><span data-stu-id="bb169-139">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="bb169-140">In genere, <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> recupererà correttamente i database, ma avrà esito negativo con <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> per indicare che le dimensioni del file di log non sono configurate correttamente.</span><span class="sxs-lookup"><span data-stu-id="bb169-140">Normally, <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> will successfully recover the databases but will fail with <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="bb169-141">Tuttavia, quando questo parametro è impostato su true, il motore di database eliminerà automaticamente tutti i vecchi file di log, avviando un nuovo set di file di log delle transazioni usando le dimensioni del file di log configurate.</span><span class="sxs-lookup"><span data-stu-id="bb169-141">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="bb169-142">Questo parametro è utile quando l'applicazione desidera modificare in modo trasparente le dimensioni del file del log delle transazioni, ma continua a funzionare in modo trasparente negli scenari di aggiornamento e ripristino.</span><span class="sxs-lookup"><span data-stu-id="bb169-142">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-144"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span><span class="sxs-lookup"><span data-stu-id="bb169-144"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span></span></td>
<td><span data-ttu-id="bb169-145">Ottiene o imposta un valore che indica se ESENT creerà automaticamente le cartelle mancanti nei percorsi del file System.</span><span class="sxs-lookup"><span data-stu-id="bb169-145">Gets or sets a value indicating whether ESENT will silently create folders that are missing in its filesystem paths.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-147"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span><span class="sxs-lookup"><span data-stu-id="bb169-147"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span></span></td>
<td><span data-ttu-id="bb169-148">Ottiene o imposta il numero di pagine aggiunte a un file di database ogni volta che è necessario aumentare per contenere più dati.</span><span class="sxs-lookup"><span data-stu-id="bb169-148">Gets or sets the number of pages that are added to a database file each time it needs to grow to accommodate more data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-150"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span><span class="sxs-lookup"><span data-stu-id="bb169-150"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span></span></td>
<td><span data-ttu-id="bb169-151">Ottiene o imposta l'intervallo massimo consentito per il completamento dell'analisi del database, in secondi.</span><span class="sxs-lookup"><span data-stu-id="bb169-151">Gets or sets the maximum interval to allow the database scan to finish, in seconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-153"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span><span class="sxs-lookup"><span data-stu-id="bb169-153"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span></span></td>
<td><span data-ttu-id="bb169-154">Ottiene o imposta l'intervallo minimo per la ripetizione dell'analisi del database, in secondi.</span><span class="sxs-lookup"><span data-stu-id="bb169-154">Gets or sets the minimum interval to repeat the database scan, in seconds.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-156"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span><span class="sxs-lookup"><span data-stu-id="bb169-156"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span></span></td>
<td><span data-ttu-id="bb169-157">Ottiene o imposta la limitazione dell'analisi del database, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="bb169-157">Gets or sets the throttling of the database scan, in milliseconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-159"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span><span class="sxs-lookup"><span data-stu-id="bb169-159"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span></span></td>
<td><span data-ttu-id="bb169-160">Ottiene o imposta un valore che indica se è necessario eseguire la manutenzione del database durante il ripristino.</span><span class="sxs-lookup"><span data-stu-id="bb169-160">Gets or sets a value indicating whether Database Maintenance should run during recovery.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-162"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span><span class="sxs-lookup"><span data-stu-id="bb169-162"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span></span></td>
<td><span data-ttu-id="bb169-163">Ottiene o imposta un valore che indica se la serializzazione della manutenzione del database è abilitata per i database che condividono lo stesso disco.</span><span class="sxs-lookup"><span data-stu-id="bb169-163">Gets or sets a value indicating whether database Maintenance serialization is enabled for databases sharing the same disk.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-165"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span><span class="sxs-lookup"><span data-stu-id="bb169-165"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span></span></td>
<td><span data-ttu-id="bb169-166">Ottiene o imposta un valore che indica se <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a> verificherà la presenza di indici compilati utilizzando una versione precedente della libreria NLS nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bb169-166">Gets or sets a value indicating whether <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a> will check for indexes that were build using an older version of the NLS library in the operating system.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-168"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span><span class="sxs-lookup"><span data-stu-id="bb169-168"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span></span></td>
<td><span data-ttu-id="bb169-169">Ottiene o imposta un valore che indica se la deframmentazione in linea è abilitata.</span><span class="sxs-lookup"><span data-stu-id="bb169-169">Gets or sets a value indicating whether online defragmentation is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span><span class="sxs-lookup"><span data-stu-id="bb169-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span></span></td>
<td><span data-ttu-id="bb169-172">Ottiene o imposta una stringa specifica dell'applicazione che verrà aggiunta a qualsiasi messaggio del registro eventi emesso dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="bb169-172">Gets or sets an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="bb169-173">In questo modo è possibile correlare facilmente i messaggi del log eventi con l'applicazione di origine.</span><span class="sxs-lookup"><span data-stu-id="bb169-173">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="bb169-174">Per impostazione predefinita, verrà usato il nome dell'eseguibile dell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="bb169-174">By default the host application executable name will be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-176"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span><span class="sxs-lookup"><span data-stu-id="bb169-176"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span></span></td>
<td><span data-ttu-id="bb169-177">Ottiene o imposta il nome del registro eventi utilizzato dal motore di database per i messaggi del log eventi.</span><span class="sxs-lookup"><span data-stu-id="bb169-177">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="bb169-178">Per impostazione predefinita, tutti i messaggi del registro eventi vengono inviati al registro eventi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bb169-178">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="bb169-179">Se viene configurato il nome della chiave del registro di sistema per un altro log eventi, i messaggi del registro eventi verranno invece inseriti.</span><span class="sxs-lookup"><span data-stu-id="bb169-179">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-181"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span><span class="sxs-lookup"><span data-stu-id="bb169-181"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span></span></td>
<td><span data-ttu-id="bb169-182">Ottiene o imposta la quantità di memoria utilizzata per memorizzare nella cache i record del log prima che vengano scritti nel file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="bb169-182">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="bb169-183">L'unità per questo parametro è la dimensione settoriale del volume che include i file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="bb169-183">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="bb169-184">La dimensione del settore è quasi sempre di 512 byte, quindi è sicuro presupporre che le dimensioni dell'unità.</span><span class="sxs-lookup"><span data-stu-id="bb169-184">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="bb169-185">Questo parametro ha un effetto sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="bb169-185">This parameter has an impact on performance.</span></span> <span data-ttu-id="bb169-186">Quando il motore di database è sottoposto a un carico di aggiornamento intenso, questo buffer può essere pieno molto rapidamente.</span><span class="sxs-lookup"><span data-stu-id="bb169-186">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="bb169-187">Una dimensione della cache maggiore per il file di log delle transazioni è essenziale per le prestazioni di aggiornamento ottimali in una condizione di carico elevato.</span><span class="sxs-lookup"><span data-stu-id="bb169-187">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="bb169-188">Il valore predefinito è troppo piccolo per questo caso.</span><span class="sxs-lookup"><span data-stu-id="bb169-188">The default is known to be too small for this case.</span></span> <span data-ttu-id="bb169-189">Non impostare questo parametro su un numero di buffer maggiore (in byte) della metà delle dimensioni di un file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="bb169-189">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-191"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span><span class="sxs-lookup"><span data-stu-id="bb169-191"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span></span></td>
<td><span data-ttu-id="bb169-192">Ottiene o imposta il percorso di file system relativo o assoluto della cartella che conterrà i log delle transazioni per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="bb169-192">Gets or sets the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span><span class="sxs-lookup"><span data-stu-id="bb169-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span></span></td>
<td><span data-ttu-id="bb169-195">Ottiene o imposta le dimensioni dei file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="bb169-195">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="bb169-196">Questo parametro deve essere impostato in unità di 1024 byte (ad esempio, un'impostazione di 2048 fornirà 2MB di logfile).</span><span class="sxs-lookup"><span data-stu-id="bb169-196">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-198"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span><span class="sxs-lookup"><span data-stu-id="bb169-198"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span></span></td>
<td><span data-ttu-id="bb169-199">Ottiene o imposta il numero di risorse del cursore riservate per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="bb169-199">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="bb169-200">Una risorsa di cursore corrisponde direttamente a una JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="bb169-200">A cursor resource directly corresponds to a JET_TABLEID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-202"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span><span class="sxs-lookup"><span data-stu-id="bb169-202"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span></span></td>
<td><span data-ttu-id="bb169-203">Ottiene o imposta il numero di risorse dell'albero B + riservate per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="bb169-203">Gets or sets the number of B+ Tree resources reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span><span class="sxs-lookup"><span data-stu-id="bb169-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span></span></td>
<td><span data-ttu-id="bb169-206">Ottiene o imposta il numero di risorse delle sessioni riservate per questa istanza.</span><span class="sxs-lookup"><span data-stu-id="bb169-206">Gets or sets the number of sessions resources reserved for this instance.</span></span> <span data-ttu-id="bb169-207">Una risorsa di sessione corrisponde direttamente a una JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="bb169-207">A session resource directly corresponds to a JET_SESID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-209"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span><span class="sxs-lookup"><span data-stu-id="bb169-209"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span></span></td>
<td><span data-ttu-id="bb169-210">Ottiene o imposta il numero di risorse della tabella temporanea utilizzate da un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="bb169-210">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="bb169-211">Questa impostazione influirà sul numero di tabelle temporanee che possono essere usate contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="bb169-211">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="bb169-212">Se questo parametro di sistema è impostato su zero, non verrà creato alcun database temporaneo e le attività che richiedono l'utilizzo del database temporaneo avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="bb169-212">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="bb169-213">Questa impostazione può essere utile per evitare l'i/O necessario per creare il database temporaneo se è noto che non verrà utilizzato.</span><span class="sxs-lookup"><span data-stu-id="bb169-213">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-215"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span><span class="sxs-lookup"><span data-stu-id="bb169-215"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span></span></td>
<td><span data-ttu-id="bb169-216">Ottiene o imposta la percentuale di archivio versioni che può essere utilizzata dalla transazione meno recente prima di <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (impostazione predefinita = 100).</span><span class="sxs-lookup"><span data-stu-id="bb169-216">Gets or sets the percentage of version store that can be used by oldest transaction before <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span><span class="sxs-lookup"><span data-stu-id="bb169-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span></span></td>
<td><span data-ttu-id="bb169-219">Ottiene o imposta il numero massimo di pagine dell'archivio versioni riservate per questa istanza.</span><span class="sxs-lookup"><span data-stu-id="bb169-219">Gets or sets the maximum number of version store pages reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-221"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span><span class="sxs-lookup"><span data-stu-id="bb169-221"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span></span></td>
<td><span data-ttu-id="bb169-222">Ottiene o imposta un valore che indica se i messaggi di registro eventi informativi che verrebbero normalmente generati dal motore di database verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="bb169-222">Gets or sets a value indicating whether informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-224"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span><span class="sxs-lookup"><span data-stu-id="bb169-224"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span></span></td>
<td><span data-ttu-id="bb169-225">Ottiene o imposta un valore che indica se è consentito l'apertura di un solo database tramite JetOpenDatabase da una sessione specificata.</span><span class="sxs-lookup"><span data-stu-id="bb169-225">Gets or sets a value indicating whether only one database is allowed to be opened using JetOpenDatabase by a given session at one time.</span></span> <span data-ttu-id="bb169-226">Il database temporaneo è escluso da questa restrizione.</span><span class="sxs-lookup"><span data-stu-id="bb169-226">The temporary database is excluded from this restriction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-228"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span><span class="sxs-lookup"><span data-stu-id="bb169-228"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span></span></td>
<td><span data-ttu-id="bb169-229">Ottiene o imposta le dimensioni iniziali del database temporaneo.</span><span class="sxs-lookup"><span data-stu-id="bb169-229">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="bb169-230">Le dimensioni sono le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="bb169-230">The size is in database pages.</span></span> <span data-ttu-id="bb169-231">Una dimensione pari a zero indica che devono essere utilizzate le dimensioni predefinite di un database normale.</span><span class="sxs-lookup"><span data-stu-id="bb169-231">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="bb169-232">È spesso consigliabile che le piccole applicazioni configurino il database temporaneo in modo che sia il più piccolo possibile.</span><span class="sxs-lookup"><span data-stu-id="bb169-232">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="bb169-233">L'impostazione di questo parametro su <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> consente di ottenere il database temporaneo più piccolo possibile.</span><span class="sxs-lookup"><span data-stu-id="bb169-233">Setting this parameter to <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> will achieve the smallest temporary database possible.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-235"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span><span class="sxs-lookup"><span data-stu-id="bb169-235"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span></span></td>
<td><span data-ttu-id="bb169-236">Ottiene o imposta il numero preferito di pagine dell'archivio versioni riservate per questa istanza.</span><span class="sxs-lookup"><span data-stu-id="bb169-236">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="bb169-237">Se la dimensione dell'archivio versioni supera questa soglia, le informazioni utilizzate solo per le attività in background facoltative, ad esempio il ripristino dello spazio eliminato nel database, vengono invece sacrificate per mantenere la stanza per le informazioni transazionali.</span><span class="sxs-lookup"><span data-stu-id="bb169-237">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-239"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span><span class="sxs-lookup"><span data-stu-id="bb169-239"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span></span></td>
<td><span data-ttu-id="bb169-240">Ottiene o imposta il numero massimo di operazioni di I/O inviate per uno scopo specifico.</span><span class="sxs-lookup"><span data-stu-id="bb169-240">Gets or sets the maximum number of I/O operations dispatched for a given purpose.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-242"><a href="dn350981(v=exchg.10).md">Ripristino</a></span><span class="sxs-lookup"><span data-stu-id="bb169-242"><a href="dn350981(v=exchg.10).md">Recovery</a></span></span></td>
<td><span data-ttu-id="bb169-243">Ottiene o imposta un valore che indica se il ripristino dell'arresto anomalo è impostato su on.</span><span class="sxs-lookup"><span data-stu-id="bb169-243">Gets or sets a value indicating whether crash recovery is on.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-245"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span><span class="sxs-lookup"><span data-stu-id="bb169-245"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span></span></td>
<td><span data-ttu-id="bb169-246">Ottiene o imposta il percorso file system relativo o assoluto della cartella che conterrà il file del checkpoint per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="bb169-246">Gets or sets the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span><span class="sxs-lookup"><span data-stu-id="bb169-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span></span></td>
<td><span data-ttu-id="bb169-249">Ottiene o imposta il percorso di file system relativo o assoluto della cartella che conterrà il database temporaneo per l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="bb169-249">Gets or sets the relative or absolute file system path of the folder that will contain the temporary database for the instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-251"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span><span class="sxs-lookup"><span data-stu-id="bb169-251"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span></span></td>
<td><span data-ttu-id="bb169-252">Ottiene o imposta il numero di elementi di lavoro di pulitura in background che possono essere accodati al pool di thread del motore di database in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="bb169-252">Gets or sets the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="bb169-254"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span><span class="sxs-lookup"><span data-stu-id="bb169-254"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span></span></td>
<td><span data-ttu-id="bb169-255">Ottiene o imposta il numero di registri per i quali ESENT rinvia gli scaricamenti del database.</span><span class="sxs-lookup"><span data-stu-id="bb169-255">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="bb169-256">Questa operazione può essere utilizzata per aumentare la recuperabilità del database se gli errori determinano la perdita di file di registro.</span><span class="sxs-lookup"><span data-stu-id="bb169-256">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="bb169-257">Supportato su Windows 7 e su.</span><span class="sxs-lookup"><span data-stu-id="bb169-257">Supported on Windows 7 and up.</span></span> <span data-ttu-id="bb169-258">Ignorato in Windows XP, Windows Server 2003, Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="bb169-258">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bb169-259">Inizio</span><span class="sxs-lookup"><span data-stu-id="bb169-259">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="bb169-260">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb169-260">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bb169-261">Riferimento</span><span class="sxs-lookup"><span data-stu-id="bb169-261">Reference</span></span>

[<span data-ttu-id="bb169-262">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="bb169-262">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="bb169-263">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="bb169-263">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
