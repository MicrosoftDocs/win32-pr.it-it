---
description: Criteri per i metadati delle foto per la proprietà System. Photo. FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Criteri per i metadati delle foto di System. Photo. FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c518ef2a05dde8fd7e812d1d76a79cbe3efb4217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232314"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="39463-103">Criteri per i metadati delle foto di System. Photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="39463-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="39463-104">Criteri per i metadati delle foto per la proprietà [System. Photo. fnumber](../properties/props-system-photo-fnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="39463-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="39463-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="39463-105">PKEY</span></span>

<span data-ttu-id="39463-106">PKEY \_ Photo \_ fnumber</span><span class="sxs-lookup"><span data-stu-id="39463-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="39463-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="39463-107">Containers</span></span>

<span data-ttu-id="39463-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="39463-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="39463-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="39463-109">Read-Only</span></span>

<span data-ttu-id="39463-110">Sì</span><span class="sxs-lookup"><span data-stu-id="39463-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="39463-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="39463-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="39463-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="39463-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="39463-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="39463-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="39463-114">Questo valore viene generato da System. Photo. FNumberNumerator e System. Photo. FNumberDenominator.</span><span class="sxs-lookup"><span data-stu-id="39463-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="39463-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="39463-115">It cannot be written directly.</span></span> <span data-ttu-id="39463-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="39463-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="39463-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="39463-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="39463-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="39463-118">Read Paths</span></span>



| <span data-ttu-id="39463-119">JSON</span><span class="sxs-lookup"><span data-stu-id="39463-119">Order</span></span> | <span data-ttu-id="39463-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="39463-120">Path</span></span>                          | <span data-ttu-id="39463-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="39463-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="39463-122">1</span><span class="sxs-lookup"><span data-stu-id="39463-122">1</span></span>     | <span data-ttu-id="39463-123">/App1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="39463-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="39463-124">2</span><span class="sxs-lookup"><span data-stu-id="39463-124">2</span></span>     | <span data-ttu-id="39463-125">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="39463-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="39463-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="39463-126">Write Paths</span></span>



|       |                               |             |     |
|-------|-------------------------------|-------------|-----|
| <span data-ttu-id="39463-127">JSON</span><span class="sxs-lookup"><span data-stu-id="39463-127">Order</span></span> | <span data-ttu-id="39463-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="39463-128">Path</span></span>                          | <span data-ttu-id="39463-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="39463-129">Disk Format</span></span> |     |
| <span data-ttu-id="39463-130">1</span><span class="sxs-lookup"><span data-stu-id="39463-130">1</span></span>     | <span data-ttu-id="39463-131">/App1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="39463-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |     |
| <span data-ttu-id="39463-132">2</span><span class="sxs-lookup"><span data-stu-id="39463-132">2</span></span>     | <span data-ttu-id="39463-133">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="39463-133">/xmp/exif:FNumber</span></span>             |             |     |



 

### <a name="remove-paths"></a><span data-ttu-id="39463-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="39463-134">Remove Paths</span></span>



| <span data-ttu-id="39463-135">JSON</span><span class="sxs-lookup"><span data-stu-id="39463-135">Order</span></span> | <span data-ttu-id="39463-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="39463-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="39463-137">1</span><span class="sxs-lookup"><span data-stu-id="39463-137">1</span></span>     | <span data-ttu-id="39463-138">/App1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="39463-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="39463-139">2</span><span class="sxs-lookup"><span data-stu-id="39463-139">2</span></span>     | <span data-ttu-id="39463-140">/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="39463-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="39463-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="39463-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="39463-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="39463-142">Read Paths</span></span>



| <span data-ttu-id="39463-143">JSON</span><span class="sxs-lookup"><span data-stu-id="39463-143">Order</span></span> | <span data-ttu-id="39463-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="39463-144">Path</span></span>                     | <span data-ttu-id="39463-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="39463-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="39463-146">1</span><span class="sxs-lookup"><span data-stu-id="39463-146">1</span></span>     | <span data-ttu-id="39463-147">/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="39463-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="39463-148">2</span><span class="sxs-lookup"><span data-stu-id="39463-148">2</span></span>     | <span data-ttu-id="39463-149">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="39463-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="39463-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="39463-150">Write Paths</span></span>



| <span data-ttu-id="39463-151">JSON</span><span class="sxs-lookup"><span data-stu-id="39463-151">Order</span></span> | <span data-ttu-id="39463-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="39463-152">Path</span></span>                     | <span data-ttu-id="39463-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="39463-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="39463-154">1</span><span class="sxs-lookup"><span data-stu-id="39463-154">1</span></span>     | <span data-ttu-id="39463-155">/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="39463-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="39463-156">2</span><span class="sxs-lookup"><span data-stu-id="39463-156">2</span></span>     | <span data-ttu-id="39463-157">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="39463-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="39463-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="39463-158">Remove Paths</span></span>



| <span data-ttu-id="39463-159">JSON</span><span class="sxs-lookup"><span data-stu-id="39463-159">Order</span></span> | <span data-ttu-id="39463-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="39463-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="39463-161">1</span><span class="sxs-lookup"><span data-stu-id="39463-161">1</span></span>     | <span data-ttu-id="39463-162">/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="39463-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="39463-163">2</span><span class="sxs-lookup"><span data-stu-id="39463-163">2</span></span>     | <span data-ttu-id="39463-164">/ifd/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="39463-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="39463-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="39463-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="39463-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="39463-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39463-167">System. Photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="39463-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
