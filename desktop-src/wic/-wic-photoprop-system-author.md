---
description: Criteri per i metadati delle foto per la proprietà System. Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Criteri per i metadati delle foto di System. Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317891"
---
# <a name="systemauthor-photo-metadata-policy"></a><span data-ttu-id="e57d6-103">Criteri per i metadati delle foto di System. Author</span><span class="sxs-lookup"><span data-stu-id="e57d6-103">System.Author Photo Metadata Policy</span></span>

<span data-ttu-id="e57d6-104">Criteri per i metadati delle foto per la proprietà [System. Author](../properties/props-system-author.md) .</span><span class="sxs-lookup"><span data-stu-id="e57d6-104">The photo metadata policy for the [System.Author](../properties/props-system-author.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e57d6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e57d6-105">PKEY</span></span>

<span data-ttu-id="e57d6-106">Autore di PKEY \_</span><span class="sxs-lookup"><span data-stu-id="e57d6-106">PKEY\_Author</span></span>

### <a name="containers"></a><span data-ttu-id="e57d6-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="e57d6-107">Containers</span></span>

<span data-ttu-id="e57d6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e57d6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e57d6-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="e57d6-109">Read-Only</span></span>

<span data-ttu-id="e57d6-110">No</span><span class="sxs-lookup"><span data-stu-id="e57d6-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e57d6-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="e57d6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e57d6-112">VT \_ vettore \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e57d6-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="e57d6-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="e57d6-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="e57d6-114">\_ \| \_ È preferibile il vettore VT LPWSTR, ma \_ è anche accettato VT LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="e57d6-114">VT\_VECTOR \| VT\_LPWSTR is preferred, but VT\_LPWSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e57d6-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="e57d6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e57d6-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="e57d6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e57d6-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="e57d6-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e57d6-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="e57d6-118">Read Paths</span></span>



| <span data-ttu-id="e57d6-119">JSON</span><span class="sxs-lookup"><span data-stu-id="e57d6-119">Order</span></span> | <span data-ttu-id="e57d6-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="e57d6-120">Path</span></span>                             | <span data-ttu-id="e57d6-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e57d6-121">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="e57d6-122">1</span><span class="sxs-lookup"><span data-stu-id="e57d6-122">1</span></span>     | <span data-ttu-id="e57d6-123">/App1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="e57d6-123">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="e57d6-124">ascii</span><span class="sxs-lookup"><span data-stu-id="e57d6-124">ascii</span></span>          |
| <span data-ttu-id="e57d6-125">2</span><span class="sxs-lookup"><span data-stu-id="e57d6-125">2</span></span>     | <span data-ttu-id="e57d6-126">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="e57d6-126">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="e57d6-127">3</span><span class="sxs-lookup"><span data-stu-id="e57d6-127">3</span></span>     | <span data-ttu-id="e57d6-128">/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="e57d6-128">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="e57d6-129">unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-129">unicode</span></span>        |
| <span data-ttu-id="e57d6-130">4</span><span class="sxs-lookup"><span data-stu-id="e57d6-130">4</span></span>     | <span data-ttu-id="e57d6-131">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="e57d6-131">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="e57d6-132">5</span><span class="sxs-lookup"><span data-stu-id="e57d6-132">5</span></span>     | <span data-ttu-id="e57d6-133">/App1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="e57d6-133">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="e57d6-134">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-134">unicode\_bytes</span></span> |
| <span data-ttu-id="e57d6-135">6</span><span class="sxs-lookup"><span data-stu-id="e57d6-135">6</span></span>     | <span data-ttu-id="e57d6-136">/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="e57d6-136">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="e57d6-137">unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-137">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="e57d6-138">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="e57d6-138">Write Paths</span></span>



| <span data-ttu-id="e57d6-139">JSON</span><span class="sxs-lookup"><span data-stu-id="e57d6-139">Order</span></span> | <span data-ttu-id="e57d6-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="e57d6-140">Path</span></span>                             | <span data-ttu-id="e57d6-141">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e57d6-141">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="e57d6-142">1</span><span class="sxs-lookup"><span data-stu-id="e57d6-142">1</span></span>     | <span data-ttu-id="e57d6-143">/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="e57d6-143">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="e57d6-144">unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-144">unicode</span></span>        |
| <span data-ttu-id="e57d6-145">2</span><span class="sxs-lookup"><span data-stu-id="e57d6-145">2</span></span>     | <span data-ttu-id="e57d6-146">/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="e57d6-146">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="e57d6-147">unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-147">unicode</span></span>        |
| <span data-ttu-id="e57d6-148">3</span><span class="sxs-lookup"><span data-stu-id="e57d6-148">3</span></span>     | <span data-ttu-id="e57d6-149">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="e57d6-149">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="e57d6-150">4</span><span class="sxs-lookup"><span data-stu-id="e57d6-150">4</span></span>     | <span data-ttu-id="e57d6-151">/App1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="e57d6-151">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="e57d6-152">ascii</span><span class="sxs-lookup"><span data-stu-id="e57d6-152">ascii</span></span>          |
| <span data-ttu-id="e57d6-153">5</span><span class="sxs-lookup"><span data-stu-id="e57d6-153">5</span></span>     | <span data-ttu-id="e57d6-154">/App1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="e57d6-154">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="e57d6-155">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-155">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="e57d6-156">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="e57d6-156">Remove Paths</span></span>



| <span data-ttu-id="e57d6-157">JSON</span><span class="sxs-lookup"><span data-stu-id="e57d6-157">Order</span></span> | <span data-ttu-id="e57d6-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="e57d6-158">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="e57d6-159">1</span><span class="sxs-lookup"><span data-stu-id="e57d6-159">1</span></span>     | <span data-ttu-id="e57d6-160">/XMP/DC: creatore</span><span class="sxs-lookup"><span data-stu-id="e57d6-160">/xmp/dc:creator</span></span>                  |
| <span data-ttu-id="e57d6-161">2</span><span class="sxs-lookup"><span data-stu-id="e57d6-161">2</span></span>     | <span data-ttu-id="e57d6-162">/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="e57d6-162">/xmp/tiff:artist</span></span>                 |
| <span data-ttu-id="e57d6-163">3</span><span class="sxs-lookup"><span data-stu-id="e57d6-163">3</span></span>     | <span data-ttu-id="e57d6-164">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="e57d6-164">/app13/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="e57d6-165">4</span><span class="sxs-lookup"><span data-stu-id="e57d6-165">4</span></span>     | <span data-ttu-id="e57d6-166">/App1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="e57d6-166">/app1/ifd/{ushort=315}</span></span>           |
| <span data-ttu-id="e57d6-167">5</span><span class="sxs-lookup"><span data-stu-id="e57d6-167">5</span></span>     | <span data-ttu-id="e57d6-168">/App1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="e57d6-168">/app1/ifd/{ushort=40093}</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="e57d6-169">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="e57d6-169">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e57d6-170">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="e57d6-170">Read Paths</span></span>



| <span data-ttu-id="e57d6-171">JSON</span><span class="sxs-lookup"><span data-stu-id="e57d6-171">Order</span></span> | <span data-ttu-id="e57d6-172">Percorso</span><span class="sxs-lookup"><span data-stu-id="e57d6-172">Path</span></span>                              | <span data-ttu-id="e57d6-173">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e57d6-173">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="e57d6-174">1</span><span class="sxs-lookup"><span data-stu-id="e57d6-174">1</span></span>     | <span data-ttu-id="e57d6-175">/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="e57d6-175">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="e57d6-176">ascii</span><span class="sxs-lookup"><span data-stu-id="e57d6-176">ascii</span></span>          |
| <span data-ttu-id="e57d6-177">2</span><span class="sxs-lookup"><span data-stu-id="e57d6-177">2</span></span>     | <span data-ttu-id="e57d6-178">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="e57d6-178">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="e57d6-179">3</span><span class="sxs-lookup"><span data-stu-id="e57d6-179">3</span></span>     | <span data-ttu-id="e57d6-180">/IFD/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="e57d6-180">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="e57d6-181">unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-181">unicode</span></span>        |
| <span data-ttu-id="e57d6-182">4</span><span class="sxs-lookup"><span data-stu-id="e57d6-182">4</span></span>     | <span data-ttu-id="e57d6-183">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="e57d6-183">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="e57d6-184">5</span><span class="sxs-lookup"><span data-stu-id="e57d6-184">5</span></span>     | <span data-ttu-id="e57d6-185">/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="e57d6-185">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="e57d6-186">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-186">unicode\_bytes</span></span> |
| <span data-ttu-id="e57d6-187">6</span><span class="sxs-lookup"><span data-stu-id="e57d6-187">6</span></span>     | <span data-ttu-id="e57d6-188">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="e57d6-188">/ifd/irb/8bimiptc/iptc/by-line</span></span>    |                |
| <span data-ttu-id="e57d6-189">7</span><span class="sxs-lookup"><span data-stu-id="e57d6-189">7</span></span>     | <span data-ttu-id="e57d6-190">/IFD/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="e57d6-190">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="e57d6-191">unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-191">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="e57d6-192">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="e57d6-192">Write Paths</span></span>



| <span data-ttu-id="e57d6-193">JSON</span><span class="sxs-lookup"><span data-stu-id="e57d6-193">Order</span></span> | <span data-ttu-id="e57d6-194">Percorso</span><span class="sxs-lookup"><span data-stu-id="e57d6-194">Path</span></span>                              | <span data-ttu-id="e57d6-195">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e57d6-195">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="e57d6-196">1</span><span class="sxs-lookup"><span data-stu-id="e57d6-196">1</span></span>     | <span data-ttu-id="e57d6-197">/IFD/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="e57d6-197">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="e57d6-198">unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-198">unicode</span></span>        |
| <span data-ttu-id="e57d6-199">2</span><span class="sxs-lookup"><span data-stu-id="e57d6-199">2</span></span>     | <span data-ttu-id="e57d6-200">/IFD/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="e57d6-200">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="e57d6-201">unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-201">unicode</span></span>        |
| <span data-ttu-id="e57d6-202">3</span><span class="sxs-lookup"><span data-stu-id="e57d6-202">3</span></span>     | <span data-ttu-id="e57d6-203">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="e57d6-203">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="e57d6-204">4</span><span class="sxs-lookup"><span data-stu-id="e57d6-204">4</span></span>     | <span data-ttu-id="e57d6-205">/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="e57d6-205">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="e57d6-206">\_vettore ASCII</span><span class="sxs-lookup"><span data-stu-id="e57d6-206">ascii\_vector</span></span>  |
| <span data-ttu-id="e57d6-207">5</span><span class="sxs-lookup"><span data-stu-id="e57d6-207">5</span></span>     | <span data-ttu-id="e57d6-208">/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="e57d6-208">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="e57d6-209">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="e57d6-209">unicode\_bytes</span></span> |
| <span data-ttu-id="e57d6-210">6</span><span class="sxs-lookup"><span data-stu-id="e57d6-210">6</span></span>     | <span data-ttu-id="e57d6-211">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="e57d6-211">/ifd/iptc/by-line</span></span>                 |                |



 

### <a name="remove-paths"></a><span data-ttu-id="e57d6-212">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="e57d6-212">Remove Paths</span></span>



| <span data-ttu-id="e57d6-213">JSON</span><span class="sxs-lookup"><span data-stu-id="e57d6-213">Order</span></span> | <span data-ttu-id="e57d6-214">Percorso</span><span class="sxs-lookup"><span data-stu-id="e57d6-214">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="e57d6-215">1</span><span class="sxs-lookup"><span data-stu-id="e57d6-215">1</span></span>     | <span data-ttu-id="e57d6-216">/IFD/XMP/DC: creatore</span><span class="sxs-lookup"><span data-stu-id="e57d6-216">/ifd/xmp/dc:creator</span></span>            |
| <span data-ttu-id="e57d6-217">2</span><span class="sxs-lookup"><span data-stu-id="e57d6-217">2</span></span>     | <span data-ttu-id="e57d6-218">/IFD/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="e57d6-218">/ifd/xmp/tiff:artist</span></span>           |
| <span data-ttu-id="e57d6-219">3</span><span class="sxs-lookup"><span data-stu-id="e57d6-219">3</span></span>     | <span data-ttu-id="e57d6-220">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="e57d6-220">/ifd/iptc/by-line</span></span>              |
| <span data-ttu-id="e57d6-221">4</span><span class="sxs-lookup"><span data-stu-id="e57d6-221">4</span></span>     | <span data-ttu-id="e57d6-222">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="e57d6-222">/ifd/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="e57d6-223">5</span><span class="sxs-lookup"><span data-stu-id="e57d6-223">5</span></span>     | <span data-ttu-id="e57d6-224">/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="e57d6-224">/ifd/{ushort=315}</span></span>              |
| <span data-ttu-id="e57d6-225">6</span><span class="sxs-lookup"><span data-stu-id="e57d6-225">6</span></span>     | <span data-ttu-id="e57d6-226">/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="e57d6-226">/ifd/{ushort=40093}</span></span>            |



 

### <a name="remarks"></a><span data-ttu-id="e57d6-227">Commenti</span><span class="sxs-lookup"><span data-stu-id="e57d6-227">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e57d6-228">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e57d6-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e57d6-229">System.Author</span><span class="sxs-lookup"><span data-stu-id="e57d6-229">System.Author</span></span>](../properties/props-system-author.md)
</dt> </dl>

 

 
