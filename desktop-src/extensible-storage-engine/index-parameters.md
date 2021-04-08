---
description: 'Altre informazioni su: parametri di indice'
title: Parametri dell'indice
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058292"
---
# <a name="index-parameters"></a><span data-ttu-id="faf13-103">Parametri dell'indice</span><span class="sxs-lookup"><span data-stu-id="faf13-103">Index Parameters</span></span>


<span data-ttu-id="faf13-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="faf13-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="index-parameters"></a><span data-ttu-id="faf13-105">Parametri dell'indice</span><span class="sxs-lookup"><span data-stu-id="faf13-105">Index Parameters</span></span>

<span data-ttu-id="faf13-106">Questo argomento contiene i parametri usati per l'indice.</span><span class="sxs-lookup"><span data-stu-id="faf13-106">This topic contains parameters that are used for the index.</span></span>

<span data-ttu-id="faf13-107">*JET_paramIndexTupleIncrement*</span><span class="sxs-lookup"><span data-stu-id="faf13-107">*JET_paramIndexTupleIncrement*</span></span>  
<span data-ttu-id="faf13-108">132</span><span class="sxs-lookup"><span data-stu-id="faf13-108">132</span></span>  

<span data-ttu-id="faf13-109">Questo parametro specifica l'impostazione predefinita per l'incremento di offset utilizzato per scorrere il valore della colonna di origine durante la generazione di ogni tupla.</span><span class="sxs-lookup"><span data-stu-id="faf13-109">This parameter specifies the default for the offset increment used to step through the source column value while generating each tuple.</span></span> <span data-ttu-id="faf13-110">Per ulteriori informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="faf13-110">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faf13-111">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="faf13-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faf13-112">1</span><span class="sxs-lookup"><span data-stu-id="faf13-112">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-113">Digitare:</span><span class="sxs-lookup"><span data-stu-id="faf13-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="faf13-114">Integer</span><span class="sxs-lookup"><span data-stu-id="faf13-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-115">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="faf13-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faf13-116">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="faf13-116">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-117">Ambito:</span><span class="sxs-lookup"><span data-stu-id="faf13-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faf13-118">Istanza</span><span class="sxs-lookup"><span data-stu-id="faf13-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-119">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-120">Sì</span><span class="sxs-lookup"><span data-stu-id="faf13-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-121">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-122">No</span><span class="sxs-lookup"><span data-stu-id="faf13-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-123">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="faf13-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faf13-124">No</span><span class="sxs-lookup"><span data-stu-id="faf13-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-125">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-126">No</span><span class="sxs-lookup"><span data-stu-id="faf13-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-127">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="faf13-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faf13-128">No</span><span class="sxs-lookup"><span data-stu-id="faf13-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-129">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="faf13-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faf13-130">No</span><span class="sxs-lookup"><span data-stu-id="faf13-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-131">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-132">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="faf13-132">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faf13-133">*JET_paramIndexTupleStart*</span><span class="sxs-lookup"><span data-stu-id="faf13-133">*JET_paramIndexTupleStart*</span></span>  
<span data-ttu-id="faf13-134">133</span><span class="sxs-lookup"><span data-stu-id="faf13-134">133</span></span>  

<span data-ttu-id="faf13-135">Questo parametro specifica il valore predefinito per l'offset nel valore della colonna di origine in corrispondenza del quale verrà avviata la generazione della tupla.</span><span class="sxs-lookup"><span data-stu-id="faf13-135">This parameter specifies the default for the offset in the source column value at which tuple generation will start.</span></span> <span data-ttu-id="faf13-136">Per ulteriori informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="faf13-136">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faf13-137">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="faf13-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faf13-138">0</span><span class="sxs-lookup"><span data-stu-id="faf13-138">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-139">Digitare:</span><span class="sxs-lookup"><span data-stu-id="faf13-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="faf13-140">Integer</span><span class="sxs-lookup"><span data-stu-id="faf13-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-141">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="faf13-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faf13-142">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="faf13-142">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-143">Ambito:</span><span class="sxs-lookup"><span data-stu-id="faf13-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faf13-144">Istanza</span><span class="sxs-lookup"><span data-stu-id="faf13-144">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-145">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-146">Sì</span><span class="sxs-lookup"><span data-stu-id="faf13-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-147">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-148">No</span><span class="sxs-lookup"><span data-stu-id="faf13-148">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-149">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="faf13-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faf13-150">No</span><span class="sxs-lookup"><span data-stu-id="faf13-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-151">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-152">No</span><span class="sxs-lookup"><span data-stu-id="faf13-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-153">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="faf13-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faf13-154">No</span><span class="sxs-lookup"><span data-stu-id="faf13-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-155">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="faf13-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faf13-156">No</span><span class="sxs-lookup"><span data-stu-id="faf13-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-157">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-158">Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="faf13-158">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faf13-159">*JET_paramIndexTuplesLengthMax*</span><span class="sxs-lookup"><span data-stu-id="faf13-159">*JET_paramIndexTuplesLengthMax*</span></span>  
<span data-ttu-id="faf13-160">111</span><span class="sxs-lookup"><span data-stu-id="faf13-160">111</span></span>  

