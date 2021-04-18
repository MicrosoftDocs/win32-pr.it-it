---
description: 'Altre informazioni su: parametri delle risorse'
title: Parametri delle risorse
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: 953488a273092413df78d4fe396899d284c7a01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313078"
---
# <a name="resource-parameters"></a><span data-ttu-id="1817a-103">Parametri delle risorse</span><span class="sxs-lookup"><span data-stu-id="1817a-103">Resource Parameters</span></span>


<span data-ttu-id="1817a-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1817a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="resource-parameters"></a><span data-ttu-id="1817a-105">Parametri delle risorse</span><span class="sxs-lookup"><span data-stu-id="1817a-105">Resource Parameters</span></span>

<span data-ttu-id="1817a-106">Questo argomento contiene i parametri usati per le risorse.</span><span class="sxs-lookup"><span data-stu-id="1817a-106">This topic contains parameters that are used for resources.</span></span>

<span data-ttu-id="1817a-107">*JET_paramCachedClosedTables*</span><span class="sxs-lookup"><span data-stu-id="1817a-107">*JET_paramCachedClosedTables*</span></span>  
<span data-ttu-id="1817a-108">125</span><span class="sxs-lookup"><span data-stu-id="1817a-108">125</span></span>  

<span data-ttu-id="1817a-109">Questo parametro controlla il numero di risorse dell'albero B + memorizzato nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1817a-109">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span>

<span data-ttu-id="1817a-110">I valori di grandi dimensioni per questo parametro comportano l'utilizzo di una maggiore quantità di memoria da parte del motore di database, ma aumentano la velocità con cui l'applicazione può aprire in modo casuale un numero elevato di tabelle.</span><span class="sxs-lookup"><span data-stu-id="1817a-110">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="1817a-111">Questa operazione è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle.</span><span class="sxs-lookup"><span data-stu-id="1817a-111">This is useful for applications that have a schema with a very large number of tables.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-112">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-113">64</span><span class="sxs-lookup"><span data-stu-id="1817a-113">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-114">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-115">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-116">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-117">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="1817a-117">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-118">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-119">Istanza</span><span class="sxs-lookup"><span data-stu-id="1817a-119">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-120">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-121">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-121">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-122">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-123">No</span><span class="sxs-lookup"><span data-stu-id="1817a-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-124">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-125">No</span><span class="sxs-lookup"><span data-stu-id="1817a-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-126">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-127">No</span><span class="sxs-lookup"><span data-stu-id="1817a-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-128">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-129">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-130">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-131">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-132">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-133">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="1817a-133">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-134">*JET_paramDisablePerfmon*</span><span class="sxs-lookup"><span data-stu-id="1817a-134">*JET_paramDisablePerfmon*</span></span>  
<span data-ttu-id="1817a-135">107</span><span class="sxs-lookup"><span data-stu-id="1817a-135">107</span></span>  

<span data-ttu-id="1817a-136">Questo parametro può essere utilizzato per impedire al motore di database di pubblicare dati sulle prestazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="1817a-136">This parameter can be used to prevent the database engine from publishing data about its performance to Windows.</span></span> <span data-ttu-id="1817a-137">Questa operazione può essere eseguita per ridurre l'attività del thread del servizio del motore di database.</span><span class="sxs-lookup"><span data-stu-id="1817a-137">This can be done to reduce the service thread activity of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-138">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-138">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-139">Falso</span><span class="sxs-lookup"><span data-stu-id="1817a-139">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-140">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-140">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="1817a-141">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-142">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-142">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-143">False, True</span><span class="sxs-lookup"><span data-stu-id="1817a-143">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-144">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-144">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-145">Globale</span><span class="sxs-lookup"><span data-stu-id="1817a-145">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-146">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-146">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-147">No</span><span class="sxs-lookup"><span data-stu-id="1817a-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-148">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-148">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-149">No</span><span class="sxs-lookup"><span data-stu-id="1817a-149">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-150">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-150">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-151">No</span><span class="sxs-lookup"><span data-stu-id="1817a-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-152">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-152">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-153">No</span><span class="sxs-lookup"><span data-stu-id="1817a-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-154">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-154">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-155">No</span><span class="sxs-lookup"><span data-stu-id="1817a-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-156">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-156">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-157">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-157">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-158">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-158">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-159">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="1817a-159">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-160">*JET_paramGlobalMinVerPages*</span><span class="sxs-lookup"><span data-stu-id="1817a-160">*JET_paramGlobalMinVerPages*</span></span>  
<span data-ttu-id="1817a-161">81</span><span class="sxs-lookup"><span data-stu-id="1817a-161">81</span></span>  

