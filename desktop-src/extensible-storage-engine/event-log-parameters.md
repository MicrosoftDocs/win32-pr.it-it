---
description: 'Altre informazioni su: parametri del registro eventi'
title: Parametri del registro eventi
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
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
ms.openlocfilehash: 912dc3e1e8588e18ef0d1db8fbf7edccfca7bdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050199"
---
# <a name="event-log-parameters"></a><span data-ttu-id="d35e8-103">Parametri del registro eventi</span><span class="sxs-lookup"><span data-stu-id="d35e8-103">Event Log Parameters</span></span>


<span data-ttu-id="d35e8-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d35e8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="event-log-parameters"></a><span data-ttu-id="d35e8-105">Parametri del registro eventi</span><span class="sxs-lookup"><span data-stu-id="d35e8-105">Event Log Parameters</span></span>

<span data-ttu-id="d35e8-106">Questo argomento contiene i parametri usati per il registro eventi.</span><span class="sxs-lookup"><span data-stu-id="d35e8-106">This topic contains parameters that are used for the event log.</span></span>

<span data-ttu-id="d35e8-107">JET_paramEventLogCache</span><span class="sxs-lookup"><span data-stu-id="d35e8-107">JET_paramEventLogCache</span></span>  
<span data-ttu-id="d35e8-108">Questo parametro controlla la dimensione (in byte) di una cache dei messaggi del registro eventi che conterrà i messaggi del log eventi emessi dal motore di database mentre il servizio EventLog viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="d35e8-108">This parameter controls the size (in bytes) of an eventlog message cache that will hold eventlog messages emitted by the database engine while the eventlog service is stopped.</span></span> <span data-ttu-id="d35e8-109">Questi messaggi memorizzati nella cache verranno scaricati nel log eventi quando il servizio diventa operativo.</span><span class="sxs-lookup"><span data-stu-id="d35e8-109">These cached messages will be flushed to the eventlog when the service becomes operational.</span></span> <span data-ttu-id="d35e8-110">Tutti i messaggi che hanno overflow la cache verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="d35e8-110">Any messages that overflow the cache will be dropped.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-111">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="d35e8-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-112">0</span><span class="sxs-lookup"><span data-stu-id="d35e8-112">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-113">Digitare:</span><span class="sxs-lookup"><span data-stu-id="d35e8-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-114">Integer</span><span class="sxs-lookup"><span data-stu-id="d35e8-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-115">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="d35e8-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-116">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="d35e8-116">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-117">Ambito:</span><span class="sxs-lookup"><span data-stu-id="d35e8-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-118">Globale</span><span class="sxs-lookup"><span data-stu-id="d35e8-118">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-119">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35e8-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-120">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-121">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35e8-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-122">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-123">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="d35e8-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-124">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-125">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="d35e8-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-126">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-127">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="d35e8-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-128">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-129">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="d35e8-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-130">Sì</span><span class="sxs-lookup"><span data-stu-id="d35e8-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-131">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="d35e8-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-132">Tutti</span><span class="sxs-lookup"><span data-stu-id="d35e8-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35e8-133">*JET_paramEventLoggingLevel*</span><span class="sxs-lookup"><span data-stu-id="d35e8-133">*JET_paramEventLoggingLevel*</span></span>  
  
<span data-ttu-id="d35e8-134">Questo parametro consente di configurare il livello di dettaglio dei messaggi EventLog emessi al log eventi dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="d35e8-134">This parameter configures the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="d35e8-135">I numeri più alti comporteranno messaggi EventLog più dettagliati.</span><span class="sxs-lookup"><span data-stu-id="d35e8-135">Higher numbers will result in more detailed eventlog messages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-136">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="d35e8-136">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-137">JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="d35e8-137">JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-138">Digitare:</span><span class="sxs-lookup"><span data-stu-id="d35e8-138">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-139">Integer</span><span class="sxs-lookup"><span data-stu-id="d35e8-139">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-140">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="d35e8-140">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-141">JET_EventLoggingDisable-JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="d35e8-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-142">Ambito:</span><span class="sxs-lookup"><span data-stu-id="d35e8-142">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-143">Istanza</span><span class="sxs-lookup"><span data-stu-id="d35e8-143">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-144">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35e8-144">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-145">Sì</span><span class="sxs-lookup"><span data-stu-id="d35e8-145">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-146">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35e8-146">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-147">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-147">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-148">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="d35e8-148">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-149">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-150">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="d35e8-150">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-151">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-151">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-152">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="d35e8-152">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-153">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-154">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="d35e8-154">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-155">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-155">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-156">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="d35e8-156">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-157">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="d35e8-157">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35e8-158">*JET_paramEventSource*</span><span class="sxs-lookup"><span data-stu-id="d35e8-158">*JET_paramEventSource*</span></span>  
<span data-ttu-id="d35e8-159">4</span><span class="sxs-lookup"><span data-stu-id="d35e8-159">4</span></span>  