<span data-ttu-id="faf13-161">Questo parametro specifica il valore predefinito per la lunghezza massima della tupla in un indice della tupla.</span><span class="sxs-lookup"><span data-stu-id="faf13-161">This parameter specifies the default for the maximum tuple length in a tuple index.</span></span> <span data-ttu-id="faf13-162">Per ulteriori informazioni, vedere la struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="faf13-162">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<span data-ttu-id="faf13-163">**Windows Vista:**  Prima di Windows Vista, impostando questo parametro su zero sarebbe stato impostato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="faf13-163">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="faf13-164">Per Windows Vista, questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="faf13-164">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faf13-165">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="faf13-165">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faf13-166">10</span><span class="sxs-lookup"><span data-stu-id="faf13-166">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-167">Digitare:</span><span class="sxs-lookup"><span data-stu-id="faf13-167">Type:</span></span></p></td>
<td><p><span data-ttu-id="faf13-168">Integer</span><span class="sxs-lookup"><span data-stu-id="faf13-168">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-169">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="faf13-169">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faf13-170"><strong>Windows 2000, Windows XP e Windows Server 2003: </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="faf13-170"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="faf13-171"><strong>Windows Vista:</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="faf13-171"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-172">Ambito:</span><span class="sxs-lookup"><span data-stu-id="faf13-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faf13-173">Istanza</span><span class="sxs-lookup"><span data-stu-id="faf13-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-174">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-175">Sì</span><span class="sxs-lookup"><span data-stu-id="faf13-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-176">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-177">No</span><span class="sxs-lookup"><span data-stu-id="faf13-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-178">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="faf13-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faf13-179">No</span><span class="sxs-lookup"><span data-stu-id="faf13-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-180">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-181">No</span><span class="sxs-lookup"><span data-stu-id="faf13-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-182">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="faf13-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faf13-183">No</span><span class="sxs-lookup"><span data-stu-id="faf13-183">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-184">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="faf13-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faf13-185">No</span><span class="sxs-lookup"><span data-stu-id="faf13-185">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-186">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-187">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="faf13-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faf13-188">*JET_paramIndexTuplesLengthMin*</span><span class="sxs-lookup"><span data-stu-id="faf13-188">*JET_paramIndexTuplesLengthMin*</span></span>  
<span data-ttu-id="faf13-189">110</span><span class="sxs-lookup"><span data-stu-id="faf13-189">110</span></span>  

