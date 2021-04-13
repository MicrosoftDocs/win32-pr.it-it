---
description: Criteri per i metadati delle foto per la proprietà System. Photo. DigitalZoom.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Criteri per i metadati delle foto di System. Photo. DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347426"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a><span data-ttu-id="bfb73-103">Criteri per i metadati delle foto di System. Photo. DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="bfb73-103">System.Photo.DigitalZoom Photo Metadata Policy</span></span>

<span data-ttu-id="bfb73-104">Criteri per i metadati delle foto per la proprietà [System. Photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md) .</span><span class="sxs-lookup"><span data-stu-id="bfb73-104">The photo metadata policy for the [System.Photo.DigitalZoom](../properties/props-system-photo-digitalzoom.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bfb73-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="bfb73-105">PKEY</span></span>

<span data-ttu-id="bfb73-106">PKEY \_ Photo \_ DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="bfb73-106">PKEY\_Photo\_DigitalZoom</span></span>

### <a name="containers"></a><span data-ttu-id="bfb73-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="bfb73-107">Containers</span></span>

<span data-ttu-id="bfb73-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="bfb73-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bfb73-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="bfb73-109">Read-Only</span></span>

<span data-ttu-id="bfb73-110">Sì</span><span class="sxs-lookup"><span data-stu-id="bfb73-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="bfb73-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="bfb73-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="bfb73-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="bfb73-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bfb73-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="bfb73-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="bfb73-114">Questo valore viene generato da System. Photo. DigitalZoomNumerator e System. Photo. DigitalZoomDenominator.</span><span class="sxs-lookup"><span data-stu-id="bfb73-114">This value is generated from System.Photo.DigitalZoomNumerator and System.Photo.DigitalZoomDenominator.</span></span> <span data-ttu-id="bfb73-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="bfb73-115">It cannot be written directly.</span></span> <span data-ttu-id="bfb73-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="bfb73-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="bfb73-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="bfb73-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="bfb73-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="bfb73-118">Read Paths</span></span>



| <span data-ttu-id="bfb73-119">JSON</span><span class="sxs-lookup"><span data-stu-id="bfb73-119">Order</span></span> | <span data-ttu-id="bfb73-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="bfb73-120">Path</span></span>                          | <span data-ttu-id="bfb73-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="bfb73-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bfb73-122">1</span><span class="sxs-lookup"><span data-stu-id="bfb73-122">1</span></span>     | <span data-ttu-id="bfb73-123">/App1/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="bfb73-123">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="bfb73-124">2</span><span class="sxs-lookup"><span data-stu-id="bfb73-124">2</span></span>     | <span data-ttu-id="bfb73-125">/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="bfb73-125">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="bfb73-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="bfb73-126">Write Paths</span></span>



| <span data-ttu-id="bfb73-127">JSON</span><span class="sxs-lookup"><span data-stu-id="bfb73-127">Order</span></span> | <span data-ttu-id="bfb73-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="bfb73-128">Path</span></span>                          | <span data-ttu-id="bfb73-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="bfb73-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bfb73-130">1</span><span class="sxs-lookup"><span data-stu-id="bfb73-130">1</span></span>     | <span data-ttu-id="bfb73-131">/App1/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="bfb73-131">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="bfb73-132">2</span><span class="sxs-lookup"><span data-stu-id="bfb73-132">2</span></span>     | <span data-ttu-id="bfb73-133">/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="bfb73-133">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="bfb73-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="bfb73-134">Remove Paths</span></span>



| <span data-ttu-id="bfb73-135">JSON</span><span class="sxs-lookup"><span data-stu-id="bfb73-135">Order</span></span> | <span data-ttu-id="bfb73-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="bfb73-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="bfb73-137">1</span><span class="sxs-lookup"><span data-stu-id="bfb73-137">1</span></span>     | <span data-ttu-id="bfb73-138">/App1/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="bfb73-138">/app1/ifd/exif/{ushort=41988}</span></span> |
| <span data-ttu-id="bfb73-139">2</span><span class="sxs-lookup"><span data-stu-id="bfb73-139">2</span></span>     | <span data-ttu-id="bfb73-140">/xmp/exif:digitalzoomratio</span><span class="sxs-lookup"><span data-stu-id="bfb73-140">/xmp/exif:digitalzoomratio</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="bfb73-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="bfb73-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="bfb73-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="bfb73-142">Read Paths</span></span>



| <span data-ttu-id="bfb73-143">JSON</span><span class="sxs-lookup"><span data-stu-id="bfb73-143">Order</span></span> | <span data-ttu-id="bfb73-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="bfb73-144">Path</span></span>                           | <span data-ttu-id="bfb73-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="bfb73-145">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="bfb73-146">1</span><span class="sxs-lookup"><span data-stu-id="bfb73-146">1</span></span>     | <span data-ttu-id="bfb73-147">/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="bfb73-147">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="bfb73-148">2</span><span class="sxs-lookup"><span data-stu-id="bfb73-148">2</span></span>     | <span data-ttu-id="bfb73-149">/ifd/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="bfb73-149">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="bfb73-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="bfb73-150">Write Paths</span></span>



| <span data-ttu-id="bfb73-151">JSON</span><span class="sxs-lookup"><span data-stu-id="bfb73-151">Order</span></span> | <span data-ttu-id="bfb73-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="bfb73-152">Path</span></span>                           | <span data-ttu-id="bfb73-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="bfb73-153">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="bfb73-154">1</span><span class="sxs-lookup"><span data-stu-id="bfb73-154">1</span></span>     | <span data-ttu-id="bfb73-155">/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="bfb73-155">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="bfb73-156">2</span><span class="sxs-lookup"><span data-stu-id="bfb73-156">2</span></span>     | <span data-ttu-id="bfb73-157">/ifd/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="bfb73-157">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="bfb73-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="bfb73-158">Remove Paths</span></span>



| <span data-ttu-id="bfb73-159">JSON</span><span class="sxs-lookup"><span data-stu-id="bfb73-159">Order</span></span> | <span data-ttu-id="bfb73-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="bfb73-160">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="bfb73-161">1</span><span class="sxs-lookup"><span data-stu-id="bfb73-161">1</span></span>     | <span data-ttu-id="bfb73-162">/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="bfb73-162">/ifd/exif/{ushort=41988}</span></span>       |
| <span data-ttu-id="bfb73-163">2</span><span class="sxs-lookup"><span data-stu-id="bfb73-163">2</span></span>     | <span data-ttu-id="bfb73-164">/ifd/xmp/exif:digitalzoomratio</span><span class="sxs-lookup"><span data-stu-id="bfb73-164">/ifd/xmp/exif:digitalzoomratio</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bfb73-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfb73-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfb73-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bfb73-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfb73-167">System. Photo. DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="bfb73-167">System.Photo.DigitalZoom</span></span>](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
