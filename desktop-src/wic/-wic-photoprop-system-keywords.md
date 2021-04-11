---
description: Criteri per i metadati delle foto per la proprietà System. keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Criteri per i metadati di Photo System. Keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233334"
---
# <a name="systemkeywords-photo-metadata-policy"></a><span data-ttu-id="d3d45-103">Criteri per i metadati di Photo System. Keywords</span><span class="sxs-lookup"><span data-stu-id="d3d45-103">System.Keywords Photo Metadata Policy</span></span>

<span data-ttu-id="d3d45-104">Criteri per i metadati delle foto per la proprietà [System. Keywords](../properties/props-system-keywords.md) .</span><span class="sxs-lookup"><span data-stu-id="d3d45-104">The photo metadata policy for the [System.Keywords](../properties/props-system-keywords.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d3d45-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d3d45-105">PKEY</span></span>

<span data-ttu-id="d3d45-106">\_Parole chiave pkey</span><span class="sxs-lookup"><span data-stu-id="d3d45-106">PKEY\_Keywords</span></span>

### <a name="containers"></a><span data-ttu-id="d3d45-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="d3d45-107">Containers</span></span>

<span data-ttu-id="d3d45-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d3d45-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d3d45-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="d3d45-109">Read-Only</span></span>

<span data-ttu-id="d3d45-110">No</span><span class="sxs-lookup"><span data-stu-id="d3d45-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d3d45-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="d3d45-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d3d45-112">VT \_ vettore \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="d3d45-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="d3d45-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="d3d45-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="d3d45-114">\_ \| \_ È preferibile il vettore VT LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="d3d45-114">VT\_VECTOR \| VT\_LPWSTR is preferred.</span></span> <span data-ttu-id="d3d45-115">\_Viene anche accettato un LPWSTR VT contenente una stringa delimitata da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="d3d45-115">A VT\_LPWSTR containing a semicolon-delimited string is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d3d45-116">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="d3d45-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="d3d45-117">I valori di schemi diversi vengono uniti.</span><span class="sxs-lookup"><span data-stu-id="d3d45-117">Values from different schemas are merged.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d3d45-118">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="d3d45-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d3d45-119">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="d3d45-119">Read Paths</span></span>



| <span data-ttu-id="d3d45-120">JSON</span><span class="sxs-lookup"><span data-stu-id="d3d45-120">Order</span></span> | <span data-ttu-id="d3d45-121">Percorso</span><span class="sxs-lookup"><span data-stu-id="d3d45-121">Path</span></span>                              | <span data-ttu-id="d3d45-122">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d3d45-122">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="d3d45-123">1</span><span class="sxs-lookup"><span data-stu-id="d3d45-123">1</span></span>     | <span data-ttu-id="d3d45-124">/XMP/ <xmpbag> DC: oggetto</span><span class="sxs-lookup"><span data-stu-id="d3d45-124">/xmp/<xmpbag>dc:subject</span></span>     | <span data-ttu-id="d3d45-125">unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-125">unicode</span></span>        |
| <span data-ttu-id="d3d45-126">2</span><span class="sxs-lookup"><span data-stu-id="d3d45-126">2</span></span>     | <span data-ttu-id="d3d45-127">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="d3d45-127">/app13/irb/8bimiptc/iptc/keywords</span></span> |                |
| <span data-ttu-id="d3d45-128">3</span><span class="sxs-lookup"><span data-stu-id="d3d45-128">3</span></span>     | <span data-ttu-id="d3d45-129">/App1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="d3d45-129">/app1/ifd/{ushort=18247}</span></span>          | <span data-ttu-id="d3d45-130">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-130">unicode\_bytes</span></span> |
| <span data-ttu-id="d3d45-131">4</span><span class="sxs-lookup"><span data-stu-id="d3d45-131">4</span></span>     | <span data-ttu-id="d3d45-132">/App1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="d3d45-132">/app1/ifd/{ushort=40094}</span></span>          | <span data-ttu-id="d3d45-133">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-133">unicode\_bytes</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="d3d45-134">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="d3d45-134">Write Paths</span></span>



| <span data-ttu-id="d3d45-135">JSON</span><span class="sxs-lookup"><span data-stu-id="d3d45-135">Order</span></span> | <span data-ttu-id="d3d45-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="d3d45-136">Path</span></span>                                              | <span data-ttu-id="d3d45-137">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d3d45-137">Disk Format</span></span>    |
|-------|---------------------------------------------------|----------------|
| <span data-ttu-id="d3d45-138">1</span><span class="sxs-lookup"><span data-stu-id="d3d45-138">1</span></span>     | <span data-ttu-id="d3d45-139">/XMP/ <xmpbag> DC: oggetto</span><span class="sxs-lookup"><span data-stu-id="d3d45-139">/xmp/<xmpbag>dc:subject</span></span>                     | <span data-ttu-id="d3d45-140">unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-140">unicode</span></span>        |
| <span data-ttu-id="d3d45-141">2</span><span class="sxs-lookup"><span data-stu-id="d3d45-141">2</span></span>     | <span data-ttu-id="d3d45-142">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="d3d45-142">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |                |
| <span data-ttu-id="d3d45-143">3</span><span class="sxs-lookup"><span data-stu-id="d3d45-143">3</span></span>     | <span data-ttu-id="d3d45-144">/App1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="d3d45-144">/app1/ifd/{ushort=18247}</span></span>                          | <span data-ttu-id="d3d45-145">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-145">unicode\_bytes</span></span> |
| <span data-ttu-id="d3d45-146">4</span><span class="sxs-lookup"><span data-stu-id="d3d45-146">4</span></span>     | <span data-ttu-id="d3d45-147">/App1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="d3d45-147">/app1/ifd/{ushort=40094}</span></span>                          | <span data-ttu-id="d3d45-148">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-148">unicode\_bytes</span></span> |
| <span data-ttu-id="d3d45-149">5</span><span class="sxs-lookup"><span data-stu-id="d3d45-149">5</span></span>     | <span data-ttu-id="d3d45-150">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="d3d45-150">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  | <span data-ttu-id="d3d45-151">unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-151">unicode</span></span>        |
| <span data-ttu-id="d3d45-152">6</span><span class="sxs-lookup"><span data-stu-id="d3d45-152">6</span></span>     | <span data-ttu-id="d3d45-153">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="d3d45-153">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> | <span data-ttu-id="d3d45-154">unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-154">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="d3d45-155">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="d3d45-155">Remove Paths</span></span>



| <span data-ttu-id="d3d45-156">JSON</span><span class="sxs-lookup"><span data-stu-id="d3d45-156">Order</span></span> | <span data-ttu-id="d3d45-157">Percorso</span><span class="sxs-lookup"><span data-stu-id="d3d45-157">Path</span></span>                                              |
|-------|---------------------------------------------------|
| <span data-ttu-id="d3d45-158">1</span><span class="sxs-lookup"><span data-stu-id="d3d45-158">1</span></span>     | <span data-ttu-id="d3d45-159">/XMP/DC: oggetto</span><span class="sxs-lookup"><span data-stu-id="d3d45-159">/xmp/dc:subject</span></span>                                   |
| <span data-ttu-id="d3d45-160">2</span><span class="sxs-lookup"><span data-stu-id="d3d45-160">2</span></span>     | <span data-ttu-id="d3d45-161">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="d3d45-161">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |
| <span data-ttu-id="d3d45-162">3</span><span class="sxs-lookup"><span data-stu-id="d3d45-162">3</span></span>     | <span data-ttu-id="d3d45-163">/App1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="d3d45-163">/app1/ifd/{ushort=18247}</span></span>                          |
| <span data-ttu-id="d3d45-164">4</span><span class="sxs-lookup"><span data-stu-id="d3d45-164">4</span></span>     | <span data-ttu-id="d3d45-165">/App1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="d3d45-165">/app1/ifd/{ushort=40094}</span></span>                          |
| <span data-ttu-id="d3d45-166">5</span><span class="sxs-lookup"><span data-stu-id="d3d45-166">5</span></span>     | <span data-ttu-id="d3d45-167">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="d3d45-167">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  |
| <span data-ttu-id="d3d45-168">6</span><span class="sxs-lookup"><span data-stu-id="d3d45-168">6</span></span>     | <span data-ttu-id="d3d45-169">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="d3d45-169">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="d3d45-170">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="d3d45-170">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d3d45-171">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="d3d45-171">Read Paths</span></span>



| <span data-ttu-id="d3d45-172">JSON</span><span class="sxs-lookup"><span data-stu-id="d3d45-172">Order</span></span> | <span data-ttu-id="d3d45-173">Percorso</span><span class="sxs-lookup"><span data-stu-id="d3d45-173">Path</span></span>                              | <span data-ttu-id="d3d45-174">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d3d45-174">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="d3d45-175">1</span><span class="sxs-lookup"><span data-stu-id="d3d45-175">1</span></span>     | <span data-ttu-id="d3d45-176">/IFD/XMP/ <xmpbag> DC: oggetto</span><span class="sxs-lookup"><span data-stu-id="d3d45-176">/ifd/xmp/<xmpbag>dc:subject</span></span> | <span data-ttu-id="d3d45-177">unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-177">unicode</span></span>        |
| <span data-ttu-id="d3d45-178">2</span><span class="sxs-lookup"><span data-stu-id="d3d45-178">2</span></span>     | <span data-ttu-id="d3d45-179">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="d3d45-179">/ifd/iptc/keywords</span></span>                |                |
| <span data-ttu-id="d3d45-180">3</span><span class="sxs-lookup"><span data-stu-id="d3d45-180">3</span></span>     | <span data-ttu-id="d3d45-181">/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="d3d45-181">/ifd/{ushort=18247}</span></span>               | <span data-ttu-id="d3d45-182">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-182">unicode\_bytes</span></span> |
| <span data-ttu-id="d3d45-183">4</span><span class="sxs-lookup"><span data-stu-id="d3d45-183">4</span></span>     | <span data-ttu-id="d3d45-184">/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="d3d45-184">/ifd/{ushort=40094}</span></span>               | <span data-ttu-id="d3d45-185">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-185">unicode\_bytes</span></span> |
| <span data-ttu-id="d3d45-186">5</span><span class="sxs-lookup"><span data-stu-id="d3d45-186">5</span></span>     | <span data-ttu-id="d3d45-187">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="d3d45-187">/ifd/irb/8bimiptc/iptc/keywords</span></span>   |                |



 

### <a name="write-paths"></a><span data-ttu-id="d3d45-188">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="d3d45-188">Write Paths</span></span>



| <span data-ttu-id="d3d45-189">JSON</span><span class="sxs-lookup"><span data-stu-id="d3d45-189">Order</span></span> | <span data-ttu-id="d3d45-190">Percorso</span><span class="sxs-lookup"><span data-stu-id="d3d45-190">Path</span></span>                                                             | <span data-ttu-id="d3d45-191">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d3d45-191">Disk Format</span></span>    |
|-------|------------------------------------------------------------------|----------------|
| <span data-ttu-id="d3d45-192">1</span><span class="sxs-lookup"><span data-stu-id="d3d45-192">1</span></span>     | <span data-ttu-id="d3d45-193">/IFD/XMP/ <xmpbag> DC: oggetto</span><span class="sxs-lookup"><span data-stu-id="d3d45-193">/ifd/xmp/<xmpbag>dc:subject</span></span>                                | <span data-ttu-id="d3d45-194">unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-194">unicode</span></span>        |
| <span data-ttu-id="d3d45-195">2</span><span class="sxs-lookup"><span data-stu-id="d3d45-195">2</span></span>     | <span data-ttu-id="d3d45-196">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="d3d45-196">/ifd/iptc/keywords</span></span>                                               |                |
| <span data-ttu-id="d3d45-197">3</span><span class="sxs-lookup"><span data-stu-id="d3d45-197">3</span></span>     | <span data-ttu-id="d3d45-198">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="d3d45-198">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |                |
| <span data-ttu-id="d3d45-199">4</span><span class="sxs-lookup"><span data-stu-id="d3d45-199">4</span></span>     | <span data-ttu-id="d3d45-200">/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="d3d45-200">/ifd/{ushort=18247}</span></span>                                              | <span data-ttu-id="d3d45-201">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-201">unicode\_bytes</span></span> |
| <span data-ttu-id="d3d45-202">5</span><span class="sxs-lookup"><span data-stu-id="d3d45-202">5</span></span>     | <span data-ttu-id="d3d45-203">/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="d3d45-203">/ifd/{ushort=40094}</span></span>                                              | <span data-ttu-id="d3d45-204">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-204">unicode\_bytes</span></span> |
| <span data-ttu-id="d3d45-205">6</span><span class="sxs-lookup"><span data-stu-id="d3d45-205">6</span></span>     | <span data-ttu-id="d3d45-206">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="d3d45-206">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             | <span data-ttu-id="d3d45-207">unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-207">unicode</span></span>        |
| <span data-ttu-id="d3d45-208">7</span><span class="sxs-lookup"><span data-stu-id="d3d45-208">7</span></span>     | <span data-ttu-id="d3d45-209">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="d3d45-209">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            | <span data-ttu-id="d3d45-210">unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-210">unicode</span></span>        |
| <span data-ttu-id="d3d45-211">8</span><span class="sxs-lookup"><span data-stu-id="d3d45-211">8</span></span>     | <span data-ttu-id="d3d45-212">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB</span><span class="sxs-lookup"><span data-stu-id="d3d45-212">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> | <span data-ttu-id="d3d45-213">unicode</span><span class="sxs-lookup"><span data-stu-id="d3d45-213">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="d3d45-214">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="d3d45-214">Remove Paths</span></span>



| <span data-ttu-id="d3d45-215">JSON</span><span class="sxs-lookup"><span data-stu-id="d3d45-215">Order</span></span> | <span data-ttu-id="d3d45-216">Percorso</span><span class="sxs-lookup"><span data-stu-id="d3d45-216">Path</span></span>                                                             |
|-------|------------------------------------------------------------------|
| <span data-ttu-id="d3d45-217">1</span><span class="sxs-lookup"><span data-stu-id="d3d45-217">1</span></span>     | <span data-ttu-id="d3d45-218">/IFD/XMP/DC: oggetto</span><span class="sxs-lookup"><span data-stu-id="d3d45-218">/ifd/xmp/dc:subject</span></span>                                              |
| <span data-ttu-id="d3d45-219">2</span><span class="sxs-lookup"><span data-stu-id="d3d45-219">2</span></span>     | <span data-ttu-id="d3d45-220">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="d3d45-220">/ifd/iptc/keywords</span></span>                                               |
| <span data-ttu-id="d3d45-221">3</span><span class="sxs-lookup"><span data-stu-id="d3d45-221">3</span></span>     | <span data-ttu-id="d3d45-222">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="d3d45-222">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |
| <span data-ttu-id="d3d45-223">4</span><span class="sxs-lookup"><span data-stu-id="d3d45-223">4</span></span>     | <span data-ttu-id="d3d45-224">/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="d3d45-224">/ifd/{ushort=18247}</span></span>                                              |
| <span data-ttu-id="d3d45-225">5</span><span class="sxs-lookup"><span data-stu-id="d3d45-225">5</span></span>     | <span data-ttu-id="d3d45-226">/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="d3d45-226">/ifd/{ushort=40094}</span></span>                                              |
| <span data-ttu-id="d3d45-227">6</span><span class="sxs-lookup"><span data-stu-id="d3d45-227">6</span></span>     | <span data-ttu-id="d3d45-228">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="d3d45-228">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             |
| <span data-ttu-id="d3d45-229">7</span><span class="sxs-lookup"><span data-stu-id="d3d45-229">7</span></span>     | <span data-ttu-id="d3d45-230">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="d3d45-230">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            |
| <span data-ttu-id="d3d45-231">8</span><span class="sxs-lookup"><span data-stu-id="d3d45-231">8</span></span>     | <span data-ttu-id="d3d45-232">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB</span><span class="sxs-lookup"><span data-stu-id="d3d45-232">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="d3d45-233">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3d45-233">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3d45-234">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d3d45-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3d45-235">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="d3d45-235">System.Keywords</span></span>](../properties/props-system-keywords.md)
</dt> </dl>

 

 
