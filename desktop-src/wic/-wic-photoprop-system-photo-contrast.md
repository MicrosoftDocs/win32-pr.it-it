---
description: Criteri di metadati della foto per la proprietà System. Photo. Contrast.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Criteri dei metadati della foto System. Photo. Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530264"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a><span data-ttu-id="1996c-103">Criteri dei metadati della foto System. Photo. Contrast</span><span class="sxs-lookup"><span data-stu-id="1996c-103">System.Photo.Contrast Photo Metadata Policy</span></span>

<span data-ttu-id="1996c-104">Criteri di metadati della foto per la proprietà [System. Photo. Contrast](../properties/props-system-photo-contrast.md) .</span><span class="sxs-lookup"><span data-stu-id="1996c-104">The photo metadata policy for the [System.Photo.Contrast](../properties/props-system-photo-contrast.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1996c-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="1996c-105">PKEY</span></span>

<span data-ttu-id="1996c-106">\_Contrasto foto \_ pkey</span><span class="sxs-lookup"><span data-stu-id="1996c-106">PKEY\_Photo\_Contrast</span></span>

### <a name="containers"></a><span data-ttu-id="1996c-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="1996c-107">Containers</span></span>

<span data-ttu-id="1996c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1996c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1996c-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="1996c-109">Read-Only</span></span>

<span data-ttu-id="1996c-110">No</span><span class="sxs-lookup"><span data-stu-id="1996c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1996c-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="1996c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1996c-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="1996c-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="1996c-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="1996c-113">Input Type</span></span>

<span data-ttu-id="1996c-114">UShort</span><span class="sxs-lookup"><span data-stu-id="1996c-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1996c-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="1996c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="1996c-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="1996c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1996c-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="1996c-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1996c-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="1996c-118">Read Paths</span></span>



| <span data-ttu-id="1996c-119">JSON</span><span class="sxs-lookup"><span data-stu-id="1996c-119">Order</span></span> | <span data-ttu-id="1996c-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="1996c-120">Path</span></span>                          | <span data-ttu-id="1996c-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1996c-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1996c-122">1</span><span class="sxs-lookup"><span data-stu-id="1996c-122">1</span></span>     | <span data-ttu-id="1996c-123">/App1/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="1996c-123">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="1996c-124">ushort</span><span class="sxs-lookup"><span data-stu-id="1996c-124">ushort</span></span>      |
| <span data-ttu-id="1996c-125">2</span><span class="sxs-lookup"><span data-stu-id="1996c-125">2</span></span>     | <span data-ttu-id="1996c-126">/XMP/EXIF: contrasto</span><span class="sxs-lookup"><span data-stu-id="1996c-126">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="1996c-127">unicode</span><span class="sxs-lookup"><span data-stu-id="1996c-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1996c-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="1996c-128">Write Paths</span></span>



| <span data-ttu-id="1996c-129">JSON</span><span class="sxs-lookup"><span data-stu-id="1996c-129">Order</span></span> | <span data-ttu-id="1996c-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="1996c-130">Path</span></span>                          | <span data-ttu-id="1996c-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1996c-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1996c-132">1</span><span class="sxs-lookup"><span data-stu-id="1996c-132">1</span></span>     | <span data-ttu-id="1996c-133">/App1/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="1996c-133">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="1996c-134">ushort</span><span class="sxs-lookup"><span data-stu-id="1996c-134">ushort</span></span>      |
| <span data-ttu-id="1996c-135">2</span><span class="sxs-lookup"><span data-stu-id="1996c-135">2</span></span>     | <span data-ttu-id="1996c-136">/XMP/EXIF: contrasto</span><span class="sxs-lookup"><span data-stu-id="1996c-136">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="1996c-137">unicode</span><span class="sxs-lookup"><span data-stu-id="1996c-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1996c-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="1996c-138">Remove Paths</span></span>



| <span data-ttu-id="1996c-139">JSON</span><span class="sxs-lookup"><span data-stu-id="1996c-139">Order</span></span> | <span data-ttu-id="1996c-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="1996c-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="1996c-141">1</span><span class="sxs-lookup"><span data-stu-id="1996c-141">1</span></span>     | <span data-ttu-id="1996c-142">/App1/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="1996c-142">/app1/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="1996c-143">2</span><span class="sxs-lookup"><span data-stu-id="1996c-143">2</span></span>     | <span data-ttu-id="1996c-144">/XMP/EXIF: contrasto</span><span class="sxs-lookup"><span data-stu-id="1996c-144">/xmp/exif:contrast</span></span>            |



 

### <a name="tiff-policies"></a><span data-ttu-id="1996c-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="1996c-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1996c-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="1996c-146">Read Paths</span></span>



| <span data-ttu-id="1996c-147">JSON</span><span class="sxs-lookup"><span data-stu-id="1996c-147">Order</span></span> | <span data-ttu-id="1996c-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="1996c-148">Path</span></span>                     | <span data-ttu-id="1996c-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1996c-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1996c-150">1</span><span class="sxs-lookup"><span data-stu-id="1996c-150">1</span></span>     | <span data-ttu-id="1996c-151">/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="1996c-151">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="1996c-152">ushort</span><span class="sxs-lookup"><span data-stu-id="1996c-152">ushort</span></span>      |
| <span data-ttu-id="1996c-153">2</span><span class="sxs-lookup"><span data-stu-id="1996c-153">2</span></span>     | <span data-ttu-id="1996c-154">/IFD/XMP/EXIF: contrasto</span><span class="sxs-lookup"><span data-stu-id="1996c-154">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="1996c-155">unicode</span><span class="sxs-lookup"><span data-stu-id="1996c-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1996c-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="1996c-156">Write Paths</span></span>



| <span data-ttu-id="1996c-157">JSON</span><span class="sxs-lookup"><span data-stu-id="1996c-157">Order</span></span> | <span data-ttu-id="1996c-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="1996c-158">Path</span></span>                     | <span data-ttu-id="1996c-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1996c-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1996c-160">1</span><span class="sxs-lookup"><span data-stu-id="1996c-160">1</span></span>     | <span data-ttu-id="1996c-161">/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="1996c-161">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="1996c-162">ushort</span><span class="sxs-lookup"><span data-stu-id="1996c-162">ushort</span></span>      |
| <span data-ttu-id="1996c-163">2</span><span class="sxs-lookup"><span data-stu-id="1996c-163">2</span></span>     | <span data-ttu-id="1996c-164">/IFD/XMP/EXIF: contrasto</span><span class="sxs-lookup"><span data-stu-id="1996c-164">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="1996c-165">unicode</span><span class="sxs-lookup"><span data-stu-id="1996c-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1996c-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="1996c-166">Remove Paths</span></span>



| <span data-ttu-id="1996c-167">JSON</span><span class="sxs-lookup"><span data-stu-id="1996c-167">Order</span></span> | <span data-ttu-id="1996c-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="1996c-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="1996c-169">1</span><span class="sxs-lookup"><span data-stu-id="1996c-169">1</span></span>     | <span data-ttu-id="1996c-170">/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="1996c-170">/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="1996c-171">2</span><span class="sxs-lookup"><span data-stu-id="1996c-171">2</span></span>     | <span data-ttu-id="1996c-172">/IFD/XMP/EXIF: contrasto</span><span class="sxs-lookup"><span data-stu-id="1996c-172">/ifd/xmp/exif:contrast</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="1996c-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="1996c-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1996c-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1996c-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1996c-175">System. Photo. Contrast</span><span class="sxs-lookup"><span data-stu-id="1996c-175">System.Photo.Contrast</span></span>](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
