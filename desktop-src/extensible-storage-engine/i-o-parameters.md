---
description: 'Altre informazioni su: parametri di I/O'
title: Parametri di I/O
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ba0e89602f7e5d4b9df395e89c73c8dc735692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753986"
---
# <a name="io-parameters"></a><span data-ttu-id="15960-103">Parametri di I/O</span><span class="sxs-lookup"><span data-stu-id="15960-103">I/O Parameters</span></span>


<span data-ttu-id="15960-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="15960-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="io-parameters"></a><span data-ttu-id="15960-105">Parametri di I/O</span><span class="sxs-lookup"><span data-stu-id="15960-105">I/O Parameters</span></span>

<span data-ttu-id="15960-106">Questo argomento contiene I parametri usati per l'input e l'output (I/O).</span><span class="sxs-lookup"><span data-stu-id="15960-106">This topic contains parameters that are used for input and output (I/O).</span></span>

<span data-ttu-id="15960-107">*JET_paramAccessDeniedRetryPeriod*</span><span class="sxs-lookup"><span data-stu-id="15960-107">*JET_paramAccessDeniedRetryPeriod*</span></span>  
<span data-ttu-id="15960-108">53</span><span class="sxs-lookup"><span data-stu-id="15960-108">53</span></span>  

<span data-ttu-id="15960-109">**Windows XP e versioni successive:**  Questo parametro consente di configurare la durata (in millisecondi) utilizzata dal motore di database per accedere a un file bloccato prima di avere esito negativo con JET_errFileAccessDenied.</span><span class="sxs-lookup"><span data-stu-id="15960-109">**Windows XP and later:**  This parameter configures the duration of time (in milliseconds) that the database engine will use to access a file that is locked before failing with JET_errFileAccessDenied.</span></span> <span data-ttu-id="15960-110">Questo ritardo è progettato per aggirare il software antivirus che può mantenere alcuni file del motore di database aperti brevemente dopo la chiusura.</span><span class="sxs-lookup"><span data-stu-id="15960-110">This time delay is designed to work around anti-virus software that may hold some of the database engine's files open briefly after they are closed.</span></span>

<span data-ttu-id="15960-111">**Nota**  In seguito alla logica di ripetizione dei tentativi precedente, qualsiasi tentativo di connessione a un database o di utilizzo di un file di log già utilizzato dal motore di database comporterà un ritardo di questa dimensione prima che la chiamata API restituisca un errore (legittimo).</span><span class="sxs-lookup"><span data-stu-id="15960-111">**Note**  As a result of the above retry logic, any attempt to attach to a database or use a log file that is already in use by the database engine will result in a delay of this size before the API call returns a (legitimate) failure.</span></span> <span data-ttu-id="15960-112">Questo parametro può essere usato per disattivare tale ritardo nel caso in cui si tratti di uno scenario comune.</span><span class="sxs-lookup"><span data-stu-id="15960-112">This parameter can be used to turn down that delay in case this is a common scenario.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15960-113">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="15960-113">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="15960-114">10000</span><span class="sxs-lookup"><span data-stu-id="15960-114">10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-115">Digitare:</span><span class="sxs-lookup"><span data-stu-id="15960-115">Type:</span></span></p></td>
<td><p><span data-ttu-id="15960-116">Integer</span><span class="sxs-lookup"><span data-stu-id="15960-116">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-117">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="15960-117">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="15960-118">0 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="15960-118">0 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-119">Ambito:</span><span class="sxs-lookup"><span data-stu-id="15960-119">Scope:</span></span></p></td>
<td><p><span data-ttu-id="15960-120">Globale</span><span class="sxs-lookup"><span data-stu-id="15960-120">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-121">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-121">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-122">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-123">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-123">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-124">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-124">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-125">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="15960-125">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="15960-126">No</span><span class="sxs-lookup"><span data-stu-id="15960-126">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-127">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="15960-127">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="15960-128">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-128">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-129">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="15960-129">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="15960-130">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-130">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-131">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="15960-131">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="15960-132">No</span><span class="sxs-lookup"><span data-stu-id="15960-132">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-133">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="15960-133">Availability:</span></span></p></td>
<td><p><span data-ttu-id="15960-134">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="15960-134">Windows XP and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="15960-135">*JET_paramCreatePathIfNotExist*</span><span class="sxs-lookup"><span data-stu-id="15960-135">*JET_paramCreatePathIfNotExist*</span></span>  
<span data-ttu-id="15960-136">100</span><span class="sxs-lookup"><span data-stu-id="15960-136">100</span></span>  

