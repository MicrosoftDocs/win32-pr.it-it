---
description: 'Altre informazioni su: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313139"
---
# <a name="jet_errcat"></a><span data-ttu-id="6603d-103">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="6603d-103">JET_ERRCAT</span></span>


<span data-ttu-id="6603d-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6603d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errcat"></a><span data-ttu-id="6603d-105">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="6603d-105">JET_ERRCAT</span></span>

<span data-ttu-id="6603d-106">Il gruppo **JET_ERRCAT** di costanti descrive le classificazioni di livello superiore o le categorie di errori.</span><span class="sxs-lookup"><span data-stu-id="6603d-106">The **JET_ERRCAT** group of constants describes higher-level classifications or categories of errors.</span></span> <span data-ttu-id="6603d-107">Questo gruppo di costanti consente alle applicazioni di definire il trattamento predefinito per una classificazione degli errori, anziché gestire singolarmente ogni caso di errore.</span><span class="sxs-lookup"><span data-stu-id="6603d-107">This group of constants enables applications to define default treatment for a classification of errors, rather than handling each error case individually.</span></span> <span data-ttu-id="6603d-108">Garantisce inoltre che non sia necessario che l'applicazione gestisca le nuove condizioni di errore incluse nelle classificazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="6603d-108">It also ensures that the application does not have to handle new error conditions that are included in existing classifications.</span></span>

<span data-ttu-id="6603d-109">Nota: questa documentazione si basa su una versione preliminare del motore di archiviazione estendibile.</span><span class="sxs-lookup"><span data-stu-id="6603d-109">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="6603d-110">Queste informazioni sono soggette a modifiche.</span><span class="sxs-lookup"><span data-stu-id="6603d-110">This information is subject to change.</span></span>

<span data-ttu-id="6603d-111">Le costanti **JET_ERRCAT** sono disposte in una gerarchia specifica di condizioni e sottocondizioni, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6603d-111">The **JET_ERRCAT** constants are arranged in a specific hierarchy of conditions and subconditions, as follows:</span></span>

<span data-ttu-id="6603d-112">|---Error |---Operation (al) | |---Fatal | |---IO | |---Resource | |---Memory | |---quota | |---disco | |---dati | |---danneggiamento | |---incoerente | |---frammentazione | |---API |---utilizzo |---stato</span><span class="sxs-lookup"><span data-stu-id="6603d-112">|--- Error |--- Operation(al) | |--- Fatal | |--- IO | |--- Resource | |--- Memory | |--- Quota | |--- Disk | |--- Data | |--- Corruption | |--- Inconsistent | |--- Fragmentation | |--- Api |--- Usage |--- State</span></span>

