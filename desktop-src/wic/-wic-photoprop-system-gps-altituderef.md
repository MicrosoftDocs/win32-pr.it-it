---
description: Criteri per i metadati delle foto per la proprietà System. GPS. AltitudeRef.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Criteri per i metadati delle foto di System. GPS. AltitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317885"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a><span data-ttu-id="1e293-103">Criteri per i metadati delle foto di System. GPS. AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1e293-103">System.GPS.AltitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="1e293-104">Criteri per i metadati delle foto per la proprietà [System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="1e293-104">The photo metadata policy for the [System.GPS.AltitudeRef](../properties/props-system-gps-altituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1e293-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="1e293-105">PKEY</span></span>

<span data-ttu-id="1e293-106">PKEY \_ GPS \_ AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1e293-106">PKEY\_GPS\_AltitudeRef</span></span>

### <a name="description"></a><span data-ttu-id="1e293-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e293-107">Description</span></span>

<span data-ttu-id="1e293-108">Indica l'altitudine utilizzata come altitudine di riferimento.</span><span class="sxs-lookup"><span data-stu-id="1e293-108">Indicates the altitude used as the reference altitude.</span></span> <span data-ttu-id="1e293-109">Il valore 0 indica che l'altitudine è superiore al livello del mare.</span><span class="sxs-lookup"><span data-stu-id="1e293-109">A value of 0 indicates the altitude is above sea level.</span></span> <span data-ttu-id="1e293-110">Il valore 1 indica un'altitudine sotto il livello Sea.</span><span class="sxs-lookup"><span data-stu-id="1e293-110">A value of 1 indicates an altitude below sea level.</span></span>

### <a name="containers"></a><span data-ttu-id="1e293-111">Contenitori</span><span class="sxs-lookup"><span data-stu-id="1e293-111">Containers</span></span>

<span data-ttu-id="1e293-112">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1e293-112">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1e293-113">Read-Only</span><span class="sxs-lookup"><span data-stu-id="1e293-113">Read-Only</span></span>

<span data-ttu-id="1e293-114">No</span><span class="sxs-lookup"><span data-stu-id="1e293-114">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1e293-115">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="1e293-115">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1e293-116">\_Ui1 VT</span><span class="sxs-lookup"><span data-stu-id="1e293-116">VT\_UI1</span></span>

### <a name="input-type"></a><span data-ttu-id="1e293-117">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="1e293-117">Input Type</span></span>

<span data-ttu-id="1e293-118">Byte.</span><span class="sxs-lookup"><span data-stu-id="1e293-118">Byte.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1e293-119">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="1e293-119">Conflict Resolution Policy</span></span>

<span data-ttu-id="1e293-120">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="1e293-120">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="1e293-121">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="1e293-121">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1e293-122">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="1e293-122">Read Paths</span></span>



| <span data-ttu-id="1e293-123">JSON</span><span class="sxs-lookup"><span data-stu-id="1e293-123">Order</span></span> | <span data-ttu-id="1e293-124">Percorso</span><span class="sxs-lookup"><span data-stu-id="1e293-124">Path</span></span>                     | <span data-ttu-id="1e293-125">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1e293-125">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1e293-126">1</span><span class="sxs-lookup"><span data-stu-id="1e293-126">1</span></span>     | <span data-ttu-id="1e293-127">/App1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1e293-127">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="1e293-128">byte</span><span class="sxs-lookup"><span data-stu-id="1e293-128">byte</span></span>        |
| <span data-ttu-id="1e293-129">2</span><span class="sxs-lookup"><span data-stu-id="1e293-129">2</span></span>     | <span data-ttu-id="1e293-130">/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1e293-130">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="1e293-131">unicode</span><span class="sxs-lookup"><span data-stu-id="1e293-131">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1e293-132">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="1e293-132">Write Paths</span></span>



| <span data-ttu-id="1e293-133">JSON</span><span class="sxs-lookup"><span data-stu-id="1e293-133">Order</span></span> | <span data-ttu-id="1e293-134">Percorso</span><span class="sxs-lookup"><span data-stu-id="1e293-134">Path</span></span>                     | <span data-ttu-id="1e293-135">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1e293-135">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1e293-136">1</span><span class="sxs-lookup"><span data-stu-id="1e293-136">1</span></span>     | <span data-ttu-id="1e293-137">/App1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1e293-137">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="1e293-138">byte</span><span class="sxs-lookup"><span data-stu-id="1e293-138">byte</span></span>        |
| <span data-ttu-id="1e293-139">2</span><span class="sxs-lookup"><span data-stu-id="1e293-139">2</span></span>     | <span data-ttu-id="1e293-140">/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1e293-140">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="1e293-141">unicode</span><span class="sxs-lookup"><span data-stu-id="1e293-141">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1e293-142">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="1e293-142">Remove Paths</span></span>



| <span data-ttu-id="1e293-143">JSON</span><span class="sxs-lookup"><span data-stu-id="1e293-143">Order</span></span> | <span data-ttu-id="1e293-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="1e293-144">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="1e293-145">1</span><span class="sxs-lookup"><span data-stu-id="1e293-145">1</span></span>     | <span data-ttu-id="1e293-146">/App1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1e293-146">/app1/ifd/gps/{ushort=5}</span></span> |
| <span data-ttu-id="1e293-147">2</span><span class="sxs-lookup"><span data-stu-id="1e293-147">2</span></span>     | <span data-ttu-id="1e293-148">/xmp/exif:gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="1e293-148">/xmp/exif:gpsaltituderef</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="1e293-149">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="1e293-149">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1e293-150">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="1e293-150">Read Paths</span></span>



| <span data-ttu-id="1e293-151">JSON</span><span class="sxs-lookup"><span data-stu-id="1e293-151">Order</span></span> | <span data-ttu-id="1e293-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="1e293-152">Path</span></span>                         | <span data-ttu-id="1e293-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1e293-153">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="1e293-154">1</span><span class="sxs-lookup"><span data-stu-id="1e293-154">1</span></span>     | <span data-ttu-id="1e293-155">/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1e293-155">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="1e293-156">byte</span><span class="sxs-lookup"><span data-stu-id="1e293-156">byte</span></span>        |
| <span data-ttu-id="1e293-157">2</span><span class="sxs-lookup"><span data-stu-id="1e293-157">2</span></span>     | <span data-ttu-id="1e293-158">/ifd/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1e293-158">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="1e293-159">unicode</span><span class="sxs-lookup"><span data-stu-id="1e293-159">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1e293-160">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="1e293-160">Write Paths</span></span>



| <span data-ttu-id="1e293-161">JSON</span><span class="sxs-lookup"><span data-stu-id="1e293-161">Order</span></span> | <span data-ttu-id="1e293-162">Percorso</span><span class="sxs-lookup"><span data-stu-id="1e293-162">Path</span></span>                         | <span data-ttu-id="1e293-163">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1e293-163">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="1e293-164">1</span><span class="sxs-lookup"><span data-stu-id="1e293-164">1</span></span>     | <span data-ttu-id="1e293-165">/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1e293-165">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="1e293-166">byte</span><span class="sxs-lookup"><span data-stu-id="1e293-166">byte</span></span>        |
| <span data-ttu-id="1e293-167">2</span><span class="sxs-lookup"><span data-stu-id="1e293-167">2</span></span>     | <span data-ttu-id="1e293-168">/ifd/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1e293-168">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="1e293-169">unicode</span><span class="sxs-lookup"><span data-stu-id="1e293-169">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1e293-170">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="1e293-170">Remove Paths</span></span>



| <span data-ttu-id="1e293-171">JSON</span><span class="sxs-lookup"><span data-stu-id="1e293-171">Order</span></span> | <span data-ttu-id="1e293-172">Percorso</span><span class="sxs-lookup"><span data-stu-id="1e293-172">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="1e293-173">1</span><span class="sxs-lookup"><span data-stu-id="1e293-173">1</span></span>     | <span data-ttu-id="1e293-174">/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="1e293-174">/ifd/gps/{ushort=5}</span></span>          |
| <span data-ttu-id="1e293-175">2</span><span class="sxs-lookup"><span data-stu-id="1e293-175">2</span></span>     | <span data-ttu-id="1e293-176">/ifd/xmp/exif:gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="1e293-176">/ifd/xmp/exif:gpsaltituderef</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1e293-177">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e293-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e293-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e293-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e293-179">System. GPS. AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="1e293-179">System.GPS.AltitudeRef</span></span>](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
