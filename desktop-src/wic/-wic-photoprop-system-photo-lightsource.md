---
description: Criteri per i metadati delle foto per la proprietà System. Photo. LightSource.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Criteri per i metadati delle foto di System. Photo. LightSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529935"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a><span data-ttu-id="321c7-103">Criteri per i metadati delle foto di System. Photo. LightSource</span><span class="sxs-lookup"><span data-stu-id="321c7-103">System.Photo.LightSource Photo Metadata Policy</span></span>

<span data-ttu-id="321c7-104">Criteri per i metadati delle foto per la proprietà [System. Photo. LightSource](../properties/props-system-photo-lightsource.md) .</span><span class="sxs-lookup"><span data-stu-id="321c7-104">The photo metadata policy for the [System.Photo.LightSource](../properties/props-system-photo-lightsource.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="321c7-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="321c7-105">PKEY</span></span>

<span data-ttu-id="321c7-106">PKEY \_ Photo \_ LightSource</span><span class="sxs-lookup"><span data-stu-id="321c7-106">PKEY\_Photo\_LightSource</span></span>

### <a name="containers"></a><span data-ttu-id="321c7-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="321c7-107">Containers</span></span>

<span data-ttu-id="321c7-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="321c7-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="321c7-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="321c7-109">Read-Only</span></span>

<span data-ttu-id="321c7-110">No</span><span class="sxs-lookup"><span data-stu-id="321c7-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="321c7-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="321c7-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="321c7-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="321c7-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="321c7-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="321c7-113">Input Type</span></span>

<span data-ttu-id="321c7-114">UShort</span><span class="sxs-lookup"><span data-stu-id="321c7-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="321c7-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="321c7-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="321c7-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="321c7-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="321c7-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="321c7-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="321c7-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="321c7-118">Read Paths</span></span>



| <span data-ttu-id="321c7-119">JSON</span><span class="sxs-lookup"><span data-stu-id="321c7-119">Order</span></span> | <span data-ttu-id="321c7-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="321c7-120">Path</span></span>                          | <span data-ttu-id="321c7-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="321c7-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="321c7-122">1</span><span class="sxs-lookup"><span data-stu-id="321c7-122">1</span></span>     | <span data-ttu-id="321c7-123">/App1/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="321c7-123">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="321c7-124">ushort</span><span class="sxs-lookup"><span data-stu-id="321c7-124">ushort</span></span>      |
| <span data-ttu-id="321c7-125">2</span><span class="sxs-lookup"><span data-stu-id="321c7-125">2</span></span>     | <span data-ttu-id="321c7-126">/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="321c7-126">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="321c7-127">unicode</span><span class="sxs-lookup"><span data-stu-id="321c7-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="321c7-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="321c7-128">Write Paths</span></span>



| <span data-ttu-id="321c7-129">JSON</span><span class="sxs-lookup"><span data-stu-id="321c7-129">Order</span></span> | <span data-ttu-id="321c7-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="321c7-130">Path</span></span>                          | <span data-ttu-id="321c7-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="321c7-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="321c7-132">1</span><span class="sxs-lookup"><span data-stu-id="321c7-132">1</span></span>     | <span data-ttu-id="321c7-133">/App1/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="321c7-133">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="321c7-134">ushort</span><span class="sxs-lookup"><span data-stu-id="321c7-134">ushort</span></span>      |
| <span data-ttu-id="321c7-135">2</span><span class="sxs-lookup"><span data-stu-id="321c7-135">2</span></span>     | <span data-ttu-id="321c7-136">/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="321c7-136">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="321c7-137">unicode</span><span class="sxs-lookup"><span data-stu-id="321c7-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="321c7-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="321c7-138">Remove Paths</span></span>



| <span data-ttu-id="321c7-139">JSON</span><span class="sxs-lookup"><span data-stu-id="321c7-139">Order</span></span> | <span data-ttu-id="321c7-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="321c7-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="321c7-141">1</span><span class="sxs-lookup"><span data-stu-id="321c7-141">1</span></span>     | <span data-ttu-id="321c7-142">/App1/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="321c7-142">/app1/ifd/exif/{ushort=37384}</span></span> |
| <span data-ttu-id="321c7-143">2</span><span class="sxs-lookup"><span data-stu-id="321c7-143">2</span></span>     | <span data-ttu-id="321c7-144">/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="321c7-144">/xmp/exif:lightsource</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="321c7-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="321c7-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="321c7-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="321c7-146">Read Paths</span></span>



| <span data-ttu-id="321c7-147">JSON</span><span class="sxs-lookup"><span data-stu-id="321c7-147">Order</span></span> | <span data-ttu-id="321c7-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="321c7-148">Path</span></span>                      | <span data-ttu-id="321c7-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="321c7-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="321c7-150">1</span><span class="sxs-lookup"><span data-stu-id="321c7-150">1</span></span>     | <span data-ttu-id="321c7-151">/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="321c7-151">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="321c7-152">ushort</span><span class="sxs-lookup"><span data-stu-id="321c7-152">ushort</span></span>      |
| <span data-ttu-id="321c7-153">2</span><span class="sxs-lookup"><span data-stu-id="321c7-153">2</span></span>     | <span data-ttu-id="321c7-154">/IFD/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="321c7-154">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="321c7-155">unicode</span><span class="sxs-lookup"><span data-stu-id="321c7-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="321c7-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="321c7-156">Write Paths</span></span>



| <span data-ttu-id="321c7-157">JSON</span><span class="sxs-lookup"><span data-stu-id="321c7-157">Order</span></span> | <span data-ttu-id="321c7-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="321c7-158">Path</span></span>                      | <span data-ttu-id="321c7-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="321c7-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="321c7-160">1</span><span class="sxs-lookup"><span data-stu-id="321c7-160">1</span></span>     | <span data-ttu-id="321c7-161">/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="321c7-161">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="321c7-162">ushort</span><span class="sxs-lookup"><span data-stu-id="321c7-162">ushort</span></span>      |
| <span data-ttu-id="321c7-163">2</span><span class="sxs-lookup"><span data-stu-id="321c7-163">2</span></span>     | <span data-ttu-id="321c7-164">/IFD/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="321c7-164">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="321c7-165">unicode</span><span class="sxs-lookup"><span data-stu-id="321c7-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="321c7-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="321c7-166">Remove Paths</span></span>



| <span data-ttu-id="321c7-167">JSON</span><span class="sxs-lookup"><span data-stu-id="321c7-167">Order</span></span> | <span data-ttu-id="321c7-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="321c7-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="321c7-169">1</span><span class="sxs-lookup"><span data-stu-id="321c7-169">1</span></span>     | <span data-ttu-id="321c7-170">/IFD/EXIF/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="321c7-170">/ifd/exif/{ushort=37384}</span></span>  |
| <span data-ttu-id="321c7-171">2</span><span class="sxs-lookup"><span data-stu-id="321c7-171">2</span></span>     | <span data-ttu-id="321c7-172">/IFD/XMP/EXIF: LightSource</span><span class="sxs-lookup"><span data-stu-id="321c7-172">/ifd/xmp/exif:lightsource</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="321c7-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="321c7-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="321c7-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="321c7-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="321c7-175">System. Photo. LightSource</span><span class="sxs-lookup"><span data-stu-id="321c7-175">System.Photo.LightSource</span></span>](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