<span data-ttu-id="d35e8-160">Questo parametro fornisce una stringa specifica dell'applicazione che verrà aggiunta a qualsiasi messaggio del registro eventi emesso dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="d35e8-160">This parameter supplies an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="d35e8-161">In questo modo è possibile correlare facilmente i messaggi del log eventi con l'applicazione di origine.</span><span class="sxs-lookup"><span data-stu-id="d35e8-161">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="d35e8-162">Se viene specificata una stringa vuota (come il valore predefinito), verrà usato il nome dell'eseguibile dell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="d35e8-162">If an empty string is specified (as is the default) then the host application executable name will be used.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-163">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="d35e8-163">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-164">Digitare:</span><span class="sxs-lookup"><span data-stu-id="d35e8-164">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-165">string</span><span class="sxs-lookup"><span data-stu-id="d35e8-165">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-166">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="d35e8-166">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-167">da 0 a 259 caratteri</span><span class="sxs-lookup"><span data-stu-id="d35e8-167">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-168">Ambito:</span><span class="sxs-lookup"><span data-stu-id="d35e8-168">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-169">Istanza</span><span class="sxs-lookup"><span data-stu-id="d35e8-169">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-170">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35e8-170">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-171">Sì</span><span class="sxs-lookup"><span data-stu-id="d35e8-171">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-172">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35e8-172">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-173">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-173">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-174">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="d35e8-174">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-175">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-175">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-176">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="d35e8-176">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-177">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-178">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="d35e8-178">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-179">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-180">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="d35e8-180">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-181">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-182">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="d35e8-182">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-183">Tutti</span><span class="sxs-lookup"><span data-stu-id="d35e8-183">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35e8-184">*JET_paramEventSourceKey*</span><span class="sxs-lookup"><span data-stu-id="d35e8-184">*JET_paramEventSourceKey*</span></span>  
<span data-ttu-id="d35e8-185">49</span><span class="sxs-lookup"><span data-stu-id="d35e8-185">49</span></span>  

<span data-ttu-id="d35e8-186">Questo parametro può essere utilizzato per controllare il registro eventi utilizzato dal motore di database per i messaggi del log eventi.</span><span class="sxs-lookup"><span data-stu-id="d35e8-186">This parameter can be used to control which event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="d35e8-187">Per impostazione predefinita, tutti i messaggi del registro eventi vengono inviati al registro eventi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d35e8-187">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="d35e8-188">Se viene configurato il nome della chiave del registro di sistema per un altro log eventi, i messaggi del registro eventi verranno invece inseriti.</span><span class="sxs-lookup"><span data-stu-id="d35e8-188">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-189">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="d35e8-189">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-190">Digitare:</span><span class="sxs-lookup"><span data-stu-id="d35e8-190">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-191">string</span><span class="sxs-lookup"><span data-stu-id="d35e8-191">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-192">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="d35e8-192">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-193">da 0 a 259 caratteri</span><span class="sxs-lookup"><span data-stu-id="d35e8-193">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-194">Ambito:</span><span class="sxs-lookup"><span data-stu-id="d35e8-194">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-195">Istanza</span><span class="sxs-lookup"><span data-stu-id="d35e8-195">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-196">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35e8-196">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-197">Sì</span><span class="sxs-lookup"><span data-stu-id="d35e8-197">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-198">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35e8-198">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-199">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-199">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-200">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="d35e8-200">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-201">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-201">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-202">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="d35e8-202">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-203">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-203">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-204">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="d35e8-204">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-205">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-205">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-206">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="d35e8-206">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-207">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-208">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="d35e8-208">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-209">Tutti</span><span class="sxs-lookup"><span data-stu-id="d35e8-209">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35e8-210">*JET_paramNoInformationEvent*</span><span class="sxs-lookup"><span data-stu-id="d35e8-210">*JET_paramNoInformationEvent*</span></span>  
<span data-ttu-id="d35e8-211">50</span><span class="sxs-lookup"><span data-stu-id="d35e8-211">50</span></span>  

<span data-ttu-id="d35e8-212">Quando questo parametro è impostato su true, i messaggi del registro eventi informativi normalmente generati dal motore di database verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="d35e8-212">When this parameter is true, informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-213">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="d35e8-213">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-214">Falso</span><span class="sxs-lookup"><span data-stu-id="d35e8-214">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-215">Digitare:</span><span class="sxs-lookup"><span data-stu-id="d35e8-215">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="d35e8-216">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-217">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="d35e8-217">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-218">False, True</span><span class="sxs-lookup"><span data-stu-id="d35e8-218">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-219">Ambito:</span><span class="sxs-lookup"><span data-stu-id="d35e8-219">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-220">Istanza</span><span class="sxs-lookup"><span data-stu-id="d35e8-220">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-221">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35e8-221">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-222">Sì</span><span class="sxs-lookup"><span data-stu-id="d35e8-222">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-223">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35e8-223">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-224">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-224">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-225">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="d35e8-225">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-226">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-226">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-227">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="d35e8-227">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-228">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-228">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-229">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="d35e8-229">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-230">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-231">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="d35e8-231">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-232">No</span><span class="sxs-lookup"><span data-stu-id="d35e8-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-233">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="d35e8-233">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35e8-234">Tutti</span><span class="sxs-lookup"><span data-stu-id="d35e8-234">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="d35e8-235">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d35e8-235">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-236"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d35e8-236"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d35e8-237">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d35e8-237">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35e8-238"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d35e8-238"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d35e8-239">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d35e8-239">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35e8-240"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="d35e8-240"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d35e8-241">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="d35e8-241">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d35e8-242">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d35e8-242">See Also</span></span>

[<span data-ttu-id="d35e8-243">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="d35e8-243">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="d35e8-244">JetInit</span><span class="sxs-lookup"><span data-stu-id="d35e8-244">JetInit</span></span>](./jetinit-function.md)
