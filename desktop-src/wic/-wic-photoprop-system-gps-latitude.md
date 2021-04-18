---
description: Criteri per i metadati delle foto per la proprietà System. GPS. Latitude.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: Criteri dei metadati delle foto di System. GPS. Latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5320869c1e8fd0d4b17bb17da455fc939bf44b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316386"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a><span data-ttu-id="90dbd-103">Criteri dei metadati delle foto di System. GPS. Latitude</span><span class="sxs-lookup"><span data-stu-id="90dbd-103">System.GPS.Latitude Photo Metadata Policy</span></span>

<span data-ttu-id="90dbd-104">Criteri per i metadati delle foto per la proprietà [System. GPS. Latitude](../properties/props-system-gps-latitude.md) .</span><span class="sxs-lookup"><span data-stu-id="90dbd-104">The photo metadata policy for the [System.GPS.Latitude](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="90dbd-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="90dbd-105">PKEY</span></span>

<span data-ttu-id="90dbd-106">\_Latitudine GPS \_ pkey</span><span class="sxs-lookup"><span data-stu-id="90dbd-106">PKEY\_GPS\_Latitude</span></span>

### <a name="containers"></a><span data-ttu-id="90dbd-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="90dbd-107">Containers</span></span>

<span data-ttu-id="90dbd-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="90dbd-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="90dbd-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="90dbd-109">Read-Only</span></span>

<span data-ttu-id="90dbd-110">Sì</span><span class="sxs-lookup"><span data-stu-id="90dbd-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="90dbd-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="90dbd-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="90dbd-112">VT \_ vettore \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="90dbd-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="90dbd-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="90dbd-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="90dbd-114">Questo valore può essere scritto scrivendo in System. GPS. LatitudeNumerator e System. GPS. LatitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="90dbd-114">This value can be written by writing to System.GPS.LatitudeNumerator and System.GPS.LatitudeDenominator.</span></span> <span data-ttu-id="90dbd-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="90dbd-115">It cannot be written directly.</span></span> <span data-ttu-id="90dbd-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="90dbd-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="90dbd-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="90dbd-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="90dbd-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="90dbd-118">Read Paths</span></span>



| <span data-ttu-id="90dbd-119">JSON</span><span class="sxs-lookup"><span data-stu-id="90dbd-119">Order</span></span> | <span data-ttu-id="90dbd-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="90dbd-120">Path</span></span>                     | <span data-ttu-id="90dbd-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="90dbd-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="90dbd-122">1</span><span class="sxs-lookup"><span data-stu-id="90dbd-122">1</span></span>     | <span data-ttu-id="90dbd-123">/App1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="90dbd-123">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="90dbd-124">2</span><span class="sxs-lookup"><span data-stu-id="90dbd-124">2</span></span>     | <span data-ttu-id="90dbd-125">/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="90dbd-125">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="90dbd-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="90dbd-126">Write Paths</span></span>



| <span data-ttu-id="90dbd-127">JSON</span><span class="sxs-lookup"><span data-stu-id="90dbd-127">Order</span></span> | <span data-ttu-id="90dbd-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="90dbd-128">Path</span></span>                     | <span data-ttu-id="90dbd-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="90dbd-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="90dbd-130">1</span><span class="sxs-lookup"><span data-stu-id="90dbd-130">1</span></span>     | <span data-ttu-id="90dbd-131">/App1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="90dbd-131">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="90dbd-132">2</span><span class="sxs-lookup"><span data-stu-id="90dbd-132">2</span></span>     | <span data-ttu-id="90dbd-133">/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="90dbd-133">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="90dbd-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="90dbd-134">Remove Paths</span></span>



| <span data-ttu-id="90dbd-135">JSON</span><span class="sxs-lookup"><span data-stu-id="90dbd-135">Order</span></span> | <span data-ttu-id="90dbd-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="90dbd-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="90dbd-137">1</span><span class="sxs-lookup"><span data-stu-id="90dbd-137">1</span></span>     | <span data-ttu-id="90dbd-138">/App1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="90dbd-138">/app1/ifd/gps/{ushort=2}</span></span> |
| <span data-ttu-id="90dbd-139">2</span><span class="sxs-lookup"><span data-stu-id="90dbd-139">2</span></span>     | <span data-ttu-id="90dbd-140">/xmp/exif:gpslatitude</span><span class="sxs-lookup"><span data-stu-id="90dbd-140">/xmp/exif:gpslatitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="90dbd-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="90dbd-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="90dbd-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="90dbd-142">Read Paths</span></span>



| <span data-ttu-id="90dbd-143">JSON</span><span class="sxs-lookup"><span data-stu-id="90dbd-143">Order</span></span> | <span data-ttu-id="90dbd-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="90dbd-144">Path</span></span>                      | <span data-ttu-id="90dbd-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="90dbd-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="90dbd-146">1</span><span class="sxs-lookup"><span data-stu-id="90dbd-146">1</span></span>     | <span data-ttu-id="90dbd-147">/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="90dbd-147">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="90dbd-148">2</span><span class="sxs-lookup"><span data-stu-id="90dbd-148">2</span></span>     | <span data-ttu-id="90dbd-149">/ifd/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="90dbd-149">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="90dbd-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="90dbd-150">Write Paths</span></span>



| <span data-ttu-id="90dbd-151">JSON</span><span class="sxs-lookup"><span data-stu-id="90dbd-151">Order</span></span> | <span data-ttu-id="90dbd-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="90dbd-152">Path</span></span>                      | <span data-ttu-id="90dbd-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="90dbd-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="90dbd-154">1</span><span class="sxs-lookup"><span data-stu-id="90dbd-154">1</span></span>     | <span data-ttu-id="90dbd-155">/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="90dbd-155">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="90dbd-156">2</span><span class="sxs-lookup"><span data-stu-id="90dbd-156">2</span></span>     | <span data-ttu-id="90dbd-157">/ifd/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="90dbd-157">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="90dbd-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="90dbd-158">Remove Paths</span></span>



| <span data-ttu-id="90dbd-159">JSON</span><span class="sxs-lookup"><span data-stu-id="90dbd-159">Order</span></span> | <span data-ttu-id="90dbd-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="90dbd-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="90dbd-161">1</span><span class="sxs-lookup"><span data-stu-id="90dbd-161">1</span></span>     | <span data-ttu-id="90dbd-162">/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="90dbd-162">/ifd/gps/{ushort=2}</span></span>       |
| <span data-ttu-id="90dbd-163">2</span><span class="sxs-lookup"><span data-stu-id="90dbd-163">2</span></span>     | <span data-ttu-id="90dbd-164">/ifd/xmp/exif:gpslatitude</span><span class="sxs-lookup"><span data-stu-id="90dbd-164">/ifd/xmp/exif:gpslatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="90dbd-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="90dbd-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="90dbd-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90dbd-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90dbd-167">System. GPS. Latitude</span><span class="sxs-lookup"><span data-stu-id="90dbd-167">System.GPS.Latitude</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
