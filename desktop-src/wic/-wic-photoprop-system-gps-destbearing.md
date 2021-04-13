---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestBearing.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: Criteri per i metadati delle foto di System. GPS. DestBearing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a084a0633579afe646403fb4dcad0ca8a1b9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348586"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a><span data-ttu-id="2cb2a-103">Criteri per i metadati delle foto di System. GPS. DestBearing</span><span class="sxs-lookup"><span data-stu-id="2cb2a-103">System.GPS.DestBearing Photo Metadata Policy</span></span>

<span data-ttu-id="2cb2a-104">Criteri per i metadati delle foto per la proprietà [System. GPS. DestBearing](../properties/props-system-gps-destbearing.md) .</span><span class="sxs-lookup"><span data-stu-id="2cb2a-104">The photo metadata policy for the [System.GPS.DestBearing](../properties/props-system-gps-destbearing.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="2cb2a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="2cb2a-105">PKEY</span></span>

<span data-ttu-id="2cb2a-106">PKEY \_ GPS \_ DestBearing</span><span class="sxs-lookup"><span data-stu-id="2cb2a-106">PKEY\_GPS\_DestBearing</span></span>

### <a name="containers"></a><span data-ttu-id="2cb2a-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="2cb2a-107">Containers</span></span>

<span data-ttu-id="2cb2a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="2cb2a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="2cb2a-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="2cb2a-109">Read-Only</span></span>

<span data-ttu-id="2cb2a-110">Sì</span><span class="sxs-lookup"><span data-stu-id="2cb2a-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="2cb2a-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="2cb2a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="2cb2a-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="2cb2a-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="2cb2a-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="2cb2a-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="2cb2a-114">Questo valore può essere scritto scrivendo in System. GPS. DestBearingNumerator e System. GPS. DestBearingDenominator.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-114">This value can be written by writing to System.GPS.DestBearingNumerator and System.GPS.DestBearingDenominator.</span></span> <span data-ttu-id="2cb2a-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-115">It cannot be written directly.</span></span> <span data-ttu-id="2cb2a-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="2cb2a-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="2cb2a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="2cb2a-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="2cb2a-118">Read Paths</span></span>



| <span data-ttu-id="2cb2a-119">JSON</span><span class="sxs-lookup"><span data-stu-id="2cb2a-119">Order</span></span> | <span data-ttu-id="2cb2a-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="2cb2a-120">Path</span></span>                      | <span data-ttu-id="2cb2a-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="2cb2a-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="2cb2a-122">1</span><span class="sxs-lookup"><span data-stu-id="2cb2a-122">1</span></span>     | <span data-ttu-id="2cb2a-123">/App1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="2cb2a-123">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="2cb2a-124">2</span><span class="sxs-lookup"><span data-stu-id="2cb2a-124">2</span></span>     | <span data-ttu-id="2cb2a-125">/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="2cb2a-125">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="write-paths"></a><span data-ttu-id="2cb2a-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="2cb2a-126">Write Paths</span></span>



| <span data-ttu-id="2cb2a-127">JSON</span><span class="sxs-lookup"><span data-stu-id="2cb2a-127">Order</span></span> | <span data-ttu-id="2cb2a-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="2cb2a-128">Path</span></span>                      | <span data-ttu-id="2cb2a-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="2cb2a-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="2cb2a-130">1</span><span class="sxs-lookup"><span data-stu-id="2cb2a-130">1</span></span>     | <span data-ttu-id="2cb2a-131">/App1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="2cb2a-131">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="2cb2a-132">2</span><span class="sxs-lookup"><span data-stu-id="2cb2a-132">2</span></span>     | <span data-ttu-id="2cb2a-133">/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="2cb2a-133">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="remove-paths"></a><span data-ttu-id="2cb2a-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="2cb2a-134">Remove Paths</span></span>



| <span data-ttu-id="2cb2a-135">JSON</span><span class="sxs-lookup"><span data-stu-id="2cb2a-135">Order</span></span> | <span data-ttu-id="2cb2a-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="2cb2a-136">Path</span></span>                      | <span data-ttu-id="2cb2a-137">Formato del disco</span><span class="sxs-lookup"><span data-stu-id="2cb2a-137">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="2cb2a-138">1</span><span class="sxs-lookup"><span data-stu-id="2cb2a-138">1</span></span>     | <span data-ttu-id="2cb2a-139">/App1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="2cb2a-139">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="2cb2a-140">2</span><span class="sxs-lookup"><span data-stu-id="2cb2a-140">2</span></span>     | <span data-ttu-id="2cb2a-141">/xmp/exif:gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="2cb2a-141">/xmp/exif:gpsdestbearing</span></span>  |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="2cb2a-142">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="2cb2a-142">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="2cb2a-143">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="2cb2a-143">Read Paths</span></span>



| <span data-ttu-id="2cb2a-144">JSON</span><span class="sxs-lookup"><span data-stu-id="2cb2a-144">Order</span></span> | <span data-ttu-id="2cb2a-145">Percorso</span><span class="sxs-lookup"><span data-stu-id="2cb2a-145">Path</span></span>                         | <span data-ttu-id="2cb2a-146">Formato disco</span><span class="sxs-lookup"><span data-stu-id="2cb2a-146">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="2cb2a-147">1</span><span class="sxs-lookup"><span data-stu-id="2cb2a-147">1</span></span>     | <span data-ttu-id="2cb2a-148">/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="2cb2a-148">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="2cb2a-149">2</span><span class="sxs-lookup"><span data-stu-id="2cb2a-149">2</span></span>     | <span data-ttu-id="2cb2a-150">/ifd/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="2cb2a-150">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="2cb2a-151">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="2cb2a-151">Write Paths</span></span>



| <span data-ttu-id="2cb2a-152">JSON</span><span class="sxs-lookup"><span data-stu-id="2cb2a-152">Order</span></span> | <span data-ttu-id="2cb2a-153">Percorso</span><span class="sxs-lookup"><span data-stu-id="2cb2a-153">Path</span></span>                         | <span data-ttu-id="2cb2a-154">Formato disco</span><span class="sxs-lookup"><span data-stu-id="2cb2a-154">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="2cb2a-155">1</span><span class="sxs-lookup"><span data-stu-id="2cb2a-155">1</span></span>     | <span data-ttu-id="2cb2a-156">/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="2cb2a-156">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="2cb2a-157">2</span><span class="sxs-lookup"><span data-stu-id="2cb2a-157">2</span></span>     | <span data-ttu-id="2cb2a-158">/ifd/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="2cb2a-158">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="2cb2a-159">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="2cb2a-159">Remove Paths</span></span>



| <span data-ttu-id="2cb2a-160">JSON</span><span class="sxs-lookup"><span data-stu-id="2cb2a-160">Order</span></span> | <span data-ttu-id="2cb2a-161">Percorso</span><span class="sxs-lookup"><span data-stu-id="2cb2a-161">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="2cb2a-162">1</span><span class="sxs-lookup"><span data-stu-id="2cb2a-162">1</span></span>     | <span data-ttu-id="2cb2a-163">/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="2cb2a-163">/ifd/gps/{ushort=24}</span></span>         |
| <span data-ttu-id="2cb2a-164">2</span><span class="sxs-lookup"><span data-stu-id="2cb2a-164">2</span></span>     | <span data-ttu-id="2cb2a-165">/ifd/xmp/exif:gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="2cb2a-165">/ifd/xmp/exif:gpsdestbearing</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2cb2a-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cb2a-166">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cb2a-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2cb2a-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cb2a-168">System. GPS. DestBearing</span><span class="sxs-lookup"><span data-stu-id="2cb2a-168">System.GPS.DestBearing</span></span>](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