<span data-ttu-id="15960-137">Se questo parametro è impostato su true, tutte le cartelle mancanti in un percorso di file system in uso dal motore di database verranno create automaticamente.</span><span class="sxs-lookup"><span data-stu-id="15960-137">When this parameter is set to true then any folder that is missing in a file system path in use by the database engine will be silently created.</span></span> <span data-ttu-id="15960-138">In caso contrario, l'operazione che usa il percorso di file system mancante avrà esito negativo con JET_errInvalidPath.</span><span class="sxs-lookup"><span data-stu-id="15960-138">Otherwise, the operation that uses the missing file system path will fail with JET_errInvalidPath.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15960-139">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="15960-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="15960-140">Falso</span><span class="sxs-lookup"><span data-stu-id="15960-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-141">Digitare:</span><span class="sxs-lookup"><span data-stu-id="15960-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="15960-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="15960-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-143">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="15960-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="15960-144">False, True</span><span class="sxs-lookup"><span data-stu-id="15960-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-145">Ambito:</span><span class="sxs-lookup"><span data-stu-id="15960-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="15960-146">Istanza</span><span class="sxs-lookup"><span data-stu-id="15960-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-147">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-148">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-149">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-150">No</span><span class="sxs-lookup"><span data-stu-id="15960-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-151">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="15960-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="15960-152">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-153">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="15960-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="15960-154">No</span><span class="sxs-lookup"><span data-stu-id="15960-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-155">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="15960-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="15960-156">No</span><span class="sxs-lookup"><span data-stu-id="15960-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-157">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="15960-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="15960-158">No</span><span class="sxs-lookup"><span data-stu-id="15960-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-159">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="15960-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="15960-160">Tutti</span><span class="sxs-lookup"><span data-stu-id="15960-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="15960-161">*JET_paramEnableFileCache*</span><span class="sxs-lookup"><span data-stu-id="15960-161">*JET_paramEnableFileCache*</span></span>  
<span data-ttu-id="15960-162">126</span><span class="sxs-lookup"><span data-stu-id="15960-162">126</span></span>  

<span data-ttu-id="15960-163">Quando questo parametro è impostato su **true**, il motore di database utilizzerà la cache dei file di Windows come cache di lettura per tutti i vari file.</span><span class="sxs-lookup"><span data-stu-id="15960-163">When this parameter is **True**, the database engine will use the Windows file cache as a read cache for all of its various files.</span></span> <span data-ttu-id="15960-164">Lo utilizzerà anche come cache di scrittura per il database temporaneo o per i database aperti con il ripristino disabilitato.</span><span class="sxs-lookup"><span data-stu-id="15960-164">It will also use it as a write cache for the temporary database or for databases that are opened with recovery disabled.</span></span> <span data-ttu-id="15960-165">Il motore di database deve disabilitare la memorizzazione nella cache in scrittura per i database normali, i file di log delle transazioni e i file del checkpoint per proteggere l'integrità transazionale dei database.</span><span class="sxs-lookup"><span data-stu-id="15960-165">The database engine must disable write caching for ordinary databases, transaction log files, and checkpoint files to protect the transactional integrity of the databases.</span></span>

