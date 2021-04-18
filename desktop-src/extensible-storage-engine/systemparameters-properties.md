---
description: 'Altre informazioni su: Proprietà SystemParameters'
title: Proprietà SystemParameters
TOCTitle: SystemParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55104035
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 12e18b6c045758c8e9fd7ffb91f728c78dcf2e24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561395"
---
# <a name="systemparameters-properties"></a><span data-ttu-id="ec7d5-103">Proprietà SystemParameters</span><span class="sxs-lookup"><span data-stu-id="ec7d5-103">SystemParameters properties</span></span>

<span data-ttu-id="ec7d5-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="ec7d5-104">Include protected members</span></span>  
<span data-ttu-id="ec7d5-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="ec7d5-105">Include inherited members</span></span>  

<span data-ttu-id="ec7d5-106">Il tipo [SystemParameters](./systemparameters-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-106">The [SystemParameters](./systemparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="ec7d5-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ec7d5-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ec7d5-108">Nome</span><span class="sxs-lookup"><span data-stu-id="ec7d5-108">Name</span></span></th>
<th><span data-ttu-id="ec7d5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec7d5-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-112"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-112"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span></span></td>
<td><span data-ttu-id="ec7d5-113">Ottiene la dimensione massima di un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-113">Gets the maximum size of a bookmark.</span></span> <span data-ttu-id="ec7d5-114"><a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-114"><a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-117"><a href="dn351214(v=exchg.10).md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-117"><a href="dn351214(v=exchg.10).md">CacheSize</a></span></span></td>
<td><span data-ttu-id="ec7d5-118">Ottiene o imposta le dimensioni della cache del database in pagine.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-118">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="ec7d5-119">Per impostazione predefinita, le dimensioni della cache del database vengono ottimizzate automaticamente, impostando questa proprietà su un valore diverso da zero, la cache verrà adattata alle dimensioni di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-119">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-122"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-122"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span></span></td>
<td><span data-ttu-id="ec7d5-123">Ottiene o imposta la dimensione massima della cache delle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-123">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="ec7d5-124">Le dimensioni sono le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-124">The size is in database pages.</span></span> <span data-ttu-id="ec7d5-125">Se questo parametro viene lasciato al valore predefinito, le dimensioni massime della cache verranno impostate sulle dimensioni della memoria fisica quando viene chiamato JetInit.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-125">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-128"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-128"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span></span></td>
<td><span data-ttu-id="ec7d5-129">Ottiene o imposta le dimensioni minime della cache delle pagine del database, nelle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-129">Gets or sets the minimum size of the database page cache, in database pages.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-132"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-132"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span></span></td>
<td><span data-ttu-id="ec7d5-133">Ottiene il numero massimo di componenti in una chiave di ordinamento o di indice.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-133">Gets the maximum number of components in a sort or index key.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-136"><a href="dn351218(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-136"><a href="dn351218(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="ec7d5-137">Ottiene o imposta un valore che specifica i valori predefiniti per l'intero set di parametri di sistema.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-137">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="ec7d5-138">Quando questo parametro è impostato su una configurazione specifica, tutti i valori dei parametri di sistema vengono reimpostati sui valori predefiniti per tale configurazione.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-138">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="ec7d5-139">Se la configurazione è impostata per un'istanza specifica, i parametri di sistema globali non verranno reimpostati sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-139">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="ec7d5-140">Small Configuration (0): il motore di database è ottimizzato per l'uso della memoria.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-140">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="ec7d5-141">Configurazione legacy (1): il motore di database presenta le impostazioni predefinite tradizionali.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-141">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="ec7d5-142">Supportato in Windows Vista e in alto.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-142">Supported on Windows Vista and up.</span></span> <span data-ttu-id="ec7d5-143">Ignorato in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-143">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-146"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-146"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span></span></td>
<td><span data-ttu-id="ec7d5-147">Ottiene o imposta le dimensioni in byte delle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-147">Gets or sets the size of the database pages, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-150"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-150"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="ec7d5-151">Ottiene o imposta un valore che indica se il motore di database accetta o rifiuta le modifiche apportate a un subset dei parametri di sistema.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-151">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="ec7d5-152">Questo parametro viene usato in combinazione con la <a href="dn351218(v=exchg.10).md">configurazione</a> per impedire che alcuni parametri di sistema vengano impostati dalle impostazioni predefinite della configurazione selezionata.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-152">This parameter is used in conjunction with <a href="dn351218(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="ec7d5-153">Supportato in Windows Vista e in alto.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-153">Supported on Windows Vista and up.</span></span> <span data-ttu-id="ec7d5-154">Ignorato in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-154">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-157"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-157"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="ec7d5-158">Ottiene o imposta un valore che indica se il motore di database deve utilizzare la cache dei file del sistema operativo per tutti i file gestiti.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-158">Gets or sets a value indicating whether the database engine should use the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-161"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-161"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="ec7d5-162">Ottiene o imposta un valore che indica se il motore di database deve utilizzare l'I/O di file mappato alla memoria per i file di database.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-162">Gets or sets a value indicating whether the database engine should use memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-165"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-165"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span></span></td>
<td><span data-ttu-id="ec7d5-166">Ottiene o imposta il livello di dettaglio dei messaggi EventLog emessi al log eventi dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-166">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="ec7d5-167">I numeri più alti comporteranno messaggi EventLog più dettagliati.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-167">Higher numbers will result in more detailed eventlog messages.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-170"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-170"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span></span></td>
<td><span data-ttu-id="ec7d5-171">Ottiene o imposta la codifica dei valori da eseguire con le eccezioni generate all'interno di JET.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-171">Gets or sets the value encoding what to do with exceptions generated within JET.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-174"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-174"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span></span></td>
<td><span data-ttu-id="ec7d5-175">Ottiene o imposta il set di azioni da intraprendere su IOs che appaiono sospese.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-175">Gets or sets the set of actions to be taken on IOs that appear hung.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-178"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-178"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span></span></td>
<td><span data-ttu-id="ec7d5-179">Ottiene o imposta la soglia per le operazioni di i/o sospese su cui si deve agire.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-179">Gets or sets the threshold for what is considered a hung IO that should be acted upon.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-182"><a href="dn351156(v=exchg.10).md">Per la maggior parte</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-182"><a href="dn351156(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="ec7d5-183">Ottiene le dimensioni massime della chiave.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-183">Gets the maximum key size.</span></span> <span data-ttu-id="ec7d5-184">Questo dipende dalla versione di ESENT e dalle dimensioni della pagina del database.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-184">This depends on the Esent version and database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-187"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-187"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="ec7d5-188">Ottiene o imposta la compatibilità con le versioni precedenti con le convenzioni di denominazione dei file delle versioni precedenti del motore di database.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-188">Gets or sets backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-191"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-191"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span></span></td>
<td><span data-ttu-id="ec7d5-192">Ottiene le dimensioni dei blocchi LV.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-192">Gets the lv chunks size.</span></span> <span data-ttu-id="ec7d5-193">Dipende dalle dimensioni della pagina del database.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-193">This depends on the database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-196"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-196"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span></span></td>
<td><span data-ttu-id="ec7d5-197">Ottiene o imposta il numero massimo di istanze che è possibile creare.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-197">Gets or sets the maximum number of instances that can be created.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-200"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-200"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span></span></td>
<td><span data-ttu-id="ec7d5-201">Ottiene o imposta la quantità minima di dati che devono essere compressi con la compressione Xpress.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-201">Gets or sets the smallest amount of data that should be compressed with xpress compression.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-204"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-204"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span></span></td>
<td><span data-ttu-id="ec7d5-205">Questo parametro controlla il numero di I/o di file di database che possono essere accodati per singolo disco nel sistema operativo host alla volta.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-205">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="ec7d5-206">Un valore più elevato per questo parametro può migliorare significativamente le prestazioni di un'applicazione di database di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-206">A larger value for this parameter can significantly help the performance of a large database application.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-209"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-209"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span></span></td>
<td><span data-ttu-id="ec7d5-210">Ottiene o imposta il nome descrittivo per questa istanza del processo.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-210">Gets or sets the friendly name for this instance of the process.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-213"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-213"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span></span></td>
<td><span data-ttu-id="ec7d5-214">Ottiene o imposta la soglia in corrispondenza della quale la cache delle pagine del database inizia a rimuovere le pagine dalla cache per creare spazio per le pagine che non sono memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-214">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="ec7d5-215">Quando il numero di buffer di pagina nella cache scende al di sotto di questa soglia, viene avviato un processo in background per ripristinare il pool di buffer disponibili.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-215">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="ec7d5-216">Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-216">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="ec7d5-217">Anche questa soglia deve essere sempre inferiore alla soglia di arresto impostata dal JET_paramStopFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-217">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="ec7d5-218">L'altezza della distanza della soglia iniziale determina il tempo di risposta che la cache delle pagine del database deve avere per produrre i buffer disponibili prima che siano necessari per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-218">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="ec7d5-219">Una soglia di inizio elevata offrirà al processo in background più tempo per rispondere.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-219">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="ec7d5-220">Tuttavia, una soglia di avvio elevata implica una soglia di arresto superiore e che ridurrà le dimensioni effettive della cache delle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-220">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="ec7d5-223"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="ec7d5-223"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span></span></td>
<td><span data-ttu-id="ec7d5-224">Ottiene o imposta la soglia in corrispondenza della quale la cache delle pagine del database smette di rimuovere le pagine dalla cache per creare spazio per le pagine non memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-224">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="ec7d5-225">Quando il numero di buffer di pagina nella cache supera questa soglia, il processo in background che è stato avviato per ripristinare il pool di buffer disponibili viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-225">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="ec7d5-226">Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-226">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="ec7d5-227">Anche questa soglia deve essere sempre maggiore della soglia iniziale impostata da JET_paramStartFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-227">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="ec7d5-228">La distanza tra la soglia iniziale e la soglia di arresto influiscono sull'efficienza con cui le pagine del database vengono scaricate dal processo in background.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-228">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="ec7d5-229">Un gap maggiore renderà più probabile che le Scritture nelle pagine adiacenti vengano combinate.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-229">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="ec7d5-230">Tuttavia, una soglia di arresto elevata ridurrà le dimensioni effettive della cache delle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="ec7d5-230">However, a high stop threshold will reduce the effective size of the database page cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec7d5-231">Inizio</span><span class="sxs-lookup"><span data-stu-id="ec7d5-231">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ec7d5-232">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec7d5-232">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ec7d5-233">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ec7d5-233">Reference</span></span>

[<span data-ttu-id="ec7d5-234">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="ec7d5-234">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="ec7d5-235">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ec7d5-235">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
