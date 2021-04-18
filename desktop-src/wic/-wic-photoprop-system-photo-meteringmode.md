---
description: Criteri per i metadati delle foto per la proprietà System. Photo. MeteringMode.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: Criteri per i metadati delle foto di System. Photo. MeteringMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a4443521c84113e4e2a6f4c2b9b2b3f822ae90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315967"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a><span data-ttu-id="a909d-103">Criteri per i metadati delle foto di System. Photo. MeteringMode</span><span class="sxs-lookup"><span data-stu-id="a909d-103">System.Photo.MeteringMode Photo Metadata Policy</span></span>

<span data-ttu-id="a909d-104">Criteri per i metadati delle foto per la proprietà [System. Photo. meteringmode](../properties/props-system-photo-meteringmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a909d-104">The photo metadata policy for the [System.Photo.MeteringMode](../properties/props-system-photo-meteringmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a909d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a909d-105">PKEY</span></span>

<span data-ttu-id="a909d-106">PKEY \_ Photo \_ meteringmode</span><span class="sxs-lookup"><span data-stu-id="a909d-106">PKEY\_Photo\_MeteringMode</span></span>

### <a name="containers"></a><span data-ttu-id="a909d-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="a909d-107">Containers</span></span>

<span data-ttu-id="a909d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a909d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a909d-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="a909d-109">Read-Only</span></span>

<span data-ttu-id="a909d-110">No</span><span class="sxs-lookup"><span data-stu-id="a909d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a909d-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="a909d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a909d-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="a909d-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="a909d-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="a909d-113">Input Type</span></span>

<span data-ttu-id="a909d-114">UShort</span><span class="sxs-lookup"><span data-stu-id="a909d-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a909d-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="a909d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a909d-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="a909d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a909d-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="a909d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a909d-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="a909d-118">Read Paths</span></span>



| <span data-ttu-id="a909d-119">JSON</span><span class="sxs-lookup"><span data-stu-id="a909d-119">Order</span></span> | <span data-ttu-id="a909d-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="a909d-120">Path</span></span>                          | <span data-ttu-id="a909d-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="a909d-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a909d-122">1</span><span class="sxs-lookup"><span data-stu-id="a909d-122">1</span></span>     | <span data-ttu-id="a909d-123">/App1/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="a909d-123">/app1/ifd/exif/{ushort=37383}</span></span> | <span data-ttu-id="a909d-124">ushort</span><span class="sxs-lookup"><span data-stu-id="a909d-124">ushort</span></span>      |
| <span data-ttu-id="a909d-125">2</span><span class="sxs-lookup"><span data-stu-id="a909d-125">2</span></span>     | <span data-ttu-id="a909d-126">/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="a909d-126">/xmp/exif:MeteringMode</span></span>        | <span data-ttu-id="a909d-127">unicode</span><span class="sxs-lookup"><span data-stu-id="a909d-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a909d-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="a909d-128">Write Paths</span></span>



| <span data-ttu-id="a909d-129">JSON</span><span class="sxs-lookup"><span data-stu-id="a909d-129">Order</span></span> | <span data-ttu-id="a909d-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="a909d-130">Path</span></span>                          | <span data-ttu-id="a909d-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="a909d-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a909d-132">1</span><span class="sxs-lookup"><span data-stu-id="a909d-132">1</span></span>     | <span data-ttu-id="a909d-133">/App1/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="a909d-133">/app1/ifd/exif/{ushort=37383}</span></span> | <span data-ttu-id="a909d-134">ushort</span><span class="sxs-lookup"><span data-stu-id="a909d-134">ushort</span></span>      |
| <span data-ttu-id="a909d-135">2</span><span class="sxs-lookup"><span data-stu-id="a909d-135">2</span></span>     | <span data-ttu-id="a909d-136">/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="a909d-136">/xmp/exif:MeteringMode</span></span>        | <span data-ttu-id="a909d-137">unicode</span><span class="sxs-lookup"><span data-stu-id="a909d-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a909d-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="a909d-138">Remove Paths</span></span>



| <span data-ttu-id="a909d-139">JSON</span><span class="sxs-lookup"><span data-stu-id="a909d-139">Order</span></span> | <span data-ttu-id="a909d-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="a909d-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a909d-141">1</span><span class="sxs-lookup"><span data-stu-id="a909d-141">1</span></span>     | <span data-ttu-id="a909d-142">/App1/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="a909d-142">/app1/ifd/exif/{ushort=37383}</span></span> |
| <span data-ttu-id="a909d-143">2</span><span class="sxs-lookup"><span data-stu-id="a909d-143">2</span></span>     | <span data-ttu-id="a909d-144">/xmp/exif:meteringmode</span><span class="sxs-lookup"><span data-stu-id="a909d-144">/xmp/exif:meteringmode</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="a909d-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="a909d-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a909d-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="a909d-146">Read Paths</span></span>



| <span data-ttu-id="a909d-147">JSON</span><span class="sxs-lookup"><span data-stu-id="a909d-147">Order</span></span> | <span data-ttu-id="a909d-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="a909d-148">Path</span></span>                       | <span data-ttu-id="a909d-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="a909d-149">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="a909d-150">1</span><span class="sxs-lookup"><span data-stu-id="a909d-150">1</span></span>     | <span data-ttu-id="a909d-151">/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="a909d-151">/ifd/exif/{ushort=37383}</span></span>   | <span data-ttu-id="a909d-152">ushort</span><span class="sxs-lookup"><span data-stu-id="a909d-152">ushort</span></span>      |
| <span data-ttu-id="a909d-153">2</span><span class="sxs-lookup"><span data-stu-id="a909d-153">2</span></span>     | <span data-ttu-id="a909d-154">/ifd/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="a909d-154">/ifd/xmp/exif:MeteringMode</span></span> | <span data-ttu-id="a909d-155">unicode</span><span class="sxs-lookup"><span data-stu-id="a909d-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a909d-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="a909d-156">Write Paths</span></span>



| <span data-ttu-id="a909d-157">JSON</span><span class="sxs-lookup"><span data-stu-id="a909d-157">Order</span></span> | <span data-ttu-id="a909d-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="a909d-158">Path</span></span>                       | <span data-ttu-id="a909d-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="a909d-159">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="a909d-160">1</span><span class="sxs-lookup"><span data-stu-id="a909d-160">1</span></span>     | <span data-ttu-id="a909d-161">/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="a909d-161">/ifd/exif/{ushort=37383}</span></span>   | <span data-ttu-id="a909d-162">ushort</span><span class="sxs-lookup"><span data-stu-id="a909d-162">ushort</span></span>      |
| <span data-ttu-id="a909d-163">2</span><span class="sxs-lookup"><span data-stu-id="a909d-163">2</span></span>     | <span data-ttu-id="a909d-164">/ifd/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="a909d-164">/ifd/xmp/exif:MeteringMode</span></span> | <span data-ttu-id="a909d-165">unicode</span><span class="sxs-lookup"><span data-stu-id="a909d-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a909d-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="a909d-166">Remove Paths</span></span>



| <span data-ttu-id="a909d-167">JSON</span><span class="sxs-lookup"><span data-stu-id="a909d-167">Order</span></span> | <span data-ttu-id="a909d-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="a909d-168">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="a909d-169">1</span><span class="sxs-lookup"><span data-stu-id="a909d-169">1</span></span>     | <span data-ttu-id="a909d-170">/IFD/EXIF/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="a909d-170">/ifd/exif/{ushort=37383}</span></span>   |
| <span data-ttu-id="a909d-171">2</span><span class="sxs-lookup"><span data-stu-id="a909d-171">2</span></span>     | <span data-ttu-id="a909d-172">/ifd/xmp/exif:meteringmode</span><span class="sxs-lookup"><span data-stu-id="a909d-172">/ifd/xmp/exif:meteringmode</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a909d-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="a909d-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a909d-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a909d-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a909d-175">System. Photo. MeteringMode</span><span class="sxs-lookup"><span data-stu-id="a909d-175">System.Photo.MeteringMode</span></span>](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
