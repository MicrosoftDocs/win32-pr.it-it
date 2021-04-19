---
description: Criteri per i metadati delle foto per la proprietà System. Photo. DateTaken.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: Criteri per i metadati delle foto di System. Photo. DateTaken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc1d3fb50a9a94e4bb13b35a0a5726572d78429f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319107"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a><span data-ttu-id="84654-103">Criteri per i metadati delle foto di System. Photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="84654-103">System.Photo.DateTaken Photo Metadata Policy</span></span>

<span data-ttu-id="84654-104">Criteri per i metadati delle foto per la proprietà [System. Photo. DateTaken](../properties/props-system-photo-datetaken.md) .</span><span class="sxs-lookup"><span data-stu-id="84654-104">The photo metadata policy for the [System.Photo.DateTaken](../properties/props-system-photo-datetaken.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="84654-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="84654-105">PKEY</span></span>

<span data-ttu-id="84654-106">PKEY \_ Photo \_ DateTaken</span><span class="sxs-lookup"><span data-stu-id="84654-106">PKEY\_Photo\_DateTaken</span></span>

### <a name="containers"></a><span data-ttu-id="84654-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="84654-107">Containers</span></span>

<span data-ttu-id="84654-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="84654-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="84654-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="84654-109">Read-Only</span></span>

<span data-ttu-id="84654-110">No</span><span class="sxs-lookup"><span data-stu-id="84654-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="84654-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="84654-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="84654-112">FILETIME VT \_</span><span class="sxs-lookup"><span data-stu-id="84654-112">VT\_FILETIME</span></span>

### <a name="input-type"></a><span data-ttu-id="84654-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="84654-113">Input Type</span></span>

<span data-ttu-id="84654-114">Datetime</span><span class="sxs-lookup"><span data-stu-id="84654-114">DateTime</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="84654-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="84654-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="84654-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="84654-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="84654-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="84654-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="84654-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="84654-118">Read Paths</span></span>



| <span data-ttu-id="84654-119">JSON</span><span class="sxs-lookup"><span data-stu-id="84654-119">Order</span></span> | <span data-ttu-id="84654-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="84654-120">Path</span></span>                                  | <span data-ttu-id="84654-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="84654-121">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="84654-122">1</span><span class="sxs-lookup"><span data-stu-id="84654-122">1</span></span>     | <span data-ttu-id="84654-123">/App1/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="84654-123">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="84654-124">ascii</span><span class="sxs-lookup"><span data-stu-id="84654-124">ascii</span></span>       |
| <span data-ttu-id="84654-125">2</span><span class="sxs-lookup"><span data-stu-id="84654-125">2</span></span>     | <span data-ttu-id="84654-126">/App13/IRB/8bimiptc/IPTC/date creato</span><span class="sxs-lookup"><span data-stu-id="84654-126">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="84654-127">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-127">unicode</span></span>     |
| <span data-ttu-id="84654-128">3</span><span class="sxs-lookup"><span data-stu-id="84654-128">3</span></span>     | <span data-ttu-id="84654-129">/XMP/XMP: creato</span><span class="sxs-lookup"><span data-stu-id="84654-129">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="84654-130">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-130">unicode</span></span>     |
| <span data-ttu-id="84654-131">4</span><span class="sxs-lookup"><span data-stu-id="84654-131">4</span></span>     | <span data-ttu-id="84654-132">/App1/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="84654-132">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="84654-133">ascii</span><span class="sxs-lookup"><span data-stu-id="84654-133">ascii</span></span>       |
| <span data-ttu-id="84654-134">5</span><span class="sxs-lookup"><span data-stu-id="84654-134">5</span></span>     | <span data-ttu-id="84654-135">/App13/IRB/8bimiptc/IPTC/date creato</span><span class="sxs-lookup"><span data-stu-id="84654-135">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="84654-136">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-136">unicode</span></span>     |
| <span data-ttu-id="84654-137">6</span><span class="sxs-lookup"><span data-stu-id="84654-137">6</span></span>     | <span data-ttu-id="84654-138">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="84654-138">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="84654-139">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-139">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="84654-140">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="84654-140">Write Paths</span></span>



| <span data-ttu-id="84654-141">JSON</span><span class="sxs-lookup"><span data-stu-id="84654-141">Order</span></span> | <span data-ttu-id="84654-142">Percorso</span><span class="sxs-lookup"><span data-stu-id="84654-142">Path</span></span>                                  | <span data-ttu-id="84654-143">Formato disco</span><span class="sxs-lookup"><span data-stu-id="84654-143">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="84654-144">1</span><span class="sxs-lookup"><span data-stu-id="84654-144">1</span></span>     | <span data-ttu-id="84654-145">/App1/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="84654-145">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="84654-146">ascii</span><span class="sxs-lookup"><span data-stu-id="84654-146">ascii</span></span>       |
| <span data-ttu-id="84654-147">2</span><span class="sxs-lookup"><span data-stu-id="84654-147">2</span></span>     | <span data-ttu-id="84654-148">/App13/IRB/8bimiptc/IPTC/date creato</span><span class="sxs-lookup"><span data-stu-id="84654-148">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="84654-149">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-149">unicode</span></span>     |
| <span data-ttu-id="84654-150">3</span><span class="sxs-lookup"><span data-stu-id="84654-150">3</span></span>     | <span data-ttu-id="84654-151">/XMP/XMP: creato</span><span class="sxs-lookup"><span data-stu-id="84654-151">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="84654-152">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-152">unicode</span></span>     |
| <span data-ttu-id="84654-153">4</span><span class="sxs-lookup"><span data-stu-id="84654-153">4</span></span>     | <span data-ttu-id="84654-154">/App1/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="84654-154">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="84654-155">ascii</span><span class="sxs-lookup"><span data-stu-id="84654-155">ascii</span></span>       |
| <span data-ttu-id="84654-156">5</span><span class="sxs-lookup"><span data-stu-id="84654-156">5</span></span>     | <span data-ttu-id="84654-157">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="84654-157">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="84654-158">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-158">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="84654-159">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="84654-159">Remove Paths</span></span>



| <span data-ttu-id="84654-160">JSON</span><span class="sxs-lookup"><span data-stu-id="84654-160">Order</span></span> | <span data-ttu-id="84654-161">Percorso</span><span class="sxs-lookup"><span data-stu-id="84654-161">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="84654-162">1</span><span class="sxs-lookup"><span data-stu-id="84654-162">1</span></span>     | <span data-ttu-id="84654-163">/App1/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="84654-163">/app1/ifd/exif/{ushort=36867}</span></span>         |
| <span data-ttu-id="84654-164">2</span><span class="sxs-lookup"><span data-stu-id="84654-164">2</span></span>     | <span data-ttu-id="84654-165">/App1/IFD/EXIF/{ushort = 37521}</span><span class="sxs-lookup"><span data-stu-id="84654-165">/app1/ifd/exif/{ushort=37521}</span></span>         |
| <span data-ttu-id="84654-166">3</span><span class="sxs-lookup"><span data-stu-id="84654-166">3</span></span>     | <span data-ttu-id="84654-167">/App1/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="84654-167">/app1/ifd/exif/{ushort=36868}</span></span>         |
| <span data-ttu-id="84654-168">4</span><span class="sxs-lookup"><span data-stu-id="84654-168">4</span></span>     | <span data-ttu-id="84654-169">/App1/IFD/EXIF/{ushort = 37522}</span><span class="sxs-lookup"><span data-stu-id="84654-169">/app1/ifd/exif/{ushort=37522}</span></span>         |
| <span data-ttu-id="84654-170">5</span><span class="sxs-lookup"><span data-stu-id="84654-170">5</span></span>     | <span data-ttu-id="84654-171">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="84654-171">/xmp/exif:DateTimeOriginal</span></span>            |
| <span data-ttu-id="84654-172">6</span><span class="sxs-lookup"><span data-stu-id="84654-172">6</span></span>     | <span data-ttu-id="84654-173">/XMP/XMP: creato</span><span class="sxs-lookup"><span data-stu-id="84654-173">/xmp/xmp:CreateDate</span></span>                   |
| <span data-ttu-id="84654-174">7</span><span class="sxs-lookup"><span data-stu-id="84654-174">7</span></span>     | <span data-ttu-id="84654-175">/App13/IRB/8bimiptc/IPTC/date creato</span><span class="sxs-lookup"><span data-stu-id="84654-175">/app13/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="84654-176">8</span><span class="sxs-lookup"><span data-stu-id="84654-176">8</span></span>     | <span data-ttu-id="84654-177">/App13/IRB/8bimiptc/IPTC/time creato</span><span class="sxs-lookup"><span data-stu-id="84654-177">/app13/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="84654-178">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="84654-178">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="84654-179">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="84654-179">Read Paths</span></span>



| <span data-ttu-id="84654-180">JSON</span><span class="sxs-lookup"><span data-stu-id="84654-180">Order</span></span> | <span data-ttu-id="84654-181">Percorso</span><span class="sxs-lookup"><span data-stu-id="84654-181">Path</span></span>                                | <span data-ttu-id="84654-182">Formato disco</span><span class="sxs-lookup"><span data-stu-id="84654-182">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="84654-183">1</span><span class="sxs-lookup"><span data-stu-id="84654-183">1</span></span>     | <span data-ttu-id="84654-184">/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="84654-184">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="84654-185">ascii</span><span class="sxs-lookup"><span data-stu-id="84654-185">ascii</span></span>       |
| <span data-ttu-id="84654-186">2</span><span class="sxs-lookup"><span data-stu-id="84654-186">2</span></span>     | <span data-ttu-id="84654-187">/IFD/IPTC/date creato</span><span class="sxs-lookup"><span data-stu-id="84654-187">/ifd/iptc/date created</span></span>              | <span data-ttu-id="84654-188">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-188">unicode</span></span>     |
| <span data-ttu-id="84654-189">3</span><span class="sxs-lookup"><span data-stu-id="84654-189">3</span></span>     | <span data-ttu-id="84654-190">/IFD/XMP/XMP: creato</span><span class="sxs-lookup"><span data-stu-id="84654-190">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="84654-191">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-191">unicode</span></span>     |
| <span data-ttu-id="84654-192">4</span><span class="sxs-lookup"><span data-stu-id="84654-192">4</span></span>     | <span data-ttu-id="84654-193">/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="84654-193">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="84654-194">ascii</span><span class="sxs-lookup"><span data-stu-id="84654-194">ascii</span></span>       |
| <span data-ttu-id="84654-195">5</span><span class="sxs-lookup"><span data-stu-id="84654-195">5</span></span>     | <span data-ttu-id="84654-196">/IFD/IPTC/date creato</span><span class="sxs-lookup"><span data-stu-id="84654-196">/ifd/iptc/date created</span></span>              | <span data-ttu-id="84654-197">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-197">unicode</span></span>     |
| <span data-ttu-id="84654-198">6</span><span class="sxs-lookup"><span data-stu-id="84654-198">6</span></span>     | <span data-ttu-id="84654-199">/IFD/IRB/8bimiptc/IPTC/date creato</span><span class="sxs-lookup"><span data-stu-id="84654-199">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="84654-200">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-200">unicode</span></span>     |
| <span data-ttu-id="84654-201">7</span><span class="sxs-lookup"><span data-stu-id="84654-201">7</span></span>     | <span data-ttu-id="84654-202">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="84654-202">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="84654-203">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-203">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="84654-204">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="84654-204">Write Paths</span></span>



| <span data-ttu-id="84654-205">JSON</span><span class="sxs-lookup"><span data-stu-id="84654-205">Order</span></span> | <span data-ttu-id="84654-206">Percorso</span><span class="sxs-lookup"><span data-stu-id="84654-206">Path</span></span>                                | <span data-ttu-id="84654-207">Formato disco</span><span class="sxs-lookup"><span data-stu-id="84654-207">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="84654-208">1</span><span class="sxs-lookup"><span data-stu-id="84654-208">1</span></span>     | <span data-ttu-id="84654-209">/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="84654-209">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="84654-210">ascii</span><span class="sxs-lookup"><span data-stu-id="84654-210">ascii</span></span>       |
| <span data-ttu-id="84654-211">2</span><span class="sxs-lookup"><span data-stu-id="84654-211">2</span></span>     | <span data-ttu-id="84654-212">/IFD/IPTC/date creato</span><span class="sxs-lookup"><span data-stu-id="84654-212">/ifd/iptc/date created</span></span>              | <span data-ttu-id="84654-213">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-213">unicode</span></span>     |
| <span data-ttu-id="84654-214">3</span><span class="sxs-lookup"><span data-stu-id="84654-214">3</span></span>     | <span data-ttu-id="84654-215">/IFD/XMP/XMP: creato</span><span class="sxs-lookup"><span data-stu-id="84654-215">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="84654-216">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-216">unicode</span></span>     |
| <span data-ttu-id="84654-217">4</span><span class="sxs-lookup"><span data-stu-id="84654-217">4</span></span>     | <span data-ttu-id="84654-218">/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="84654-218">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="84654-219">ascii</span><span class="sxs-lookup"><span data-stu-id="84654-219">ascii</span></span>       |
| <span data-ttu-id="84654-220">5</span><span class="sxs-lookup"><span data-stu-id="84654-220">5</span></span>     | <span data-ttu-id="84654-221">/IFD/IRB/8bimiptc/IPTC/date creato</span><span class="sxs-lookup"><span data-stu-id="84654-221">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="84654-222">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-222">unicode</span></span>     |
| <span data-ttu-id="84654-223">6</span><span class="sxs-lookup"><span data-stu-id="84654-223">6</span></span>     | <span data-ttu-id="84654-224">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="84654-224">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="84654-225">unicode</span><span class="sxs-lookup"><span data-stu-id="84654-225">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="84654-226">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="84654-226">Remove Paths</span></span>



| <span data-ttu-id="84654-227">JSON</span><span class="sxs-lookup"><span data-stu-id="84654-227">Order</span></span> | <span data-ttu-id="84654-228">Percorso</span><span class="sxs-lookup"><span data-stu-id="84654-228">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="84654-229">1</span><span class="sxs-lookup"><span data-stu-id="84654-229">1</span></span>     | <span data-ttu-id="84654-230">/IFD/EXIF/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="84654-230">/ifd/exif/{ushort=36867}</span></span>            |
| <span data-ttu-id="84654-231">2</span><span class="sxs-lookup"><span data-stu-id="84654-231">2</span></span>     | <span data-ttu-id="84654-232">/IFD/EXIF/{ushort = 37521}</span><span class="sxs-lookup"><span data-stu-id="84654-232">/ifd/exif/{ushort=37521}</span></span>            |
| <span data-ttu-id="84654-233">3</span><span class="sxs-lookup"><span data-stu-id="84654-233">3</span></span>     | <span data-ttu-id="84654-234">/IFD/EXIF/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="84654-234">/ifd/exif/{ushort=36868}</span></span>            |
| <span data-ttu-id="84654-235">4</span><span class="sxs-lookup"><span data-stu-id="84654-235">4</span></span>     | <span data-ttu-id="84654-236">/IFD/EXIF/{ushort = 37522}</span><span class="sxs-lookup"><span data-stu-id="84654-236">/ifd/exif/{ushort=37522}</span></span>            |
| <span data-ttu-id="84654-237">5</span><span class="sxs-lookup"><span data-stu-id="84654-237">5</span></span>     | <span data-ttu-id="84654-238">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="84654-238">/ifd/xmp/exif:DateTimeOriginal</span></span>      |
| <span data-ttu-id="84654-239">6</span><span class="sxs-lookup"><span data-stu-id="84654-239">6</span></span>     | <span data-ttu-id="84654-240">/IFD/XMP/XMP: creato</span><span class="sxs-lookup"><span data-stu-id="84654-240">/ifd/xmp/xmp:CreateDate</span></span>             |
| <span data-ttu-id="84654-241">7</span><span class="sxs-lookup"><span data-stu-id="84654-241">7</span></span>     | <span data-ttu-id="84654-242">/IFD/IPTC/date creato</span><span class="sxs-lookup"><span data-stu-id="84654-242">/ifd/iptc/date created</span></span>              |
| <span data-ttu-id="84654-243">8</span><span class="sxs-lookup"><span data-stu-id="84654-243">8</span></span>     | <span data-ttu-id="84654-244">/IFD/IPTC/time creato</span><span class="sxs-lookup"><span data-stu-id="84654-244">/ifd/iptc/time created</span></span>              |
| <span data-ttu-id="84654-245">9</span><span class="sxs-lookup"><span data-stu-id="84654-245">9</span></span>     | <span data-ttu-id="84654-246">/IFD/IRB/8bimiptc/IPTC/date creato</span><span class="sxs-lookup"><span data-stu-id="84654-246">/ifd/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="84654-247">10</span><span class="sxs-lookup"><span data-stu-id="84654-247">10</span></span>    | <span data-ttu-id="84654-248">/IFD/IRB/8bimiptc/IPTC/time creato</span><span class="sxs-lookup"><span data-stu-id="84654-248">/ifd/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="png-policy"></a><span data-ttu-id="84654-249">Criteri PNG</span><span class="sxs-lookup"><span data-stu-id="84654-249">PNG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="84654-250">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="84654-250">Read Paths</span></span>



| <span data-ttu-id="84654-251">JSON</span><span class="sxs-lookup"><span data-stu-id="84654-251">Order</span></span> | <span data-ttu-id="84654-252">Percorso</span><span class="sxs-lookup"><span data-stu-id="84654-252">Path</span></span>                      | <span data-ttu-id="84654-253">Formato disco</span><span class="sxs-lookup"><span data-stu-id="84654-253">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="84654-254">1</span><span class="sxs-lookup"><span data-stu-id="84654-254">1</span></span>     | <span data-ttu-id="84654-255">/\[\*\]Tempo di creazione/testo</span><span class="sxs-lookup"><span data-stu-id="84654-255">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="84654-256">ascii</span><span class="sxs-lookup"><span data-stu-id="84654-256">ascii</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="84654-257">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="84654-257">Write Paths</span></span>



| <span data-ttu-id="84654-258">JSON</span><span class="sxs-lookup"><span data-stu-id="84654-258">Order</span></span> | <span data-ttu-id="84654-259">Percorso</span><span class="sxs-lookup"><span data-stu-id="84654-259">Path</span></span>                      | <span data-ttu-id="84654-260">Formato disco</span><span class="sxs-lookup"><span data-stu-id="84654-260">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="84654-261">2</span><span class="sxs-lookup"><span data-stu-id="84654-261">2</span></span>     | <span data-ttu-id="84654-262">/\[\*\]Tempo di creazione/testo</span><span class="sxs-lookup"><span data-stu-id="84654-262">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="84654-263">ascii</span><span class="sxs-lookup"><span data-stu-id="84654-263">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="84654-264">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="84654-264">Remove Paths</span></span>



| <span data-ttu-id="84654-265">JSON</span><span class="sxs-lookup"><span data-stu-id="84654-265">Order</span></span> | <span data-ttu-id="84654-266">Percorso</span><span class="sxs-lookup"><span data-stu-id="84654-266">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="84654-267">3</span><span class="sxs-lookup"><span data-stu-id="84654-267">3</span></span>     | <span data-ttu-id="84654-268">/\[\*\]Tempo di creazione/testo</span><span class="sxs-lookup"><span data-stu-id="84654-268">/\[\*\]tEXt/Creation Time</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="84654-269">Commenti</span><span class="sxs-lookup"><span data-stu-id="84654-269">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="84654-270">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84654-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84654-271">System. Photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="84654-271">System.Photo.DateTaken</span></span>](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
