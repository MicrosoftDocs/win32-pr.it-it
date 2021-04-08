---
description: Criteri di metadati della foto per la proprietà System. Photo. Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Criteri dei metadati delle foto di System. Photo. Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058049"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a><span data-ttu-id="b95d3-103">Criteri dei metadati delle foto di System. Photo. Orientation</span><span class="sxs-lookup"><span data-stu-id="b95d3-103">System.Photo.Orientation Photo Metadata Policy</span></span>

<span data-ttu-id="b95d3-104">Criteri di metadati della foto per la proprietà [System. Photo. Orientation](../properties/props-system-photo-meteringmode.md) .</span><span class="sxs-lookup"><span data-stu-id="b95d3-104">The photo metadata policy for the [System.Photo.Orientation](../properties/props-system-photo-meteringmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b95d3-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b95d3-105">PKEY</span></span>

<span data-ttu-id="b95d3-106">\_Orientamento foto \_ pkey</span><span class="sxs-lookup"><span data-stu-id="b95d3-106">PKEY\_Photo\_Orientation</span></span>

### <a name="containers"></a><span data-ttu-id="b95d3-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="b95d3-107">Containers</span></span>

<span data-ttu-id="b95d3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b95d3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b95d3-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="b95d3-109">Read-Only</span></span>

<span data-ttu-id="b95d3-110">No</span><span class="sxs-lookup"><span data-stu-id="b95d3-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b95d3-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="b95d3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b95d3-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="b95d3-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="b95d3-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="b95d3-113">Input Type</span></span>

<span data-ttu-id="b95d3-114">UShort</span><span class="sxs-lookup"><span data-stu-id="b95d3-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b95d3-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="b95d3-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b95d3-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="b95d3-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b95d3-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="b95d3-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b95d3-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="b95d3-118">Read Paths</span></span>



| <span data-ttu-id="b95d3-119">JSON</span><span class="sxs-lookup"><span data-stu-id="b95d3-119">Order</span></span> | <span data-ttu-id="b95d3-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="b95d3-120">Path</span></span>                   | <span data-ttu-id="b95d3-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b95d3-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="b95d3-122">1</span><span class="sxs-lookup"><span data-stu-id="b95d3-122">1</span></span>     | <span data-ttu-id="b95d3-123">/App1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="b95d3-123">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="b95d3-124">ushort</span><span class="sxs-lookup"><span data-stu-id="b95d3-124">ushort</span></span>      |
| <span data-ttu-id="b95d3-125">2</span><span class="sxs-lookup"><span data-stu-id="b95d3-125">2</span></span>     | <span data-ttu-id="b95d3-126">/XMP/TIFF: orientamento</span><span class="sxs-lookup"><span data-stu-id="b95d3-126">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="b95d3-127">unicode</span><span class="sxs-lookup"><span data-stu-id="b95d3-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b95d3-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="b95d3-128">Write Paths</span></span>



| <span data-ttu-id="b95d3-129">JSON</span><span class="sxs-lookup"><span data-stu-id="b95d3-129">Order</span></span> | <span data-ttu-id="b95d3-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="b95d3-130">Path</span></span>                   | <span data-ttu-id="b95d3-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b95d3-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="b95d3-132">1</span><span class="sxs-lookup"><span data-stu-id="b95d3-132">1</span></span>     | <span data-ttu-id="b95d3-133">/App1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="b95d3-133">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="b95d3-134">ushort</span><span class="sxs-lookup"><span data-stu-id="b95d3-134">ushort</span></span>      |
| <span data-ttu-id="b95d3-135">2</span><span class="sxs-lookup"><span data-stu-id="b95d3-135">2</span></span>     | <span data-ttu-id="b95d3-136">/XMP/TIFF: orientamento</span><span class="sxs-lookup"><span data-stu-id="b95d3-136">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="b95d3-137">unicode</span><span class="sxs-lookup"><span data-stu-id="b95d3-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b95d3-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="b95d3-138">Remove Paths</span></span>



| <span data-ttu-id="b95d3-139">JSON</span><span class="sxs-lookup"><span data-stu-id="b95d3-139">Order</span></span> | <span data-ttu-id="b95d3-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="b95d3-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="b95d3-141">1</span><span class="sxs-lookup"><span data-stu-id="b95d3-141">1</span></span>     | <span data-ttu-id="b95d3-142">/App1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="b95d3-142">/app1/ifd/{ushort=274}</span></span> |
| <span data-ttu-id="b95d3-143">2</span><span class="sxs-lookup"><span data-stu-id="b95d3-143">2</span></span>     | <span data-ttu-id="b95d3-144">/XMP/TIFF: orientamento</span><span class="sxs-lookup"><span data-stu-id="b95d3-144">/xmp/tiff:orientation</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="b95d3-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="b95d3-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b95d3-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="b95d3-146">Read Paths</span></span>



| <span data-ttu-id="b95d3-147">JSON</span><span class="sxs-lookup"><span data-stu-id="b95d3-147">Order</span></span> | <span data-ttu-id="b95d3-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="b95d3-148">Path</span></span>                      | <span data-ttu-id="b95d3-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b95d3-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b95d3-150">1</span><span class="sxs-lookup"><span data-stu-id="b95d3-150">1</span></span>     | <span data-ttu-id="b95d3-151">/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="b95d3-151">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="b95d3-152">ushort</span><span class="sxs-lookup"><span data-stu-id="b95d3-152">ushort</span></span>      |
| <span data-ttu-id="b95d3-153">2</span><span class="sxs-lookup"><span data-stu-id="b95d3-153">2</span></span>     | <span data-ttu-id="b95d3-154">/IFD/XMP/TIFF: orientamento</span><span class="sxs-lookup"><span data-stu-id="b95d3-154">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="b95d3-155">unicode</span><span class="sxs-lookup"><span data-stu-id="b95d3-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b95d3-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="b95d3-156">Write Paths</span></span>



| <span data-ttu-id="b95d3-157">JSON</span><span class="sxs-lookup"><span data-stu-id="b95d3-157">Order</span></span> | <span data-ttu-id="b95d3-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="b95d3-158">Path</span></span>                      | <span data-ttu-id="b95d3-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b95d3-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b95d3-160">1</span><span class="sxs-lookup"><span data-stu-id="b95d3-160">1</span></span>     | <span data-ttu-id="b95d3-161">/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="b95d3-161">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="b95d3-162">ushort</span><span class="sxs-lookup"><span data-stu-id="b95d3-162">ushort</span></span>      |
| <span data-ttu-id="b95d3-163">2</span><span class="sxs-lookup"><span data-stu-id="b95d3-163">2</span></span>     | <span data-ttu-id="b95d3-164">/IFD/XMP/TIFF: orientamento</span><span class="sxs-lookup"><span data-stu-id="b95d3-164">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="b95d3-165">unicode</span><span class="sxs-lookup"><span data-stu-id="b95d3-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b95d3-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="b95d3-166">Remove Paths</span></span>



| <span data-ttu-id="b95d3-167">JSON</span><span class="sxs-lookup"><span data-stu-id="b95d3-167">Order</span></span> | <span data-ttu-id="b95d3-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="b95d3-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="b95d3-169">1</span><span class="sxs-lookup"><span data-stu-id="b95d3-169">1</span></span>     | <span data-ttu-id="b95d3-170">/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="b95d3-170">/ifd/{ushort=274}</span></span>         |
| <span data-ttu-id="b95d3-171">2</span><span class="sxs-lookup"><span data-stu-id="b95d3-171">2</span></span>     | <span data-ttu-id="b95d3-172">/IFD/XMP/TIFF: orientamento</span><span class="sxs-lookup"><span data-stu-id="b95d3-172">/ifd/xmp/tiff:orientation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b95d3-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="b95d3-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b95d3-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b95d3-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b95d3-175">System. Photo. Orientation</span><span class="sxs-lookup"><span data-stu-id="b95d3-175">System.Photo.Orientation</span></span>](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