<span data-ttu-id="6603d-113">Nella tabella seguente sono elencate le costanti **JET_ERRCAT** e vengono fornite una descrizione e informazioni di ripristino, come applicabile.</span><span class="sxs-lookup"><span data-stu-id="6603d-113">The following table lists the **JET_ERRCAT** constants and provides a description and recovery information, as applicable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6603d-114">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="6603d-114">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="6603d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6603d-115">Description</span></span></p></th>
<th><p><span data-ttu-id="6603d-116">Ripristino</span><span class="sxs-lookup"><span data-stu-id="6603d-116">Recovery</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6603d-117">JET_errcatUnknown 0</span><span class="sxs-lookup"><span data-stu-id="6603d-117">JET_errcatUnknown 0</span></span></p></td>
<td><p><span data-ttu-id="6603d-118">Categoria di errore non valida.</span><span class="sxs-lookup"><span data-stu-id="6603d-118">An invalid error category.</span></span></p></td>
<td><p><span data-ttu-id="6603d-119">N/D.</span><span class="sxs-lookup"><span data-stu-id="6603d-119">N/A.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6603d-120">JET_errcatError 1</span><span class="sxs-lookup"><span data-stu-id="6603d-120">JET_errcatError 1</span></span></p></td>
<td><p><span data-ttu-id="6603d-121">Categoria di primo livello (nessun errore deve essere di questa classe).</span><span class="sxs-lookup"><span data-stu-id="6603d-121">The top level category (no errors should be of this class).</span></span></p></td>
<td><p><span data-ttu-id="6603d-122">Vedere le costanti di errore specifiche.</span><span class="sxs-lookup"><span data-stu-id="6603d-122">See the specific error constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6603d-123">JET_errcatOperation 2</span><span class="sxs-lookup"><span data-stu-id="6603d-123">JET_errcatOperation 2</span></span></p></td>
<td><p><span data-ttu-id="6603d-124">Rappresenta gli errori che possono verificarsi in qualsiasi momento a causa di condizioni incontrollabili e sono spesso temporanei.</span><span class="sxs-lookup"><span data-stu-id="6603d-124">Represents errors that can happen at any time due to uncontrollable conditions and are often temporary.</span></span> <span data-ttu-id="6603d-125">Se specificato, vedere le sottocategorie.</span><span class="sxs-lookup"><span data-stu-id="6603d-125">See subcategories if specified.</span></span></p></td>
<td><p><span data-ttu-id="6603d-126">Riprovare e, se l'errore persiste, informare l'operatore.</span><span class="sxs-lookup"><span data-stu-id="6603d-126">Retry and if the error continues, inform the operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6603d-127">JET_errcatFatal 3</span><span class="sxs-lookup"><span data-stu-id="6603d-127">JET_errcatFatal 3</span></span></p></td>
<td><p><span data-ttu-id="6603d-128">Rappresenta gli errori irreversibili che, quando si verificano, creano un rischio che ESE non possa continuare in modo sicuro (spesso transazionale) e i dati potrebbero essere danneggiati.</span><span class="sxs-lookup"><span data-stu-id="6603d-128">Represents fatal errors that, when they occur, create a risk that ESE cannot continue in a safe (often transactional) way, and data may become corrupted.</span></span></p></td>
<td><p><span data-ttu-id="6603d-129">Riavviare l'istanza o il processo.</span><span class="sxs-lookup"><span data-stu-id="6603d-129">Restart the instance or process.</span></span> <span data-ttu-id="6603d-130">Se il problema persiste, informare l'operatore.</span><span class="sxs-lookup"><span data-stu-id="6603d-130">If the problem persists, inform the operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6603d-131">JET_errcatIO 4</span><span class="sxs-lookup"><span data-stu-id="6603d-131">JET_errcatIO 4</span></span></p></td>
<td><p><span data-ttu-id="6603d-132">Rappresenta gli errori di i/o, provenienti dal sistema operativo, e sono fuori dal controllo ESE.</span><span class="sxs-lookup"><span data-stu-id="6603d-132">Represents IO errors, which come from the operating system, and are out of ESE's control.</span></span> <span data-ttu-id="6603d-133">Questo tipo di errore può essere temporaneo.</span><span class="sxs-lookup"><span data-stu-id="6603d-133">This type of error may be temporary.</span></span></p></td>
<td><p><span data-ttu-id="6603d-134">Riprovare. se l'errore persiste, richiedere all'operatore di controllare il disco.</span><span class="sxs-lookup"><span data-stu-id="6603d-134">Retry, and if the error continues, ask the operator to check the disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6603d-135">JET_errcatResource 5</span><span class="sxs-lookup"><span data-stu-id="6603d-135">JET_errcatResource 5</span></span></p></td>
<td><p><span data-ttu-id="6603d-136">Rappresenta una categoria di errori correlati a condizioni di risorse insufficienti.</span><span class="sxs-lookup"><span data-stu-id="6603d-136">Represents a category of errors related to lack of resource conditions.</span></span></p></td>
<td><p><span data-ttu-id="6603d-137">Vedere le sottocategorie.</span><span class="sxs-lookup"><span data-stu-id="6603d-137">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6603d-138">JET_errcatMemory 6</span><span class="sxs-lookup"><span data-stu-id="6603d-138">JET_errcatMemory 6</span></span></p></td>
<td><p><span data-ttu-id="6603d-139">Rappresenta un errore causato dalla mancanza di memoria.</span><span class="sxs-lookup"><span data-stu-id="6603d-139">Represents an error caused by lack of memory.</span></span></p></td>
<td><p><span data-ttu-id="6603d-140">Riprovare dopo un periodo di tempo, liberare memoria o uscire.</span><span class="sxs-lookup"><span data-stu-id="6603d-140">Retry after a period of time, free up memory, or quit.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6603d-141">JET_errcatQuota 7</span><span class="sxs-lookup"><span data-stu-id="6603d-141">JET_errcatQuota 7</span></span></p></td>
<td><p><span data-ttu-id="6603d-142">Alcune &quot; &quot; risorse speciali sono in pool di una determinata dimensione, semplificando il rilevamento delle perdite di queste risorse.</span><span class="sxs-lookup"><span data-stu-id="6603d-142">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span></p></td>
<td><p><span data-ttu-id="6603d-143">L'applicazione deve <strong>dichiarare ()</strong> per rilevare questi problemi durante lo sviluppo.</span><span class="sxs-lookup"><span data-stu-id="6603d-143">The application should <strong>Assert()</strong> to detect these issues during development .</span></span> <span data-ttu-id="6603d-144">Tuttavia, nel codice per la vendita al dettaglio, l'applicazione deve considerarla come un errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="6603d-144">However, in retail code, the application should treat this as a memory error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6603d-145">JET_errcatDisk 8</span><span class="sxs-lookup"><span data-stu-id="6603d-145">JET_errcatDisk 8</span></span></p></td>
<td><p><span data-ttu-id="6603d-146">Rappresenta un errore causato dalla mancanza di spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="6603d-146">Represents an error caused by lack of disk space.</span></span></p></td>
<td><p><span data-ttu-id="6603d-147">Riprovare in seguito per determinare se è disponibile più spazio su disco o richiedere all'operatore di liberare spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="6603d-147">Retry later to determine whether more disk space is available, or ask the operator to free some disk space.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6603d-148">JET_errcatData 9</span><span class="sxs-lookup"><span data-stu-id="6603d-148">JET_errcatData 9</span></span></p></td>
<td><p><span data-ttu-id="6603d-149">Rappresenta una categoria di primo livello per gli errori correlati ai dati.</span><span class="sxs-lookup"><span data-stu-id="6603d-149">Represents a top-level category for errors related to data.</span></span></p></td>
<td><p><span data-ttu-id="6603d-150">Vedere le sottocategorie.</span><span class="sxs-lookup"><span data-stu-id="6603d-150">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6603d-151">JET_errcatCorruption 10</span><span class="sxs-lookup"><span data-stu-id="6603d-151">JET_errcatCorruption 10</span></span></p></td>
<td><p><span data-ttu-id="6603d-152">Rappresenta un problema di danneggiamento, che è spesso permanente senza azioni correttive.</span><span class="sxs-lookup"><span data-stu-id="6603d-152">Represents a corruption issue, which is often permanent without corrective action.</span></span></p></td>
<td><p><span data-ttu-id="6603d-153">Ripristino da backup tramite l'operazione di ripristino delle utilità ESE. questa operazione consente di ripristinare solo i dati a sinistra/con perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="6603d-153">Restore from backup by using the ESE utilities repair operation (this operation restores only the data that is left/lossy).</span></span> <span data-ttu-id="6603d-154">Inoltre, quando si utilizza il metodo Recovery (JetInit), il ripristino può essere eseguito consentendo la perdita di dati. per ulteriori informazioni, vedere <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="6603d-154">Also when the recovery(JetInit) method is used, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6603d-155">JET_errcatInconsistent 11</span><span class="sxs-lookup"><span data-stu-id="6603d-155">JET_errcatInconsistent 11</span></span></p></td>
<td><p><span data-ttu-id="6603d-156">Rappresenta un errore in cui i file di database e/o di log si trovano in uno stato incoerente e non possono essere risolti.</span><span class="sxs-lookup"><span data-stu-id="6603d-156">Represents an error in which the database and/or log files are in a state that is inconsistent and cannot be reconciled.</span></span> <span data-ttu-id="6603d-157">Questo errore potrebbe essere causato da un errore di gestione dell'applicazione o dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="6603d-157">This error might be caused by application/administrator mishandling.</span></span></p></td>
<td><p><span data-ttu-id="6603d-158">Eseguire il ripristino da un backup tramite l'operazione di ripristino delle utilità ESE, che consente di ripristinare solo i dati a sinistra/con perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="6603d-158">Restore from backup by using the ESE utilities repair operation (which only restores the data that is left/lossy).</span></span> <span data-ttu-id="6603d-159">Inoltre, nel caso dell'operazione di <strong>ripristino (JetInit)</strong> , il ripristino può essere eseguito consentendo la perdita di dati. per altre informazioni, vedere <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="6603d-159">Also in the case of the <strong>recovery(JetInit)</strong> operation, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6603d-160">JET_errcatFragmentation 12</span><span class="sxs-lookup"><span data-stu-id="6603d-160">JET_errcatFragmentation 12</span></span></p></td>
<td><p><span data-ttu-id="6603d-161">Rappresenta una classe di errori in cui è stata eseguita una risorsa interna permanente.</span><span class="sxs-lookup"><span data-stu-id="6603d-161">Represents a class of errors in which some persisted internal resource ran out.</span></span></p></td>
<td><p><span data-ttu-id="6603d-162">Per gli errori del database, la deframmentazione non in linea risolverà il problema.</span><span class="sxs-lookup"><span data-stu-id="6603d-162">For database errors, offline defragmentation will fix the problem.</span></span> <span data-ttu-id="6603d-163">Per i file di log, è necessario innanzitutto ripristinare tutti i database collegati a una chiusura normale, quindi eliminare tutti i file di log e il checkpoint.</span><span class="sxs-lookup"><span data-stu-id="6603d-163">For the log files, first recover all attached databases to a clean shutdown, and then delete all the log files and the checkpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6603d-164">JET_errcatApi 13</span><span class="sxs-lookup"><span data-stu-id="6603d-164">JET_errcatApi 13</span></span></p></td>
<td><p><span data-ttu-id="6603d-165">Vedere le sottocategorie.</span><span class="sxs-lookup"><span data-stu-id="6603d-165">See subcategories.</span></span></p></td>
<td><p><span data-ttu-id="6603d-166">Vedere le sottocategorie.</span><span class="sxs-lookup"><span data-stu-id="6603d-166">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6603d-167">JET_errcatUsage 14</span><span class="sxs-lookup"><span data-stu-id="6603d-167">JET_errcatUsage 14</span></span></p></td>
<td><p><span data-ttu-id="6603d-168">Rappresenta un errore di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="6603d-168">Represents a usage error.</span></span> <span data-ttu-id="6603d-169">Il codice client non ha passato gli argomenti corretti all'API <strong>Jet</strong> .</span><span class="sxs-lookup"><span data-stu-id="6603d-169">The client code did not pass the correct arguments to the <strong>JET</strong> API.</span></span> <span data-ttu-id="6603d-170">Questo errore verrà mantenuto con un nuovo tentativo.</span><span class="sxs-lookup"><span data-stu-id="6603d-170">This error will persist with retry.</span></span></p></td>
<td><p><span data-ttu-id="6603d-171">Il codice client deve usare il metodo <strong>Assert ()</strong> per assicurarsi che questa classe di errori non venga restituita, quindi i problemi possono essere rilevati durante lo sviluppo.</span><span class="sxs-lookup"><span data-stu-id="6603d-171">Client code should use the <strong>Assert()</strong> method to ensure that this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="6603d-172">In dettaglio, l'applicazione deve notificare all'operatore l'errore.</span><span class="sxs-lookup"><span data-stu-id="6603d-172">In retail, the application should notify the operator about the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6603d-173">JET_errcatState 15</span><span class="sxs-lookup"><span data-stu-id="6603d-173">JET_errcatState 15</span></span></p></td>
<td><p><span data-ttu-id="6603d-174">Rappresenta una classe di messaggi che l'API può restituire per descrivere lo stato del database.</span><span class="sxs-lookup"><span data-stu-id="6603d-174">Represents a class of messages that the API can return to describe the state of the database.</span></span> <span data-ttu-id="6603d-175">Ad esempio, il metodo <a href="gg294103(v=exchg.10).md">JetSeek ()</a> potrebbe restituire <strong>JET_errRecordNotFound</strong> quando il record richiesto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="6603d-175">For example, the <a href="gg294103(v=exchg.10).md">JetSeek()</a> method might return <strong>JET_errRecordNotFound</strong> when the requested record was not found.</span></span></p></td>
<td><p><span data-ttu-id="6603d-176">Varia a seconda dell'API.</span><span class="sxs-lookup"><span data-stu-id="6603d-176">Varies based on the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6603d-177">JET_errcatObsolete 16</span><span class="sxs-lookup"><span data-stu-id="6603d-177">JET_errcatObsolete 16</span></span></p></td>
<td><p><span data-ttu-id="6603d-178">Rappresenta gli errori provenienti da una versione precedente del motore.</span><span class="sxs-lookup"><span data-stu-id="6603d-178">Represents errors that are from a previous version of the engine.</span></span> <span data-ttu-id="6603d-179">Questi errori non devono essere restituiti dal motore corrente.</span><span class="sxs-lookup"><span data-stu-id="6603d-179">These errors should not be returned by the current engine.</span></span></p></td>
<td><p><span data-ttu-id="6603d-180">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6603d-180">Unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6603d-181">JET_errcatMax 17</span><span class="sxs-lookup"><span data-stu-id="6603d-181">JET_errcatMax 17</span></span></p></td>
<td><p><span data-ttu-id="6603d-182">Costante che indica la fine dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="6603d-182">A constant that indicates the end of the enumeration.</span></span></p></td>
<td><p><span data-ttu-id="6603d-183">N/D.</span><span class="sxs-lookup"><span data-stu-id="6603d-183">N/A.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="6603d-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6603d-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6603d-185"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6603d-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6603d-186">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6603d-186">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6603d-187"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6603d-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6603d-188">Richiede Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="6603d-188">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6603d-189"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="6603d-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6603d-190">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="6603d-190">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