<span data-ttu-id="15960-166">È importante notare che l'uso della cache dei file di Windows aggiungerà un secondo livello di memorizzazione nella cache per i file di database.</span><span class="sxs-lookup"><span data-stu-id="15960-166">It is important to note that the use of the Windows file cache will add a second layering of caching for database files.</span></span> <span data-ttu-id="15960-167">La cache del database utilizzerà comunque la propria memoria per memorizzare i file di database.</span><span class="sxs-lookup"><span data-stu-id="15960-167">The database cache will still use its own memory to cache the database files.</span></span> <span data-ttu-id="15960-168">Lo scopo di questa modalità è consentire all'applicazione di configurare il motore di database con una piccola cache dedicata e consentire a Windows di donare memoria di riserva per migliorare ulteriormente la memorizzazione nella cache dei dati del database.</span><span class="sxs-lookup"><span data-stu-id="15960-168">The intent of this mode is to allow the application to configure the database engine with a small dedicated cache and to allow Windows to donate spare memory to further improve the caching of database data.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15960-169">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="15960-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="15960-170">Falso</span><span class="sxs-lookup"><span data-stu-id="15960-170">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-171">Digitare:</span><span class="sxs-lookup"><span data-stu-id="15960-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="15960-172">Boolean</span><span class="sxs-lookup"><span data-stu-id="15960-172">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-173">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="15960-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="15960-174">False, True</span><span class="sxs-lookup"><span data-stu-id="15960-174">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-175">Ambito:</span><span class="sxs-lookup"><span data-stu-id="15960-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="15960-176">Globale</span><span class="sxs-lookup"><span data-stu-id="15960-176">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-177">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-178">No</span><span class="sxs-lookup"><span data-stu-id="15960-178">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-179">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-180">No</span><span class="sxs-lookup"><span data-stu-id="15960-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-181">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="15960-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="15960-182">No</span><span class="sxs-lookup"><span data-stu-id="15960-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-183">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="15960-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="15960-184">No</span><span class="sxs-lookup"><span data-stu-id="15960-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-185">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="15960-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="15960-186">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-187">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="15960-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="15960-188">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-188">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-189">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="15960-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="15960-190">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="15960-190">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="15960-191">*JET_paramIOPriority*</span><span class="sxs-lookup"><span data-stu-id="15960-191">*JET_paramIOPriority*</span></span>  
<span data-ttu-id="15960-192">152</span><span class="sxs-lookup"><span data-stu-id="15960-192">152</span></span>  

<span data-ttu-id="15960-193">Questo parametro controlla il modo in cui ESE gestisce le operazioni di I/O.</span><span class="sxs-lookup"><span data-stu-id="15960-193">This parameter controls how ESE handles I/O operations.</span></span> <span data-ttu-id="15960-194">I valori possono essere impostati su 0 (JET_IOPriorityNormal) per il normale funzionamento oppure su 1 (JET_IOPriorityLow) per operazioni con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="15960-194">The values can be set to 0 (JET_IOPriorityNormal) for normal operation, or 1 (JET_IOPriorityLow) for low priority operation.</span></span> <span data-ttu-id="15960-195">Quando la priorità è impostata su JET_IOPriorityLow, ESE utilizza la nuova funzionalità di priorità di I/O del thread disponibile in Windows Vista per ridurre la priorità di I/O nel thread in modo che le operazioni di I/O successive vengano emesse con la nuova priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="15960-195">When the priority is set to JET_IOPriorityLow, ESE uses the new thread I/O priority functionality available in Windows Vista to reduce the I/O priority on the thread so that subsequent I/O operations are issued at the new low priority.</span></span>

<span data-ttu-id="15960-196">**Windows Vista:**  JET_paramIOPriority è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="15960-196">**Windows Vista:**  JET_paramIOPriority is introduced in Windows Vista.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15960-197">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="15960-197">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="15960-198">0</span><span class="sxs-lookup"><span data-stu-id="15960-198">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-199">Digitare:</span><span class="sxs-lookup"><span data-stu-id="15960-199">Type:</span></span></p></td>
<td><p><span data-ttu-id="15960-200">Integer</span><span class="sxs-lookup"><span data-stu-id="15960-200">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-201">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="15960-201">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="15960-202">0 - 1</span><span class="sxs-lookup"><span data-stu-id="15960-202">0 - 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-203">Ambito:</span><span class="sxs-lookup"><span data-stu-id="15960-203">Scope:</span></span></p></td>
<td><p><span data-ttu-id="15960-204">Istanza</span><span class="sxs-lookup"><span data-stu-id="15960-204">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-205">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-205">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-206">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-206">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-207">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-207">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-208">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-208">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-209">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="15960-209">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="15960-210">No</span><span class="sxs-lookup"><span data-stu-id="15960-210">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-211">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="15960-211">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="15960-212">No</span><span class="sxs-lookup"><span data-stu-id="15960-212">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-213">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="15960-213">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="15960-214">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-214">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-215">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="15960-215">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="15960-216">No</span><span class="sxs-lookup"><span data-stu-id="15960-216">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-217">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="15960-217">Availability:</span></span></p></td>
<td><p><span data-ttu-id="15960-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15960-218">Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="15960-219">*JET_paramOutstandingIOMax*</span><span class="sxs-lookup"><span data-stu-id="15960-219">*JET_paramOutstandingIOMax*</span></span>  
<span data-ttu-id="15960-220">30</span><span class="sxs-lookup"><span data-stu-id="15960-220">30</span></span> 

