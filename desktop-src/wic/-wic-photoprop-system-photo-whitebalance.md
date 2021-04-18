---
description: Criteri per i metadati delle foto per la proprietà System. Photo. WhiteBalance.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: Criteri per i metadati delle foto di System. Photo. WhiteBalance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315958"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a><span data-ttu-id="abc80-103">Criteri per i metadati delle foto di System. Photo. WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="abc80-103">System.Photo.WhiteBalance Photo Metadata Policy</span></span>

<span data-ttu-id="abc80-104">Criteri per i metadati delle foto per la proprietà [System. Photo. whitebalance](../properties/props-system-photo-whitebalance.md) .</span><span class="sxs-lookup"><span data-stu-id="abc80-104">The photo metadata policy for the [System.Photo.WhiteBalance](../properties/props-system-photo-whitebalance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="abc80-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="abc80-105">PKEY</span></span>

<span data-ttu-id="abc80-106">PKEY \_ Photo \_ whitebalance</span><span class="sxs-lookup"><span data-stu-id="abc80-106">PKEY\_Photo\_WhiteBalance</span></span>

### <a name="containers"></a><span data-ttu-id="abc80-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="abc80-107">Containers</span></span>

<span data-ttu-id="abc80-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="abc80-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="abc80-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="abc80-109">Read-Only</span></span>

<span data-ttu-id="abc80-110">No</span><span class="sxs-lookup"><span data-stu-id="abc80-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="abc80-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="abc80-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="abc80-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="abc80-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="abc80-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="abc80-113">Input Type</span></span>

<span data-ttu-id="abc80-114">UShort</span><span class="sxs-lookup"><span data-stu-id="abc80-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="abc80-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="abc80-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="abc80-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="abc80-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="abc80-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="abc80-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="abc80-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="abc80-118">Read Paths</span></span>



| <span data-ttu-id="abc80-119">JSON</span><span class="sxs-lookup"><span data-stu-id="abc80-119">Order</span></span> | <span data-ttu-id="abc80-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="abc80-120">Path</span></span>                          | <span data-ttu-id="abc80-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="abc80-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="abc80-122">1</span><span class="sxs-lookup"><span data-stu-id="abc80-122">1</span></span>     | <span data-ttu-id="abc80-123">/App1/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="abc80-123">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="abc80-124">ushort</span><span class="sxs-lookup"><span data-stu-id="abc80-124">ushort</span></span>      |
| <span data-ttu-id="abc80-125">2</span><span class="sxs-lookup"><span data-stu-id="abc80-125">2</span></span>     | <span data-ttu-id="abc80-126">/XMP/EXIF: WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="abc80-126">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="abc80-127">unicode</span><span class="sxs-lookup"><span data-stu-id="abc80-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="abc80-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="abc80-128">Write Paths</span></span>



| <span data-ttu-id="abc80-129">JSON</span><span class="sxs-lookup"><span data-stu-id="abc80-129">Order</span></span> | <span data-ttu-id="abc80-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="abc80-130">Path</span></span>                          | <span data-ttu-id="abc80-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="abc80-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="abc80-132">1</span><span class="sxs-lookup"><span data-stu-id="abc80-132">1</span></span>     | <span data-ttu-id="abc80-133">/App1/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="abc80-133">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="abc80-134">ushort</span><span class="sxs-lookup"><span data-stu-id="abc80-134">ushort</span></span>      |
| <span data-ttu-id="abc80-135">2</span><span class="sxs-lookup"><span data-stu-id="abc80-135">2</span></span>     | <span data-ttu-id="abc80-136">/XMP/EXIF: WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="abc80-136">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="abc80-137">unicode</span><span class="sxs-lookup"><span data-stu-id="abc80-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="abc80-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="abc80-138">Remove Paths</span></span>



| <span data-ttu-id="abc80-139">JSON</span><span class="sxs-lookup"><span data-stu-id="abc80-139">Order</span></span> | <span data-ttu-id="abc80-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="abc80-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="abc80-141">1</span><span class="sxs-lookup"><span data-stu-id="abc80-141">1</span></span>     | <span data-ttu-id="abc80-142">/App1/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="abc80-142">/app1/ifd/exif/{ushort=41987}</span></span> |
| <span data-ttu-id="abc80-143">2</span><span class="sxs-lookup"><span data-stu-id="abc80-143">2</span></span>     | <span data-ttu-id="abc80-144">/XMP/EXIF: whitebalance</span><span class="sxs-lookup"><span data-stu-id="abc80-144">/xmp/exif:whitebalance</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="abc80-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="abc80-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="abc80-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="abc80-146">Read Paths</span></span>



| <span data-ttu-id="abc80-147">JSON</span><span class="sxs-lookup"><span data-stu-id="abc80-147">Order</span></span> | <span data-ttu-id="abc80-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="abc80-148">Path</span></span>                       | <span data-ttu-id="abc80-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="abc80-149">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="abc80-150">1</span><span class="sxs-lookup"><span data-stu-id="abc80-150">1</span></span>     | <span data-ttu-id="abc80-151">/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="abc80-151">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="abc80-152">ushort</span><span class="sxs-lookup"><span data-stu-id="abc80-152">ushort</span></span>      |
| <span data-ttu-id="abc80-153">2</span><span class="sxs-lookup"><span data-stu-id="abc80-153">2</span></span>     | <span data-ttu-id="abc80-154">/IFD/XMP/EXIF: WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="abc80-154">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="abc80-155">unicode</span><span class="sxs-lookup"><span data-stu-id="abc80-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="abc80-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="abc80-156">Write Paths</span></span>



| <span data-ttu-id="abc80-157">JSON</span><span class="sxs-lookup"><span data-stu-id="abc80-157">Order</span></span> | <span data-ttu-id="abc80-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="abc80-158">Path</span></span>                       | <span data-ttu-id="abc80-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="abc80-159">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="abc80-160">1</span><span class="sxs-lookup"><span data-stu-id="abc80-160">1</span></span>     | <span data-ttu-id="abc80-161">/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="abc80-161">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="abc80-162">ushort</span><span class="sxs-lookup"><span data-stu-id="abc80-162">ushort</span></span>      |
| <span data-ttu-id="abc80-163">2</span><span class="sxs-lookup"><span data-stu-id="abc80-163">2</span></span>     | <span data-ttu-id="abc80-164">/IFD/XMP/EXIF: WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="abc80-164">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="abc80-165">unicode</span><span class="sxs-lookup"><span data-stu-id="abc80-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="abc80-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="abc80-166">Remove Paths</span></span>



| <span data-ttu-id="abc80-167">JSON</span><span class="sxs-lookup"><span data-stu-id="abc80-167">Order</span></span> | <span data-ttu-id="abc80-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="abc80-168">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="abc80-169">1</span><span class="sxs-lookup"><span data-stu-id="abc80-169">1</span></span>     | <span data-ttu-id="abc80-170">/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="abc80-170">/ifd/exif/{ushort=41987}</span></span>   |
| <span data-ttu-id="abc80-171">2</span><span class="sxs-lookup"><span data-stu-id="abc80-171">2</span></span>     | <span data-ttu-id="abc80-172">/IFD/XMP/EXIF: whitebalance</span><span class="sxs-lookup"><span data-stu-id="abc80-172">/ifd/xmp/exif:whitebalance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="abc80-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="abc80-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="abc80-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="abc80-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abc80-175">System. Photo. WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="abc80-175">System.Photo.WhiteBalance</span></span>](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
