---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestLongitude.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Criteri per i metadati delle foto di System. GPS. DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058054"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a><span data-ttu-id="304a4-103">Criteri per i metadati delle foto di System. GPS. DestLongitude</span><span class="sxs-lookup"><span data-stu-id="304a4-103">System.GPS.DestLongitude Photo Metadata Policy</span></span>

<span data-ttu-id="304a4-104">Criteri per i metadati delle foto per la proprietà [System. GPS. DestLongitude](../properties/props-system-gps-destlongitude.md) .</span><span class="sxs-lookup"><span data-stu-id="304a4-104">The photo metadata policy for the [System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="304a4-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="304a4-105">PKEY</span></span>

<span data-ttu-id="304a4-106">PKEY \_ GPS \_ DestLongitude</span><span class="sxs-lookup"><span data-stu-id="304a4-106">PKEY\_GPS\_DestLongitude</span></span>

### <a name="containers"></a><span data-ttu-id="304a4-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="304a4-107">Containers</span></span>

<span data-ttu-id="304a4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="304a4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="304a4-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="304a4-109">Read-Only</span></span>

<span data-ttu-id="304a4-110">Sì</span><span class="sxs-lookup"><span data-stu-id="304a4-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="304a4-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="304a4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="304a4-112">VT \_ vettore \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="304a4-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="304a4-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="304a4-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="304a4-114">VT \_ vettore \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="304a4-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="304a4-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="304a4-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="304a4-116">Questo valore viene generato da System. GPS. DestLongitudeNumerator e System. GPS. DestLongitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="304a4-116">This value is generated from System.GPS.DestLongitudeNumerator and System.GPS.DestLongitudeDenominator.</span></span> <span data-ttu-id="304a4-117">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="304a4-117">It cannot be written directly.</span></span> <span data-ttu-id="304a4-118">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="304a4-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="304a4-119">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="304a4-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="304a4-120">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="304a4-120">Read Paths</span></span>



| <span data-ttu-id="304a4-121">JSON</span><span class="sxs-lookup"><span data-stu-id="304a4-121">Order</span></span> | <span data-ttu-id="304a4-122">Percorso</span><span class="sxs-lookup"><span data-stu-id="304a4-122">Path</span></span>                       | <span data-ttu-id="304a4-123">Formato disco</span><span class="sxs-lookup"><span data-stu-id="304a4-123">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="304a4-124">1</span><span class="sxs-lookup"><span data-stu-id="304a4-124">1</span></span>     | <span data-ttu-id="304a4-125">/App1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="304a4-125">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="304a4-126">2</span><span class="sxs-lookup"><span data-stu-id="304a4-126">2</span></span>     | <span data-ttu-id="304a4-127">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="304a4-127">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="304a4-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="304a4-128">Write Paths</span></span>



| <span data-ttu-id="304a4-129">JSON</span><span class="sxs-lookup"><span data-stu-id="304a4-129">Order</span></span> | <span data-ttu-id="304a4-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="304a4-130">Path</span></span>                       | <span data-ttu-id="304a4-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="304a4-131">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="304a4-132">1</span><span class="sxs-lookup"><span data-stu-id="304a4-132">1</span></span>     | <span data-ttu-id="304a4-133">/App1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="304a4-133">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="304a4-134">2</span><span class="sxs-lookup"><span data-stu-id="304a4-134">2</span></span>     | <span data-ttu-id="304a4-135">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="304a4-135">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="304a4-136">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="304a4-136">Remove Paths</span></span>



| <span data-ttu-id="304a4-137">JSON</span><span class="sxs-lookup"><span data-stu-id="304a4-137">Order</span></span> | <span data-ttu-id="304a4-138">Percorso</span><span class="sxs-lookup"><span data-stu-id="304a4-138">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="304a4-139">1</span><span class="sxs-lookup"><span data-stu-id="304a4-139">1</span></span>     | <span data-ttu-id="304a4-140">/App1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="304a4-140">/app1/ifd/gps/{ushort=22}</span></span>  |
| <span data-ttu-id="304a4-141">2</span><span class="sxs-lookup"><span data-stu-id="304a4-141">2</span></span>     | <span data-ttu-id="304a4-142">/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="304a4-142">/xmp/exif:gpsdestlongitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="304a4-143">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="304a4-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="304a4-144">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="304a4-144">Read Paths</span></span>



| <span data-ttu-id="304a4-145">JSON</span><span class="sxs-lookup"><span data-stu-id="304a4-145">Order</span></span> | <span data-ttu-id="304a4-146">Percorso</span><span class="sxs-lookup"><span data-stu-id="304a4-146">Path</span></span>                           | <span data-ttu-id="304a4-147">Formato disco</span><span class="sxs-lookup"><span data-stu-id="304a4-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="304a4-148">1</span><span class="sxs-lookup"><span data-stu-id="304a4-148">1</span></span>     | <span data-ttu-id="304a4-149">/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="304a4-149">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="304a4-150">2</span><span class="sxs-lookup"><span data-stu-id="304a4-150">2</span></span>     | <span data-ttu-id="304a4-151">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="304a4-151">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="304a4-152">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="304a4-152">Write Paths</span></span>



| <span data-ttu-id="304a4-153">JSON</span><span class="sxs-lookup"><span data-stu-id="304a4-153">Order</span></span> | <span data-ttu-id="304a4-154">Percorso</span><span class="sxs-lookup"><span data-stu-id="304a4-154">Path</span></span>                           | <span data-ttu-id="304a4-155">Formato disco</span><span class="sxs-lookup"><span data-stu-id="304a4-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="304a4-156">1</span><span class="sxs-lookup"><span data-stu-id="304a4-156">1</span></span>     | <span data-ttu-id="304a4-157">/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="304a4-157">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="304a4-158">2</span><span class="sxs-lookup"><span data-stu-id="304a4-158">2</span></span>     | <span data-ttu-id="304a4-159">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="304a4-159">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="304a4-160">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="304a4-160">Remove Paths</span></span>



| <span data-ttu-id="304a4-161">JSON</span><span class="sxs-lookup"><span data-stu-id="304a4-161">Order</span></span> | <span data-ttu-id="304a4-162">Percorso</span><span class="sxs-lookup"><span data-stu-id="304a4-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="304a4-163">1</span><span class="sxs-lookup"><span data-stu-id="304a4-163">1</span></span>     | <span data-ttu-id="304a4-164">/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="304a4-164">/ifd/gps/{ushort=22}</span></span>           |
| <span data-ttu-id="304a4-165">2</span><span class="sxs-lookup"><span data-stu-id="304a4-165">2</span></span>     | <span data-ttu-id="304a4-166">/ifd/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="304a4-166">/ifd/xmp/exif:gpsdestlongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="304a4-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="304a4-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="304a4-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="304a4-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="304a4-169">System. GPS. DestLongitude</span><span class="sxs-lookup"><span data-stu-id="304a4-169">System.GPS.DestLongitude</span></span>](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
