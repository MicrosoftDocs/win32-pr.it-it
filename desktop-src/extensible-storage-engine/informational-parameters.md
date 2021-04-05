---
description: 'Ulteriori informazioni su: parametri informativi'
title: Parametri informativi
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753319"
---
# <a name="informational-parameters"></a><span data-ttu-id="21e74-103">Parametri informativi</span><span class="sxs-lookup"><span data-stu-id="21e74-103">Informational Parameters</span></span>


<span data-ttu-id="21e74-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="21e74-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="informational-parameters"></a><span data-ttu-id="21e74-105">Parametri informativi</span><span class="sxs-lookup"><span data-stu-id="21e74-105">Informational Parameters</span></span>

<span data-ttu-id="21e74-106">Questo argomento contiene i parametri usati per esporre le informazioni sul motore di database.</span><span class="sxs-lookup"><span data-stu-id="21e74-106">This topic contains parameters that are used to expose information about the database engine.</span></span>

<span data-ttu-id="21e74-107">*JET_paramKeyMost*</span><span class="sxs-lookup"><span data-stu-id="21e74-107">*JET_paramKeyMost*</span></span>  
<span data-ttu-id="21e74-108">134</span><span class="sxs-lookup"><span data-stu-id="21e74-108">134</span></span>  

<span data-ttu-id="21e74-109">Questo parametro di sola lettura indica la lunghezza massima consentita della chiave di indice che è possibile selezionare per le dimensioni correnti della pagina del database (come configurato dal JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="21e74-109">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by JET_paramDatabasePageSize).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21e74-110">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="21e74-110">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="21e74-111">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="21e74-111">JET_cbKeyMost4KBytePage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-112">Digitare:</span><span class="sxs-lookup"><span data-stu-id="21e74-112">Type:</span></span></p></td>
<td><p><span data-ttu-id="21e74-113">Integer</span><span class="sxs-lookup"><span data-stu-id="21e74-113">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-114">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="21e74-114">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="21e74-115">255 – 65535</span><span class="sxs-lookup"><span data-stu-id="21e74-115">255 – 65535</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-116">Ambito:</span><span class="sxs-lookup"><span data-stu-id="21e74-116">Scope:</span></span></p></td>
<td><p><span data-ttu-id="21e74-117">Globale</span><span class="sxs-lookup"><span data-stu-id="21e74-117">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-118">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="21e74-118">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="21e74-119">N/D</span><span class="sxs-lookup"><span data-stu-id="21e74-119">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-120">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="21e74-120">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="21e74-121">N/D</span><span class="sxs-lookup"><span data-stu-id="21e74-121">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-122">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="21e74-122">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="21e74-123">No</span><span class="sxs-lookup"><span data-stu-id="21e74-123">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-124">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="21e74-124">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="21e74-125">No</span><span class="sxs-lookup"><span data-stu-id="21e74-125">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-126">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="21e74-126">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="21e74-127">No</span><span class="sxs-lookup"><span data-stu-id="21e74-127">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-128">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="21e74-128">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="21e74-129">No</span><span class="sxs-lookup"><span data-stu-id="21e74-129">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-130">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="21e74-130">Availability:</span></span></p></td>
<td><p><span data-ttu-id="21e74-131">A partire da Windows Server 2008 e Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21e74-131">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="21e74-132">*JET_paramMaxColtyp*</span><span class="sxs-lookup"><span data-stu-id="21e74-132">*JET_paramMaxColtyp*</span></span>  
<span data-ttu-id="21e74-133">131</span><span class="sxs-lookup"><span data-stu-id="21e74-133">131</span></span>  

