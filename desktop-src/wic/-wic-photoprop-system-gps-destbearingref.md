---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestBearingRef.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: Criteri per i metadati delle foto di System. GPS. DestBearingRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f00d3083459fe365fc54e81dc485ddd26887a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232318"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a><span data-ttu-id="e82b0-103">Criteri per i metadati delle foto di System. GPS. DestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e82b0-103">System.GPS.DestBearingRef Photo Metadata Policy</span></span>

<span data-ttu-id="e82b0-104">Criteri per i metadati delle foto per la proprietà [System. GPS. DestBearingRef](../properties/props-system-gps-destbearingref.md) .</span><span class="sxs-lookup"><span data-stu-id="e82b0-104">The photo metadata policy for the [System.GPS.DestBearingRef](../properties/props-system-gps-destbearingref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e82b0-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e82b0-105">PKEY</span></span>

<span data-ttu-id="e82b0-106">PKEY \_ GPS \_ DestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e82b0-106">PKEY\_GPS\_DestBearingRef</span></span>

### <a name="containers"></a><span data-ttu-id="e82b0-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="e82b0-107">Containers</span></span>

<span data-ttu-id="e82b0-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e82b0-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e82b0-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="e82b0-109">Read-Only</span></span>

<span data-ttu-id="e82b0-110">No</span><span class="sxs-lookup"><span data-stu-id="e82b0-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e82b0-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="e82b0-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e82b0-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="e82b0-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="e82b0-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="e82b0-113">Input Type</span></span>

<span data-ttu-id="e82b0-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="e82b0-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e82b0-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="e82b0-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e82b0-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="e82b0-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="e82b0-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="e82b0-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e82b0-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="e82b0-118">Read Paths</span></span>



| <span data-ttu-id="e82b0-119">JSON</span><span class="sxs-lookup"><span data-stu-id="e82b0-119">Order</span></span> | <span data-ttu-id="e82b0-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="e82b0-120">Path</span></span>                        | <span data-ttu-id="e82b0-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e82b0-121">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="e82b0-122">1</span><span class="sxs-lookup"><span data-stu-id="e82b0-122">1</span></span>     | <span data-ttu-id="e82b0-123">/App1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="e82b0-123">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="e82b0-124">ascii</span><span class="sxs-lookup"><span data-stu-id="e82b0-124">ascii</span></span>       |
| <span data-ttu-id="e82b0-125">2</span><span class="sxs-lookup"><span data-stu-id="e82b0-125">2</span></span>     | <span data-ttu-id="e82b0-126">/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e82b0-126">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="e82b0-127">unicode</span><span class="sxs-lookup"><span data-stu-id="e82b0-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e82b0-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="e82b0-128">Write Paths</span></span>



| <span data-ttu-id="e82b0-129">JSON</span><span class="sxs-lookup"><span data-stu-id="e82b0-129">Order</span></span> | <span data-ttu-id="e82b0-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="e82b0-130">Path</span></span>                        | <span data-ttu-id="e82b0-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e82b0-131">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="e82b0-132">1</span><span class="sxs-lookup"><span data-stu-id="e82b0-132">1</span></span>     | <span data-ttu-id="e82b0-133">/App1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="e82b0-133">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="e82b0-134">ascii</span><span class="sxs-lookup"><span data-stu-id="e82b0-134">ascii</span></span>       |
| <span data-ttu-id="e82b0-135">2</span><span class="sxs-lookup"><span data-stu-id="e82b0-135">2</span></span>     | <span data-ttu-id="e82b0-136">/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e82b0-136">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="e82b0-137">unicode</span><span class="sxs-lookup"><span data-stu-id="e82b0-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e82b0-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="e82b0-138">Remove Paths</span></span>



| <span data-ttu-id="e82b0-139">JSON</span><span class="sxs-lookup"><span data-stu-id="e82b0-139">Order</span></span> | <span data-ttu-id="e82b0-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="e82b0-140">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="e82b0-141">1</span><span class="sxs-lookup"><span data-stu-id="e82b0-141">1</span></span>     | <span data-ttu-id="e82b0-142">/App1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="e82b0-142">/app1/ifd/gps/{ushort=23}</span></span>   |
| <span data-ttu-id="e82b0-143">2</span><span class="sxs-lookup"><span data-stu-id="e82b0-143">2</span></span>     | <span data-ttu-id="e82b0-144">/xmp/exif:gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="e82b0-144">/xmp/exif:gpsdestbearingref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="e82b0-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="e82b0-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e82b0-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="e82b0-146">Read Paths</span></span>



| <span data-ttu-id="e82b0-147">JSON</span><span class="sxs-lookup"><span data-stu-id="e82b0-147">Order</span></span> | <span data-ttu-id="e82b0-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="e82b0-148">Path</span></span>                            | <span data-ttu-id="e82b0-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e82b0-149">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="e82b0-150">1</span><span class="sxs-lookup"><span data-stu-id="e82b0-150">1</span></span>     | <span data-ttu-id="e82b0-151">/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="e82b0-151">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="e82b0-152">ascii</span><span class="sxs-lookup"><span data-stu-id="e82b0-152">ascii</span></span>       |
| <span data-ttu-id="e82b0-153">2</span><span class="sxs-lookup"><span data-stu-id="e82b0-153">2</span></span>     | <span data-ttu-id="e82b0-154">/ifd/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e82b0-154">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="e82b0-155">unicode</span><span class="sxs-lookup"><span data-stu-id="e82b0-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e82b0-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="e82b0-156">Write Paths</span></span>



| <span data-ttu-id="e82b0-157">JSON</span><span class="sxs-lookup"><span data-stu-id="e82b0-157">Order</span></span> | <span data-ttu-id="e82b0-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="e82b0-158">Path</span></span>                            | <span data-ttu-id="e82b0-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e82b0-159">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="e82b0-160">1</span><span class="sxs-lookup"><span data-stu-id="e82b0-160">1</span></span>     | <span data-ttu-id="e82b0-161">/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="e82b0-161">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="e82b0-162">ascii</span><span class="sxs-lookup"><span data-stu-id="e82b0-162">ascii</span></span>       |
| <span data-ttu-id="e82b0-163">2</span><span class="sxs-lookup"><span data-stu-id="e82b0-163">2</span></span>     | <span data-ttu-id="e82b0-164">/ifd/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e82b0-164">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="e82b0-165">unicode</span><span class="sxs-lookup"><span data-stu-id="e82b0-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e82b0-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="e82b0-166">Remove Paths</span></span>



| <span data-ttu-id="e82b0-167">order</span><span class="sxs-lookup"><span data-stu-id="e82b0-167">order</span></span> | <span data-ttu-id="e82b0-168">path</span><span class="sxs-lookup"><span data-stu-id="e82b0-168">path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="e82b0-169">1</span><span class="sxs-lookup"><span data-stu-id="e82b0-169">1</span></span>     | <span data-ttu-id="e82b0-170">/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="e82b0-170">/ifd/gps/{ushort=23}</span></span>            |
| <span data-ttu-id="e82b0-171">2</span><span class="sxs-lookup"><span data-stu-id="e82b0-171">2</span></span>     | <span data-ttu-id="e82b0-172">/ifd/xmp/exif:gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="e82b0-172">/ifd/xmp/exif:gpsdestbearingref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e82b0-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="e82b0-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e82b0-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e82b0-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e82b0-175">System. GPS. DestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e82b0-175">System.GPS.DestBearingRef</span></span>](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