<span data-ttu-id="15960-221">Questo parametro controlla il numero di I/o di file di database che possono essere accodati contemporaneamente nel sistema operativo host.</span><span class="sxs-lookup"><span data-stu-id="15960-221">This parameter controls how many database file I/Os can be queued in the host operating system at one time.</span></span>

<span data-ttu-id="15960-222">Un valore più elevato per questo parametro può migliorare significativamente le prestazioni di un'applicazione di database di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="15960-222">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="15960-223">**Windows XP e Windows Server 2003:**  Questo parametro viene ignorato in Windows XP e Windows Server 2003 e non influisce sul funzionamento del motore di database.</span><span class="sxs-lookup"><span data-stu-id="15960-223">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15960-224">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="15960-224">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="15960-225"><strong>Windows 2000: </strong>  64</span><span class="sxs-lookup"><span data-stu-id="15960-225"><strong>Windows 2000: </strong>  64</span></span></p>
<p><span data-ttu-id="15960-226"><strong>Windows Vista:</strong>   1024</span><span class="sxs-lookup"><span data-stu-id="15960-226"><strong>Windows Vista:</strong>   1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-227">Digitare:</span><span class="sxs-lookup"><span data-stu-id="15960-227">Type:</span></span></p></td>
<td><p><span data-ttu-id="15960-228">Integer</span><span class="sxs-lookup"><span data-stu-id="15960-228">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-229">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="15960-229">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="15960-230"><strong>Windows 2000:</strong>  8 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="15960-230"><strong>Windows 2000:</strong>  8 – 2147483647</span></span></p>
<p><span data-ttu-id="15960-231"><strong>Windows Vista:</strong>  0-65536</span><span class="sxs-lookup"><span data-stu-id="15960-231"><strong>Windows Vista:</strong>  0 – 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-232">Ambito:</span><span class="sxs-lookup"><span data-stu-id="15960-232">Scope:</span></span></p></td>
<td><p><span data-ttu-id="15960-233">Globale</span><span class="sxs-lookup"><span data-stu-id="15960-233">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-234">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-234">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-235">No</span><span class="sxs-lookup"><span data-stu-id="15960-235">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-236">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-236">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-237">No</span><span class="sxs-lookup"><span data-stu-id="15960-237">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-238">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="15960-238">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="15960-239">No</span><span class="sxs-lookup"><span data-stu-id="15960-239">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-240">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="15960-240">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="15960-241">No</span><span class="sxs-lookup"><span data-stu-id="15960-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-242">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="15960-242">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="15960-243">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-243">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-244">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="15960-244">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="15960-245">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-246">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="15960-246">Availability:</span></span></p></td>
<td><p><span data-ttu-id="15960-247">Tutti</span><span class="sxs-lookup"><span data-stu-id="15960-247">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="15960-248">*JET_paramMaxCoalesceReadSize*</span><span class="sxs-lookup"><span data-stu-id="15960-248">*JET_paramMaxCoalesceReadSize*</span></span>  
<span data-ttu-id="15960-249">164</span><span class="sxs-lookup"><span data-stu-id="15960-249">164</span></span>  

