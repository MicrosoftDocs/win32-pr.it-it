---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestDistanceRef.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Criteri per i metadati delle foto di System. GPS. DestDistanceRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317882"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a><span data-ttu-id="d89a8-103">Criteri per i metadati delle foto di System. GPS. DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="d89a8-103">System.GPS.DestDistanceRef Photo Metadata Policy</span></span>

<span data-ttu-id="d89a8-104">Criteri per i metadati delle foto per la proprietà [System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md) .</span><span class="sxs-lookup"><span data-stu-id="d89a8-104">The photo metadata policy for the [System.GPS.DestDistanceRef](../properties/props-system-gps-destdistanceref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d89a8-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d89a8-105">PKEY</span></span>

<span data-ttu-id="d89a8-106">\_DESTDISTANCEREF pkey</span><span class="sxs-lookup"><span data-stu-id="d89a8-106">PKEY\_DestDistanceRef</span></span>

### <a name="containers"></a><span data-ttu-id="d89a8-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="d89a8-107">Containers</span></span>

<span data-ttu-id="d89a8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d89a8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d89a8-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="d89a8-109">Read-Only</span></span>

<span data-ttu-id="d89a8-110">No</span><span class="sxs-lookup"><span data-stu-id="d89a8-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d89a8-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="d89a8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d89a8-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="d89a8-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="d89a8-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="d89a8-113">Input Type</span></span>

<span data-ttu-id="d89a8-114">VT \_ LPWSTR o VT \_ LPSTR sono accettati.</span><span class="sxs-lookup"><span data-stu-id="d89a8-114">VT\_LPWSTR or VT\_LPSTR are accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d89a8-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="d89a8-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d89a8-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="d89a8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="d89a8-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="d89a8-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d89a8-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="d89a8-118">Read Paths</span></span>



| <span data-ttu-id="d89a8-119">JSON</span><span class="sxs-lookup"><span data-stu-id="d89a8-119">Order</span></span> | <span data-ttu-id="d89a8-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="d89a8-120">Path</span></span>                         | <span data-ttu-id="d89a8-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d89a8-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="d89a8-122">1</span><span class="sxs-lookup"><span data-stu-id="d89a8-122">1</span></span>     | <span data-ttu-id="d89a8-123">/App1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="d89a8-123">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="d89a8-124">ascii</span><span class="sxs-lookup"><span data-stu-id="d89a8-124">ascii</span></span>       |
| <span data-ttu-id="d89a8-125">2</span><span class="sxs-lookup"><span data-stu-id="d89a8-125">2</span></span>     | <span data-ttu-id="d89a8-126">/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="d89a8-126">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="d89a8-127">unicode</span><span class="sxs-lookup"><span data-stu-id="d89a8-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d89a8-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="d89a8-128">Write Paths</span></span>



| <span data-ttu-id="d89a8-129">JSON</span><span class="sxs-lookup"><span data-stu-id="d89a8-129">Order</span></span> | <span data-ttu-id="d89a8-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="d89a8-130">Path</span></span>                         | <span data-ttu-id="d89a8-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d89a8-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="d89a8-132">1</span><span class="sxs-lookup"><span data-stu-id="d89a8-132">1</span></span>     | <span data-ttu-id="d89a8-133">/App1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="d89a8-133">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="d89a8-134">ascii</span><span class="sxs-lookup"><span data-stu-id="d89a8-134">ascii</span></span>       |
| <span data-ttu-id="d89a8-135">2</span><span class="sxs-lookup"><span data-stu-id="d89a8-135">2</span></span>     | <span data-ttu-id="d89a8-136">/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="d89a8-136">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="d89a8-137">unicode</span><span class="sxs-lookup"><span data-stu-id="d89a8-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d89a8-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="d89a8-138">Remove Paths</span></span>



| <span data-ttu-id="d89a8-139">JSON</span><span class="sxs-lookup"><span data-stu-id="d89a8-139">Order</span></span> | <span data-ttu-id="d89a8-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="d89a8-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="d89a8-141">1</span><span class="sxs-lookup"><span data-stu-id="d89a8-141">1</span></span>     | <span data-ttu-id="d89a8-142">/App1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="d89a8-142">/app1/ifd/gps/{ushort=25}</span></span>    |
| <span data-ttu-id="d89a8-143">2</span><span class="sxs-lookup"><span data-stu-id="d89a8-143">2</span></span>     | <span data-ttu-id="d89a8-144">/xmp/exif:gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="d89a8-144">/xmp/exif:gpsdestdistanceref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="d89a8-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="d89a8-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d89a8-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="d89a8-146">Read Paths</span></span>



| <span data-ttu-id="d89a8-147">JSON</span><span class="sxs-lookup"><span data-stu-id="d89a8-147">Order</span></span> | <span data-ttu-id="d89a8-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="d89a8-148">Path</span></span>                             | <span data-ttu-id="d89a8-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d89a8-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="d89a8-150">1</span><span class="sxs-lookup"><span data-stu-id="d89a8-150">1</span></span>     | <span data-ttu-id="d89a8-151">/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="d89a8-151">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="d89a8-152">ascii</span><span class="sxs-lookup"><span data-stu-id="d89a8-152">ascii</span></span>       |
| <span data-ttu-id="d89a8-153">2</span><span class="sxs-lookup"><span data-stu-id="d89a8-153">2</span></span>     | <span data-ttu-id="d89a8-154">/ifd/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="d89a8-154">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="d89a8-155">unicode</span><span class="sxs-lookup"><span data-stu-id="d89a8-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d89a8-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="d89a8-156">Write Paths</span></span>



| <span data-ttu-id="d89a8-157">JSON</span><span class="sxs-lookup"><span data-stu-id="d89a8-157">Order</span></span> | <span data-ttu-id="d89a8-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="d89a8-158">Path</span></span>                             | <span data-ttu-id="d89a8-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d89a8-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="d89a8-160">1</span><span class="sxs-lookup"><span data-stu-id="d89a8-160">1</span></span>     | <span data-ttu-id="d89a8-161">/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="d89a8-161">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="d89a8-162">ascii</span><span class="sxs-lookup"><span data-stu-id="d89a8-162">ascii</span></span>       |
| <span data-ttu-id="d89a8-163">2</span><span class="sxs-lookup"><span data-stu-id="d89a8-163">2</span></span>     | <span data-ttu-id="d89a8-164">/ifd/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="d89a8-164">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="d89a8-165">unicode</span><span class="sxs-lookup"><span data-stu-id="d89a8-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d89a8-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="d89a8-166">Remove Paths</span></span>



| <span data-ttu-id="d89a8-167">JSON</span><span class="sxs-lookup"><span data-stu-id="d89a8-167">Order</span></span> | <span data-ttu-id="d89a8-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="d89a8-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="d89a8-169">1</span><span class="sxs-lookup"><span data-stu-id="d89a8-169">1</span></span>     | <span data-ttu-id="d89a8-170">/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="d89a8-170">/ifd/gps/{ushort=25}</span></span>             |
| <span data-ttu-id="d89a8-171">2</span><span class="sxs-lookup"><span data-stu-id="d89a8-171">2</span></span>     | <span data-ttu-id="d89a8-172">/ifd/xmp/exif:gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="d89a8-172">/ifd/xmp/exif:gpsdestdistanceref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d89a8-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="d89a8-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d89a8-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d89a8-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d89a8-175">System. GPS. DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="d89a8-175">System.GPS.DestDistanceRef</span></span>](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
