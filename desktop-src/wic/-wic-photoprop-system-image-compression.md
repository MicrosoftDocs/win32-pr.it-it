---
description: Criteri di metadati della foto per la proprietà System. image. Compression.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: Criteri dei metadati della foto di System. image. Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312954"
---
# <a name="systemimagecompression-photo-metadata-policy"></a><span data-ttu-id="acac3-103">Criteri dei metadati della foto di System. image. Compression</span><span class="sxs-lookup"><span data-stu-id="acac3-103">System.Image.Compression Photo Metadata Policy</span></span>

<span data-ttu-id="acac3-104">Criteri di metadati della foto per la proprietà [System. image. Compression](../properties/props-system-image-compression.md) .</span><span class="sxs-lookup"><span data-stu-id="acac3-104">The photo metadata policy for the [System.Image.Compression](../properties/props-system-image-compression.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="acac3-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="acac3-105">PKEY</span></span>

<span data-ttu-id="acac3-106">\_Compressione immagini \_ pkey</span><span class="sxs-lookup"><span data-stu-id="acac3-106">PKEY\_Image\_Compression</span></span>

### <a name="containers"></a><span data-ttu-id="acac3-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="acac3-107">Containers</span></span>

<span data-ttu-id="acac3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="acac3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="acac3-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="acac3-109">Read-Only</span></span>

<span data-ttu-id="acac3-110">Sì</span><span class="sxs-lookup"><span data-stu-id="acac3-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="acac3-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="acac3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="acac3-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="acac3-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="acac3-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="acac3-113">Input Type</span></span>

<span data-ttu-id="acac3-114">UShort</span><span class="sxs-lookup"><span data-stu-id="acac3-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="acac3-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="acac3-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="acac3-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="acac3-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="acac3-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="acac3-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="acac3-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="acac3-118">Read Paths</span></span>



| <span data-ttu-id="acac3-119">JSON</span><span class="sxs-lookup"><span data-stu-id="acac3-119">Order</span></span> | <span data-ttu-id="acac3-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="acac3-120">Path</span></span>                   | <span data-ttu-id="acac3-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="acac3-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="acac3-122">1</span><span class="sxs-lookup"><span data-stu-id="acac3-122">1</span></span>     | <span data-ttu-id="acac3-123">/App1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="acac3-123">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="acac3-124">ushort</span><span class="sxs-lookup"><span data-stu-id="acac3-124">ushort</span></span>      |
| <span data-ttu-id="acac3-125">2</span><span class="sxs-lookup"><span data-stu-id="acac3-125">2</span></span>     | <span data-ttu-id="acac3-126">/XMP/TIFF: compressione</span><span class="sxs-lookup"><span data-stu-id="acac3-126">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="acac3-127">unicode</span><span class="sxs-lookup"><span data-stu-id="acac3-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="acac3-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="acac3-128">Write Paths</span></span>



| <span data-ttu-id="acac3-129">JSON</span><span class="sxs-lookup"><span data-stu-id="acac3-129">Order</span></span> | <span data-ttu-id="acac3-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="acac3-130">Path</span></span>                   | <span data-ttu-id="acac3-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="acac3-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="acac3-132">1</span><span class="sxs-lookup"><span data-stu-id="acac3-132">1</span></span>     | <span data-ttu-id="acac3-133">/App1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="acac3-133">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="acac3-134">ushort</span><span class="sxs-lookup"><span data-stu-id="acac3-134">ushort</span></span>      |
| <span data-ttu-id="acac3-135">2</span><span class="sxs-lookup"><span data-stu-id="acac3-135">2</span></span>     | <span data-ttu-id="acac3-136">/XMP/TIFF: compressione</span><span class="sxs-lookup"><span data-stu-id="acac3-136">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="acac3-137">unicode</span><span class="sxs-lookup"><span data-stu-id="acac3-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="acac3-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="acac3-138">Remove Paths</span></span>



| <span data-ttu-id="acac3-139">JSON</span><span class="sxs-lookup"><span data-stu-id="acac3-139">Order</span></span> | <span data-ttu-id="acac3-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="acac3-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="acac3-141">1</span><span class="sxs-lookup"><span data-stu-id="acac3-141">1</span></span>     | <span data-ttu-id="acac3-142">/App1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="acac3-142">/app1/ifd/{ushort=259}</span></span> |
| <span data-ttu-id="acac3-143">2</span><span class="sxs-lookup"><span data-stu-id="acac3-143">2</span></span>     | <span data-ttu-id="acac3-144">/XMP/TIFF: compressione</span><span class="sxs-lookup"><span data-stu-id="acac3-144">/xmp/tiff:compression</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="acac3-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="acac3-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="acac3-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="acac3-146">Read Paths</span></span>



| <span data-ttu-id="acac3-147">JSON</span><span class="sxs-lookup"><span data-stu-id="acac3-147">Order</span></span> | <span data-ttu-id="acac3-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="acac3-148">Path</span></span>                      | <span data-ttu-id="acac3-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="acac3-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="acac3-150">1</span><span class="sxs-lookup"><span data-stu-id="acac3-150">1</span></span>     | <span data-ttu-id="acac3-151">/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="acac3-151">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="acac3-152">ushort</span><span class="sxs-lookup"><span data-stu-id="acac3-152">ushort</span></span>      |
| <span data-ttu-id="acac3-153">2</span><span class="sxs-lookup"><span data-stu-id="acac3-153">2</span></span>     | <span data-ttu-id="acac3-154">/IFD/XMP/TIFF: compressione</span><span class="sxs-lookup"><span data-stu-id="acac3-154">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="acac3-155">unicode</span><span class="sxs-lookup"><span data-stu-id="acac3-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="acac3-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="acac3-156">Write Paths</span></span>



| <span data-ttu-id="acac3-157">JSON</span><span class="sxs-lookup"><span data-stu-id="acac3-157">Order</span></span> | <span data-ttu-id="acac3-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="acac3-158">Path</span></span>                      | <span data-ttu-id="acac3-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="acac3-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="acac3-160">1</span><span class="sxs-lookup"><span data-stu-id="acac3-160">1</span></span>     | <span data-ttu-id="acac3-161">/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="acac3-161">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="acac3-162">ushort</span><span class="sxs-lookup"><span data-stu-id="acac3-162">ushort</span></span>      |
| <span data-ttu-id="acac3-163">2</span><span class="sxs-lookup"><span data-stu-id="acac3-163">2</span></span>     | <span data-ttu-id="acac3-164">/IFD/XMP/TIFF: compressione</span><span class="sxs-lookup"><span data-stu-id="acac3-164">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="acac3-165">unicode</span><span class="sxs-lookup"><span data-stu-id="acac3-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="acac3-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="acac3-166">Remove Paths</span></span>



| <span data-ttu-id="acac3-167">JSON</span><span class="sxs-lookup"><span data-stu-id="acac3-167">Order</span></span> | <span data-ttu-id="acac3-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="acac3-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="acac3-169">1</span><span class="sxs-lookup"><span data-stu-id="acac3-169">1</span></span>     | <span data-ttu-id="acac3-170">/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="acac3-170">/ifd/{ushort=259}</span></span>         |
| <span data-ttu-id="acac3-171">2</span><span class="sxs-lookup"><span data-stu-id="acac3-171">2</span></span>     | <span data-ttu-id="acac3-172">/IFD/XMP/TIFF: compressione</span><span class="sxs-lookup"><span data-stu-id="acac3-172">/ifd/xmp/tiff:compression</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="acac3-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="acac3-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="acac3-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acac3-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acac3-175">System. image. Compression</span><span class="sxs-lookup"><span data-stu-id="acac3-175">System.Image.Compression</span></span>](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
