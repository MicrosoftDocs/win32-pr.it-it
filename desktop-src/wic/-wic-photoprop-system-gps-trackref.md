---
description: Criteri per i metadati delle foto per la proprietà System. GPS. TrackRef.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: Criteri per i metadati delle foto di System. GPS. TrackRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95fc63de6eaffd697798c08ff74a46c3d15c7818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234073"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a><span data-ttu-id="662d2-103">Criteri per i metadati delle foto di System. GPS. TrackRef</span><span class="sxs-lookup"><span data-stu-id="662d2-103">System.GPS.TrackRef Photo Metadata Policy</span></span>

<span data-ttu-id="662d2-104">Criteri per i metadati delle foto per la proprietà [System. GPS. TrackRef](../properties/props-system-gps-trackref.md) .</span><span class="sxs-lookup"><span data-stu-id="662d2-104">The photo metadata policy for the [System.GPS.TrackRef](../properties/props-system-gps-trackref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="662d2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="662d2-105">PKEY</span></span>

<span data-ttu-id="662d2-106">PKEY \_ GPS \_ TrackRef</span><span class="sxs-lookup"><span data-stu-id="662d2-106">PKEY\_GPS\_TrackRef</span></span>

### <a name="containers"></a><span data-ttu-id="662d2-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="662d2-107">Containers</span></span>

<span data-ttu-id="662d2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="662d2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="662d2-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="662d2-109">Read-Only</span></span>

<span data-ttu-id="662d2-110">No</span><span class="sxs-lookup"><span data-stu-id="662d2-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="662d2-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="662d2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="662d2-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="662d2-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="662d2-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="662d2-113">Input Type</span></span>

<span data-ttu-id="662d2-114">string</span><span class="sxs-lookup"><span data-stu-id="662d2-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="662d2-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="662d2-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="662d2-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="662d2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="662d2-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="662d2-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="662d2-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="662d2-118">Read Paths</span></span>



| <span data-ttu-id="662d2-119">JSON</span><span class="sxs-lookup"><span data-stu-id="662d2-119">Order</span></span> | <span data-ttu-id="662d2-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="662d2-120">Path</span></span>                      | <span data-ttu-id="662d2-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="662d2-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="662d2-122">1</span><span class="sxs-lookup"><span data-stu-id="662d2-122">1</span></span>     | <span data-ttu-id="662d2-123">/App1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="662d2-123">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="662d2-124">ascii</span><span class="sxs-lookup"><span data-stu-id="662d2-124">ascii</span></span>       |
| <span data-ttu-id="662d2-125">2</span><span class="sxs-lookup"><span data-stu-id="662d2-125">2</span></span>     | <span data-ttu-id="662d2-126">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="662d2-126">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="662d2-127">unicode</span><span class="sxs-lookup"><span data-stu-id="662d2-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="662d2-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="662d2-128">Write Paths</span></span>



| <span data-ttu-id="662d2-129">JSON</span><span class="sxs-lookup"><span data-stu-id="662d2-129">Order</span></span> | <span data-ttu-id="662d2-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="662d2-130">Path</span></span>                      | <span data-ttu-id="662d2-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="662d2-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="662d2-132">1</span><span class="sxs-lookup"><span data-stu-id="662d2-132">1</span></span>     | <span data-ttu-id="662d2-133">/App1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="662d2-133">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="662d2-134">ascii</span><span class="sxs-lookup"><span data-stu-id="662d2-134">ascii</span></span>       |
| <span data-ttu-id="662d2-135">2</span><span class="sxs-lookup"><span data-stu-id="662d2-135">2</span></span>     | <span data-ttu-id="662d2-136">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="662d2-136">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="662d2-137">unicode</span><span class="sxs-lookup"><span data-stu-id="662d2-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="662d2-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="662d2-138">Remove Paths</span></span>



| <span data-ttu-id="662d2-139">JSON</span><span class="sxs-lookup"><span data-stu-id="662d2-139">Order</span></span> | <span data-ttu-id="662d2-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="662d2-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="662d2-141">1</span><span class="sxs-lookup"><span data-stu-id="662d2-141">1</span></span>     | <span data-ttu-id="662d2-142">/App1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="662d2-142">/app1/ifd/gps/{ushort=14}</span></span> |
| <span data-ttu-id="662d2-143">2</span><span class="sxs-lookup"><span data-stu-id="662d2-143">2</span></span>     | <span data-ttu-id="662d2-144">/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="662d2-144">/xmp/exif:gpstrackref</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="662d2-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="662d2-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="662d2-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="662d2-146">Read Paths</span></span>



| <span data-ttu-id="662d2-147">JSON</span><span class="sxs-lookup"><span data-stu-id="662d2-147">Order</span></span> | <span data-ttu-id="662d2-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="662d2-148">Path</span></span>                      | <span data-ttu-id="662d2-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="662d2-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="662d2-150">1</span><span class="sxs-lookup"><span data-stu-id="662d2-150">1</span></span>     | <span data-ttu-id="662d2-151">/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="662d2-151">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="662d2-152">ascii</span><span class="sxs-lookup"><span data-stu-id="662d2-152">ascii</span></span>       |
| <span data-ttu-id="662d2-153">2</span><span class="sxs-lookup"><span data-stu-id="662d2-153">2</span></span>     | <span data-ttu-id="662d2-154">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="662d2-154">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="662d2-155">unicode</span><span class="sxs-lookup"><span data-stu-id="662d2-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="662d2-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="662d2-156">Write Paths</span></span>



| <span data-ttu-id="662d2-157">JSON</span><span class="sxs-lookup"><span data-stu-id="662d2-157">Order</span></span> | <span data-ttu-id="662d2-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="662d2-158">Path</span></span>                      | <span data-ttu-id="662d2-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="662d2-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="662d2-160">1</span><span class="sxs-lookup"><span data-stu-id="662d2-160">1</span></span>     | <span data-ttu-id="662d2-161">/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="662d2-161">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="662d2-162">ascii</span><span class="sxs-lookup"><span data-stu-id="662d2-162">ascii</span></span>       |
| <span data-ttu-id="662d2-163">2</span><span class="sxs-lookup"><span data-stu-id="662d2-163">2</span></span>     | <span data-ttu-id="662d2-164">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="662d2-164">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="662d2-165">unicode</span><span class="sxs-lookup"><span data-stu-id="662d2-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="662d2-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="662d2-166">Remove Paths</span></span>



| <span data-ttu-id="662d2-167">JSON</span><span class="sxs-lookup"><span data-stu-id="662d2-167">Order</span></span> | <span data-ttu-id="662d2-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="662d2-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="662d2-169">1</span><span class="sxs-lookup"><span data-stu-id="662d2-169">1</span></span>     | <span data-ttu-id="662d2-170">/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="662d2-170">/ifd/gps/{ushort=14}</span></span>      |
| <span data-ttu-id="662d2-171">2</span><span class="sxs-lookup"><span data-stu-id="662d2-171">2</span></span>     | <span data-ttu-id="662d2-172">/ifd/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="662d2-172">/ifd/xmp/exif:gpstrackref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="662d2-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="662d2-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="662d2-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="662d2-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="662d2-175">System. GPS. TrackRef</span><span class="sxs-lookup"><span data-stu-id="662d2-175">System.GPS.TrackRef</span></span>](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
