---
description: Criteri per i metadati delle foto per la proprietà System. Photo. ISOSpeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Criteri per i metadati delle foto di System. Photo. ISOSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346601"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a><span data-ttu-id="df829-103">Criteri per i metadati delle foto di System. Photo. ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="df829-103">System.Photo.ISOSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="df829-104">Criteri per i metadati delle foto per la proprietà [System. Photo. ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) .</span><span class="sxs-lookup"><span data-stu-id="df829-104">The photo metadata policy for the [System.Photo.ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="df829-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="df829-105">PKEY</span></span>

<span data-ttu-id="df829-106">PKEY \_ Photo \_ ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="df829-106">PKEY\_Photo\_ISOSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="df829-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="df829-107">Containers</span></span>

<span data-ttu-id="df829-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="df829-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="df829-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="df829-109">Read-Only</span></span>

<span data-ttu-id="df829-110">No</span><span class="sxs-lookup"><span data-stu-id="df829-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="df829-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="df829-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="df829-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="df829-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="df829-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="df829-113">Input Type</span></span>

<span data-ttu-id="df829-114">UShort</span><span class="sxs-lookup"><span data-stu-id="df829-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="df829-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="df829-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="df829-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="df829-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="df829-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="df829-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="df829-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="df829-118">Read Paths</span></span>



| <span data-ttu-id="df829-119">JSON</span><span class="sxs-lookup"><span data-stu-id="df829-119">Order</span></span> | <span data-ttu-id="df829-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="df829-120">Path</span></span>                                    | <span data-ttu-id="df829-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="df829-121">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="df829-122">1</span><span class="sxs-lookup"><span data-stu-id="df829-122">1</span></span>     | <span data-ttu-id="df829-123">/App1/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="df829-123">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="df829-124">ushort</span><span class="sxs-lookup"><span data-stu-id="df829-124">ushort</span></span>      |
| <span data-ttu-id="df829-125">2</span><span class="sxs-lookup"><span data-stu-id="df829-125">2</span></span>     | <span data-ttu-id="df829-126">/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="df829-126">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="df829-127">unicode</span><span class="sxs-lookup"><span data-stu-id="df829-127">unicode</span></span>     |
| <span data-ttu-id="df829-128">3</span><span class="sxs-lookup"><span data-stu-id="df829-128">3</span></span>     | <span data-ttu-id="df829-129">/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="df829-129">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="df829-130">unicode</span><span class="sxs-lookup"><span data-stu-id="df829-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="df829-131">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="df829-131">Write Paths</span></span>



| <span data-ttu-id="df829-132">JSON</span><span class="sxs-lookup"><span data-stu-id="df829-132">Order</span></span> | <span data-ttu-id="df829-133">Percorso</span><span class="sxs-lookup"><span data-stu-id="df829-133">Path</span></span>                                    | <span data-ttu-id="df829-134">Formato disco</span><span class="sxs-lookup"><span data-stu-id="df829-134">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="df829-135">1</span><span class="sxs-lookup"><span data-stu-id="df829-135">1</span></span>     | <span data-ttu-id="df829-136">/App1/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="df829-136">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="df829-137">ushort</span><span class="sxs-lookup"><span data-stu-id="df829-137">ushort</span></span>      |
| <span data-ttu-id="df829-138">2</span><span class="sxs-lookup"><span data-stu-id="df829-138">2</span></span>     | <span data-ttu-id="df829-139">/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="df829-139">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="df829-140">unicode</span><span class="sxs-lookup"><span data-stu-id="df829-140">unicode</span></span>     |
| <span data-ttu-id="df829-141">3</span><span class="sxs-lookup"><span data-stu-id="df829-141">3</span></span>     | <span data-ttu-id="df829-142">/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="df829-142">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="df829-143">unicode</span><span class="sxs-lookup"><span data-stu-id="df829-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="df829-144">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="df829-144">Remove Paths</span></span>



| <span data-ttu-id="df829-145">JSON</span><span class="sxs-lookup"><span data-stu-id="df829-145">Order</span></span> | <span data-ttu-id="df829-146">Percorso</span><span class="sxs-lookup"><span data-stu-id="df829-146">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="df829-147">1</span><span class="sxs-lookup"><span data-stu-id="df829-147">1</span></span>     | <span data-ttu-id="df829-148">/App1/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="df829-148">/app1/ifd/exif/{ushort=34855}</span></span>           |
| <span data-ttu-id="df829-149">2</span><span class="sxs-lookup"><span data-stu-id="df829-149">2</span></span>     | <span data-ttu-id="df829-150">/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="df829-150">/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="df829-151">3</span><span class="sxs-lookup"><span data-stu-id="df829-151">3</span></span>     | <span data-ttu-id="df829-152">/xmp/exif:isospeed</span><span class="sxs-lookup"><span data-stu-id="df829-152">/xmp/exif:isospeed</span></span>                      |



 