<span data-ttu-id="15960-250">Numero massimo di byte che è possibile raggruppare per un'operazione di lettura con Unione.</span><span class="sxs-lookup"><span data-stu-id="15960-250">Maximum number of bytes that can be grouped for a coalesced read operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15960-251">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="15960-251">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="15960-252">262144</span><span class="sxs-lookup"><span data-stu-id="15960-252">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-253">Digitare:</span><span class="sxs-lookup"><span data-stu-id="15960-253">Type:</span></span></p></td>
<td><p><span data-ttu-id="15960-254">Integer</span><span class="sxs-lookup"><span data-stu-id="15960-254">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-255">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="15960-255">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="15960-256">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="15960-256">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-257">Ambito:</span><span class="sxs-lookup"><span data-stu-id="15960-257">Scope:</span></span></p></td>
<td><p><span data-ttu-id="15960-258">Globale</span><span class="sxs-lookup"><span data-stu-id="15960-258">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-259">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-259">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-260">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-260">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-261">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-261">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-262">No</span><span class="sxs-lookup"><span data-stu-id="15960-262">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-263">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="15960-263">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="15960-264">No</span><span class="sxs-lookup"><span data-stu-id="15960-264">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-265">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="15960-265">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="15960-266">No</span><span class="sxs-lookup"><span data-stu-id="15960-266">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-267">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="15960-267">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="15960-268">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-268">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-269">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="15960-269">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="15960-270">No</span><span class="sxs-lookup"><span data-stu-id="15960-270">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-271">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="15960-271">Availability:</span></span></p></td>
<td><p><span data-ttu-id="15960-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="15960-272">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="15960-273">*JET_paramMaxCoalesceWriteSize*</span><span class="sxs-lookup"><span data-stu-id="15960-273">*JET_paramMaxCoalesceWriteSize*</span></span>  
<span data-ttu-id="15960-274">165</span><span class="sxs-lookup"><span data-stu-id="15960-274">165</span></span>  

<span data-ttu-id="15960-275">Numero massimo di byte che è possibile raggruppare per un'operazione di scrittura coalesta.</span><span class="sxs-lookup"><span data-stu-id="15960-275">Maximum number of bytes that can be grouped for a coalesced write operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15960-276">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="15960-276">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="15960-277">393216</span><span class="sxs-lookup"><span data-stu-id="15960-277">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-278">Digitare:</span><span class="sxs-lookup"><span data-stu-id="15960-278">Type:</span></span></p></td>
<td><p><span data-ttu-id="15960-279">Integer</span><span class="sxs-lookup"><span data-stu-id="15960-279">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-280">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="15960-280">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="15960-281">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="15960-281">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-282">Ambito:</span><span class="sxs-lookup"><span data-stu-id="15960-282">Scope:</span></span></p></td>
<td><p><span data-ttu-id="15960-283">Globale</span><span class="sxs-lookup"><span data-stu-id="15960-283">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-284">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-284">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-285">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-285">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-286">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-286">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-287">No</span><span class="sxs-lookup"><span data-stu-id="15960-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-288">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="15960-288">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="15960-289">No</span><span class="sxs-lookup"><span data-stu-id="15960-289">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-290">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="15960-290">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="15960-291">No</span><span class="sxs-lookup"><span data-stu-id="15960-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-292">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="15960-292">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="15960-293">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-293">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-294">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="15960-294">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="15960-295">No</span><span class="sxs-lookup"><span data-stu-id="15960-295">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-296">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="15960-296">Availability:</span></span></p></td>
<td><p><span data-ttu-id="15960-297">Windows 7</span><span class="sxs-lookup"><span data-stu-id="15960-297">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="15960-298">*JET_paramMaxCoalesceReadGapSize*</span><span class="sxs-lookup"><span data-stu-id="15960-298">*JET_paramMaxCoalesceReadGapSize*</span></span>  
<span data-ttu-id="15960-299">166</span><span class="sxs-lookup"><span data-stu-id="15960-299">166</span></span>  

