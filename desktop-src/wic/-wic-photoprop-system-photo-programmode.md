---
description: Criteri per i metadati delle foto per la proprietà System. Photo. ProgramMode.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: Criteri per i metadati delle foto di System. Photo. ProgramMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968116"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a><span data-ttu-id="da4ce-103">Criteri per i metadati delle foto di System. Photo. ProgramMode</span><span class="sxs-lookup"><span data-stu-id="da4ce-103">System.Photo.ProgramMode Photo Metadata Policy</span></span>

<span data-ttu-id="da4ce-104">Criteri per i metadati delle foto per la proprietà [System. Photo. ProgramMode](../properties/props-system-photo-programmode.md) .</span><span class="sxs-lookup"><span data-stu-id="da4ce-104">The photo metadata policy for the [System.Photo.ProgramMode](../properties/props-system-photo-programmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="da4ce-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="da4ce-105">PKEY</span></span>

<span data-ttu-id="da4ce-106">PKEY \_ Photo \_ ProgramMode</span><span class="sxs-lookup"><span data-stu-id="da4ce-106">PKEY\_Photo\_ProgramMode</span></span>

### <a name="containers"></a><span data-ttu-id="da4ce-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="da4ce-107">Containers</span></span>

<span data-ttu-id="da4ce-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="da4ce-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="da4ce-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="da4ce-109">Read-Only</span></span>

<span data-ttu-id="da4ce-110">No</span><span class="sxs-lookup"><span data-stu-id="da4ce-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="da4ce-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="da4ce-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="da4ce-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="da4ce-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="da4ce-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="da4ce-113">Input Type</span></span>

<span data-ttu-id="da4ce-114">UShort</span><span class="sxs-lookup"><span data-stu-id="da4ce-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="da4ce-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="da4ce-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="da4ce-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="da4ce-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="da4ce-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="da4ce-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="da4ce-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="da4ce-118">Read Paths</span></span>



| <span data-ttu-id="da4ce-119">JSON</span><span class="sxs-lookup"><span data-stu-id="da4ce-119">Order</span></span> | <span data-ttu-id="da4ce-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="da4ce-120">Path</span></span>                          | <span data-ttu-id="da4ce-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="da4ce-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="da4ce-122">1</span><span class="sxs-lookup"><span data-stu-id="da4ce-122">1</span></span>     | <span data-ttu-id="da4ce-123">/App1/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="da4ce-123">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="da4ce-124">ushort</span><span class="sxs-lookup"><span data-stu-id="da4ce-124">ushort</span></span>      |
| <span data-ttu-id="da4ce-125">2</span><span class="sxs-lookup"><span data-stu-id="da4ce-125">2</span></span>     | <span data-ttu-id="da4ce-126">/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="da4ce-126">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="da4ce-127">unicode</span><span class="sxs-lookup"><span data-stu-id="da4ce-127">unicode</span></span>     |
| <span data-ttu-id="da4ce-128">3</span><span class="sxs-lookup"><span data-stu-id="da4ce-128">3</span></span>     | <span data-ttu-id="da4ce-129">/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="da4ce-129">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="da4ce-130">unicode</span><span class="sxs-lookup"><span data-stu-id="da4ce-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="da4ce-131">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="da4ce-131">Write Paths</span></span>



| <span data-ttu-id="da4ce-132">JSON</span><span class="sxs-lookup"><span data-stu-id="da4ce-132">Order</span></span> | <span data-ttu-id="da4ce-133">Percorso</span><span class="sxs-lookup"><span data-stu-id="da4ce-133">Path</span></span>                          | <span data-ttu-id="da4ce-134">Formato disco</span><span class="sxs-lookup"><span data-stu-id="da4ce-134">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="da4ce-135">1</span><span class="sxs-lookup"><span data-stu-id="da4ce-135">1</span></span>     | <span data-ttu-id="da4ce-136">/App1/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="da4ce-136">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="da4ce-137">ushort</span><span class="sxs-lookup"><span data-stu-id="da4ce-137">ushort</span></span>      |
| <span data-ttu-id="da4ce-138">2</span><span class="sxs-lookup"><span data-stu-id="da4ce-138">2</span></span>     | <span data-ttu-id="da4ce-139">/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="da4ce-139">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="da4ce-140">unicode</span><span class="sxs-lookup"><span data-stu-id="da4ce-140">unicode</span></span>     |
| <span data-ttu-id="da4ce-141">3</span><span class="sxs-lookup"><span data-stu-id="da4ce-141">3</span></span>     | <span data-ttu-id="da4ce-142">/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="da4ce-142">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="da4ce-143">unicode</span><span class="sxs-lookup"><span data-stu-id="da4ce-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="da4ce-144">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="da4ce-144">Remove Paths</span></span>



| <span data-ttu-id="da4ce-145">JSON</span><span class="sxs-lookup"><span data-stu-id="da4ce-145">Order</span></span> | <span data-ttu-id="da4ce-146">Percorso</span><span class="sxs-lookup"><span data-stu-id="da4ce-146">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="da4ce-147">1</span><span class="sxs-lookup"><span data-stu-id="da4ce-147">1</span></span>     | <span data-ttu-id="da4ce-148">/App1/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="da4ce-148">/app1/ifd/exif/{ushort=34850}</span></span> |
| <span data-ttu-id="da4ce-149">2</span><span class="sxs-lookup"><span data-stu-id="da4ce-149">2</span></span>     | <span data-ttu-id="da4ce-150">/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="da4ce-150">/xmp/exif:exposureprogram</span></span>     |
| <span data-ttu-id="da4ce-151">3</span><span class="sxs-lookup"><span data-stu-id="da4ce-151">3</span></span>     | <span data-ttu-id="da4ce-152">/xmp/exif:programmode</span><span class="sxs-lookup"><span data-stu-id="da4ce-152">/xmp/exif:programmode</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="da4ce-153">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="da4ce-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="da4ce-154">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="da4ce-154">Read Paths</span></span>



| <span data-ttu-id="da4ce-155">JSON</span><span class="sxs-lookup"><span data-stu-id="da4ce-155">Order</span></span> | <span data-ttu-id="da4ce-156">Percorso</span><span class="sxs-lookup"><span data-stu-id="da4ce-156">Path</span></span>                          | <span data-ttu-id="da4ce-157">Formato disco</span><span class="sxs-lookup"><span data-stu-id="da4ce-157">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="da4ce-158">1</span><span class="sxs-lookup"><span data-stu-id="da4ce-158">1</span></span>     | <span data-ttu-id="da4ce-159">/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="da4ce-159">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="da4ce-160">ushort</span><span class="sxs-lookup"><span data-stu-id="da4ce-160">ushort</span></span>      |
| <span data-ttu-id="da4ce-161">2</span><span class="sxs-lookup"><span data-stu-id="da4ce-161">2</span></span>     | <span data-ttu-id="da4ce-162">/IFD/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="da4ce-162">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="da4ce-163">unicode</span><span class="sxs-lookup"><span data-stu-id="da4ce-163">unicode</span></span>     |
| <span data-ttu-id="da4ce-164">3</span><span class="sxs-lookup"><span data-stu-id="da4ce-164">3</span></span>     | <span data-ttu-id="da4ce-165">/ifd/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="da4ce-165">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="da4ce-166">unicode</span><span class="sxs-lookup"><span data-stu-id="da4ce-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="da4ce-167">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="da4ce-167">Write Paths</span></span>



| <span data-ttu-id="da4ce-168">JSON</span><span class="sxs-lookup"><span data-stu-id="da4ce-168">Order</span></span> | <span data-ttu-id="da4ce-169">Percorso</span><span class="sxs-lookup"><span data-stu-id="da4ce-169">Path</span></span>                          | <span data-ttu-id="da4ce-170">Formato disco</span><span class="sxs-lookup"><span data-stu-id="da4ce-170">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="da4ce-171">1</span><span class="sxs-lookup"><span data-stu-id="da4ce-171">1</span></span>     | <span data-ttu-id="da4ce-172">/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="da4ce-172">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="da4ce-173">ushort</span><span class="sxs-lookup"><span data-stu-id="da4ce-173">ushort</span></span>      |
| <span data-ttu-id="da4ce-174">2</span><span class="sxs-lookup"><span data-stu-id="da4ce-174">2</span></span>     | <span data-ttu-id="da4ce-175">/IFD/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="da4ce-175">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="da4ce-176">unicode</span><span class="sxs-lookup"><span data-stu-id="da4ce-176">unicode</span></span>     |
| <span data-ttu-id="da4ce-177">3</span><span class="sxs-lookup"><span data-stu-id="da4ce-177">3</span></span>     | <span data-ttu-id="da4ce-178">/ifd/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="da4ce-178">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="da4ce-179">unicode</span><span class="sxs-lookup"><span data-stu-id="da4ce-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="da4ce-180">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="da4ce-180">Remove Paths</span></span>



| <span data-ttu-id="da4ce-181">JSON</span><span class="sxs-lookup"><span data-stu-id="da4ce-181">Order</span></span> | <span data-ttu-id="da4ce-182">Percorso</span><span class="sxs-lookup"><span data-stu-id="da4ce-182">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="da4ce-183">1</span><span class="sxs-lookup"><span data-stu-id="da4ce-183">1</span></span>     | <span data-ttu-id="da4ce-184">/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="da4ce-184">/ifd/exif/{ushort=34850}</span></span>      |
| <span data-ttu-id="da4ce-185">2</span><span class="sxs-lookup"><span data-stu-id="da4ce-185">2</span></span>     | <span data-ttu-id="da4ce-186">/IFD/XMP/EXIF: ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="da4ce-186">/ifd/xmp/exif:exposureprogram</span></span> |
| <span data-ttu-id="da4ce-187">3</span><span class="sxs-lookup"><span data-stu-id="da4ce-187">3</span></span>     | <span data-ttu-id="da4ce-188">/ifd/xmp/exif:programmode</span><span class="sxs-lookup"><span data-stu-id="da4ce-188">/ifd/xmp/exif:programmode</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="da4ce-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="da4ce-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="da4ce-190">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da4ce-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da4ce-191">System. Photo. ProgramMode</span><span class="sxs-lookup"><span data-stu-id="da4ce-191">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
