---
description: 'Altre informazioni su: parametri di callback'
title: Parametri di callback
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
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
ms.openlocfilehash: 4e06ed65bbeae195060e4de10424a76a4228f20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130211"
---
# <a name="callback-parameters"></a><span data-ttu-id="cc35d-103">Parametri di callback</span><span class="sxs-lookup"><span data-stu-id="cc35d-103">Callback Parameters</span></span>


<span data-ttu-id="cc35d-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cc35d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="callback-parameters"></a><span data-ttu-id="cc35d-105">Parametri di callback</span><span class="sxs-lookup"><span data-stu-id="cc35d-105">Callback Parameters</span></span>

<span data-ttu-id="cc35d-106">Questo argomento contiene i parametri usati per i callback.</span><span class="sxs-lookup"><span data-stu-id="cc35d-106">This topic contains parameters that are used for callbacks.</span></span>

<span data-ttu-id="cc35d-107">*JET_paramDisableCallbacks*</span><span class="sxs-lookup"><span data-stu-id="cc35d-107">*JET_paramDisableCallbacks*</span></span>  
<span data-ttu-id="cc35d-108">65</span><span class="sxs-lookup"><span data-stu-id="cc35d-108">65</span></span>  

<span data-ttu-id="cc35d-109">Questo parametro Disabilita tutti i callback del motore di database alle funzioni fornite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc35d-109">This parameter disables all database engine callbacks to application provided functions.</span></span> <span data-ttu-id="cc35d-110">È progettato principalmente per supportare le utilità del motore di database e non può essere utilizzato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc35d-110">It is primarily intended to support the database engine utilities and is not intended to be used in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-111">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="cc35d-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-112">Falso</span><span class="sxs-lookup"><span data-stu-id="cc35d-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-113">Digitare:</span><span class="sxs-lookup"><span data-stu-id="cc35d-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="cc35d-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-115">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="cc35d-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-116">False, True</span><span class="sxs-lookup"><span data-stu-id="cc35d-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-117">Ambito:</span><span class="sxs-lookup"><span data-stu-id="cc35d-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-118">Istanza</span><span class="sxs-lookup"><span data-stu-id="cc35d-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-119">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cc35d-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-120">Sì</span><span class="sxs-lookup"><span data-stu-id="cc35d-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-121">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cc35d-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-122">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-123">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="cc35d-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-124">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-125">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="cc35d-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-126">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-127">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="cc35d-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-128">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-129">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="cc35d-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-130">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-131">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="cc35d-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-132">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="cc35d-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cc35d-133">*JET_paramEnablePersistedCallbacks*</span><span class="sxs-lookup"><span data-stu-id="cc35d-133">*JET_paramEnablePersistedCallbacks*</span></span>  
<span data-ttu-id="cc35d-134">156</span><span class="sxs-lookup"><span data-stu-id="cc35d-134">156</span></span>  

