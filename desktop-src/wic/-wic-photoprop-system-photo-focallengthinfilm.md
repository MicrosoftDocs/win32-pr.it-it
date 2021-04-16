---
description: Criteri per i metadati delle foto per la proprietà System. Photo. FocalLengthInFilm.
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: Criteri per i metadati delle foto di System. Photo. FocalLengthInFilm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485701"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a><span data-ttu-id="2103a-103">Criteri per i metadati delle foto di System. Photo. FocalLengthInFilm</span><span class="sxs-lookup"><span data-stu-id="2103a-103">System.Photo.FocalLengthInFilm Photo Metadata Policy</span></span>

<span data-ttu-id="2103a-104">Criteri per i metadati delle foto per la proprietà [System. Photo. FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) .</span><span class="sxs-lookup"><span data-stu-id="2103a-104">The photo metadata policy for the [System.Photo.FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="2103a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="2103a-105">PKEY</span></span>

<span data-ttu-id="2103a-106">\_FOCALLENGTHINFILM pkey</span><span class="sxs-lookup"><span data-stu-id="2103a-106">PKEY\_FocalLengthInFilm</span></span>

### <a name="containers"></a><span data-ttu-id="2103a-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="2103a-107">Containers</span></span>

<span data-ttu-id="2103a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="2103a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="2103a-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="2103a-109">Read-Only</span></span>

<span data-ttu-id="2103a-110">No</span><span class="sxs-lookup"><span data-stu-id="2103a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="2103a-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="2103a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="2103a-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="2103a-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="2103a-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="2103a-113">Input Type</span></span>

<span data-ttu-id="2103a-114">UShort</span><span class="sxs-lookup"><span data-stu-id="2103a-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="2103a-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="2103a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="2103a-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="2103a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="2103a-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="2103a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="2103a-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="2103a-118">Read Paths</span></span>



| <span data-ttu-id="2103a-119">JSON</span><span class="sxs-lookup"><span data-stu-id="2103a-119">Order</span></span> | <span data-ttu-id="2103a-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="2103a-120">Path</span></span>                            | <span data-ttu-id="2103a-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="2103a-121">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="2103a-122">1</span><span class="sxs-lookup"><span data-stu-id="2103a-122">1</span></span>     | <span data-ttu-id="2103a-123">/App1/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="2103a-123">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="2103a-124">ushort</span><span class="sxs-lookup"><span data-stu-id="2103a-124">ushort</span></span>      |
| <span data-ttu-id="2103a-125">2</span><span class="sxs-lookup"><span data-stu-id="2103a-125">2</span></span>     | <span data-ttu-id="2103a-126">/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="2103a-126">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="2103a-127">unicode</span><span class="sxs-lookup"><span data-stu-id="2103a-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2103a-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="2103a-128">Write Paths</span></span>



| <span data-ttu-id="2103a-129">JSON</span><span class="sxs-lookup"><span data-stu-id="2103a-129">Order</span></span> | <span data-ttu-id="2103a-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="2103a-130">Path</span></span>                            | <span data-ttu-id="2103a-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="2103a-131">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="2103a-132">1</span><span class="sxs-lookup"><span data-stu-id="2103a-132">1</span></span>     | <span data-ttu-id="2103a-133">/App1/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="2103a-133">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="2103a-134">ushort</span><span class="sxs-lookup"><span data-stu-id="2103a-134">ushort</span></span>      |
| <span data-ttu-id="2103a-135">2</span><span class="sxs-lookup"><span data-stu-id="2103a-135">2</span></span>     | <span data-ttu-id="2103a-136">/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="2103a-136">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="2103a-137">unicode</span><span class="sxs-lookup"><span data-stu-id="2103a-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2103a-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="2103a-138">Remove Paths</span></span>



| <span data-ttu-id="2103a-139">JSON</span><span class="sxs-lookup"><span data-stu-id="2103a-139">Order</span></span> | <span data-ttu-id="2103a-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="2103a-140">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="2103a-141">1</span><span class="sxs-lookup"><span data-stu-id="2103a-141">1</span></span>     | <span data-ttu-id="2103a-142">/App1/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="2103a-142">/app1/ifd/exif/{ushort=41989}</span></span>   |
| <span data-ttu-id="2103a-143">2</span><span class="sxs-lookup"><span data-stu-id="2103a-143">2</span></span>     | <span data-ttu-id="2103a-144">/xmp/exif:focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="2103a-144">/xmp/exif:focallengthin35mmfilm</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="2103a-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="2103a-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="2103a-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="2103a-146">Read Paths</span></span>



| <span data-ttu-id="2103a-147">JSON</span><span class="sxs-lookup"><span data-stu-id="2103a-147">Order</span></span> | <span data-ttu-id="2103a-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="2103a-148">Path</span></span>                                | <span data-ttu-id="2103a-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="2103a-149">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="2103a-150">1</span><span class="sxs-lookup"><span data-stu-id="2103a-150">1</span></span>     | <span data-ttu-id="2103a-151">/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="2103a-151">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="2103a-152">ushort</span><span class="sxs-lookup"><span data-stu-id="2103a-152">ushort</span></span>      |
| <span data-ttu-id="2103a-153">2</span><span class="sxs-lookup"><span data-stu-id="2103a-153">2</span></span>     | <span data-ttu-id="2103a-154">/ifd/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="2103a-154">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="2103a-155">unicode</span><span class="sxs-lookup"><span data-stu-id="2103a-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2103a-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="2103a-156">Write Paths</span></span>



| <span data-ttu-id="2103a-157">JSON</span><span class="sxs-lookup"><span data-stu-id="2103a-157">Order</span></span> | <span data-ttu-id="2103a-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="2103a-158">Path</span></span>                                | <span data-ttu-id="2103a-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="2103a-159">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="2103a-160">1</span><span class="sxs-lookup"><span data-stu-id="2103a-160">1</span></span>     | <span data-ttu-id="2103a-161">/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="2103a-161">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="2103a-162">ushort</span><span class="sxs-lookup"><span data-stu-id="2103a-162">ushort</span></span>      |
| <span data-ttu-id="2103a-163">2</span><span class="sxs-lookup"><span data-stu-id="2103a-163">2</span></span>     | <span data-ttu-id="2103a-164">/ifd/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="2103a-164">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="2103a-165">unicode</span><span class="sxs-lookup"><span data-stu-id="2103a-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2103a-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="2103a-166">Remove Paths</span></span>



| <span data-ttu-id="2103a-167">JSON</span><span class="sxs-lookup"><span data-stu-id="2103a-167">Order</span></span> | <span data-ttu-id="2103a-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="2103a-168">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="2103a-169">1</span><span class="sxs-lookup"><span data-stu-id="2103a-169">1</span></span>     | <span data-ttu-id="2103a-170">/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="2103a-170">/ifd/exif/{ushort=41989}</span></span>            |
| <span data-ttu-id="2103a-171">2</span><span class="sxs-lookup"><span data-stu-id="2103a-171">2</span></span>     | <span data-ttu-id="2103a-172">/ifd/xmp/exif:focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="2103a-172">/ifd/xmp/exif:focallengthin35mmfilm</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2103a-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="2103a-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="2103a-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2103a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2103a-175">System. Photo. FocalLengthInFilm</span><span class="sxs-lookup"><span data-stu-id="2103a-175">System.Photo.FocalLengthInFilm</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