### <a name="tiff-policies"></a><span data-ttu-id="df829-153">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="df829-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="df829-154">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="df829-154">Read Paths</span></span>



| <span data-ttu-id="df829-155">JSON</span><span class="sxs-lookup"><span data-stu-id="df829-155">Order</span></span> | <span data-ttu-id="df829-156">Percorso</span><span class="sxs-lookup"><span data-stu-id="df829-156">Path</span></span>                                        | <span data-ttu-id="df829-157">Formato disco</span><span class="sxs-lookup"><span data-stu-id="df829-157">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="df829-158">1</span><span class="sxs-lookup"><span data-stu-id="df829-158">1</span></span>     | <span data-ttu-id="df829-159">/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="df829-159">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="df829-160">ushort</span><span class="sxs-lookup"><span data-stu-id="df829-160">ushort</span></span>      |
| <span data-ttu-id="df829-161">2</span><span class="sxs-lookup"><span data-stu-id="df829-161">2</span></span>     | <span data-ttu-id="df829-162">/IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="df829-162">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="df829-163">unicode</span><span class="sxs-lookup"><span data-stu-id="df829-163">unicode</span></span>     |
| <span data-ttu-id="df829-164">3</span><span class="sxs-lookup"><span data-stu-id="df829-164">3</span></span>     | <span data-ttu-id="df829-165">/ifd/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="df829-165">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="df829-166">unicode</span><span class="sxs-lookup"><span data-stu-id="df829-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="df829-167">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="df829-167">Write Paths</span></span>



| <span data-ttu-id="df829-168">JSON</span><span class="sxs-lookup"><span data-stu-id="df829-168">Order</span></span> | <span data-ttu-id="df829-169">Percorso</span><span class="sxs-lookup"><span data-stu-id="df829-169">Path</span></span>                                        | <span data-ttu-id="df829-170">Formato disco</span><span class="sxs-lookup"><span data-stu-id="df829-170">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="df829-171">1</span><span class="sxs-lookup"><span data-stu-id="df829-171">1</span></span>     | <span data-ttu-id="df829-172">/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="df829-172">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="df829-173">ushort</span><span class="sxs-lookup"><span data-stu-id="df829-173">ushort</span></span>      |
| <span data-ttu-id="df829-174">2</span><span class="sxs-lookup"><span data-stu-id="df829-174">2</span></span>     | <span data-ttu-id="df829-175">/IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="df829-175">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="df829-176">unicode</span><span class="sxs-lookup"><span data-stu-id="df829-176">unicode</span></span>     |
| <span data-ttu-id="df829-177">3</span><span class="sxs-lookup"><span data-stu-id="df829-177">3</span></span>     | <span data-ttu-id="df829-178">/ifd/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="df829-178">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="df829-179">unicode</span><span class="sxs-lookup"><span data-stu-id="df829-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="df829-180">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="df829-180">Remove Paths</span></span>



| <span data-ttu-id="df829-181">JSON</span><span class="sxs-lookup"><span data-stu-id="df829-181">Order</span></span> | <span data-ttu-id="df829-182">Percorso</span><span class="sxs-lookup"><span data-stu-id="df829-182">Path</span></span>                                        |
|-------|---------------------------------------------|
| <span data-ttu-id="df829-183">1</span><span class="sxs-lookup"><span data-stu-id="df829-183">1</span></span>     | <span data-ttu-id="df829-184">/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="df829-184">/ifd/exif/{ushort=34855}</span></span>                    |
| <span data-ttu-id="df829-185">2</span><span class="sxs-lookup"><span data-stu-id="df829-185">2</span></span>     | <span data-ttu-id="df829-186">/IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="df829-186">/ifd/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="df829-187">3</span><span class="sxs-lookup"><span data-stu-id="df829-187">3</span></span>     | <span data-ttu-id="df829-188">/ifd/xmp/exif:isospeed</span><span class="sxs-lookup"><span data-stu-id="df829-188">/ifd/xmp/exif:isospeed</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="df829-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="df829-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="df829-190">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df829-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df829-191">System. Photo. ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="df829-191">System.Photo.ISOSpeed</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
