---
description: Criteri per i metadati delle foto per la proprietà System. Photo. MaxAperture.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: Criteri per i metadati delle foto di System. Photo. MaxAperture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314446"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a><span data-ttu-id="b9c5f-103">Criteri per i metadati delle foto di System. Photo. MaxAperture</span><span class="sxs-lookup"><span data-stu-id="b9c5f-103">System.Photo.MaxAperture Photo Metadata Policy</span></span>

<span data-ttu-id="b9c5f-104">Criteri per i metadati delle foto per la proprietà [System. Photo. MaxAperture](../properties/props-system-photo-maxaperture.md) .</span><span class="sxs-lookup"><span data-stu-id="b9c5f-104">The photo metadata policy for the [System.Photo.MaxAperture](../properties/props-system-photo-maxaperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b9c5f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b9c5f-105">PKEY</span></span>

<span data-ttu-id="b9c5f-106">PKEY \_ Photo \_ MaxAperture</span><span class="sxs-lookup"><span data-stu-id="b9c5f-106">PKEY\_Photo\_MaxAperture</span></span>

### <a name="containers"></a><span data-ttu-id="b9c5f-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="b9c5f-107">Containers</span></span>

<span data-ttu-id="b9c5f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b9c5f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b9c5f-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="b9c5f-109">Read-Only</span></span>

<span data-ttu-id="b9c5f-110">Sì</span><span class="sxs-lookup"><span data-stu-id="b9c5f-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b9c5f-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="b9c5f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b9c5f-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="b9c5f-112">VT\_R8</span></span>

### <a name="input-type"></a><span data-ttu-id="b9c5f-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="b9c5f-113">Input Type</span></span>

<span data-ttu-id="b9c5f-114">Double</span><span class="sxs-lookup"><span data-stu-id="b9c5f-114">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b9c5f-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="b9c5f-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b9c5f-116">Questo valore viene generato da System. Photo. MaxApertureNumerator e System. Photo. MaxApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="b9c5f-116">This value is generated from System.Photo.MaxApertureNumerator and System.Photo.MaxApertureDenominator.</span></span> <span data-ttu-id="b9c5f-117">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="b9c5f-117">It cannot be written directly.</span></span> <span data-ttu-id="b9c5f-118">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="b9c5f-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b9c5f-119">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="b9c5f-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b9c5f-120">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="b9c5f-120">Read Paths</span></span>



| <span data-ttu-id="b9c5f-121">JSON</span><span class="sxs-lookup"><span data-stu-id="b9c5f-121">Order</span></span> | <span data-ttu-id="b9c5f-122">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9c5f-122">Path</span></span>                          | <span data-ttu-id="b9c5f-123">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b9c5f-123">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b9c5f-124">1</span><span class="sxs-lookup"><span data-stu-id="b9c5f-124">1</span></span>     | <span data-ttu-id="b9c5f-125">/App1/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="b9c5f-125">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="b9c5f-126">2</span><span class="sxs-lookup"><span data-stu-id="b9c5f-126">2</span></span>     | <span data-ttu-id="b9c5f-127">/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="b9c5f-127">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="b9c5f-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="b9c5f-128">Write Paths</span></span>



| <span data-ttu-id="b9c5f-129">JSON</span><span class="sxs-lookup"><span data-stu-id="b9c5f-129">Order</span></span> | <span data-ttu-id="b9c5f-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9c5f-130">Path</span></span>                          | <span data-ttu-id="b9c5f-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b9c5f-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b9c5f-132">1</span><span class="sxs-lookup"><span data-stu-id="b9c5f-132">1</span></span>     | <span data-ttu-id="b9c5f-133">/App1/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="b9c5f-133">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="b9c5f-134">2</span><span class="sxs-lookup"><span data-stu-id="b9c5f-134">2</span></span>     | <span data-ttu-id="b9c5f-135">/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="b9c5f-135">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b9c5f-136">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="b9c5f-136">Remove Paths</span></span>



| <span data-ttu-id="b9c5f-137">JSON</span><span class="sxs-lookup"><span data-stu-id="b9c5f-137">Order</span></span> | <span data-ttu-id="b9c5f-138">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9c5f-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="b9c5f-139">1</span><span class="sxs-lookup"><span data-stu-id="b9c5f-139">1</span></span>     | <span data-ttu-id="b9c5f-140">/App1/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="b9c5f-140">/app1/ifd/exif/{ushort=37381}</span></span> |
| <span data-ttu-id="b9c5f-141">2</span><span class="sxs-lookup"><span data-stu-id="b9c5f-141">2</span></span>     | <span data-ttu-id="b9c5f-142">/xmp/exif:maxaperturevalue</span><span class="sxs-lookup"><span data-stu-id="b9c5f-142">/xmp/exif:maxaperturevalue</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="b9c5f-143">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="b9c5f-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b9c5f-144">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="b9c5f-144">Read Paths</span></span>



| <span data-ttu-id="b9c5f-145">JSON</span><span class="sxs-lookup"><span data-stu-id="b9c5f-145">Order</span></span> | <span data-ttu-id="b9c5f-146">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9c5f-146">Path</span></span>                           | <span data-ttu-id="b9c5f-147">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b9c5f-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="b9c5f-148">1</span><span class="sxs-lookup"><span data-stu-id="b9c5f-148">1</span></span>     | <span data-ttu-id="b9c5f-149">/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="b9c5f-149">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="b9c5f-150">2</span><span class="sxs-lookup"><span data-stu-id="b9c5f-150">2</span></span>     | <span data-ttu-id="b9c5f-151">/ifd/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="b9c5f-151">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b9c5f-152">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="b9c5f-152">Write Paths</span></span>



| <span data-ttu-id="b9c5f-153">JSON</span><span class="sxs-lookup"><span data-stu-id="b9c5f-153">Order</span></span> | <span data-ttu-id="b9c5f-154">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9c5f-154">Path</span></span>                           | <span data-ttu-id="b9c5f-155">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b9c5f-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="b9c5f-156">1</span><span class="sxs-lookup"><span data-stu-id="b9c5f-156">1</span></span>     | <span data-ttu-id="b9c5f-157">/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="b9c5f-157">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="b9c5f-158">2</span><span class="sxs-lookup"><span data-stu-id="b9c5f-158">2</span></span>     | <span data-ttu-id="b9c5f-159">/ifd/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="b9c5f-159">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b9c5f-160">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="b9c5f-160">Remove Paths</span></span>



| <span data-ttu-id="b9c5f-161">JSON</span><span class="sxs-lookup"><span data-stu-id="b9c5f-161">Order</span></span> | <span data-ttu-id="b9c5f-162">Percorso</span><span class="sxs-lookup"><span data-stu-id="b9c5f-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="b9c5f-163">1</span><span class="sxs-lookup"><span data-stu-id="b9c5f-163">1</span></span>     | <span data-ttu-id="b9c5f-164">/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="b9c5f-164">/ifd/exif/{ushort=37381}</span></span>       |
| <span data-ttu-id="b9c5f-165">2</span><span class="sxs-lookup"><span data-stu-id="b9c5f-165">2</span></span>     | <span data-ttu-id="b9c5f-166">/ifd/xmp/exif:maxaperturevalue</span><span class="sxs-lookup"><span data-stu-id="b9c5f-166">/ifd/xmp/exif:maxaperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b9c5f-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9c5f-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9c5f-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9c5f-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9c5f-169">System. Photo. MaxAperture</span><span class="sxs-lookup"><span data-stu-id="b9c5f-169">System.Photo.MaxAperture</span></span>](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
