---
description: Criteri per i metadati delle foto per la proprietà System. Photo. EXIFVersion.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Criteri per i metadati delle foto di System. Photo. EXIFVersion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233332"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a><span data-ttu-id="b9005-103">Criteri per i metadati delle foto di System. Photo. EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="b9005-103">System.Photo.EXIFVersion Photo Metadata Policy</span></span>

<span data-ttu-id="b9005-104">Criteri per i metadati delle foto per la proprietà [System. Photo. EXIFVersion](../properties/props-system-photo-exifversion.md) .</span><span class="sxs-lookup"><span data-stu-id="b9005-104">The photo metadata policy for the [System.Photo.EXIFVersion](../properties/props-system-photo-exifversion.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b9005-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b9005-105">PKEY</span></span>

<span data-ttu-id="b9005-106">PKEY \_ Photo \_ EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="b9005-106">PKEY\_Photo\_EXIFVersion</span></span>

### <a name="containers"></a><span data-ttu-id="b9005-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="b9005-107">Containers</span></span>

<span data-ttu-id="b9005-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b9005-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b9005-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="b9005-109">Read-Only</span></span>

<span data-ttu-id="b9005-110">No</span><span class="sxs-lookup"><span data-stu-id="b9005-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b9005-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="b9005-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b9005-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="b9005-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="b9005-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="b9005-113">Input Type</span></span>

<span data-ttu-id="b9005-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="b9005-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b9005-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="b9005-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b9005-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="b9005-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b9005-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="b9005-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b9005-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="b9005-118">Read Paths</span></span>



| <span data-ttu-id="b9005-119">JSON</span><span class="sxs-lookup"><span data-stu-id="b9005-119">Order</span></span> | <span data-ttu-id="b9005-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9005-120">Path</span></span>                          | <span data-ttu-id="b9005-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b9005-121">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="b9005-122">1</span><span class="sxs-lookup"><span data-stu-id="b9005-122">1</span></span>     | <span data-ttu-id="b9005-123">/App1/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="b9005-123">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="b9005-124">\_versione Exif</span><span class="sxs-lookup"><span data-stu-id="b9005-124">exif\_version</span></span> |
| <span data-ttu-id="b9005-125">2</span><span class="sxs-lookup"><span data-stu-id="b9005-125">2</span></span>     | <span data-ttu-id="b9005-126">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="b9005-126">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="b9005-127">unicode</span><span class="sxs-lookup"><span data-stu-id="b9005-127">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="b9005-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="b9005-128">Write Paths</span></span>



| <span data-ttu-id="b9005-129">JSON</span><span class="sxs-lookup"><span data-stu-id="b9005-129">Order</span></span> | <span data-ttu-id="b9005-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9005-130">Path</span></span>                          | <span data-ttu-id="b9005-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b9005-131">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="b9005-132">1</span><span class="sxs-lookup"><span data-stu-id="b9005-132">1</span></span>     | <span data-ttu-id="b9005-133">/App1/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="b9005-133">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="b9005-134">\_versione Exif</span><span class="sxs-lookup"><span data-stu-id="b9005-134">exif\_version</span></span> |
| <span data-ttu-id="b9005-135">2</span><span class="sxs-lookup"><span data-stu-id="b9005-135">2</span></span>     | <span data-ttu-id="b9005-136">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="b9005-136">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="b9005-137">unicode</span><span class="sxs-lookup"><span data-stu-id="b9005-137">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="b9005-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="b9005-138">Remove Paths</span></span>



| <span data-ttu-id="b9005-139">JSON</span><span class="sxs-lookup"><span data-stu-id="b9005-139">Order</span></span> | <span data-ttu-id="b9005-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9005-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="b9005-141">1</span><span class="sxs-lookup"><span data-stu-id="b9005-141">1</span></span>     | <span data-ttu-id="b9005-142">/App1/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="b9005-142">/app1/ifd/exif/{ushort=36864}</span></span> |
| <span data-ttu-id="b9005-143">2</span><span class="sxs-lookup"><span data-stu-id="b9005-143">2</span></span>     | <span data-ttu-id="b9005-144">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="b9005-144">/xmp/exif:ExifVersion</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="b9005-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="b9005-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b9005-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="b9005-146">Read Paths</span></span>



| <span data-ttu-id="b9005-147">JSON</span><span class="sxs-lookup"><span data-stu-id="b9005-147">Order</span></span> | <span data-ttu-id="b9005-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9005-148">Path</span></span>                      | <span data-ttu-id="b9005-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b9005-149">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="b9005-150">1</span><span class="sxs-lookup"><span data-stu-id="b9005-150">1</span></span>     | <span data-ttu-id="b9005-151">/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="b9005-151">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="b9005-152">\_versione Exif</span><span class="sxs-lookup"><span data-stu-id="b9005-152">exif\_version</span></span> |
| <span data-ttu-id="b9005-153">2</span><span class="sxs-lookup"><span data-stu-id="b9005-153">2</span></span>     | <span data-ttu-id="b9005-154">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="b9005-154">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="b9005-155">unicode</span><span class="sxs-lookup"><span data-stu-id="b9005-155">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="b9005-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="b9005-156">Write Paths</span></span>



| <span data-ttu-id="b9005-157">JSON</span><span class="sxs-lookup"><span data-stu-id="b9005-157">Order</span></span> | <span data-ttu-id="b9005-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9005-158">Path</span></span>                      | <span data-ttu-id="b9005-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b9005-159">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="b9005-160">1</span><span class="sxs-lookup"><span data-stu-id="b9005-160">1</span></span>     | <span data-ttu-id="b9005-161">/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="b9005-161">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="b9005-162">\_versione Exif</span><span class="sxs-lookup"><span data-stu-id="b9005-162">exif\_version</span></span> |
| <span data-ttu-id="b9005-163">2</span><span class="sxs-lookup"><span data-stu-id="b9005-163">2</span></span>     | <span data-ttu-id="b9005-164">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="b9005-164">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="b9005-165">unicode</span><span class="sxs-lookup"><span data-stu-id="b9005-165">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="b9005-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="b9005-166">Remove Paths</span></span>



| <span data-ttu-id="b9005-167">JSON</span><span class="sxs-lookup"><span data-stu-id="b9005-167">Order</span></span> | <span data-ttu-id="b9005-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9005-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="b9005-169">1</span><span class="sxs-lookup"><span data-stu-id="b9005-169">1</span></span>     | <span data-ttu-id="b9005-170">/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="b9005-170">/ifd/exif/{ushort=36864}</span></span>  |
| <span data-ttu-id="b9005-171">2</span><span class="sxs-lookup"><span data-stu-id="b9005-171">2</span></span>     | <span data-ttu-id="b9005-172">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="b9005-172">/ifd/xmp/exif:ExifVersion</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b9005-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9005-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9005-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9005-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9005-175">System. Photo. EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="b9005-175">System.Photo.EXIFVersion</span></span>](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
