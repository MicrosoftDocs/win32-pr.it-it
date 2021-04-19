---
description: Criteri per i metadati delle foto per la proprietà System. image. TextSpazio.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Criteri per i metadati delle foto System. image. TextSpazio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312957"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a><span data-ttu-id="ed429-103">Criteri per i metadati delle foto System. image. TextSpazio</span><span class="sxs-lookup"><span data-stu-id="ed429-103">System.Image.ColorSpace Photo Metadata Policy</span></span>

<span data-ttu-id="ed429-104">Criteri per i metadati delle foto per la proprietà [System. image. TextSpazio](../properties/props-system-image-colorspace.md) .</span><span class="sxs-lookup"><span data-stu-id="ed429-104">The photo metadata policy for the [System.Image.ColorSpace](../properties/props-system-image-colorspace.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ed429-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ed429-105">PKEY</span></span>

<span data-ttu-id="ed429-106">\_ \_ Spazio colore immagine pkey</span><span class="sxs-lookup"><span data-stu-id="ed429-106">PKEY\_Image\_ColorSpace</span></span>

### <a name="containers"></a><span data-ttu-id="ed429-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="ed429-107">Containers</span></span>

<span data-ttu-id="ed429-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ed429-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ed429-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="ed429-109">Read-Only</span></span>

<span data-ttu-id="ed429-110">Sì</span><span class="sxs-lookup"><span data-stu-id="ed429-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ed429-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="ed429-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ed429-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="ed429-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="ed429-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="ed429-113">Input Type</span></span>

<span data-ttu-id="ed429-114">UShort</span><span class="sxs-lookup"><span data-stu-id="ed429-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ed429-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="ed429-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ed429-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="ed429-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ed429-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="ed429-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed429-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="ed429-118">Read Paths</span></span>



| <span data-ttu-id="ed429-119">JSON</span><span class="sxs-lookup"><span data-stu-id="ed429-119">Order</span></span> | <span data-ttu-id="ed429-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed429-120">Path</span></span>                          | <span data-ttu-id="ed429-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ed429-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="ed429-122">1</span><span class="sxs-lookup"><span data-stu-id="ed429-122">1</span></span>     | <span data-ttu-id="ed429-123">/App1/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="ed429-123">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="ed429-124">ushort</span><span class="sxs-lookup"><span data-stu-id="ed429-124">ushort</span></span>      |
| <span data-ttu-id="ed429-125">2</span><span class="sxs-lookup"><span data-stu-id="ed429-125">2</span></span>     | <span data-ttu-id="ed429-126">/XMP/EXIF: spazio colore</span><span class="sxs-lookup"><span data-stu-id="ed429-126">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="ed429-127">unicode</span><span class="sxs-lookup"><span data-stu-id="ed429-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ed429-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="ed429-128">Write Paths</span></span>



| <span data-ttu-id="ed429-129">JSON</span><span class="sxs-lookup"><span data-stu-id="ed429-129">Order</span></span> | <span data-ttu-id="ed429-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed429-130">Path</span></span>                          | <span data-ttu-id="ed429-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ed429-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="ed429-132">1</span><span class="sxs-lookup"><span data-stu-id="ed429-132">1</span></span>     | <span data-ttu-id="ed429-133">/App1/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="ed429-133">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="ed429-134">ushort</span><span class="sxs-lookup"><span data-stu-id="ed429-134">ushort</span></span>      |
| <span data-ttu-id="ed429-135">2</span><span class="sxs-lookup"><span data-stu-id="ed429-135">2</span></span>     | <span data-ttu-id="ed429-136">/XMP/EXIF: spazio colore</span><span class="sxs-lookup"><span data-stu-id="ed429-136">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="ed429-137">unicode</span><span class="sxs-lookup"><span data-stu-id="ed429-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ed429-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="ed429-138">Remove Paths</span></span>



| <span data-ttu-id="ed429-139">JSON</span><span class="sxs-lookup"><span data-stu-id="ed429-139">Order</span></span> | <span data-ttu-id="ed429-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed429-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="ed429-141">1</span><span class="sxs-lookup"><span data-stu-id="ed429-141">1</span></span>     | <span data-ttu-id="ed429-142">/App1/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="ed429-142">/app1/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="ed429-143">2</span><span class="sxs-lookup"><span data-stu-id="ed429-143">2</span></span>     | <span data-ttu-id="ed429-144">/XMP/EXIF: spazio colore</span><span class="sxs-lookup"><span data-stu-id="ed429-144">/xmp/exif:colorspace</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="ed429-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="ed429-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed429-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="ed429-146">Read Paths</span></span>



| <span data-ttu-id="ed429-147">JSON</span><span class="sxs-lookup"><span data-stu-id="ed429-147">Order</span></span> | <span data-ttu-id="ed429-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed429-148">Path</span></span>                     | <span data-ttu-id="ed429-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ed429-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="ed429-150">1</span><span class="sxs-lookup"><span data-stu-id="ed429-150">1</span></span>     | <span data-ttu-id="ed429-151">/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="ed429-151">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="ed429-152">ushort</span><span class="sxs-lookup"><span data-stu-id="ed429-152">ushort</span></span>      |
| <span data-ttu-id="ed429-153">2</span><span class="sxs-lookup"><span data-stu-id="ed429-153">2</span></span>     | <span data-ttu-id="ed429-154">/IFD/XMP/EXIF: spazio colore</span><span class="sxs-lookup"><span data-stu-id="ed429-154">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="ed429-155">unicode</span><span class="sxs-lookup"><span data-stu-id="ed429-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ed429-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="ed429-156">Write Paths</span></span>



| <span data-ttu-id="ed429-157">JSON</span><span class="sxs-lookup"><span data-stu-id="ed429-157">Order</span></span> | <span data-ttu-id="ed429-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed429-158">Path</span></span>                     | <span data-ttu-id="ed429-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ed429-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="ed429-160">1</span><span class="sxs-lookup"><span data-stu-id="ed429-160">1</span></span>     | <span data-ttu-id="ed429-161">/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="ed429-161">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="ed429-162">ushort</span><span class="sxs-lookup"><span data-stu-id="ed429-162">ushort</span></span>      |
| <span data-ttu-id="ed429-163">2</span><span class="sxs-lookup"><span data-stu-id="ed429-163">2</span></span>     | <span data-ttu-id="ed429-164">/IFD/XMP/EXIF: spazio colore</span><span class="sxs-lookup"><span data-stu-id="ed429-164">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="ed429-165">unicode</span><span class="sxs-lookup"><span data-stu-id="ed429-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ed429-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="ed429-166">Remove Paths</span></span>



| <span data-ttu-id="ed429-167">JSON</span><span class="sxs-lookup"><span data-stu-id="ed429-167">Order</span></span> | <span data-ttu-id="ed429-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed429-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="ed429-169">1</span><span class="sxs-lookup"><span data-stu-id="ed429-169">1</span></span>     | <span data-ttu-id="ed429-170">/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="ed429-170">/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="ed429-171">2</span><span class="sxs-lookup"><span data-stu-id="ed429-171">2</span></span>     | <span data-ttu-id="ed429-172">/IFD/XMP/EXIF: spazio colore</span><span class="sxs-lookup"><span data-stu-id="ed429-172">/ifd/xmp/exif:colorspace</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ed429-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed429-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed429-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed429-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed429-175">System. image. spazio colore</span><span class="sxs-lookup"><span data-stu-id="ed429-175">System.Image.ColorSpace</span></span>](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
