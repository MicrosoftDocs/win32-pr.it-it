---
description: Criteri per i metadati delle foto per la proprietà System. Photo. luminosità.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Criteri per i metadati delle foto System. Photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968332"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a><span data-ttu-id="1a316-103">Criteri per i metadati delle foto System. Photo. Brightness</span><span class="sxs-lookup"><span data-stu-id="1a316-103">System.Photo.Brightness Photo Metadata Policy</span></span>

<span data-ttu-id="1a316-104">Criteri per i metadati delle foto per la proprietà [System. Photo. luminosità](../properties/props-system-photo-aperture.md) .</span><span class="sxs-lookup"><span data-stu-id="1a316-104">The photo metadata policy for the [System.Photo.Brightness](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1a316-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="1a316-105">PKEY</span></span>

<span data-ttu-id="1a316-106">PKEY \_ \_ luminosità foto</span><span class="sxs-lookup"><span data-stu-id="1a316-106">PKEY\_Photo\_Brightness</span></span>

### <a name="containers"></a><span data-ttu-id="1a316-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="1a316-107">Containers</span></span>

<span data-ttu-id="1a316-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1a316-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1a316-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="1a316-109">Read-Only</span></span>

<span data-ttu-id="1a316-110">Sì</span><span class="sxs-lookup"><span data-stu-id="1a316-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="1a316-111">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="1a316-111">Input Type</span></span>

<span data-ttu-id="1a316-112">Double</span><span class="sxs-lookup"><span data-stu-id="1a316-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1a316-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="1a316-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="1a316-114">Questo valore viene generato da System. Photo. ApertureNumerator e System. Photo. ApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="1a316-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="1a316-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="1a316-115">It cannot be written directly.</span></span> <span data-ttu-id="1a316-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="1a316-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1a316-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="1a316-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1a316-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="1a316-118">Read Paths</span></span>



| <span data-ttu-id="1a316-119">JSON</span><span class="sxs-lookup"><span data-stu-id="1a316-119">Order</span></span> | <span data-ttu-id="1a316-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="1a316-120">Path</span></span>                          | <span data-ttu-id="1a316-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1a316-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1a316-122">1</span><span class="sxs-lookup"><span data-stu-id="1a316-122">1</span></span>     | <span data-ttu-id="1a316-123">/App1/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="1a316-123">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="1a316-124">2</span><span class="sxs-lookup"><span data-stu-id="1a316-124">2</span></span>     | <span data-ttu-id="1a316-125">/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="1a316-125">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="1a316-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="1a316-126">Write Paths</span></span>



| <span data-ttu-id="1a316-127">JSON</span><span class="sxs-lookup"><span data-stu-id="1a316-127">Order</span></span> | <span data-ttu-id="1a316-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="1a316-128">Path</span></span>                          | <span data-ttu-id="1a316-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1a316-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1a316-130">1</span><span class="sxs-lookup"><span data-stu-id="1a316-130">1</span></span>     | <span data-ttu-id="1a316-131">/App1/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="1a316-131">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="1a316-132">2</span><span class="sxs-lookup"><span data-stu-id="1a316-132">2</span></span>     | <span data-ttu-id="1a316-133">/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="1a316-133">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1a316-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="1a316-134">Remove Paths</span></span>



| <span data-ttu-id="1a316-135">JSON</span><span class="sxs-lookup"><span data-stu-id="1a316-135">Order</span></span> | <span data-ttu-id="1a316-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="1a316-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="1a316-137">1</span><span class="sxs-lookup"><span data-stu-id="1a316-137">1</span></span>     | <span data-ttu-id="1a316-138">/App1/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="1a316-138">/app1/ifd/exif/{ushort=37379}</span></span> |
| <span data-ttu-id="1a316-139">2</span><span class="sxs-lookup"><span data-stu-id="1a316-139">2</span></span>     | <span data-ttu-id="1a316-140">/xmp/exif:brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="1a316-140">/xmp/exif:brightnessvalue</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="1a316-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="1a316-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1a316-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="1a316-142">Read Paths</span></span>



| <span data-ttu-id="1a316-143">JSON</span><span class="sxs-lookup"><span data-stu-id="1a316-143">Order</span></span> | <span data-ttu-id="1a316-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="1a316-144">Path</span></span>                          | <span data-ttu-id="1a316-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1a316-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1a316-146">1</span><span class="sxs-lookup"><span data-stu-id="1a316-146">1</span></span>     | <span data-ttu-id="1a316-147">/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="1a316-147">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="1a316-148">2</span><span class="sxs-lookup"><span data-stu-id="1a316-148">2</span></span>     | <span data-ttu-id="1a316-149">/ifd/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="1a316-149">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="1a316-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="1a316-150">Write Paths</span></span>



| <span data-ttu-id="1a316-151">JSON</span><span class="sxs-lookup"><span data-stu-id="1a316-151">Order</span></span> | <span data-ttu-id="1a316-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="1a316-152">Path</span></span>                          | <span data-ttu-id="1a316-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1a316-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1a316-154">1</span><span class="sxs-lookup"><span data-stu-id="1a316-154">1</span></span>     | <span data-ttu-id="1a316-155">/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="1a316-155">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="1a316-156">2</span><span class="sxs-lookup"><span data-stu-id="1a316-156">2</span></span>     | <span data-ttu-id="1a316-157">/ifd/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="1a316-157">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1a316-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="1a316-158">Remove Paths</span></span>



| <span data-ttu-id="1a316-159">JSON</span><span class="sxs-lookup"><span data-stu-id="1a316-159">Order</span></span> | <span data-ttu-id="1a316-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="1a316-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="1a316-161">1</span><span class="sxs-lookup"><span data-stu-id="1a316-161">1</span></span>     | <span data-ttu-id="1a316-162">/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="1a316-162">/ifd/exif/{ushort=37379}</span></span>      |
| <span data-ttu-id="1a316-163">2</span><span class="sxs-lookup"><span data-stu-id="1a316-163">2</span></span>     | <span data-ttu-id="1a316-164">/ifd/xmp/exif:brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="1a316-164">/ifd/xmp/exif:brightnessvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1a316-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a316-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a316-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a316-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a316-167">System. Photo. Brightness</span><span class="sxs-lookup"><span data-stu-id="1a316-167">System.Photo.Brightness</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