<span data-ttu-id="faf13-190">Questo parametro specifica il valore predefinito per la lunghezza minima della tupla in un indice della tupla.</span><span class="sxs-lookup"><span data-stu-id="faf13-190">This parameter specifies the default for the minimum tuple length in a tuple index.</span></span> <span data-ttu-id="faf13-191">Per ulteriori informazioni, vedere [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="faf13-191">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="faf13-192">**Windows Vista:**  Prima di Windows Vista, impostando questo parametro su zero sarebbe stato impostato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="faf13-192">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="faf13-193">Per Windows Vista, questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="faf13-193">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faf13-194">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="faf13-194">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faf13-195">3</span><span class="sxs-lookup"><span data-stu-id="faf13-195">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-196">Digitare:</span><span class="sxs-lookup"><span data-stu-id="faf13-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="faf13-197">Integer</span><span class="sxs-lookup"><span data-stu-id="faf13-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-198">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="faf13-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faf13-199"><strong>Windows 2000, Windows XP e Windows Server 2003: </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="faf13-199"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="faf13-200"><strong>Windows Vista:</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="faf13-200"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-201">Ambito:</span><span class="sxs-lookup"><span data-stu-id="faf13-201">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faf13-202">Istanza</span><span class="sxs-lookup"><span data-stu-id="faf13-202">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-203">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-203">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-204">Sì</span><span class="sxs-lookup"><span data-stu-id="faf13-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-205">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-205">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-206">No</span><span class="sxs-lookup"><span data-stu-id="faf13-206">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-207">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="faf13-207">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faf13-208">No</span><span class="sxs-lookup"><span data-stu-id="faf13-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-209">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-209">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-210">No</span><span class="sxs-lookup"><span data-stu-id="faf13-210">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-211">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="faf13-211">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faf13-212">No</span><span class="sxs-lookup"><span data-stu-id="faf13-212">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-213">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="faf13-213">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faf13-214">No</span><span class="sxs-lookup"><span data-stu-id="faf13-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-215">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-215">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-216">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="faf13-216">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faf13-217">*JET_paramIndexTuplesToIndexMax*</span><span class="sxs-lookup"><span data-stu-id="faf13-217">*JET_paramIndexTuplesToIndexMax*</span></span>  
<span data-ttu-id="faf13-218">112</span><span class="sxs-lookup"><span data-stu-id="faf13-218">112</span></span>  

<span data-ttu-id="faf13-219">Questo parametro specifica il valore predefinito per la lunghezza massima di una stringa di origine per suddividere le tuple per un indice di tupla.</span><span class="sxs-lookup"><span data-stu-id="faf13-219">This parameter specifies the default for the maximum length of a source string to break into tuples for a tuple index.</span></span> <span data-ttu-id="faf13-220">Per ulteriori informazioni, vedere [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="faf13-220">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="faf13-221">**Windows Vista:**  Prima di Windows Vista, impostando questo parametro su zero sarebbe stato impostato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="faf13-221">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="faf13-222">Per Windows Vista, questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="faf13-222">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faf13-223">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="faf13-223">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faf13-224">32767</span><span class="sxs-lookup"><span data-stu-id="faf13-224">32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-225">Digitare:</span><span class="sxs-lookup"><span data-stu-id="faf13-225">Type:</span></span></p></td>
<td><p><span data-ttu-id="faf13-226">Integer</span><span class="sxs-lookup"><span data-stu-id="faf13-226">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-227">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="faf13-227">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faf13-228"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  0 – 32767</span><span class="sxs-lookup"><span data-stu-id="faf13-228"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 32767</span></span></p>
<p><span data-ttu-id="faf13-229"><strong>Windows Vista:</strong>  1 – 32767</span><span class="sxs-lookup"><span data-stu-id="faf13-229"><strong>Windows Vista:</strong>  1 – 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-230">Ambito:</span><span class="sxs-lookup"><span data-stu-id="faf13-230">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faf13-231">Istanza</span><span class="sxs-lookup"><span data-stu-id="faf13-231">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-232">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-232">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-233">Sì</span><span class="sxs-lookup"><span data-stu-id="faf13-233">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-234">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-234">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-235">No</span><span class="sxs-lookup"><span data-stu-id="faf13-235">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-236">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="faf13-236">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faf13-237">No</span><span class="sxs-lookup"><span data-stu-id="faf13-237">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-238">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-238">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-239">No</span><span class="sxs-lookup"><span data-stu-id="faf13-239">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-240">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="faf13-240">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faf13-241">No</span><span class="sxs-lookup"><span data-stu-id="faf13-241">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-242">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="faf13-242">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faf13-243">No</span><span class="sxs-lookup"><span data-stu-id="faf13-243">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-244">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-244">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-245">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="faf13-245">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="faf13-246">*JET_paramUnicodeIndexDefault*</span><span class="sxs-lookup"><span data-stu-id="faf13-246">*JET_paramUnicodeIndexDefault*</span></span>  
<span data-ttu-id="faf13-247">72</span><span class="sxs-lookup"><span data-stu-id="faf13-247">72</span></span>  

<span data-ttu-id="faf13-248">Questo parametro controlla i parametri Unicode predefiniti utilizzati da qualsiasi indice su una colonna chiave Unicode.</span><span class="sxs-lookup"><span data-stu-id="faf13-248">This parameter controls the default Unicode parameters used by any index over a Unicode key column.</span></span> <span data-ttu-id="faf13-249">Il tipo di questo parametro è [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e viene effettivamente passato utilizzando un puntatore del buffer archiviato nel parametro integer di [JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="faf13-249">The type of this parameter is [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and is actually passed using a buffer pointer stored in the integer parameter of [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="faf13-250">Le dimensioni del buffer devono essere uguali a quelle del [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e devono essere passate a [JetGetSystemParameter](./jetgetsystemparameter-function.md) utilizzando il parametro della dimensione del buffer di stringa.</span><span class="sxs-lookup"><span data-stu-id="faf13-250">The size of the buffer must equal the size of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and must be passed to [JetGetSystemParameter](./jetgetsystemparameter-function.md) using the string buffer size parameter.</span></span> <span data-ttu-id="faf13-251">Questo comportamento è chiaramente incoerente, ma questo è il comportamento di questo parametro.</span><span class="sxs-lookup"><span data-stu-id="faf13-251">This is clearly inconsistent but that is the behavior of this parameter.</span></span>

<span data-ttu-id="faf13-252">Il valore predefinito di questo parametro contiene un LCID per le impostazioni locali per l'inglese (Stati Uniti) e i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)seguenti: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="faf13-252">The default value of this parameter contains an LCID for the U.S. English locale and the following [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="faf13-253">**Windows 2000:**  SORTID nell'LCID viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="faf13-253">**Windows 2000:**  The SORTID in the LCID is ignored.</span></span> <span data-ttu-id="faf13-254">Viene sempre usato un SORTID di SORT_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="faf13-254">A SORTID of SORT_DEFAULT is always used.</span></span>

<span data-ttu-id="faf13-255">**Windows 2000:**  I flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) devono contenere i flag seguenti: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="faf13-255">**Windows 2000:**  The [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) flags must contain the following flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="faf13-256">Inoltre, i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)possono contenere i flag seguenti: NORM_IGNORENONSPACE.</span><span class="sxs-lookup"><span data-stu-id="faf13-256">In addition, the [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags may contain the following flags: NORM_IGNORENONSPACE.</span></span>

<span data-ttu-id="faf13-257">**Nota**  Se l'applicazione desidera archiviare dati Unicode, è consigliabile non fare affidamento sui parametri Unicode predefiniti per gli indici.</span><span class="sxs-lookup"><span data-stu-id="faf13-257">**Note**  If your application wishes to store Unicode data, then it is strongly recommended that you do not rely on the default Unicode parameters for your indexes.</span></span> <span data-ttu-id="faf13-258">L'uso dell'inglese (Stati Uniti) equivale all'uso delle impostazioni locali invariabili e i flag [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)predefiniti sono noti per interferire seriamente con alcune lingue.</span><span class="sxs-lookup"><span data-stu-id="faf13-258">The use of U.S. English is tantamount to using the invariant locale and the default [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags are known to seriously interfere with some languages.</span></span> <span data-ttu-id="faf13-259">È necessario specificare sempre le proprie impostazioni per i parametri Unicode in JetCreateIndex2 usando [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="faf13-259">You should always specify your own settings for the Unicode parameters to JetCreateIndex2 using [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faf13-260">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="faf13-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="faf13-261">Speciali</span><span class="sxs-lookup"><span data-stu-id="faf13-261">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-262">Digitare:</span><span class="sxs-lookup"><span data-stu-id="faf13-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="faf13-263">JET_UNICODEINDEX \* (JET_UNICODEINDEX)</span><span class="sxs-lookup"><span data-stu-id="faf13-263">JET_UNICODEINDEX\* (JET_UNICODEINDEX)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-264">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="faf13-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="faf13-265">Speciali</span><span class="sxs-lookup"><span data-stu-id="faf13-265">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-266">Ambito:</span><span class="sxs-lookup"><span data-stu-id="faf13-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="faf13-267">Istanza</span><span class="sxs-lookup"><span data-stu-id="faf13-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-268">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-269">Sì</span><span class="sxs-lookup"><span data-stu-id="faf13-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-270">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="faf13-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="faf13-271">No</span><span class="sxs-lookup"><span data-stu-id="faf13-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-272">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="faf13-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="faf13-273">No</span><span class="sxs-lookup"><span data-stu-id="faf13-273">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-274">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-275">No</span><span class="sxs-lookup"><span data-stu-id="faf13-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-276">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="faf13-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="faf13-277">No</span><span class="sxs-lookup"><span data-stu-id="faf13-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-278">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="faf13-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="faf13-279">No</span><span class="sxs-lookup"><span data-stu-id="faf13-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-280">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="faf13-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="faf13-281">Tutti</span><span class="sxs-lookup"><span data-stu-id="faf13-281">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="faf13-282">Requisiti</span><span class="sxs-lookup"><span data-stu-id="faf13-282">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faf13-283"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="faf13-283"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="faf13-284">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="faf13-284">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faf13-285"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="faf13-285"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="faf13-286">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="faf13-286">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faf13-287"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="faf13-287"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="faf13-288">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="faf13-288">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="faf13-289">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="faf13-289">See Also</span></span>

[<span data-ttu-id="faf13-290">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="faf13-290">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="faf13-291">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="faf13-291">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="faf13-292">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="faf13-292">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="faf13-293">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="faf13-293">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="faf13-294">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="faf13-294">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="faf13-295">JetInit</span><span class="sxs-lookup"><span data-stu-id="faf13-295">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="faf13-296">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="faf13-296">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
