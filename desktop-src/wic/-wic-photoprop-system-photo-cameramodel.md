---
description: Criteri per i metadati delle foto per la proprietà System. Photo. CameraModel.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Criteri per i metadati delle foto di System. Photo. CameraModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884649"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a><span data-ttu-id="70850-103">Criteri per i metadati delle foto di System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="70850-103">System.Photo.CameraModel Photo Metadata Policy</span></span>

<span data-ttu-id="70850-104">Criteri per i metadati delle foto per la proprietà [System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md) .</span><span class="sxs-lookup"><span data-stu-id="70850-104">The photo metadata policy for the [System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="70850-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="70850-105">PKEY</span></span>

<span data-ttu-id="70850-106">PKEY \_ Photo \_ CameraModel</span><span class="sxs-lookup"><span data-stu-id="70850-106">PKEY\_Photo\_CameraModel</span></span>

### <a name="containers"></a><span data-ttu-id="70850-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="70850-107">Containers</span></span>

<span data-ttu-id="70850-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="70850-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="70850-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="70850-109">Read-Only</span></span>

<span data-ttu-id="70850-110">No</span><span class="sxs-lookup"><span data-stu-id="70850-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="70850-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="70850-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="70850-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="70850-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="70850-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="70850-113">Input Type</span></span>

<span data-ttu-id="70850-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="70850-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="70850-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="70850-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="70850-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="70850-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="70850-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="70850-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="70850-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="70850-118">Read Paths</span></span>



| <span data-ttu-id="70850-119">JSON</span><span class="sxs-lookup"><span data-stu-id="70850-119">Order</span></span> | <span data-ttu-id="70850-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="70850-120">Path</span></span>                   | <span data-ttu-id="70850-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="70850-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="70850-122">1</span><span class="sxs-lookup"><span data-stu-id="70850-122">1</span></span>     | <span data-ttu-id="70850-123">/App1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="70850-123">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="70850-124">ascii</span><span class="sxs-lookup"><span data-stu-id="70850-124">ascii</span></span>       |
| <span data-ttu-id="70850-125">2</span><span class="sxs-lookup"><span data-stu-id="70850-125">2</span></span>     | <span data-ttu-id="70850-126">/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-126">/xmp/tiff:Model</span></span>        | <span data-ttu-id="70850-127">unicode</span><span class="sxs-lookup"><span data-stu-id="70850-127">unicode</span></span>     |
| <span data-ttu-id="70850-128">3</span><span class="sxs-lookup"><span data-stu-id="70850-128">3</span></span>     | <span data-ttu-id="70850-129">/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-129">/xmp/tiff:model</span></span>        | <span data-ttu-id="70850-130">unicode</span><span class="sxs-lookup"><span data-stu-id="70850-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="70850-131">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="70850-131">Write Paths</span></span>



| <span data-ttu-id="70850-132">JSON</span><span class="sxs-lookup"><span data-stu-id="70850-132">Order</span></span> | <span data-ttu-id="70850-133">Percorso</span><span class="sxs-lookup"><span data-stu-id="70850-133">Path</span></span>                   | <span data-ttu-id="70850-134">Formato disco</span><span class="sxs-lookup"><span data-stu-id="70850-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="70850-135">1</span><span class="sxs-lookup"><span data-stu-id="70850-135">1</span></span>     | <span data-ttu-id="70850-136">/App1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="70850-136">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="70850-137">ascii</span><span class="sxs-lookup"><span data-stu-id="70850-137">ascii</span></span>       |
| <span data-ttu-id="70850-138">2</span><span class="sxs-lookup"><span data-stu-id="70850-138">2</span></span>     | <span data-ttu-id="70850-139">/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-139">/xmp/tiff:Model</span></span>        | <span data-ttu-id="70850-140">unicode</span><span class="sxs-lookup"><span data-stu-id="70850-140">unicode</span></span>     |
| <span data-ttu-id="70850-141">3</span><span class="sxs-lookup"><span data-stu-id="70850-141">3</span></span>     | <span data-ttu-id="70850-142">/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-142">/xmp/tiff:model</span></span>        | <span data-ttu-id="70850-143">unicode</span><span class="sxs-lookup"><span data-stu-id="70850-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="70850-144">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="70850-144">Remove Paths</span></span>



| <span data-ttu-id="70850-145">JSON</span><span class="sxs-lookup"><span data-stu-id="70850-145">Order</span></span> | <span data-ttu-id="70850-146">Percorso</span><span class="sxs-lookup"><span data-stu-id="70850-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="70850-147">1</span><span class="sxs-lookup"><span data-stu-id="70850-147">1</span></span>     | <span data-ttu-id="70850-148">/App1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="70850-148">/app1/ifd/{ushort=272}</span></span> |
| <span data-ttu-id="70850-149">2</span><span class="sxs-lookup"><span data-stu-id="70850-149">2</span></span>     | <span data-ttu-id="70850-150">/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-150">/xmp/tiff:Model</span></span>        |
| <span data-ttu-id="70850-151">3</span><span class="sxs-lookup"><span data-stu-id="70850-151">3</span></span>     | <span data-ttu-id="70850-152">/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-152">/xmp/tiff:model</span></span>        |



 

### <a name="tiff-policy"></a><span data-ttu-id="70850-153">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="70850-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="70850-154">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="70850-154">Read Paths</span></span>



| <span data-ttu-id="70850-155">JSON</span><span class="sxs-lookup"><span data-stu-id="70850-155">Order</span></span> | <span data-ttu-id="70850-156">Percorso</span><span class="sxs-lookup"><span data-stu-id="70850-156">Path</span></span>                | <span data-ttu-id="70850-157">Formato disco</span><span class="sxs-lookup"><span data-stu-id="70850-157">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="70850-158">1</span><span class="sxs-lookup"><span data-stu-id="70850-158">1</span></span>     | <span data-ttu-id="70850-159">/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="70850-159">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="70850-160">ascii</span><span class="sxs-lookup"><span data-stu-id="70850-160">ascii</span></span>       |
| <span data-ttu-id="70850-161">2</span><span class="sxs-lookup"><span data-stu-id="70850-161">2</span></span>     | <span data-ttu-id="70850-162">/IFD/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-162">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="70850-163">unicode</span><span class="sxs-lookup"><span data-stu-id="70850-163">unicode</span></span>     |
| <span data-ttu-id="70850-164">3</span><span class="sxs-lookup"><span data-stu-id="70850-164">3</span></span>     | <span data-ttu-id="70850-165">/IFD/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-165">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="70850-166">unicode</span><span class="sxs-lookup"><span data-stu-id="70850-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="70850-167">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="70850-167">Write Paths</span></span>



| <span data-ttu-id="70850-168">JSON</span><span class="sxs-lookup"><span data-stu-id="70850-168">Order</span></span> | <span data-ttu-id="70850-169">Percorso</span><span class="sxs-lookup"><span data-stu-id="70850-169">Path</span></span>                | <span data-ttu-id="70850-170">Formato disco</span><span class="sxs-lookup"><span data-stu-id="70850-170">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="70850-171">1</span><span class="sxs-lookup"><span data-stu-id="70850-171">1</span></span>     | <span data-ttu-id="70850-172">/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="70850-172">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="70850-173">ascii</span><span class="sxs-lookup"><span data-stu-id="70850-173">ascii</span></span>       |
| <span data-ttu-id="70850-174">2</span><span class="sxs-lookup"><span data-stu-id="70850-174">2</span></span>     | <span data-ttu-id="70850-175">/IFD/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-175">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="70850-176">unicode</span><span class="sxs-lookup"><span data-stu-id="70850-176">unicode</span></span>     |
| <span data-ttu-id="70850-177">3</span><span class="sxs-lookup"><span data-stu-id="70850-177">3</span></span>     | <span data-ttu-id="70850-178">/IFD/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-178">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="70850-179">unicode</span><span class="sxs-lookup"><span data-stu-id="70850-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="70850-180">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="70850-180">Remove Paths</span></span>



| <span data-ttu-id="70850-181">JSON</span><span class="sxs-lookup"><span data-stu-id="70850-181">Order</span></span> | <span data-ttu-id="70850-182">Percorso</span><span class="sxs-lookup"><span data-stu-id="70850-182">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="70850-183">1</span><span class="sxs-lookup"><span data-stu-id="70850-183">1</span></span>     | <span data-ttu-id="70850-184">/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="70850-184">/ifd/{ushort=272}</span></span>   |
| <span data-ttu-id="70850-185">2</span><span class="sxs-lookup"><span data-stu-id="70850-185">2</span></span>     | <span data-ttu-id="70850-186">/IFD/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-186">/ifd/xmp/tiff:Model</span></span> |
| <span data-ttu-id="70850-187">3</span><span class="sxs-lookup"><span data-stu-id="70850-187">3</span></span>     | <span data-ttu-id="70850-188">/IFD/XMP/TIFF: modello</span><span class="sxs-lookup"><span data-stu-id="70850-188">/ifd/xmp/tiff:model</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="70850-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="70850-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="70850-190">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70850-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70850-191">System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="70850-191">System.Photo.CameraModel</span></span>](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
