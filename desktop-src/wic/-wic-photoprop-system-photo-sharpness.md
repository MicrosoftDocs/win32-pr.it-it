---
description: Criteri per i metadati delle foto per la proprietà System. Photo. Nitidity.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Criteri dei metadati della foto System. Photo. nitidezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315964"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a><span data-ttu-id="23316-103">Criteri dei metadati della foto System. Photo. nitidezza</span><span class="sxs-lookup"><span data-stu-id="23316-103">System.Photo.Sharpness Photo Metadata Policy</span></span>

<span data-ttu-id="23316-104">Criteri per i metadati delle foto per la proprietà [System. Photo. nitidity](../properties/props-system-photo-sharpness.md) .</span><span class="sxs-lookup"><span data-stu-id="23316-104">The photo metadata policy for the [System.Photo.Sharpness](../properties/props-system-photo-sharpness.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="23316-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="23316-105">PKEY</span></span>

<span data-ttu-id="23316-106">\_ \_ Nitidezza foto pkey</span><span class="sxs-lookup"><span data-stu-id="23316-106">PKEY\_Photo\_Sharpness</span></span>

### <a name="containers"></a><span data-ttu-id="23316-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="23316-107">Containers</span></span>

<span data-ttu-id="23316-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="23316-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="23316-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="23316-109">Read-Only</span></span>

<span data-ttu-id="23316-110">No</span><span class="sxs-lookup"><span data-stu-id="23316-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="23316-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="23316-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="23316-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="23316-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="23316-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="23316-113">Input Type</span></span>

<span data-ttu-id="23316-114">UShort</span><span class="sxs-lookup"><span data-stu-id="23316-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="23316-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="23316-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="23316-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="23316-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="23316-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="23316-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="23316-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="23316-118">Read Paths</span></span>



| <span data-ttu-id="23316-119">JSON</span><span class="sxs-lookup"><span data-stu-id="23316-119">Order</span></span> | <span data-ttu-id="23316-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="23316-120">Path</span></span>                          | <span data-ttu-id="23316-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="23316-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="23316-122">1</span><span class="sxs-lookup"><span data-stu-id="23316-122">1</span></span>     | <span data-ttu-id="23316-123">/App1/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="23316-123">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="23316-124">ushort</span><span class="sxs-lookup"><span data-stu-id="23316-124">ushort</span></span>      |
| <span data-ttu-id="23316-125">2</span><span class="sxs-lookup"><span data-stu-id="23316-125">2</span></span>     | <span data-ttu-id="23316-126">/XMP/EXIF: nitidezza</span><span class="sxs-lookup"><span data-stu-id="23316-126">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="23316-127">unicode</span><span class="sxs-lookup"><span data-stu-id="23316-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="23316-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="23316-128">Write Paths</span></span>



| <span data-ttu-id="23316-129">JSON</span><span class="sxs-lookup"><span data-stu-id="23316-129">Order</span></span> | <span data-ttu-id="23316-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="23316-130">Path</span></span>                          | <span data-ttu-id="23316-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="23316-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="23316-132">1</span><span class="sxs-lookup"><span data-stu-id="23316-132">1</span></span>     | <span data-ttu-id="23316-133">/App1/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="23316-133">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="23316-134">ushort</span><span class="sxs-lookup"><span data-stu-id="23316-134">ushort</span></span>      |
| <span data-ttu-id="23316-135">2</span><span class="sxs-lookup"><span data-stu-id="23316-135">2</span></span>     | <span data-ttu-id="23316-136">/XMP/EXIF: nitidezza</span><span class="sxs-lookup"><span data-stu-id="23316-136">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="23316-137">unicode</span><span class="sxs-lookup"><span data-stu-id="23316-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="23316-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="23316-138">Remove Paths</span></span>



| <span data-ttu-id="23316-139">JSON</span><span class="sxs-lookup"><span data-stu-id="23316-139">Order</span></span> | <span data-ttu-id="23316-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="23316-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="23316-141">1</span><span class="sxs-lookup"><span data-stu-id="23316-141">1</span></span>     | <span data-ttu-id="23316-142">/App1/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="23316-142">/app1/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="23316-143">2</span><span class="sxs-lookup"><span data-stu-id="23316-143">2</span></span>     | <span data-ttu-id="23316-144">/XMP/EXIF: nitidezza</span><span class="sxs-lookup"><span data-stu-id="23316-144">/xmp/exif:sharpness</span></span>           |



 

### <a name="tiff-policies"></a><span data-ttu-id="23316-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="23316-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="23316-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="23316-146">Read Paths</span></span>



| <span data-ttu-id="23316-147">JSON</span><span class="sxs-lookup"><span data-stu-id="23316-147">Order</span></span> | <span data-ttu-id="23316-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="23316-148">Path</span></span>                     | <span data-ttu-id="23316-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="23316-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="23316-150">1</span><span class="sxs-lookup"><span data-stu-id="23316-150">1</span></span>     | <span data-ttu-id="23316-151">/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="23316-151">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="23316-152">ushort</span><span class="sxs-lookup"><span data-stu-id="23316-152">ushort</span></span>      |
| <span data-ttu-id="23316-153">2</span><span class="sxs-lookup"><span data-stu-id="23316-153">2</span></span>     | <span data-ttu-id="23316-154">/IFD/XMP/EXIF: nitidezza</span><span class="sxs-lookup"><span data-stu-id="23316-154">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="23316-155">unicode</span><span class="sxs-lookup"><span data-stu-id="23316-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="23316-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="23316-156">Write Paths</span></span>



| <span data-ttu-id="23316-157">JSON</span><span class="sxs-lookup"><span data-stu-id="23316-157">Order</span></span> | <span data-ttu-id="23316-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="23316-158">Path</span></span>                     | <span data-ttu-id="23316-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="23316-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="23316-160">1</span><span class="sxs-lookup"><span data-stu-id="23316-160">1</span></span>     | <span data-ttu-id="23316-161">/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="23316-161">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="23316-162">ushort</span><span class="sxs-lookup"><span data-stu-id="23316-162">ushort</span></span>      |
| <span data-ttu-id="23316-163">2</span><span class="sxs-lookup"><span data-stu-id="23316-163">2</span></span>     | <span data-ttu-id="23316-164">/IFD/XMP/EXIF: nitidezza</span><span class="sxs-lookup"><span data-stu-id="23316-164">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="23316-165">unicode</span><span class="sxs-lookup"><span data-stu-id="23316-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="23316-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="23316-166">Remove Paths</span></span>



| <span data-ttu-id="23316-167">JSON</span><span class="sxs-lookup"><span data-stu-id="23316-167">Order</span></span> | <span data-ttu-id="23316-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="23316-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="23316-169">1</span><span class="sxs-lookup"><span data-stu-id="23316-169">1</span></span>     | <span data-ttu-id="23316-170">/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="23316-170">/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="23316-171">2</span><span class="sxs-lookup"><span data-stu-id="23316-171">2</span></span>     | <span data-ttu-id="23316-172">/IFD/XMP/EXIF: nitidezza</span><span class="sxs-lookup"><span data-stu-id="23316-172">/ifd/xmp/exif:sharpness</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="23316-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="23316-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="23316-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23316-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23316-175">System. Photo. nitidezza</span><span class="sxs-lookup"><span data-stu-id="23316-175">System.Photo.Sharpness</span></span>](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
