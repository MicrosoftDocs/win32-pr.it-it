---
description: Criteri per i metadati delle foto per la proprietà System. GPS. longitudine.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Criteri dei metadati della foto System. GPS. Longitudine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317873"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a><span data-ttu-id="e33d2-103">Criteri dei metadati della foto System. GPS. Longitudine</span><span class="sxs-lookup"><span data-stu-id="e33d2-103">System.GPS.Longitude Photo Metadata Policy</span></span>

<span data-ttu-id="e33d2-104">Criteri per i metadati delle foto per la proprietà [System. GPS. Longitudine](../properties/props-system-gps-longitude.md) .</span><span class="sxs-lookup"><span data-stu-id="e33d2-104">The photo metadata policy for the [System.GPS.Longitude](../properties/props-system-gps-longitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e33d2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e33d2-105">PKEY</span></span>

<span data-ttu-id="e33d2-106">\_Longitudine GPS \_ pkey</span><span class="sxs-lookup"><span data-stu-id="e33d2-106">PKEY\_GPS\_Longitude</span></span>

### <a name="containers"></a><span data-ttu-id="e33d2-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="e33d2-107">Containers</span></span>

<span data-ttu-id="e33d2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e33d2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e33d2-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="e33d2-109">Read-Only</span></span>

<span data-ttu-id="e33d2-110">Sì</span><span class="sxs-lookup"><span data-stu-id="e33d2-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e33d2-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="e33d2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e33d2-112">VT \_ vettore \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="e33d2-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e33d2-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="e33d2-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="e33d2-114">Questo valore può essere scritto scrivendo in System. GPS. LongitudeNumerator e System. GPS. LongitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="e33d2-114">This value can be written by writing to System.GPS.LongitudeNumerator and System.GPS.LongitudeDenominator.</span></span> <span data-ttu-id="e33d2-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="e33d2-115">It cannot be written directly.</span></span> <span data-ttu-id="e33d2-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="e33d2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e33d2-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="e33d2-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e33d2-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="e33d2-118">Read Paths</span></span>



| <span data-ttu-id="e33d2-119">JSON</span><span class="sxs-lookup"><span data-stu-id="e33d2-119">Order</span></span> | <span data-ttu-id="e33d2-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="e33d2-120">Path</span></span>                     | <span data-ttu-id="e33d2-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e33d2-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="e33d2-122">1</span><span class="sxs-lookup"><span data-stu-id="e33d2-122">1</span></span>     | <span data-ttu-id="e33d2-123">/App1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="e33d2-123">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="e33d2-124">2</span><span class="sxs-lookup"><span data-stu-id="e33d2-124">2</span></span>     | <span data-ttu-id="e33d2-125">/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="e33d2-125">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="e33d2-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="e33d2-126">Write Paths</span></span>



| <span data-ttu-id="e33d2-127">JSON</span><span class="sxs-lookup"><span data-stu-id="e33d2-127">Order</span></span> | <span data-ttu-id="e33d2-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="e33d2-128">Path</span></span>                     | <span data-ttu-id="e33d2-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e33d2-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="e33d2-130">1</span><span class="sxs-lookup"><span data-stu-id="e33d2-130">1</span></span>     | <span data-ttu-id="e33d2-131">/App1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="e33d2-131">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="e33d2-132">2</span><span class="sxs-lookup"><span data-stu-id="e33d2-132">2</span></span>     | <span data-ttu-id="e33d2-133">/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="e33d2-133">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e33d2-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="e33d2-134">Remove Paths</span></span>



| <span data-ttu-id="e33d2-135">JSON</span><span class="sxs-lookup"><span data-stu-id="e33d2-135">Order</span></span> | <span data-ttu-id="e33d2-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="e33d2-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="e33d2-137">1</span><span class="sxs-lookup"><span data-stu-id="e33d2-137">1</span></span>     | <span data-ttu-id="e33d2-138">/App1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="e33d2-138">/app1/ifd/gps/{ushort=4}</span></span> |
| <span data-ttu-id="e33d2-139">2</span><span class="sxs-lookup"><span data-stu-id="e33d2-139">2</span></span>     | <span data-ttu-id="e33d2-140">/xmp/exif:gpslongitude</span><span class="sxs-lookup"><span data-stu-id="e33d2-140">/xmp/exif:gpslongitude</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="e33d2-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="e33d2-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e33d2-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="e33d2-142">Read Paths</span></span>



| <span data-ttu-id="e33d2-143">JSON</span><span class="sxs-lookup"><span data-stu-id="e33d2-143">Order</span></span> | <span data-ttu-id="e33d2-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="e33d2-144">Path</span></span>                       | <span data-ttu-id="e33d2-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e33d2-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="e33d2-146">1</span><span class="sxs-lookup"><span data-stu-id="e33d2-146">1</span></span>     | <span data-ttu-id="e33d2-147">/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="e33d2-147">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="e33d2-148">2</span><span class="sxs-lookup"><span data-stu-id="e33d2-148">2</span></span>     | <span data-ttu-id="e33d2-149">/ifd/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="e33d2-149">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="e33d2-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="e33d2-150">Write Paths</span></span>



| <span data-ttu-id="e33d2-151">JSON</span><span class="sxs-lookup"><span data-stu-id="e33d2-151">Order</span></span> | <span data-ttu-id="e33d2-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="e33d2-152">Path</span></span>                       | <span data-ttu-id="e33d2-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e33d2-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="e33d2-154">1</span><span class="sxs-lookup"><span data-stu-id="e33d2-154">1</span></span>     | <span data-ttu-id="e33d2-155">/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="e33d2-155">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="e33d2-156">2</span><span class="sxs-lookup"><span data-stu-id="e33d2-156">2</span></span>     | <span data-ttu-id="e33d2-157">/ifd/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="e33d2-157">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e33d2-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="e33d2-158">Remove Paths</span></span>



| <span data-ttu-id="e33d2-159">JSON</span><span class="sxs-lookup"><span data-stu-id="e33d2-159">Order</span></span> | <span data-ttu-id="e33d2-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="e33d2-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="e33d2-161">1</span><span class="sxs-lookup"><span data-stu-id="e33d2-161">1</span></span>     | <span data-ttu-id="e33d2-162">/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="e33d2-162">/ifd/gps/{ushort=4}</span></span>        |
| <span data-ttu-id="e33d2-163">2</span><span class="sxs-lookup"><span data-stu-id="e33d2-163">2</span></span>     | <span data-ttu-id="e33d2-164">/ifd/xmp/exif:gpslongitude</span><span class="sxs-lookup"><span data-stu-id="e33d2-164">/ifd/xmp/exif:gpslongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e33d2-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="e33d2-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e33d2-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e33d2-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e33d2-167">System. GPS. Longitudine</span><span class="sxs-lookup"><span data-stu-id="e33d2-167">System.GPS.Longitude</span></span>](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