<span data-ttu-id="1817a-162">Questo parametro consente alle applicazioni che operano in modalità a istanze diverse di pre-allocare memoria per le pagine della versione in un pool globale per emulare il comportamento precedente.</span><span class="sxs-lookup"><span data-stu-id="1817a-162">This parameter allows applications that operate in multi-instance mode to pre-allocate memory for version pages in a global pool to emulate the older behavior.</span></span> <span data-ttu-id="1817a-163">Questa operazione è utile nel caso in cui l'applicazione voglia garantire che le transazioni di una determinata dimensione possano avere esito positivo in un secondo momento anche se la memoria risulterà limitata.</span><span class="sxs-lookup"><span data-stu-id="1817a-163">This is useful in case the application wishes to guarantee that transactions of a certain size can succeed later on even if memory becomes scarce.</span></span>

<span data-ttu-id="1817a-164">**Windows 2000:**  Memoria sufficiente per eseguire il backup di tutte le pagine della versione è sempre riservata in fase di [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="1817a-164">**Windows 2000:**  Enough memory to back all version pages is always reserved at [JetInit](./jetinit-function.md) time.</span></span>

<span data-ttu-id="1817a-165">**Windows XP:**  A partire da Windows XP, questo è ancora vero in modalità a istanza singola.</span><span class="sxs-lookup"><span data-stu-id="1817a-165">**Windows XP:**  As of Windows XP, this is still true when in single instance mode.</span></span> <span data-ttu-id="1817a-166">Tuttavia, la memoria della pagina della versione viene allocata in modo dinamico in modalità a istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="1817a-166">However, version page memory is dynamically allocated when in multi-instance mode.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-167">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-167">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-168">64</span><span class="sxs-lookup"><span data-stu-id="1817a-168">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-169">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-170">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-171">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-172">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="1817a-172">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-173">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-173">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-174">Globale</span><span class="sxs-lookup"><span data-stu-id="1817a-174">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-175">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-175">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-176">No</span><span class="sxs-lookup"><span data-stu-id="1817a-176">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-177">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-177">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-178">No</span><span class="sxs-lookup"><span data-stu-id="1817a-178">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-179">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-179">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-180">No</span><span class="sxs-lookup"><span data-stu-id="1817a-180">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-181">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-181">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-182">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-182">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-183">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-183">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-184">No</span><span class="sxs-lookup"><span data-stu-id="1817a-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-185">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-185">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-186">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-187">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-187">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-188">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="1817a-188">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-189">*JET_paramMaxCursors*</span><span class="sxs-lookup"><span data-stu-id="1817a-189">*JET_paramMaxCursors*</span></span>  
<span data-ttu-id="1817a-190">8</span><span class="sxs-lookup"><span data-stu-id="1817a-190">8</span></span>  

<span data-ttu-id="1817a-191">Questo parametro riserva il numero richiesto di risorse del cursore per l'utilizzo da parte di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="1817a-191">This parameter reserves the requested number of cursor resources for use by an instance.</span></span> <span data-ttu-id="1817a-192">Una risorsa di cursore corrisponde direttamente a un tipo di dati [JET_TABLEID](./jet-tableid.md) .</span><span class="sxs-lookup"><span data-stu-id="1817a-192">A cursor resource directly corresponds to a [JET_TABLEID](./jet-tableid.md) data type.</span></span> <span data-ttu-id="1817a-193">Questa impostazione influirà sul numero di cursori che possono essere utilizzati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1817a-193">This setting will affect how many cursors can be used at the same time.</span></span> <span data-ttu-id="1817a-194">Una risorsa cursore non può essere condivisa da sessioni diverse, pertanto questo parametro deve essere impostato su un valore sufficientemente elevato in modo che ogni sessione possa usare tutti i cursori richiesti.</span><span class="sxs-lookup"><span data-stu-id="1817a-194">A cursor resource cannot be shared by different sessions so this parameter must be set to a large enough value so that each session can use as many cursors as are required.</span></span>

<span data-ttu-id="1817a-195">**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzeranno lo spazio di indirizzi e potrebbero aumentare l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="1817a-195">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-196">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-196">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-197">1024</span><span class="sxs-lookup"><span data-stu-id="1817a-197">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-198">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-198">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-199">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-199">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-200">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-200">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-201">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="1817a-201">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-202">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-202">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-203">Istanza</span><span class="sxs-lookup"><span data-stu-id="1817a-203">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-204">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-204">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-205">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-205">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-206">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-206">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-207">No</span><span class="sxs-lookup"><span data-stu-id="1817a-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-208">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-208">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-209">No</span><span class="sxs-lookup"><span data-stu-id="1817a-209">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-210">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-210">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-211">No</span><span class="sxs-lookup"><span data-stu-id="1817a-211">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-212">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-212">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-213">No</span><span class="sxs-lookup"><span data-stu-id="1817a-213">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-214">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-214">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-215">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-215">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-216">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-216">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-217">Tutti</span><span class="sxs-lookup"><span data-stu-id="1817a-217">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-218">*JET_paramMaxInstances*</span><span class="sxs-lookup"><span data-stu-id="1817a-218">*JET_paramMaxInstances*</span></span>  
<span data-ttu-id="1817a-219">104</span><span class="sxs-lookup"><span data-stu-id="1817a-219">104</span></span>  

<span data-ttu-id="1817a-220">Questo parametro controlla il numero massimo di istanze che è possibile creare in un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="1817a-220">This parameter controls the maximum number of instances that can be created in a single process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-221">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-222">16</span><span class="sxs-lookup"><span data-stu-id="1817a-222">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-223">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-224">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-224">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-225">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-226">1-1024</span><span class="sxs-lookup"><span data-stu-id="1817a-226">1-1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-227">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-228">Globale</span><span class="sxs-lookup"><span data-stu-id="1817a-228">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-229">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-230">No</span><span class="sxs-lookup"><span data-stu-id="1817a-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-231">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-232">No</span><span class="sxs-lookup"><span data-stu-id="1817a-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-233">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-234">No</span><span class="sxs-lookup"><span data-stu-id="1817a-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-235">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-236">No</span><span class="sxs-lookup"><span data-stu-id="1817a-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-237">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-238">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-239">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-240">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-240">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-241">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-242">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="1817a-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-243">*JET_paramMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="1817a-243">*JET_paramMaxOpenTables*</span></span>  
<span data-ttu-id="1817a-244">6</span><span class="sxs-lookup"><span data-stu-id="1817a-244">6</span></span>  

<span data-ttu-id="1817a-245">Questo parametro riserva il numero richiesto di risorse dell'albero B + per l'utilizzo da parte di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="1817a-245">This parameter reserves the requested number of B+ Tree resources for use by an instance.</span></span> <span data-ttu-id="1817a-246">Questa impostazione influirà sul numero di tabelle che possono essere usate contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1817a-246">This setting will affect how many tables can be used at the same time.</span></span> <span data-ttu-id="1817a-247">Questo parametro deve essere impostato in relazione allo schema fisico dei database utilizzati dal motore di database, pertanto questa impostazione non è semplice come potrebbe essere.</span><span class="sxs-lookup"><span data-stu-id="1817a-247">This parameter needs to be set relative to the physical schema of the databases in use by the database engine, so this setting is not as straightforward as it could be.</span></span>

<span data-ttu-id="1817a-248">In generale, sono necessarie due risorse e una risorsa per ogni indice secondario per ogni tabella nell'uso simultaneo da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1817a-248">In general, you will need two resources plus one resource per secondary index per table in concurrent use by the application.</span></span>

<span data-ttu-id="1817a-249">**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzeranno lo spazio di indirizzi e potrebbero aumentare l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="1817a-249">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-250">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-250">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-251">300</span><span class="sxs-lookup"><span data-stu-id="1817a-251">300</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-252">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-252">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-253">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-253">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-254">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-254">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-255">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="1817a-255">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-256">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-256">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-257">Istanza</span><span class="sxs-lookup"><span data-stu-id="1817a-257">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-258">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-258">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-259">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-259">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-260">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-260">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-261">No</span><span class="sxs-lookup"><span data-stu-id="1817a-261">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-262">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-262">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-263">No</span><span class="sxs-lookup"><span data-stu-id="1817a-263">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-264">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-264">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-265">No</span><span class="sxs-lookup"><span data-stu-id="1817a-265">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-266">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-266">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-267">No</span><span class="sxs-lookup"><span data-stu-id="1817a-267">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-268">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-268">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-269">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-269">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-270">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-270">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-271">Tutti</span><span class="sxs-lookup"><span data-stu-id="1817a-271">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-272">*JET_paramMaxSessions*</span><span class="sxs-lookup"><span data-stu-id="1817a-272">*JET_paramMaxSessions*</span></span>  
<span data-ttu-id="1817a-273">5</span><span class="sxs-lookup"><span data-stu-id="1817a-273">5</span></span>  

<span data-ttu-id="1817a-274">Questo parametro riserva il numero richiesto di risorse della sessione per l'utilizzo da parte di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="1817a-274">This parameter reserves the requested number of session resources for use by an instance.</span></span> <span data-ttu-id="1817a-275">Una risorsa di sessione corrisponde direttamente a un tipo di dati [JET_SESID](./jet-sesid.md) .</span><span class="sxs-lookup"><span data-stu-id="1817a-275">A session resource directly corresponds to a [JET_SESID](./jet-sesid.md) data type.</span></span> <span data-ttu-id="1817a-276">Questa impostazione influirà sul numero di sessioni che possono essere usate contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1817a-276">This setting will affect how many sessions can be used at the same time.</span></span>

<span data-ttu-id="1817a-277">**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzeranno lo spazio di indirizzi e potrebbero aumentare l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="1817a-277">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-278">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-278">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-279">16</span><span class="sxs-lookup"><span data-stu-id="1817a-279">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-280">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-280">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-281">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-281">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-282">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-282">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-283">0 – 30000</span><span class="sxs-lookup"><span data-stu-id="1817a-283">0 – 30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-284">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-284">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-285">Istanza</span><span class="sxs-lookup"><span data-stu-id="1817a-285">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-286">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-286">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-287">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-287">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-288">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-288">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-289">No</span><span class="sxs-lookup"><span data-stu-id="1817a-289">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-290">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-290">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-291">No</span><span class="sxs-lookup"><span data-stu-id="1817a-291">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-292">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-292">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-293">No</span><span class="sxs-lookup"><span data-stu-id="1817a-293">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-294">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-294">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-295">No</span><span class="sxs-lookup"><span data-stu-id="1817a-295">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-296">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-296">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-297">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-297">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-298">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-298">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-299">Tutti</span><span class="sxs-lookup"><span data-stu-id="1817a-299">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-300">*JET_paramMaxTemporaryTables*</span><span class="sxs-lookup"><span data-stu-id="1817a-300">*JET_paramMaxTemporaryTables*</span></span>  
<span data-ttu-id="1817a-301">10</span><span class="sxs-lookup"><span data-stu-id="1817a-301">10</span></span>  

<span data-ttu-id="1817a-302">Questo parametro riserva il numero richiesto di risorse della tabella temporanea per l'utilizzo da parte di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="1817a-302">This parameter reserves the requested number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="1817a-303">Questa impostazione influirà sul numero di tabelle temporanee che possono essere usate contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1817a-303">This setting will affect how many temporary tables can be used at the same time.</span></span>

<span data-ttu-id="1817a-304">**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzeranno lo spazio di indirizzi e potrebbero aumentare l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="1817a-304">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="1817a-305">**Windows XP e versioni successive:**  Se questo parametro di sistema è impostato su zero, non verrà creato alcun database temporaneo e le attività che richiedono l'utilizzo del database temporaneo avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="1817a-305">**Windows XP and later:**  If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="1817a-306">Questa impostazione può essere utile per evitare l'i/O necessario per creare il database temporaneo se è noto che non verrà utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1817a-306">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="1817a-307">**Nota**  Per l'utilizzo di una tabella temporanea è inoltre necessaria una risorsa Cursor.</span><span class="sxs-lookup"><span data-stu-id="1817a-307">**Note**  The use of a temporary table also requires a cursor resource.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-308">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-308">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-309">20</span><span class="sxs-lookup"><span data-stu-id="1817a-309">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-310">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-310">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-311">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-311">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-312">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-312">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-313">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="1817a-313">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-314">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-314">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-315">Istanza</span><span class="sxs-lookup"><span data-stu-id="1817a-315">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-316">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-316">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-317">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-318">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-318">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-319">No</span><span class="sxs-lookup"><span data-stu-id="1817a-319">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-320">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-320">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-321">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-321">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-322">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-322">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-323">No</span><span class="sxs-lookup"><span data-stu-id="1817a-323">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-324">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-324">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-325">No</span><span class="sxs-lookup"><span data-stu-id="1817a-325">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-326">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-326">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-327">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-327">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-328">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-328">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-329">Tutti</span><span class="sxs-lookup"><span data-stu-id="1817a-329">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-330">*JET_paramMaxVerPages*</span><span class="sxs-lookup"><span data-stu-id="1817a-330">*JET_paramMaxVerPages*</span></span>  
<span data-ttu-id="1817a-331">9</span><span class="sxs-lookup"><span data-stu-id="1817a-331">9</span></span>  

<span data-ttu-id="1817a-332">Questo parametro riserva il numero richiesto di pagine dell'archivio versioni per l'utilizzo da parte di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="1817a-332">This parameter reserves the requested number of version store pages for use by an instance.</span></span> <span data-ttu-id="1817a-333">L'archivio versione include un record live di tutte le diverse versioni di ogni voce di record o di indice nel database che possono essere visualizzate da tutte le transazioni attive.</span><span class="sxs-lookup"><span data-stu-id="1817a-333">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="1817a-334">Queste versioni vengono utilizzate per supportare il controllo della concorrenza multiversione utilizzato dal motore di database per supportare le transazioni mediante l'isolamento dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="1817a-334">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="1817a-335">Questa impostazione influirà sul numero di aggiornamenti che possono essere conservati in memoria alla volta.</span><span class="sxs-lookup"><span data-stu-id="1817a-335">This setting will affect how many updates can be held in memory at a time.</span></span> <span data-ttu-id="1817a-336">Ciò a sua volta influirà sul numero massimo di aggiornamenti che possono essere eseguiti da una singola transazione, sulla durata massima consentita di una transazione, sul carico simultaneo massimo per l'aggiornamento delle transazioni nel sistema o su una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="1817a-336">This in turn will affect either the maximum number of updates a single transaction can perform, the maximum duration a transaction can be held open, the maximum concurrent load of updating transactions on the system, or a combination of these.</span></span>

<span data-ttu-id="1817a-337">Ogni pagina dell'archivio delle versioni configurata da questo parametro ha dimensioni di 16KB nei computer a 32 bit e 32 KB su computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="1817a-337">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="1817a-338">**Windows Vista e versioni successive:**  Le dimensioni della pagina dell'archivio versioni possono essere lette e modificate tramite JET_paramVerPageSize.</span><span class="sxs-lookup"><span data-stu-id="1817a-338">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="1817a-339">**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzeranno lo spazio di indirizzi e potrebbero aumentare l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="1817a-339">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="1817a-340">**Nota**  Si tratta di una risorsa di gran lunga più comune da esaurire con il motore di database.</span><span class="sxs-lookup"><span data-stu-id="1817a-340">**Note**  This is by far the most common resource to be exhausted by the database engine.</span></span> <span data-ttu-id="1817a-341">È necessario prestare attenzione all'impostazione del parametro di sistema e al carico transazionale dell'applicazione per evitare che questa risorsa venga esaurita in base al normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="1817a-341">Careful attention must be paid to the setting of the system parameter and to the transactional load of the application to avoid exhausting this resource under normal operation.</span></span> <span data-ttu-id="1817a-342">Quando questa risorsa viene esaurita, gli aggiornamenti al database verranno rifiutati con JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="1817a-342">When this resource is exhausted, updates to the database will be rejected with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="1817a-343">Per rilasciare alcune di queste risorse, è necessario interrompere la transazione in attesa meno recente.</span><span class="sxs-lookup"><span data-stu-id="1817a-343">To release some of these resources, the oldest outstanding transaction must be aborted.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-344">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-344">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-345">64</span><span class="sxs-lookup"><span data-stu-id="1817a-345">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-346">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-346">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-347">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-347">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-348">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-348">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-349">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="1817a-349">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-350">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-350">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-351">Istanza</span><span class="sxs-lookup"><span data-stu-id="1817a-351">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-352">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-352">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-353">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-353">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-354">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-354">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-355">No</span><span class="sxs-lookup"><span data-stu-id="1817a-355">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-356">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-356">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-357">No</span><span class="sxs-lookup"><span data-stu-id="1817a-357">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-358">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-358">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-359">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-359">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-360">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-360">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-361">No</span><span class="sxs-lookup"><span data-stu-id="1817a-361">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-362">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-362">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-363">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-363">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-364">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-364">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-365">Tutti</span><span class="sxs-lookup"><span data-stu-id="1817a-365">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-366">*JET_paramPageHintCacheSize*</span><span class="sxs-lookup"><span data-stu-id="1817a-366">*JET_paramPageHintCacheSize*</span></span>  
<span data-ttu-id="1817a-367">101</span><span class="sxs-lookup"><span data-stu-id="1817a-367">101</span></span>  

<span data-ttu-id="1817a-368">Questo parametro controlla la dimensione di una cache speciale utilizzata per accelerare la ricerca dei puntatori di pagina figlio dell'albero B + nella cache delle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="1817a-368">This parameter controls the size of a special cache used to accelerate the lookup of B+ Tree child page pointers in the database page cache.</span></span> <span data-ttu-id="1817a-369">Le dimensioni della cache sono in byte.</span><span class="sxs-lookup"><span data-stu-id="1817a-369">The size of the cache is in bytes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-370">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-370">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-371">262144</span><span class="sxs-lookup"><span data-stu-id="1817a-371">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-372">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-372">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-373">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-373">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-374">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-374">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-375">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="1817a-375">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-376">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-376">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-377">Globale</span><span class="sxs-lookup"><span data-stu-id="1817a-377">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-378">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-378">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-379">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-379">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-380">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-380">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-381">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-381">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-382">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-382">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-383">No</span><span class="sxs-lookup"><span data-stu-id="1817a-383">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-384">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-384">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-385">No</span><span class="sxs-lookup"><span data-stu-id="1817a-385">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-386">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-386">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-387">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-387">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-388">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-388">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-389">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-389">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-390">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-390">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-391">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="1817a-391">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-392">*JET_paramPreferredMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="1817a-392">*JET_paramPreferredMaxOpenTables*</span></span>  
<span data-ttu-id="1817a-393">7</span><span class="sxs-lookup"><span data-stu-id="1817a-393">7</span></span>  

<span data-ttu-id="1817a-394">Questo parametro tenta di evitare il numero di risorse dell'albero B + in uso al di sotto della soglia specificata.</span><span class="sxs-lookup"><span data-stu-id="1817a-394">This parameter attempts to keep the number of B+ Tree resources in use below the specified threshold.</span></span>

<span data-ttu-id="1817a-395">Se questo parametro è impostato su zero, il valore predefinito sarà pari al 100% del **JET_paramMaxOpenTables**.</span><span class="sxs-lookup"><span data-stu-id="1817a-395">If this parameter is set to zero then it will default to 100% of **JET_paramMaxOpenTables**.</span></span>

<span data-ttu-id="1817a-396">**Windows Vista e versioni successive:**  Questo parametro è obsoleto e non influisce sul funzionamento del motore di database.</span><span class="sxs-lookup"><span data-stu-id="1817a-396">**Windows Vista and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span> <span data-ttu-id="1817a-397">Le applicazioni devono invece usare JET_paramMaxCachedClosedTables.</span><span class="sxs-lookup"><span data-stu-id="1817a-397">Applications should use JET_paramMaxCachedClosedTables instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-398">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-398">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-399">0 (100% di <strong>JET_paramMaxOpenTables</strong>)</span><span class="sxs-lookup"><span data-stu-id="1817a-399">0 (100% of <strong>JET_paramMaxOpenTables</strong>)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-400">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-400">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-401">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-401">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-402">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-402">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-403">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="1817a-403">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-404">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-404">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-405">Istanza</span><span class="sxs-lookup"><span data-stu-id="1817a-405">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-406">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-406">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-407">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-407">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-408">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-408">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-409">No</span><span class="sxs-lookup"><span data-stu-id="1817a-409">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-410">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-410">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-411">No</span><span class="sxs-lookup"><span data-stu-id="1817a-411">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-412">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-412">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-413">No</span><span class="sxs-lookup"><span data-stu-id="1817a-413">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-414">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-414">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-415">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-415">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-416">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-416">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-417">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-417">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-418">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-418">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-419">Tutti</span><span class="sxs-lookup"><span data-stu-id="1817a-419">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-420">*JET_paramPreferredVerPages*</span><span class="sxs-lookup"><span data-stu-id="1817a-420">*JET_paramPreferredVerPages*</span></span>  
<span data-ttu-id="1817a-421">63</span><span class="sxs-lookup"><span data-stu-id="1817a-421">63</span></span>  

<span data-ttu-id="1817a-422">Questo parametro rappresenta una soglia relativa ai **JET_paramMaxVerPages** che controlla l'utilizzo discrezionale delle pagine della versione da parte del motore di database.</span><span class="sxs-lookup"><span data-stu-id="1817a-422">This parameter represents a threshold relative to **JET_paramMaxVerPages** that controls the discretionary use of version pages by the database engine.</span></span> <span data-ttu-id="1817a-423">Se la dimensione dell'archivio versioni supera questa soglia, le informazioni utilizzate solo per le attività in background facoltative, ad esempio il ripristino dello spazio eliminato nel database, vengono invece sacrificate per mantenere la stanza per le informazioni transazionali.</span><span class="sxs-lookup"><span data-stu-id="1817a-423">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="1817a-424">**Windows 2000, Windows XP e Windows Server 2003:**  Impostando questo parametro su zero, la soglia sarà pari al 90% del **JET_paramMaxVerPages**.</span><span class="sxs-lookup"><span data-stu-id="1817a-424">**Windows 2000, Windows XP and Windows Server 2003:**  Setting this parameter to zero would set the threshold to be 90% of **JET_paramMaxVerPages**.</span></span>

<span data-ttu-id="1817a-425">**Windows Vista e versioni successive:**  Questa operazione non è più supportata e il valore predefinito di questo parametro è stato modificato per chiarirne il comportamento.</span><span class="sxs-lookup"><span data-stu-id="1817a-425">**Windows Vista and later:**  This is no longer supported and the default value of this parameter was changed to clarify its behavior.</span></span>

<span data-ttu-id="1817a-426">Ogni pagina dell'archivio delle versioni configurata da questo parametro ha dimensioni di 16KB nei computer a 32 bit e 32 KB su computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="1817a-426">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="1817a-427">**Windows Vista e versioni successive:**  Le dimensioni della pagina dell'archivio versioni possono essere lette e modificate tramite JET_paramVerPageSize.</span><span class="sxs-lookup"><span data-stu-id="1817a-427">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="1817a-428">**Nota**  Se il motore di database opera al di sopra di questa soglia troppo spesso, è possibile che si verifichi un peggioramento delle prestazioni del database.</span><span class="sxs-lookup"><span data-stu-id="1817a-428">**Note**  If the database engine operates above this threshold too often then it is possible for the database to degrade in performance.</span></span> <span data-ttu-id="1817a-429">Ciò accade perché i processi in background che puliscono il database non possono funzionare senza le informazioni facoltative che vengono eliminate in questo scenario.</span><span class="sxs-lookup"><span data-stu-id="1817a-429">This happens because the background processes that clean up the database cannot function without the optional information that is thrown away in this scenario.</span></span> <span data-ttu-id="1817a-430">La deframmentazione in linea o non in linea condurrà questo effetto.</span><span class="sxs-lookup"><span data-stu-id="1817a-430">Online or offline defragmentation will counteract this effect.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-431">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-431">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-432"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  0 (90% di JET_paramMaxVerPages)</span><span class="sxs-lookup"><span data-stu-id="1817a-432"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 (90% of JET_paramMaxVerPages)</span></span></p>
<p><span data-ttu-id="1817a-433"><strong>Windows Vista:</strong>  58</span><span class="sxs-lookup"><span data-stu-id="1817a-433"><strong>Windows Vista:</strong>  58</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-434">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-434">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-435">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-435">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-436">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-436">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-437">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="1817a-437">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-438">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-438">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-439">Istanza</span><span class="sxs-lookup"><span data-stu-id="1817a-439">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-440">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-440">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-441">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-442">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-442">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-443">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-444">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-444">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-445">No</span><span class="sxs-lookup"><span data-stu-id="1817a-445">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-446">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-446">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-447">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-447">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-448">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-448">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-449">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-449">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-450">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-450">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-451">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-451">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-452">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-452">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-453">Tutti</span><span class="sxs-lookup"><span data-stu-id="1817a-453">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-454">*JET_paramVerPageSize*</span><span class="sxs-lookup"><span data-stu-id="1817a-454">*JET_paramVerPageSize*</span></span>  
<span data-ttu-id="1817a-455">128</span><span class="sxs-lookup"><span data-stu-id="1817a-455">128</span></span>  

<span data-ttu-id="1817a-456">Questo parametro controlla la dimensione delle pagine dell'archivio versioni utilizzate dal motore di database per contenere informazioni transazionali.</span><span class="sxs-lookup"><span data-stu-id="1817a-456">This parameter controls the size of the version store pages used by the database engine to hold transactional information.</span></span> <span data-ttu-id="1817a-457">Il valore di questo parametro corrisponde alla dimensione dell'unità per tutti gli altri parametri di sistema in termini di pagine di versione, ad esempio JET_paramMaxVerPages.</span><span class="sxs-lookup"><span data-stu-id="1817a-457">The value of this parameter is the unit size for all the other system parameters that are in terms of version pages (e.g. JET_paramMaxVerPages).</span></span>

<span data-ttu-id="1817a-458">Il motore di database può scegliere di utilizzare una dimensione di pagina di archivio versioni più grande rispetto a quella richiesta.</span><span class="sxs-lookup"><span data-stu-id="1817a-458">The database engine may choose to use a larger version store page size than requested.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-459">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-459">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-460">16384</span><span class="sxs-lookup"><span data-stu-id="1817a-460">16384</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-461">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-461">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-462">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-462">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-463">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-463">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span><span class="sxs-lookup"><span data-stu-id="1817a-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-465">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-465">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-466">Globale</span><span class="sxs-lookup"><span data-stu-id="1817a-466">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-467">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-467">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-468">No</span><span class="sxs-lookup"><span data-stu-id="1817a-468">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-469">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-469">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-470">No</span><span class="sxs-lookup"><span data-stu-id="1817a-470">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-471">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-471">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-472">No</span><span class="sxs-lookup"><span data-stu-id="1817a-472">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-473">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-473">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-474">No</span><span class="sxs-lookup"><span data-stu-id="1817a-474">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-475">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-475">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-476">No</span><span class="sxs-lookup"><span data-stu-id="1817a-476">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-477">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-477">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-478">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-478">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-479">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-479">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-480">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="1817a-480">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1817a-481">*JET_paramVersionStoreTaskQueueMax*</span><span class="sxs-lookup"><span data-stu-id="1817a-481">*JET_paramVersionStoreTaskQueueMax*</span></span>  
<span data-ttu-id="1817a-482">105</span><span class="sxs-lookup"><span data-stu-id="1817a-482">105</span></span>  

<span data-ttu-id="1817a-483">Questo parametro controlla il numero di elementi di lavoro di pulitura in background che possono essere accodati al pool di thread del motore di database in un momento qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="1817a-483">This parameter controls the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-484">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="1817a-484">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="1817a-485">32</span><span class="sxs-lookup"><span data-stu-id="1817a-485">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-486">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1817a-486">Type:</span></span></p></td>
<td><p><span data-ttu-id="1817a-487">Integer</span><span class="sxs-lookup"><span data-stu-id="1817a-487">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-488">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="1817a-488">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="1817a-489"><strong>Windows XP e Windows Server 2003:  </strong>  1 – 63</span><span class="sxs-lookup"><span data-stu-id="1817a-489"><strong>Windows XP and Windows Server 2003:  </strong>  1 – 63</span></span></p>
<p><span data-ttu-id="1817a-490"><strong>Windows Vista:</strong>  1 – 127</span><span class="sxs-lookup"><span data-stu-id="1817a-490"><strong>Windows Vista:</strong>  1 – 127</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-491">Ambito:</span><span class="sxs-lookup"><span data-stu-id="1817a-491">Scope:</span></span></p></td>
<td><p><span data-ttu-id="1817a-492">Istanza</span><span class="sxs-lookup"><span data-stu-id="1817a-492">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-493">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-493">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-494">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-494">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-495">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="1817a-495">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="1817a-496"><strong>Windows XP e Windows Server 2003:  </strong>  No</span><span class="sxs-lookup"><span data-stu-id="1817a-496"><strong>Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="1817a-497"><strong>Windows Vista:</strong>  Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-497"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-498">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="1817a-498">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="1817a-499">No</span><span class="sxs-lookup"><span data-stu-id="1817a-499">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-500">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-500">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-501">No</span><span class="sxs-lookup"><span data-stu-id="1817a-501">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-502">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="1817a-502">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="1817a-503">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-503">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-504">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="1817a-504">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="1817a-505">Sì</span><span class="sxs-lookup"><span data-stu-id="1817a-505">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-506">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="1817a-506">Availability:</span></span></p></td>
<td><p><span data-ttu-id="1817a-507">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="1817a-507">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="1817a-508">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1817a-508">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1817a-509"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1817a-509"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1817a-510">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1817a-510">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1817a-511"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1817a-511"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1817a-512">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1817a-512">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1817a-513"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="1817a-513"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1817a-514">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="1817a-514">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="1817a-515">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1817a-515">See Also</span></span>

[<span data-ttu-id="1817a-516">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="1817a-516">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="1817a-517">JetInit</span><span class="sxs-lookup"><span data-stu-id="1817a-517">JetInit</span></span>](./jetinit-function.md)