<span data-ttu-id="cc35d-135">Questo parametro consente di utilizzare callback permanenti nel database.</span><span class="sxs-lookup"><span data-stu-id="cc35d-135">This parameter enables the use of persistent callbacks in the database.</span></span> <span data-ttu-id="cc35d-136">Nelle versioni precedenti a Windows Vista, l'utilizzo di callback permanenti è stato abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cc35d-136">In releases prior to Windows Vista, the use of persistent callbacks was enabled by default.</span></span> <span data-ttu-id="cc35d-137">Le applicazioni devono ora abilitare in modo esplicito l'utilizzo di callback permanenti in fase di esecuzione utilizzando questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cc35d-137">Applications must now explicitly enable the use of persistent callbacks at runtime using this parameter.</span></span> <span data-ttu-id="cc35d-138">Se questo parametro non è impostato, tutte le operazioni di database che richiedono la chiamata di un callback avranno esito negativo con JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="cc35d-138">If this parameter is not set, then any database operation that requires the invocation of a callback will fail with JET_errCallbackFailed.</span></span> <span data-ttu-id="cc35d-139">Questo parametro non influisce sui callback specificati in fase di esecuzione con i meccanismi seguenti: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)o un parametro di callback esplicito a un'API Jet.</span><span class="sxs-lookup"><span data-stu-id="cc35d-139">This parameter does not affect any callbacks that are specified at runtime with the following mechanisms: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md), or an explicit callback parameter to a JET API.</span></span> <span data-ttu-id="cc35d-140">È comunque possibile creare elementi dello schema che contengono callback permanenti anche quando l'uso di tali callback permanenti non è consentito.</span><span class="sxs-lookup"><span data-stu-id="cc35d-140">It is still possible to create schema elements that contain persistent callbacks even when the use of those persistent callbacks is disallowed.</span></span> <span data-ttu-id="cc35d-141">Se questo parametro è impostato su false, sostituisce JET_paramDisableCallbacks.</span><span class="sxs-lookup"><span data-stu-id="cc35d-141">When this parameter is set to false it overrides JET_paramDisableCallbacks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-142">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="cc35d-142">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-143">Falso</span><span class="sxs-lookup"><span data-stu-id="cc35d-143">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-144">Digitare:</span><span class="sxs-lookup"><span data-stu-id="cc35d-144">Type:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="cc35d-145">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-146">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="cc35d-146">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-147">False, True</span><span class="sxs-lookup"><span data-stu-id="cc35d-147">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-148">Ambito:</span><span class="sxs-lookup"><span data-stu-id="cc35d-148">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-149">Istanza</span><span class="sxs-lookup"><span data-stu-id="cc35d-149">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-150">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cc35d-150">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-151">Sì</span><span class="sxs-lookup"><span data-stu-id="cc35d-151">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-152">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cc35d-152">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-153">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-154">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="cc35d-154">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-155">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-156">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="cc35d-156">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-157">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-158">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="cc35d-158">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-159">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-159">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-160">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="cc35d-160">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-161">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-161">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-162">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="cc35d-162">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-163">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="cc35d-163">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cc35d-164">*JET_paramRuntimeCallback*</span><span class="sxs-lookup"><span data-stu-id="cc35d-164">*JET_paramRuntimeCallback*</span></span>  
<span data-ttu-id="cc35d-165">73</span><span class="sxs-lookup"><span data-stu-id="cc35d-165">73</span></span>  

<span data-ttu-id="cc35d-166">Questo parametro configura il motore con una funzione di callback di runtime che implementa l'interfaccia [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cc35d-166">This parameter configures the engine with a runtime callback function implementing the [JET_CALLBACK](./jet-callback-callback-function.md) interface.</span></span> <span data-ttu-id="cc35d-167">Questo callback può essere chiamato per i motivi seguenti: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)o [JET_cbtypNull](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="cc35d-167">This callback may be called for the following reasons: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md), or [JET_cbtypNull](./jet-cbtyp.md).</span></span> <span data-ttu-id="cc35d-168">Per ulteriori informazioni, vedere [JetSetLS](./jetsetls-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cc35d-168">Please see [JetSetLS](./jetsetls-function.md) for more information.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-169">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="cc35d-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-170">NULL</span><span class="sxs-lookup"><span data-stu-id="cc35d-170">NULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-171">Digitare:</span><span class="sxs-lookup"><span data-stu-id="cc35d-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-172">Puntatore a funzione (JET_API_PTR)</span><span class="sxs-lookup"><span data-stu-id="cc35d-172">Function Pointer (JET_API_PTR)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-173">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="cc35d-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span><span class="sxs-lookup"><span data-stu-id="cc35d-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-175">Ambito:</span><span class="sxs-lookup"><span data-stu-id="cc35d-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-176">Istanza</span><span class="sxs-lookup"><span data-stu-id="cc35d-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-177">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cc35d-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-178">Sì</span><span class="sxs-lookup"><span data-stu-id="cc35d-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-179">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cc35d-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-180">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-181">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="cc35d-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-182">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-183">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="cc35d-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-184">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-185">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="cc35d-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-186">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-187">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="cc35d-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-188">No</span><span class="sxs-lookup"><span data-stu-id="cc35d-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-189">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="cc35d-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cc35d-190">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="cc35d-190">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="cc35d-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc35d-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cc35d-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cc35d-193">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc35d-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc35d-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cc35d-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cc35d-195">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cc35d-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc35d-196"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="cc35d-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cc35d-197">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="cc35d-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="cc35d-198">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cc35d-198">See Also</span></span>

[<span data-ttu-id="cc35d-199">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="cc35d-199">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="cc35d-200">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="cc35d-200">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="cc35d-201">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="cc35d-201">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="cc35d-202">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="cc35d-202">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="cc35d-203">JetInit</span><span class="sxs-lookup"><span data-stu-id="cc35d-203">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="cc35d-204">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="cc35d-204">JetSetLS</span></span>](./jetsetls-function.md)
