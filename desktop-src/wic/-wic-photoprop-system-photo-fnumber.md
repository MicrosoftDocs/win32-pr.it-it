---
description: Criteri dei metadati della foto per la proprietà System.Photo.FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Criteri metadati foto System.Photo.FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85443b849d9f810709f3e75c3082738e5377092f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443622"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="6b270-103">Criteri metadati foto System.Photo.FNumber</span><span class="sxs-lookup"><span data-stu-id="6b270-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="6b270-104">Criteri dei metadati della foto per [la proprietà System.Photo.FNumber.](../properties/props-system-photo-fnumber.md)</span><span class="sxs-lookup"><span data-stu-id="6b270-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6b270-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="6b270-105">PKEY</span></span>

<span data-ttu-id="6b270-106">PKEY \_ Photo \_ FNumber</span><span class="sxs-lookup"><span data-stu-id="6b270-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="6b270-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="6b270-107">Containers</span></span>

<span data-ttu-id="6b270-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6b270-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6b270-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="6b270-109">Read-Only</span></span>

<span data-ttu-id="6b270-110">Sì</span><span class="sxs-lookup"><span data-stu-id="6b270-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6b270-111">Tipo PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="6b270-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6b270-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="6b270-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6b270-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="6b270-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="6b270-114">Questo valore viene generato da System.Photo.FNumberNumerator e System.Photo.FNumberDenominator.</span><span class="sxs-lookup"><span data-stu-id="6b270-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="6b270-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="6b270-115">It cannot be written directly.</span></span> <span data-ttu-id="6b270-116">I valori di schemi diversi vengono riconciliati.</span><span class="sxs-lookup"><span data-stu-id="6b270-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6b270-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="6b270-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6b270-118">Percorsi di lettura</span><span class="sxs-lookup"><span data-stu-id="6b270-118">Read Paths</span></span>



| <span data-ttu-id="6b270-119">Ordine</span><span class="sxs-lookup"><span data-stu-id="6b270-119">Order</span></span> | <span data-ttu-id="6b270-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="6b270-120">Path</span></span>                          | <span data-ttu-id="6b270-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6b270-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="6b270-122">1</span><span class="sxs-lookup"><span data-stu-id="6b270-122">1</span></span>     | <span data-ttu-id="6b270-123">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="6b270-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="6b270-124">2</span><span class="sxs-lookup"><span data-stu-id="6b270-124">2</span></span>     | <span data-ttu-id="6b270-125">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="6b270-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="6b270-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="6b270-126">Write Paths</span></span>



| <span data-ttu-id="6b270-127">Ordine</span><span class="sxs-lookup"><span data-stu-id="6b270-127">Order</span></span> | <span data-ttu-id="6b270-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="6b270-128">Path</span></span>                          | <span data-ttu-id="6b270-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6b270-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="6b270-130">1</span><span class="sxs-lookup"><span data-stu-id="6b270-130">1</span></span>     | <span data-ttu-id="6b270-131">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="6b270-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="6b270-132">2</span><span class="sxs-lookup"><span data-stu-id="6b270-132">2</span></span>     | <span data-ttu-id="6b270-133">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="6b270-133">/xmp/exif:FNumber</span></span>             |             | 
 

### <a name="remove-paths"></a><span data-ttu-id="6b270-134">Rimuovere i percorsi</span><span class="sxs-lookup"><span data-stu-id="6b270-134">Remove Paths</span></span>



| <span data-ttu-id="6b270-135">Ordine</span><span class="sxs-lookup"><span data-stu-id="6b270-135">Order</span></span> | <span data-ttu-id="6b270-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="6b270-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="6b270-137">1</span><span class="sxs-lookup"><span data-stu-id="6b270-137">1</span></span>     | <span data-ttu-id="6b270-138">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="6b270-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="6b270-139">2</span><span class="sxs-lookup"><span data-stu-id="6b270-139">2</span></span>     | <span data-ttu-id="6b270-140">/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="6b270-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="6b270-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="6b270-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6b270-142">Percorsi di lettura</span><span class="sxs-lookup"><span data-stu-id="6b270-142">Read Paths</span></span>



| <span data-ttu-id="6b270-143">Ordine</span><span class="sxs-lookup"><span data-stu-id="6b270-143">Order</span></span> | <span data-ttu-id="6b270-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="6b270-144">Path</span></span>                     | <span data-ttu-id="6b270-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6b270-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6b270-146">1</span><span class="sxs-lookup"><span data-stu-id="6b270-146">1</span></span>     | <span data-ttu-id="6b270-147">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="6b270-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="6b270-148">2</span><span class="sxs-lookup"><span data-stu-id="6b270-148">2</span></span>     | <span data-ttu-id="6b270-149">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="6b270-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="6b270-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="6b270-150">Write Paths</span></span>



| <span data-ttu-id="6b270-151">Ordine</span><span class="sxs-lookup"><span data-stu-id="6b270-151">Order</span></span> | <span data-ttu-id="6b270-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="6b270-152">Path</span></span>                     | <span data-ttu-id="6b270-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6b270-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6b270-154">1</span><span class="sxs-lookup"><span data-stu-id="6b270-154">1</span></span>     | <span data-ttu-id="6b270-155">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="6b270-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="6b270-156">2</span><span class="sxs-lookup"><span data-stu-id="6b270-156">2</span></span>     | <span data-ttu-id="6b270-157">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="6b270-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6b270-158">Rimuovere i percorsi</span><span class="sxs-lookup"><span data-stu-id="6b270-158">Remove Paths</span></span>



| <span data-ttu-id="6b270-159">Ordine</span><span class="sxs-lookup"><span data-stu-id="6b270-159">Order</span></span> | <span data-ttu-id="6b270-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="6b270-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="6b270-161">1</span><span class="sxs-lookup"><span data-stu-id="6b270-161">1</span></span>     | <span data-ttu-id="6b270-162">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="6b270-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="6b270-163">2</span><span class="sxs-lookup"><span data-stu-id="6b270-163">2</span></span>     | <span data-ttu-id="6b270-164">/ifd/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="6b270-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="6b270-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b270-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b270-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b270-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b270-167">System.Photo.FNumber</span><span class="sxs-lookup"><span data-stu-id="6b270-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