<span data-ttu-id="15960-300">Numero massimo di byte che possono essere gapped per un'operazione di I/O di scrittura coalesta.</span><span class="sxs-lookup"><span data-stu-id="15960-300">Maximum number of bytes that can be gapped for a coalesced write I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15960-301">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="15960-301">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="15960-302">262144</span><span class="sxs-lookup"><span data-stu-id="15960-302">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-303">Digitare:</span><span class="sxs-lookup"><span data-stu-id="15960-303">Type:</span></span></p></td>
<td><p><span data-ttu-id="15960-304">Integer</span><span class="sxs-lookup"><span data-stu-id="15960-304">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-305">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="15960-305">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="15960-306">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="15960-306">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-307">Ambito:</span><span class="sxs-lookup"><span data-stu-id="15960-307">Scope:</span></span></p></td>
<td><p><span data-ttu-id="15960-308">Globale</span><span class="sxs-lookup"><span data-stu-id="15960-308">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-309">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-309">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-310">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-310">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-311">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-311">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-312">No</span><span class="sxs-lookup"><span data-stu-id="15960-312">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-313">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="15960-313">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="15960-314">No</span><span class="sxs-lookup"><span data-stu-id="15960-314">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-315">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="15960-315">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="15960-316">No</span><span class="sxs-lookup"><span data-stu-id="15960-316">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-317">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="15960-317">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="15960-318">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-318">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-319">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="15960-319">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="15960-320">No</span><span class="sxs-lookup"><span data-stu-id="15960-320">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-321">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="15960-321">Availability:</span></span></p></td>
<td><p><span data-ttu-id="15960-322">Windows 7</span><span class="sxs-lookup"><span data-stu-id="15960-322">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="15960-323">*JET_paramMaxCoalesceWriteGapSize*</span><span class="sxs-lookup"><span data-stu-id="15960-323">*JET_paramMaxCoalesceWriteGapSize*</span></span>  
<span data-ttu-id="15960-324">167</span><span class="sxs-lookup"><span data-stu-id="15960-324">167</span></span>  

<span data-ttu-id="15960-325">Numero massimo di byte che possono essere gapped per un'operazione di I/O di lettura con Unione.</span><span class="sxs-lookup"><span data-stu-id="15960-325">Max number of bytes that can be gapped for a coalesced read I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15960-326">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="15960-326">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="15960-327">393216</span><span class="sxs-lookup"><span data-stu-id="15960-327">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-328">Digitare:</span><span class="sxs-lookup"><span data-stu-id="15960-328">Type:</span></span></p></td>
<td><p><span data-ttu-id="15960-329">Integer</span><span class="sxs-lookup"><span data-stu-id="15960-329">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-330">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="15960-330">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="15960-331">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="15960-331">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-332">Ambito:</span><span class="sxs-lookup"><span data-stu-id="15960-332">Scope:</span></span></p></td>
<td><p><span data-ttu-id="15960-333">Globale</span><span class="sxs-lookup"><span data-stu-id="15960-333">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-334">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-334">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-335">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-335">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-336">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="15960-336">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="15960-337">No</span><span class="sxs-lookup"><span data-stu-id="15960-337">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-338">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="15960-338">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="15960-339">No</span><span class="sxs-lookup"><span data-stu-id="15960-339">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-340">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="15960-340">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="15960-341">No</span><span class="sxs-lookup"><span data-stu-id="15960-341">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-342">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="15960-342">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="15960-343">Sì</span><span class="sxs-lookup"><span data-stu-id="15960-343">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-344">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="15960-344">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="15960-345">No</span><span class="sxs-lookup"><span data-stu-id="15960-345">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-346">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="15960-346">Availability:</span></span></p></td>
<td><p><span data-ttu-id="15960-347">Windows 7</span><span class="sxs-lookup"><span data-stu-id="15960-347">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="15960-348">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15960-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15960-349"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="15960-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="15960-350">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="15960-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15960-351"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="15960-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="15960-352">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="15960-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15960-353"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="15960-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="15960-354">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="15960-354">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="15960-355">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="15960-355">See Also</span></span>

[<span data-ttu-id="15960-356">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="15960-356">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="15960-357">JetInit</span><span class="sxs-lookup"><span data-stu-id="15960-357">JetInit</span></span>](./jetinit-function.md)
