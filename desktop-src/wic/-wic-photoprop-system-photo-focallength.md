---
description: Criteri per i metadati delle foto per la proprietà System. Photo. FocalLength.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: Criteri per i metadati delle foto di System. Photo. FocalLength
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314883"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a><span data-ttu-id="9eebc-103">Criteri per i metadati delle foto di System. Photo. FocalLength</span><span class="sxs-lookup"><span data-stu-id="9eebc-103">System.Photo.FocalLength Photo Metadata Policy</span></span>

<span data-ttu-id="9eebc-104">Criteri per i metadati delle foto per la proprietà [System. Photo. focalLength](../properties/props-system-photo-focallength.md) .</span><span class="sxs-lookup"><span data-stu-id="9eebc-104">The photo metadata policy for the [System.Photo.FocalLength](../properties/props-system-photo-focallength.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9eebc-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9eebc-105">PKEY</span></span>

<span data-ttu-id="9eebc-106">PKEY \_ Photo \_ focalLength</span><span class="sxs-lookup"><span data-stu-id="9eebc-106">PKEY\_Photo\_FocalLength</span></span>

### <a name="containers"></a><span data-ttu-id="9eebc-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="9eebc-107">Containers</span></span>

<span data-ttu-id="9eebc-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9eebc-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9eebc-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="9eebc-109">Read-Only</span></span>

<span data-ttu-id="9eebc-110">Sì</span><span class="sxs-lookup"><span data-stu-id="9eebc-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9eebc-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="9eebc-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9eebc-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="9eebc-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9eebc-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="9eebc-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="9eebc-114">Questo valore viene generato da System. Photo. FocalLengthNumerator e System. Photo. FocalLengthDenominator.</span><span class="sxs-lookup"><span data-stu-id="9eebc-114">This value is generated from System.Photo.FocalLengthNumerator and System.Photo.FocalLengthDenominator.</span></span> <span data-ttu-id="9eebc-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="9eebc-115">It cannot be written directly.</span></span> <span data-ttu-id="9eebc-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="9eebc-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9eebc-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="9eebc-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9eebc-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="9eebc-118">Read Paths</span></span>



| <span data-ttu-id="9eebc-119">JSON</span><span class="sxs-lookup"><span data-stu-id="9eebc-119">Order</span></span> | <span data-ttu-id="9eebc-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="9eebc-120">Path</span></span>                          | <span data-ttu-id="9eebc-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="9eebc-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9eebc-122">1</span><span class="sxs-lookup"><span data-stu-id="9eebc-122">1</span></span>     | <span data-ttu-id="9eebc-123">/App1/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="9eebc-123">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="9eebc-124">2</span><span class="sxs-lookup"><span data-stu-id="9eebc-124">2</span></span>     | <span data-ttu-id="9eebc-125">/XMP/EXIF: FocalLength</span><span class="sxs-lookup"><span data-stu-id="9eebc-125">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="9eebc-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="9eebc-126">Write Paths</span></span>



| <span data-ttu-id="9eebc-127">JSON</span><span class="sxs-lookup"><span data-stu-id="9eebc-127">Order</span></span> | <span data-ttu-id="9eebc-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="9eebc-128">Path</span></span>                          | <span data-ttu-id="9eebc-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="9eebc-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9eebc-130">1</span><span class="sxs-lookup"><span data-stu-id="9eebc-130">1</span></span>     | <span data-ttu-id="9eebc-131">/App1/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="9eebc-131">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="9eebc-132">2</span><span class="sxs-lookup"><span data-stu-id="9eebc-132">2</span></span>     | <span data-ttu-id="9eebc-133">/XMP/EXIF: FocalLength</span><span class="sxs-lookup"><span data-stu-id="9eebc-133">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9eebc-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="9eebc-134">Remove Paths</span></span>



| <span data-ttu-id="9eebc-135">JSON</span><span class="sxs-lookup"><span data-stu-id="9eebc-135">Order</span></span> | <span data-ttu-id="9eebc-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="9eebc-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="9eebc-137">1</span><span class="sxs-lookup"><span data-stu-id="9eebc-137">1</span></span>     | <span data-ttu-id="9eebc-138">/App1/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="9eebc-138">/app1/ifd/exif/{ushort=37386}</span></span> |
| <span data-ttu-id="9eebc-139">2</span><span class="sxs-lookup"><span data-stu-id="9eebc-139">2</span></span>     | <span data-ttu-id="9eebc-140">/XMP/EXIF: focalLength</span><span class="sxs-lookup"><span data-stu-id="9eebc-140">/xmp/exif:focallength</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="9eebc-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="9eebc-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9eebc-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="9eebc-142">Read Paths</span></span>



| <span data-ttu-id="9eebc-143">JSON</span><span class="sxs-lookup"><span data-stu-id="9eebc-143">Order</span></span> | <span data-ttu-id="9eebc-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="9eebc-144">Path</span></span>                      | <span data-ttu-id="9eebc-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="9eebc-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9eebc-146">1</span><span class="sxs-lookup"><span data-stu-id="9eebc-146">1</span></span>     | <span data-ttu-id="9eebc-147">/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="9eebc-147">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="9eebc-148">2</span><span class="sxs-lookup"><span data-stu-id="9eebc-148">2</span></span>     | <span data-ttu-id="9eebc-149">/IFD/XMP/EXIF: FocalLength</span><span class="sxs-lookup"><span data-stu-id="9eebc-149">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="9eebc-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="9eebc-150">Write Paths</span></span>



| <span data-ttu-id="9eebc-151">JSON</span><span class="sxs-lookup"><span data-stu-id="9eebc-151">Order</span></span> | <span data-ttu-id="9eebc-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="9eebc-152">Path</span></span>                      | <span data-ttu-id="9eebc-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="9eebc-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9eebc-154">1</span><span class="sxs-lookup"><span data-stu-id="9eebc-154">1</span></span>     | <span data-ttu-id="9eebc-155">/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="9eebc-155">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="9eebc-156">2</span><span class="sxs-lookup"><span data-stu-id="9eebc-156">2</span></span>     | <span data-ttu-id="9eebc-157">/IFD/XMP/EXIF: FocalLength</span><span class="sxs-lookup"><span data-stu-id="9eebc-157">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9eebc-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="9eebc-158">Remove Paths</span></span>



| <span data-ttu-id="9eebc-159">JSON</span><span class="sxs-lookup"><span data-stu-id="9eebc-159">Order</span></span> | <span data-ttu-id="9eebc-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="9eebc-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="9eebc-161">1</span><span class="sxs-lookup"><span data-stu-id="9eebc-161">1</span></span>     | <span data-ttu-id="9eebc-162">/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="9eebc-162">/ifd/exif/{ushort=37386}</span></span>  |
| <span data-ttu-id="9eebc-163">2</span><span class="sxs-lookup"><span data-stu-id="9eebc-163">2</span></span>     | <span data-ttu-id="9eebc-164">/IFD/XMP/EXIF: focalLength</span><span class="sxs-lookup"><span data-stu-id="9eebc-164">/ifd/xmp/exif:focallength</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9eebc-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="9eebc-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9eebc-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9eebc-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eebc-167">System. Photo. FocalLength</span><span class="sxs-lookup"><span data-stu-id="9eebc-167">System.Photo.FocalLength</span></span>](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
