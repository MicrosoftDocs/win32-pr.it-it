---
description: Criteri per i metadati delle foto per la proprietà System. Photo. RelatedSoundFile.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: Criteri per i metadati delle foto di System. Photo. RelatedSoundFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a29adb71f572868f21b1b8427e71b09616b24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968115"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a><span data-ttu-id="11df4-103">Criteri per i metadati delle foto di System. Photo. RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="11df4-103">System.Photo.RelatedSoundFile Photo Metadata Policy</span></span>

<span data-ttu-id="11df4-104">Criteri per i metadati delle foto per la proprietà [System. Photo. RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md) .</span><span class="sxs-lookup"><span data-stu-id="11df4-104">The photo metadata policy for the [System.Photo.RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="11df4-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="11df4-105">PKEY</span></span>

<span data-ttu-id="11df4-106">PKEY \_ Photo \_ RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="11df4-106">PKEY\_Photo\_RelatedSoundFile</span></span>

### <a name="containers"></a><span data-ttu-id="11df4-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="11df4-107">Containers</span></span>

<span data-ttu-id="11df4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="11df4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="11df4-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="11df4-109">Read-Only</span></span>

<span data-ttu-id="11df4-110">No</span><span class="sxs-lookup"><span data-stu-id="11df4-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="11df4-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="11df4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="11df4-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="11df4-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="11df4-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="11df4-113">Input Type</span></span>

<span data-ttu-id="11df4-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="11df4-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="11df4-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="11df4-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="11df4-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="11df4-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="11df4-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="11df4-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="11df4-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="11df4-118">Read Paths</span></span>



| <span data-ttu-id="11df4-119">JSON</span><span class="sxs-lookup"><span data-stu-id="11df4-119">Order</span></span> | <span data-ttu-id="11df4-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="11df4-120">Path</span></span>                          | <span data-ttu-id="11df4-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="11df4-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="11df4-122">1</span><span class="sxs-lookup"><span data-stu-id="11df4-122">1</span></span>     | <span data-ttu-id="11df4-123">/App1/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="11df4-123">/app1/ifd/exif/{ushort=40964}</span></span> | <span data-ttu-id="11df4-124">ascii</span><span class="sxs-lookup"><span data-stu-id="11df4-124">ascii</span></span>       |
| <span data-ttu-id="11df4-125">2</span><span class="sxs-lookup"><span data-stu-id="11df4-125">2</span></span>     | <span data-ttu-id="11df4-126">/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="11df4-126">/xmp/exif:RelatedSoundFile</span></span>    | <span data-ttu-id="11df4-127">unicode</span><span class="sxs-lookup"><span data-stu-id="11df4-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="11df4-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="11df4-128">Write Paths</span></span>



| <span data-ttu-id="11df4-129">JSON</span><span class="sxs-lookup"><span data-stu-id="11df4-129">Order</span></span> | <span data-ttu-id="11df4-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="11df4-130">Path</span></span>                          | <span data-ttu-id="11df4-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="11df4-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="11df4-132">1</span><span class="sxs-lookup"><span data-stu-id="11df4-132">1</span></span>     | <span data-ttu-id="11df4-133">/App1/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="11df4-133">/app1/ifd/exif/{ushort=40964}</span></span> | <span data-ttu-id="11df4-134">ascii</span><span class="sxs-lookup"><span data-stu-id="11df4-134">ascii</span></span>       |
| <span data-ttu-id="11df4-135">2</span><span class="sxs-lookup"><span data-stu-id="11df4-135">2</span></span>     | <span data-ttu-id="11df4-136">/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="11df4-136">/xmp/exif:RelatedSoundFile</span></span>    | <span data-ttu-id="11df4-137">unicode</span><span class="sxs-lookup"><span data-stu-id="11df4-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="11df4-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="11df4-138">Remove Paths</span></span>



| <span data-ttu-id="11df4-139">JSON</span><span class="sxs-lookup"><span data-stu-id="11df4-139">Order</span></span> | <span data-ttu-id="11df4-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="11df4-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="11df4-141">1</span><span class="sxs-lookup"><span data-stu-id="11df4-141">1</span></span>     | <span data-ttu-id="11df4-142">/App1/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="11df4-142">/app1/ifd/exif/{ushort=40964}</span></span> |
| <span data-ttu-id="11df4-143">2</span><span class="sxs-lookup"><span data-stu-id="11df4-143">2</span></span>     | <span data-ttu-id="11df4-144">/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="11df4-144">/xmp/exif:RelatedSoundFile</span></span>    |



 

### <a name="tiff-policy"></a><span data-ttu-id="11df4-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="11df4-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="11df4-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="11df4-146">Read Paths</span></span>



| <span data-ttu-id="11df4-147">JSON</span><span class="sxs-lookup"><span data-stu-id="11df4-147">Order</span></span> | <span data-ttu-id="11df4-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="11df4-148">Path</span></span>                           | <span data-ttu-id="11df4-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="11df4-149">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="11df4-150">1</span><span class="sxs-lookup"><span data-stu-id="11df4-150">1</span></span>     | <span data-ttu-id="11df4-151">/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="11df4-151">/ifd/exif/{ushort=40964}</span></span>       | <span data-ttu-id="11df4-152">ascii</span><span class="sxs-lookup"><span data-stu-id="11df4-152">ascii</span></span>       |
| <span data-ttu-id="11df4-153">2</span><span class="sxs-lookup"><span data-stu-id="11df4-153">2</span></span>     | <span data-ttu-id="11df4-154">/ifd/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="11df4-154">/ifd/xmp/exif:RelatedSoundFile</span></span> | <span data-ttu-id="11df4-155">unicode</span><span class="sxs-lookup"><span data-stu-id="11df4-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="11df4-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="11df4-156">Write Paths</span></span>



| <span data-ttu-id="11df4-157">JSON</span><span class="sxs-lookup"><span data-stu-id="11df4-157">Order</span></span> | <span data-ttu-id="11df4-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="11df4-158">Path</span></span>                           | <span data-ttu-id="11df4-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="11df4-159">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="11df4-160">1</span><span class="sxs-lookup"><span data-stu-id="11df4-160">1</span></span>     | <span data-ttu-id="11df4-161">/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="11df4-161">/ifd/exif/{ushort=40964}</span></span>       | <span data-ttu-id="11df4-162">ascii</span><span class="sxs-lookup"><span data-stu-id="11df4-162">ascii</span></span>       |
| <span data-ttu-id="11df4-163">2</span><span class="sxs-lookup"><span data-stu-id="11df4-163">2</span></span>     | <span data-ttu-id="11df4-164">/ifd/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="11df4-164">/ifd/xmp/exif:RelatedSoundFile</span></span> | <span data-ttu-id="11df4-165">unicode</span><span class="sxs-lookup"><span data-stu-id="11df4-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="11df4-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="11df4-166">Remove Paths</span></span>



| <span data-ttu-id="11df4-167">JSON</span><span class="sxs-lookup"><span data-stu-id="11df4-167">Order</span></span> | <span data-ttu-id="11df4-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="11df4-168">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="11df4-169">1</span><span class="sxs-lookup"><span data-stu-id="11df4-169">1</span></span>     | <span data-ttu-id="11df4-170">/IFD/EXIF/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="11df4-170">/ifd/exif/{ushort=40964}</span></span>       |
| <span data-ttu-id="11df4-171">2</span><span class="sxs-lookup"><span data-stu-id="11df4-171">2</span></span>     | <span data-ttu-id="11df4-172">/ifd/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="11df4-172">/ifd/xmp/exif:RelatedSoundFile</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="11df4-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="11df4-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="11df4-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11df4-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11df4-175">System. Photo. RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="11df4-175">System.Photo.RelatedSoundFile</span></span>](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