<span data-ttu-id="21e74-134">Questo parametro di sola lettura restituisce la [JET_COLTYP](./jet-coltyp.md) massima (JET_coltypMax) per la versione del motore di database.</span><span class="sxs-lookup"><span data-stu-id="21e74-134">This read only parameter returns the maximum [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) for that version of the database engine.</span></span> <span data-ttu-id="21e74-135">Questo valore può essere utilizzato per verificare il supporto di un [JET_COLTYP](./jet-coltyp.md)specifico.</span><span class="sxs-lookup"><span data-stu-id="21e74-135">This value can be used to test for support of a specific [JET_COLTYP](./jet-coltyp.md).</span></span> <span data-ttu-id="21e74-136">Se un [JET_COLTYP](./jet-coltyp.md) specificato è minore del valore di questo parametro, è supportato dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="21e74-136">If a given [JET_COLTYP](./jet-coltyp.md) is less than the value of this parameter then it is supported by the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21e74-137">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="21e74-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="21e74-138">JET_coltypUnsignedShort + 1</span><span class="sxs-lookup"><span data-stu-id="21e74-138">JET_coltypUnsignedShort + 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-139">Digitare:</span><span class="sxs-lookup"><span data-stu-id="21e74-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="21e74-140">Integer</span><span class="sxs-lookup"><span data-stu-id="21e74-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-141">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="21e74-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="21e74-142">0 – 255</span><span class="sxs-lookup"><span data-stu-id="21e74-142">0 – 255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-143">Ambito:</span><span class="sxs-lookup"><span data-stu-id="21e74-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="21e74-144">Globale</span><span class="sxs-lookup"><span data-stu-id="21e74-144">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-145">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="21e74-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="21e74-146">N/D</span><span class="sxs-lookup"><span data-stu-id="21e74-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-147">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="21e74-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="21e74-148">N/D</span><span class="sxs-lookup"><span data-stu-id="21e74-148">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-149">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="21e74-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="21e74-150">No</span><span class="sxs-lookup"><span data-stu-id="21e74-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-151">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="21e74-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="21e74-152">No</span><span class="sxs-lookup"><span data-stu-id="21e74-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-153">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="21e74-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="21e74-154">No</span><span class="sxs-lookup"><span data-stu-id="21e74-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-155">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="21e74-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="21e74-156">No</span><span class="sxs-lookup"><span data-stu-id="21e74-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-157">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="21e74-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="21e74-158">A partire da Windows Server 2008 e Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21e74-158">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="21e74-159">*JET_paramLVChunkSizeMost*</span><span class="sxs-lookup"><span data-stu-id="21e74-159">*JET_paramLVChunkSizeMost*</span></span>  
<span data-ttu-id="21e74-160">163</span><span class="sxs-lookup"><span data-stu-id="21e74-160">163</span></span>  

<span data-ttu-id="21e74-161">Parametro di sola lettura che restituisce la dimensione del blocco di valore Long in base alle dimensioni di pagina configurate.</span><span class="sxs-lookup"><span data-stu-id="21e74-161">Read only parameter that returns the long-value chunk size based on configured page size.</span></span> <span data-ttu-id="21e74-162">Se è necessario leggere o scrivere un valore Long con più chiamate jet {set, retrieve}, utilizzare un buffer le cui dimensioni sono un multiplo della dimensione del blocco è più efficiente.</span><span class="sxs-lookup"><span data-stu-id="21e74-162">If a long-value is to be read or written with multiple Jet{Set,Retrieve}Column calls then using a buffer whose size is a multiple of the chunk size is more efficient.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21e74-163">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="21e74-163">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="21e74-164">Pagina 2 KB = 1966 byte</span><span class="sxs-lookup"><span data-stu-id="21e74-164">2kb page = 1966 bytes</span></span><br />
<span data-ttu-id="21e74-165">pagina 4KB = 4014 byte</span><span class="sxs-lookup"><span data-stu-id="21e74-165">4kb page = 4014 bytes</span></span><br />
<span data-ttu-id="21e74-166">pagina 8KB = 8110 byte</span><span class="sxs-lookup"><span data-stu-id="21e74-166">8kb page = 8110 bytes</span></span><br />
<span data-ttu-id="21e74-167">pagina 16KB = 4050 byte</span><span class="sxs-lookup"><span data-stu-id="21e74-167">16kb page = 4050 bytes</span></span><br />
<span data-ttu-id="21e74-168">pagina 32 KB = 8150 byte</span><span class="sxs-lookup"><span data-stu-id="21e74-168">32kb page = 8150 bytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-169">Digitare:</span><span class="sxs-lookup"><span data-stu-id="21e74-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="21e74-170">Integer</span><span class="sxs-lookup"><span data-stu-id="21e74-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-171">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="21e74-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="21e74-172">0-10000</span><span class="sxs-lookup"><span data-stu-id="21e74-172">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-173">Ambito:</span><span class="sxs-lookup"><span data-stu-id="21e74-173">Scope:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-174">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="21e74-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-175">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="21e74-175">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-176">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="21e74-176">Affects Physical Layout:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-177">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="21e74-177">Affects Reliability:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-178">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="21e74-178">Affects Performance:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-179">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="21e74-179">Affects Resources:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-180">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="21e74-180">Availability:</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="21e74-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21e74-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21e74-182"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="21e74-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="21e74-183">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="21e74-183">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e74-184"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="21e74-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="21e74-185">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="21e74-185">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e74-186"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="21e74-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="21e74-187">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="21e74-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="21e74-188">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="21e74-188">See Also</span></span>

[<span data-ttu-id="21e74-189">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="21e74-189">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="21e74-190">JetInit</span><span class="sxs-lookup"><span data-stu-id="21e74-190">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="21e74-191">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="21e74-191">JET_COLTYP</span></span>](./jet-coltyp.md)
