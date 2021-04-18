---
description: Criteri per i metadati delle foto per la proprietà System. title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Criteri per i metadati delle foto System. title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315956"
---
# <a name="systemtitle-photo-metadata-policy"></a><span data-ttu-id="788be-103">Criteri per i metadati delle foto System. title</span><span class="sxs-lookup"><span data-stu-id="788be-103">System.Title Photo Metadata Policy</span></span>

<span data-ttu-id="788be-104">Criteri per i metadati delle foto per la proprietà [System. title](../properties/props-system-title.md) .</span><span class="sxs-lookup"><span data-stu-id="788be-104">The photo metadata policy for the [System.Title](../properties/props-system-title.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="788be-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="788be-105">PKEY</span></span>

<span data-ttu-id="788be-106">\_Titolo pkey</span><span class="sxs-lookup"><span data-stu-id="788be-106">PKEY\_Title</span></span>

### <a name="containers"></a><span data-ttu-id="788be-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="788be-107">Containers</span></span>

<span data-ttu-id="788be-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="788be-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="788be-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="788be-109">Read-Only</span></span>

<span data-ttu-id="788be-110">No</span><span class="sxs-lookup"><span data-stu-id="788be-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="788be-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="788be-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="788be-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="788be-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="788be-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="788be-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="788be-114">VT \_ LPWSTR o VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="788be-114">Either VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="788be-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="788be-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="788be-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="788be-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="788be-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="788be-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="788be-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="788be-118">Read Paths</span></span>



| <span data-ttu-id="788be-119">JSON</span><span class="sxs-lookup"><span data-stu-id="788be-119">Order</span></span> | <span data-ttu-id="788be-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="788be-120">Path</span></span>                                | <span data-ttu-id="788be-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="788be-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="788be-122">1</span><span class="sxs-lookup"><span data-stu-id="788be-122">1</span></span>     | <span data-ttu-id="788be-123">/App1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="788be-123">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="788be-124">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="788be-124">unicode\_bytes</span></span> |
| <span data-ttu-id="788be-125">2</span><span class="sxs-lookup"><span data-stu-id="788be-125">2</span></span>     | <span data-ttu-id="788be-126">/XMP/ <xmpalt> DC: titolo</span><span class="sxs-lookup"><span data-stu-id="788be-126">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="788be-127">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-127">unicode</span></span>        |
| <span data-ttu-id="788be-128">3</span><span class="sxs-lookup"><span data-stu-id="788be-128">3</span></span>     | <span data-ttu-id="788be-129">/XMP/DC: titolo</span><span class="sxs-lookup"><span data-stu-id="788be-129">/xmp/dc:title</span></span>                       | <span data-ttu-id="788be-130">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-130">unicode</span></span>        |
| <span data-ttu-id="788be-131">4</span><span class="sxs-lookup"><span data-stu-id="788be-131">4</span></span>     | <span data-ttu-id="788be-132">/App1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="788be-132">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="788be-133">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-133">unicode</span></span>        |
| <span data-ttu-id="788be-134">5</span><span class="sxs-lookup"><span data-stu-id="788be-134">5</span></span>     | <span data-ttu-id="788be-135">/App1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="788be-135">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="788be-136">ascii</span><span class="sxs-lookup"><span data-stu-id="788be-136">ascii</span></span>          |
| <span data-ttu-id="788be-137">6</span><span class="sxs-lookup"><span data-stu-id="788be-137">6</span></span>     | <span data-ttu-id="788be-138">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="788be-138">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="788be-139">7</span><span class="sxs-lookup"><span data-stu-id="788be-139">7</span></span>     | <span data-ttu-id="788be-140">/XMP/ <xmpalt> DC: Descrizione</span><span class="sxs-lookup"><span data-stu-id="788be-140">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="788be-141">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-141">unicode</span></span>        |
| <span data-ttu-id="788be-142">8</span><span class="sxs-lookup"><span data-stu-id="788be-142">8</span></span>     | <span data-ttu-id="788be-143">/XMP/DC: Descrizione</span><span class="sxs-lookup"><span data-stu-id="788be-143">/xmp/dc:description</span></span>                 | <span data-ttu-id="788be-144">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-144">unicode</span></span>        |
| <span data-ttu-id="788be-145">9</span><span class="sxs-lookup"><span data-stu-id="788be-145">9</span></span>     | <span data-ttu-id="788be-146">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="788be-146">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="788be-147">10</span><span class="sxs-lookup"><span data-stu-id="788be-147">10</span></span>    | <span data-ttu-id="788be-148">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="788be-148">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="788be-149">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-149">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="788be-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="788be-150">Write Paths</span></span>



| <span data-ttu-id="788be-151">JSON</span><span class="sxs-lookup"><span data-stu-id="788be-151">Order</span></span> | <span data-ttu-id="788be-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="788be-152">Path</span></span>                                | <span data-ttu-id="788be-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="788be-153">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="788be-154">1</span><span class="sxs-lookup"><span data-stu-id="788be-154">1</span></span>     | <span data-ttu-id="788be-155">/App1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="788be-155">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="788be-156">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="788be-156">unicode\_bytes</span></span> |
| <span data-ttu-id="788be-157">2</span><span class="sxs-lookup"><span data-stu-id="788be-157">2</span></span>     | <span data-ttu-id="788be-158">/XMP/DC: titolo</span><span class="sxs-lookup"><span data-stu-id="788be-158">/xmp/dc:title</span></span>                       | <span data-ttu-id="788be-159">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-159">unicode</span></span>        |
| <span data-ttu-id="788be-160">3</span><span class="sxs-lookup"><span data-stu-id="788be-160">3</span></span>     | <span data-ttu-id="788be-161">/XMP/ <xmpalt> DC: titolo</span><span class="sxs-lookup"><span data-stu-id="788be-161">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="788be-162">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-162">unicode</span></span>        |
| <span data-ttu-id="788be-163">4</span><span class="sxs-lookup"><span data-stu-id="788be-163">4</span></span>     | <span data-ttu-id="788be-164">/App1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="788be-164">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="788be-165">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-165">unicode</span></span>        |
| <span data-ttu-id="788be-166">5</span><span class="sxs-lookup"><span data-stu-id="788be-166">5</span></span>     | <span data-ttu-id="788be-167">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="788be-167">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="788be-168">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-168">unicode</span></span>        |
| <span data-ttu-id="788be-169">6</span><span class="sxs-lookup"><span data-stu-id="788be-169">6</span></span>     | <span data-ttu-id="788be-170">/App1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="788be-170">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="788be-171">ascii</span><span class="sxs-lookup"><span data-stu-id="788be-171">ascii</span></span>          |
| <span data-ttu-id="788be-172">7</span><span class="sxs-lookup"><span data-stu-id="788be-172">7</span></span>     | <span data-ttu-id="788be-173">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="788be-173">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="788be-174">8</span><span class="sxs-lookup"><span data-stu-id="788be-174">8</span></span>     | <span data-ttu-id="788be-175">/XMP/DC: Descrizione</span><span class="sxs-lookup"><span data-stu-id="788be-175">/xmp/dc:description</span></span>                 | <span data-ttu-id="788be-176">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-176">unicode</span></span>        |
| <span data-ttu-id="788be-177">9</span><span class="sxs-lookup"><span data-stu-id="788be-177">9</span></span>     | <span data-ttu-id="788be-178">/XMP/ <xmpalt> DC: Descrizione</span><span class="sxs-lookup"><span data-stu-id="788be-178">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="788be-179">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-179">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="788be-180">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="788be-180">Remove Paths</span></span>



| <span data-ttu-id="788be-181">JSON</span><span class="sxs-lookup"><span data-stu-id="788be-181">Order</span></span> | <span data-ttu-id="788be-182">Percorso</span><span class="sxs-lookup"><span data-stu-id="788be-182">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="788be-183">1</span><span class="sxs-lookup"><span data-stu-id="788be-183">1</span></span>     | <span data-ttu-id="788be-184">/App1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="788be-184">/app1/ifd/{ushort=40091}</span></span>            |
| <span data-ttu-id="788be-185">2</span><span class="sxs-lookup"><span data-stu-id="788be-185">2</span></span>     | <span data-ttu-id="788be-186">/XMP/DC: titolo</span><span class="sxs-lookup"><span data-stu-id="788be-186">/xmp/dc:title</span></span>                       |
| <span data-ttu-id="788be-187">3</span><span class="sxs-lookup"><span data-stu-id="788be-187">3</span></span>     | <span data-ttu-id="788be-188">/App1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="788be-188">/app1/ifd/exif/{ushort=37510}</span></span>       |
| <span data-ttu-id="788be-189">4</span><span class="sxs-lookup"><span data-stu-id="788be-189">4</span></span>     | <span data-ttu-id="788be-190">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="788be-190">/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="788be-191">5</span><span class="sxs-lookup"><span data-stu-id="788be-191">5</span></span>     | <span data-ttu-id="788be-192">/App1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="788be-192">/app1/ifd/{ushort=270}</span></span>              |
| <span data-ttu-id="788be-193">6</span><span class="sxs-lookup"><span data-stu-id="788be-193">6</span></span>     | <span data-ttu-id="788be-194">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="788be-194">/app13/irb/8bimiptc/iptc/caption</span></span>    |
| <span data-ttu-id="788be-195">7</span><span class="sxs-lookup"><span data-stu-id="788be-195">7</span></span>     | <span data-ttu-id="788be-196">/XMP/DC: Descrizione</span><span class="sxs-lookup"><span data-stu-id="788be-196">/xmp/dc:description</span></span>                 |



 

### <a name="tiff-policy"></a><span data-ttu-id="788be-197">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="788be-197">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="788be-198">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="788be-198">Read Paths</span></span>



| <span data-ttu-id="788be-199">JSON</span><span class="sxs-lookup"><span data-stu-id="788be-199">Order</span></span> | <span data-ttu-id="788be-200">Percorso</span><span class="sxs-lookup"><span data-stu-id="788be-200">Path</span></span>                                    | <span data-ttu-id="788be-201">Formato disco</span><span class="sxs-lookup"><span data-stu-id="788be-201">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="788be-202">1</span><span class="sxs-lookup"><span data-stu-id="788be-202">1</span></span>     | <span data-ttu-id="788be-203">/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="788be-203">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="788be-204">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="788be-204">unicode\_bytes</span></span> |
| <span data-ttu-id="788be-205">2</span><span class="sxs-lookup"><span data-stu-id="788be-205">2</span></span>     | <span data-ttu-id="788be-206">/IFD/XMP/ <xmpalt> DC: titolo</span><span class="sxs-lookup"><span data-stu-id="788be-206">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="788be-207">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-207">unicode</span></span>        |
| <span data-ttu-id="788be-208">3</span><span class="sxs-lookup"><span data-stu-id="788be-208">3</span></span>     | <span data-ttu-id="788be-209">/IFD/XMP/DC: titolo</span><span class="sxs-lookup"><span data-stu-id="788be-209">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="788be-210">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-210">unicode</span></span>        |
| <span data-ttu-id="788be-211">4</span><span class="sxs-lookup"><span data-stu-id="788be-211">4</span></span>     | <span data-ttu-id="788be-212">/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="788be-212">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="788be-213">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-213">unicode</span></span>        |
| <span data-ttu-id="788be-214">5</span><span class="sxs-lookup"><span data-stu-id="788be-214">5</span></span>     | <span data-ttu-id="788be-215">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="788be-215">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="788be-216">ascii</span><span class="sxs-lookup"><span data-stu-id="788be-216">ascii</span></span>          |
| <span data-ttu-id="788be-217">6</span><span class="sxs-lookup"><span data-stu-id="788be-217">6</span></span>     | <span data-ttu-id="788be-218">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="788be-218">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="788be-219">7</span><span class="sxs-lookup"><span data-stu-id="788be-219">7</span></span>     | <span data-ttu-id="788be-220">/IFD/XMP/ <xmpalt> DC: Descrizione</span><span class="sxs-lookup"><span data-stu-id="788be-220">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="788be-221">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-221">unicode</span></span>        |
| <span data-ttu-id="788be-222">8</span><span class="sxs-lookup"><span data-stu-id="788be-222">8</span></span>     | <span data-ttu-id="788be-223">/IFD/XMP/DC: Descrizione</span><span class="sxs-lookup"><span data-stu-id="788be-223">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="788be-224">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-224">unicode</span></span>        |
| <span data-ttu-id="788be-225">9</span><span class="sxs-lookup"><span data-stu-id="788be-225">9</span></span>     | <span data-ttu-id="788be-226">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="788be-226">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="788be-227">10</span><span class="sxs-lookup"><span data-stu-id="788be-227">10</span></span>    | <span data-ttu-id="788be-228">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="788be-228">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="788be-229">11</span><span class="sxs-lookup"><span data-stu-id="788be-229">11</span></span>    | <span data-ttu-id="788be-230">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="788be-230">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="788be-231">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-231">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="788be-232">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="788be-232">Write Paths</span></span>



| <span data-ttu-id="788be-233">JSON</span><span class="sxs-lookup"><span data-stu-id="788be-233">Order</span></span> | <span data-ttu-id="788be-234">Percorso</span><span class="sxs-lookup"><span data-stu-id="788be-234">Path</span></span>                                    | <span data-ttu-id="788be-235">Formato disco</span><span class="sxs-lookup"><span data-stu-id="788be-235">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="788be-236">1</span><span class="sxs-lookup"><span data-stu-id="788be-236">1</span></span>     | <span data-ttu-id="788be-237">/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="788be-237">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="788be-238">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="788be-238">unicode\_bytes</span></span> |
| <span data-ttu-id="788be-239">2</span><span class="sxs-lookup"><span data-stu-id="788be-239">2</span></span>     | <span data-ttu-id="788be-240">/IFD/XMP/DC: titolo</span><span class="sxs-lookup"><span data-stu-id="788be-240">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="788be-241">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-241">unicode</span></span>        |
| <span data-ttu-id="788be-242">3</span><span class="sxs-lookup"><span data-stu-id="788be-242">3</span></span>     | <span data-ttu-id="788be-243">/IFD/XMP/ <xmpalt> DC: titolo</span><span class="sxs-lookup"><span data-stu-id="788be-243">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="788be-244">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-244">unicode</span></span>        |
| <span data-ttu-id="788be-245">4</span><span class="sxs-lookup"><span data-stu-id="788be-245">4</span></span>     | <span data-ttu-id="788be-246">/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="788be-246">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="788be-247">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-247">unicode</span></span>        |
| <span data-ttu-id="788be-248">5</span><span class="sxs-lookup"><span data-stu-id="788be-248">5</span></span>     | <span data-ttu-id="788be-249">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="788be-249">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="788be-250">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-250">unicode</span></span>        |
| <span data-ttu-id="788be-251">6</span><span class="sxs-lookup"><span data-stu-id="788be-251">6</span></span>     | <span data-ttu-id="788be-252">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="788be-252">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="788be-253">ascii</span><span class="sxs-lookup"><span data-stu-id="788be-253">ascii</span></span>          |
| <span data-ttu-id="788be-254">7</span><span class="sxs-lookup"><span data-stu-id="788be-254">7</span></span>     | <span data-ttu-id="788be-255">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="788be-255">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="788be-256">8</span><span class="sxs-lookup"><span data-stu-id="788be-256">8</span></span>     | <span data-ttu-id="788be-257">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="788be-257">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="788be-258">9</span><span class="sxs-lookup"><span data-stu-id="788be-258">9</span></span>     | <span data-ttu-id="788be-259">/IFD/XMP/DC: Descrizione</span><span class="sxs-lookup"><span data-stu-id="788be-259">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="788be-260">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-260">unicode</span></span>        |
| <span data-ttu-id="788be-261">10</span><span class="sxs-lookup"><span data-stu-id="788be-261">10</span></span>    | <span data-ttu-id="788be-262">/IFD/XMP/ <xmpalt> DC: Descrizione</span><span class="sxs-lookup"><span data-stu-id="788be-262">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="788be-263">unicode</span><span class="sxs-lookup"><span data-stu-id="788be-263">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="788be-264">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="788be-264">Remove Paths</span></span>



| <span data-ttu-id="788be-265">JSON</span><span class="sxs-lookup"><span data-stu-id="788be-265">Order</span></span> | <span data-ttu-id="788be-266">Percorso</span><span class="sxs-lookup"><span data-stu-id="788be-266">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="788be-267">1</span><span class="sxs-lookup"><span data-stu-id="788be-267">1</span></span>     | <span data-ttu-id="788be-268">/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="788be-268">/ifd/{ushort=40091}</span></span>                     |
| <span data-ttu-id="788be-269">2</span><span class="sxs-lookup"><span data-stu-id="788be-269">2</span></span>     | <span data-ttu-id="788be-270">/IFD/XMP/DC: titolo</span><span class="sxs-lookup"><span data-stu-id="788be-270">/ifd/xmp/dc:title</span></span>                       |
| <span data-ttu-id="788be-271">3</span><span class="sxs-lookup"><span data-stu-id="788be-271">3</span></span>     | <span data-ttu-id="788be-272">/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="788be-272">/ifd/exif/{ushort=37510}</span></span>                |
| <span data-ttu-id="788be-273">4</span><span class="sxs-lookup"><span data-stu-id="788be-273">4</span></span>     | <span data-ttu-id="788be-274">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="788be-274">/ifd/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="788be-275">5</span><span class="sxs-lookup"><span data-stu-id="788be-275">5</span></span>     | <span data-ttu-id="788be-276">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="788be-276">/ifd/{ushort=270}</span></span>                       |
| <span data-ttu-id="788be-277">6</span><span class="sxs-lookup"><span data-stu-id="788be-277">6</span></span>     | <span data-ttu-id="788be-278">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="788be-278">/ifd/iptc/caption</span></span>                       |
| <span data-ttu-id="788be-279">7</span><span class="sxs-lookup"><span data-stu-id="788be-279">7</span></span>     | <span data-ttu-id="788be-280">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="788be-280">/ifd/irb/8bimiptc/iptc/caption</span></span>          |
| <span data-ttu-id="788be-281">8</span><span class="sxs-lookup"><span data-stu-id="788be-281">8</span></span>     | <span data-ttu-id="788be-282">/IFD/XMP/DC: Descrizione</span><span class="sxs-lookup"><span data-stu-id="788be-282">/ifd/xmp/dc:description</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="788be-283">Commenti</span><span class="sxs-lookup"><span data-stu-id="788be-283">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="788be-284">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="788be-284">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="788be-285">System.Title</span><span class="sxs-lookup"><span data-stu-id="788be-285">System.Title</span></span>](../properties/props-system-title.md)
</dt> </dl>

 

 
