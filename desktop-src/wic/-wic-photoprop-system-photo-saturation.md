---
description: Criteri di metadati della foto per la proprietà System. Photo. saturation.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Criteri dei metadati Photo System. Photo. Saturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058048"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a><span data-ttu-id="9c0a4-103">Criteri dei metadati Photo System. Photo. Saturation</span><span class="sxs-lookup"><span data-stu-id="9c0a4-103">System.Photo.Saturation Photo Metadata Policy</span></span>

<span data-ttu-id="9c0a4-104">Criteri di metadati della foto per la proprietà [System. Photo. Saturation](../properties/props-system-photo-saturation.md) .</span><span class="sxs-lookup"><span data-stu-id="9c0a4-104">The photo metadata policy for the [System.Photo.Saturation](../properties/props-system-photo-saturation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9c0a4-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9c0a4-105">PKEY</span></span>

<span data-ttu-id="9c0a4-106">\_ \_ Saturazione foto pkey</span><span class="sxs-lookup"><span data-stu-id="9c0a4-106">PKEY\_Photo\_Saturation</span></span>

### <a name="containers"></a><span data-ttu-id="9c0a4-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="9c0a4-107">Containers</span></span>

<span data-ttu-id="9c0a4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9c0a4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9c0a4-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="9c0a4-109">Read-Only</span></span>

<span data-ttu-id="9c0a4-110">No</span><span class="sxs-lookup"><span data-stu-id="9c0a4-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9c0a4-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="9c0a4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9c0a4-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="9c0a4-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="9c0a4-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="9c0a4-113">Input Type</span></span>

<span data-ttu-id="9c0a4-114">UShort</span><span class="sxs-lookup"><span data-stu-id="9c0a4-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9c0a4-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="9c0a4-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9c0a4-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9c0a4-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="9c0a4-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9c0a4-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="9c0a4-118">Read Paths</span></span>



| <span data-ttu-id="9c0a4-119">JSON</span><span class="sxs-lookup"><span data-stu-id="9c0a4-119">Order</span></span> | <span data-ttu-id="9c0a4-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="9c0a4-120">Path</span></span>                          | <span data-ttu-id="9c0a4-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="9c0a4-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9c0a4-122">1</span><span class="sxs-lookup"><span data-stu-id="9c0a4-122">1</span></span>     | <span data-ttu-id="9c0a4-123">/App1/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="9c0a4-123">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="9c0a4-124">ushort</span><span class="sxs-lookup"><span data-stu-id="9c0a4-124">ushort</span></span>      |
| <span data-ttu-id="9c0a4-125">2</span><span class="sxs-lookup"><span data-stu-id="9c0a4-125">2</span></span>     | <span data-ttu-id="9c0a4-126">/XMP/EXIF: saturazione</span><span class="sxs-lookup"><span data-stu-id="9c0a4-126">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="9c0a4-127">unicode</span><span class="sxs-lookup"><span data-stu-id="9c0a4-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9c0a4-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="9c0a4-128">Write Paths</span></span>



| <span data-ttu-id="9c0a4-129">JSON</span><span class="sxs-lookup"><span data-stu-id="9c0a4-129">Order</span></span> | <span data-ttu-id="9c0a4-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="9c0a4-130">Path</span></span>                          | <span data-ttu-id="9c0a4-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="9c0a4-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9c0a4-132">1</span><span class="sxs-lookup"><span data-stu-id="9c0a4-132">1</span></span>     | <span data-ttu-id="9c0a4-133">/App1/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="9c0a4-133">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="9c0a4-134">ushort</span><span class="sxs-lookup"><span data-stu-id="9c0a4-134">ushort</span></span>      |
| <span data-ttu-id="9c0a4-135">2</span><span class="sxs-lookup"><span data-stu-id="9c0a4-135">2</span></span>     | <span data-ttu-id="9c0a4-136">/XMP/EXIF: saturazione</span><span class="sxs-lookup"><span data-stu-id="9c0a4-136">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="9c0a4-137">unicode</span><span class="sxs-lookup"><span data-stu-id="9c0a4-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9c0a4-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="9c0a4-138">Remove Paths</span></span>



| <span data-ttu-id="9c0a4-139">JSON</span><span class="sxs-lookup"><span data-stu-id="9c0a4-139">Order</span></span> | <span data-ttu-id="9c0a4-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="9c0a4-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="9c0a4-141">1</span><span class="sxs-lookup"><span data-stu-id="9c0a4-141">1</span></span>     | <span data-ttu-id="9c0a4-142">/App1/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="9c0a4-142">/app1/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="9c0a4-143">2</span><span class="sxs-lookup"><span data-stu-id="9c0a4-143">2</span></span>     | <span data-ttu-id="9c0a4-144">/XMP/EXIF: saturazione</span><span class="sxs-lookup"><span data-stu-id="9c0a4-144">/xmp/exif:saturation</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="9c0a4-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="9c0a4-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9c0a4-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="9c0a4-146">Read Paths</span></span>



| <span data-ttu-id="9c0a4-147">JSON</span><span class="sxs-lookup"><span data-stu-id="9c0a4-147">Order</span></span> | <span data-ttu-id="9c0a4-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="9c0a4-148">Path</span></span>                     | <span data-ttu-id="9c0a4-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="9c0a4-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="9c0a4-150">1</span><span class="sxs-lookup"><span data-stu-id="9c0a4-150">1</span></span>     | <span data-ttu-id="9c0a4-151">/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="9c0a4-151">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="9c0a4-152">ushort</span><span class="sxs-lookup"><span data-stu-id="9c0a4-152">ushort</span></span>      |
| <span data-ttu-id="9c0a4-153">2</span><span class="sxs-lookup"><span data-stu-id="9c0a4-153">2</span></span>     | <span data-ttu-id="9c0a4-154">/IFD/XMP/EXIF: saturazione</span><span class="sxs-lookup"><span data-stu-id="9c0a4-154">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="9c0a4-155">unicode</span><span class="sxs-lookup"><span data-stu-id="9c0a4-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9c0a4-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="9c0a4-156">Write Paths</span></span>



| <span data-ttu-id="9c0a4-157">JSON</span><span class="sxs-lookup"><span data-stu-id="9c0a4-157">Order</span></span> | <span data-ttu-id="9c0a4-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="9c0a4-158">Path</span></span>                     | <span data-ttu-id="9c0a4-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="9c0a4-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="9c0a4-160">1</span><span class="sxs-lookup"><span data-stu-id="9c0a4-160">1</span></span>     | <span data-ttu-id="9c0a4-161">/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="9c0a4-161">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="9c0a4-162">ushort</span><span class="sxs-lookup"><span data-stu-id="9c0a4-162">ushort</span></span>      |
| <span data-ttu-id="9c0a4-163">2</span><span class="sxs-lookup"><span data-stu-id="9c0a4-163">2</span></span>     | <span data-ttu-id="9c0a4-164">/IFD/XMP/EXIF: saturazione</span><span class="sxs-lookup"><span data-stu-id="9c0a4-164">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="9c0a4-165">unicode</span><span class="sxs-lookup"><span data-stu-id="9c0a4-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9c0a4-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="9c0a4-166">Remove Paths</span></span>



| <span data-ttu-id="9c0a4-167">JSON</span><span class="sxs-lookup"><span data-stu-id="9c0a4-167">Order</span></span> | <span data-ttu-id="9c0a4-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="9c0a4-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="9c0a4-169">1</span><span class="sxs-lookup"><span data-stu-id="9c0a4-169">1</span></span>     | <span data-ttu-id="9c0a4-170">/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="9c0a4-170">/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="9c0a4-171">2</span><span class="sxs-lookup"><span data-stu-id="9c0a4-171">2</span></span>     | <span data-ttu-id="9c0a4-172">/IFD/XMP/EXIF: saturazione</span><span class="sxs-lookup"><span data-stu-id="9c0a4-172">/ifd/xmp/exif:saturation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9c0a4-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c0a4-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c0a4-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c0a4-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c0a4-175">System. Photo. saturazione</span><span class="sxs-lookup"><span data-stu-id="9c0a4-175">System.Photo.Saturation</span></span>](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
