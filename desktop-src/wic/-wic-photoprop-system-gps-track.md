---
description: Criteri per i metadati delle foto per la proprietà System. GPS. Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Criteri di metadati di Photo System. GPS. Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319108"
---
# <a name="systemgpstrack-photo-metadata-policy"></a><span data-ttu-id="04747-103">Criteri di metadati di Photo System. GPS. Track</span><span class="sxs-lookup"><span data-stu-id="04747-103">System.GPS.Track Photo Metadata Policy</span></span>

<span data-ttu-id="04747-104">Criteri per i metadati delle foto per la proprietà [System. GPS. Track](../properties/props-system-gps-track.md) .</span><span class="sxs-lookup"><span data-stu-id="04747-104">The photo metadata policy for the [System.GPS.Track](../properties/props-system-gps-track.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="04747-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="04747-105">PKEY</span></span>

<span data-ttu-id="04747-106">\_Traccia GPS \_ pkey</span><span class="sxs-lookup"><span data-stu-id="04747-106">PKEY\_GPS\_Track</span></span>

### <a name="containers"></a><span data-ttu-id="04747-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="04747-107">Containers</span></span>

<span data-ttu-id="04747-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="04747-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="04747-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="04747-109">Read-Only</span></span>

<span data-ttu-id="04747-110">Sì</span><span class="sxs-lookup"><span data-stu-id="04747-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="04747-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="04747-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="04747-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="04747-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="04747-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="04747-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="04747-114">Questo valore viene generato da System. GPS. TrackNumerator e System. GPS. TrackDenominator.</span><span class="sxs-lookup"><span data-stu-id="04747-114">This value is generated from System.GPS.TrackNumerator and System.GPS.TrackDenominator.</span></span> <span data-ttu-id="04747-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="04747-115">It cannot be written directly.</span></span> <span data-ttu-id="04747-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="04747-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="04747-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="04747-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="04747-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="04747-118">Read Paths</span></span>



| <span data-ttu-id="04747-119">JSON</span><span class="sxs-lookup"><span data-stu-id="04747-119">Order</span></span> | <span data-ttu-id="04747-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="04747-120">Path</span></span>                      | <span data-ttu-id="04747-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="04747-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="04747-122">1</span><span class="sxs-lookup"><span data-stu-id="04747-122">1</span></span>     | <span data-ttu-id="04747-123">/App1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="04747-123">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="04747-124">2</span><span class="sxs-lookup"><span data-stu-id="04747-124">2</span></span>     | <span data-ttu-id="04747-125">/XMP/EXIF: GPSTrack</span><span class="sxs-lookup"><span data-stu-id="04747-125">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="04747-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="04747-126">Write Paths</span></span>



| <span data-ttu-id="04747-127">JSON</span><span class="sxs-lookup"><span data-stu-id="04747-127">Order</span></span> | <span data-ttu-id="04747-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="04747-128">Path</span></span>                      | <span data-ttu-id="04747-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="04747-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="04747-130">1</span><span class="sxs-lookup"><span data-stu-id="04747-130">1</span></span>     | <span data-ttu-id="04747-131">/App1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="04747-131">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="04747-132">2</span><span class="sxs-lookup"><span data-stu-id="04747-132">2</span></span>     | <span data-ttu-id="04747-133">/XMP/EXIF: GPSTrack</span><span class="sxs-lookup"><span data-stu-id="04747-133">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="04747-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="04747-134">Remove Paths</span></span>



| <span data-ttu-id="04747-135">JSON</span><span class="sxs-lookup"><span data-stu-id="04747-135">Order</span></span> | <span data-ttu-id="04747-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="04747-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="04747-137">1</span><span class="sxs-lookup"><span data-stu-id="04747-137">1</span></span>     | <span data-ttu-id="04747-138">/App1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="04747-138">/app1/ifd/gps/{ushort=15}</span></span> |
| <span data-ttu-id="04747-139">2</span><span class="sxs-lookup"><span data-stu-id="04747-139">2</span></span>     | <span data-ttu-id="04747-140">/XMP/EXIF: Gpstrack</span><span class="sxs-lookup"><span data-stu-id="04747-140">/xmp/exif:gpstrack</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="04747-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="04747-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="04747-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="04747-142">Read Paths</span></span>



| <span data-ttu-id="04747-143">JSON</span><span class="sxs-lookup"><span data-stu-id="04747-143">Order</span></span> | <span data-ttu-id="04747-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="04747-144">Path</span></span>                   | <span data-ttu-id="04747-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="04747-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="04747-146">1</span><span class="sxs-lookup"><span data-stu-id="04747-146">1</span></span>     | <span data-ttu-id="04747-147">/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="04747-147">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="04747-148">2</span><span class="sxs-lookup"><span data-stu-id="04747-148">2</span></span>     | <span data-ttu-id="04747-149">/IFD/XMP/EXIF: GPSTrack</span><span class="sxs-lookup"><span data-stu-id="04747-149">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="04747-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="04747-150">Write Paths</span></span>



| <span data-ttu-id="04747-151">JSON</span><span class="sxs-lookup"><span data-stu-id="04747-151">Order</span></span> | <span data-ttu-id="04747-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="04747-152">Path</span></span>                   | <span data-ttu-id="04747-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="04747-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="04747-154">1</span><span class="sxs-lookup"><span data-stu-id="04747-154">1</span></span>     | <span data-ttu-id="04747-155">/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="04747-155">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="04747-156">2</span><span class="sxs-lookup"><span data-stu-id="04747-156">2</span></span>     | <span data-ttu-id="04747-157">/IFD/XMP/EXIF: GPSTrack</span><span class="sxs-lookup"><span data-stu-id="04747-157">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="04747-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="04747-158">Remove Paths</span></span>



| <span data-ttu-id="04747-159">JSON</span><span class="sxs-lookup"><span data-stu-id="04747-159">Order</span></span> | <span data-ttu-id="04747-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="04747-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="04747-161">1</span><span class="sxs-lookup"><span data-stu-id="04747-161">1</span></span>     | <span data-ttu-id="04747-162">/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="04747-162">/ifd/gps/{ushort=15}</span></span>   |
| <span data-ttu-id="04747-163">2</span><span class="sxs-lookup"><span data-stu-id="04747-163">2</span></span>     | <span data-ttu-id="04747-164">/IFD/XMP/EXIF: Gpstrack</span><span class="sxs-lookup"><span data-stu-id="04747-164">/ifd/xmp/exif:gpstrack</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="04747-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="04747-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="04747-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04747-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04747-167">System. GPS. Track</span><span class="sxs-lookup"><span data-stu-id="04747-167">System.GPS.Track</span></span>](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
