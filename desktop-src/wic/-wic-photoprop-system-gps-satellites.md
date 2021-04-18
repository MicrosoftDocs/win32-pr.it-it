---
description: Criteri per i metadati delle foto per la proprietà System. GPS. satellites.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Criteri dei metadati delle foto di System. GPS. Satellites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312967"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a><span data-ttu-id="80a1b-103">Criteri dei metadati delle foto di System. GPS. Satellites</span><span class="sxs-lookup"><span data-stu-id="80a1b-103">System.GPS.Satellites Photo Metadata Policy</span></span>

<span data-ttu-id="80a1b-104">Criteri per i metadati delle foto per la proprietà [System. GPS. Satellites](../properties/props-system-gps-satellites.md) .</span><span class="sxs-lookup"><span data-stu-id="80a1b-104">The photo metadata policy for the [System.GPS.Satellites](../properties/props-system-gps-satellites.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="80a1b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="80a1b-105">PKEY</span></span>

<span data-ttu-id="80a1b-106">\_ \_ Satelliti GPS pkey</span><span class="sxs-lookup"><span data-stu-id="80a1b-106">PKEY\_GPS\_Satellites</span></span>

### <a name="containers"></a><span data-ttu-id="80a1b-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="80a1b-107">Containers</span></span>

<span data-ttu-id="80a1b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="80a1b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="80a1b-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="80a1b-109">Read-Only</span></span>

<span data-ttu-id="80a1b-110">No</span><span class="sxs-lookup"><span data-stu-id="80a1b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="80a1b-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="80a1b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="80a1b-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="80a1b-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="80a1b-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="80a1b-113">Input Type</span></span>

<span data-ttu-id="80a1b-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="80a1b-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="80a1b-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="80a1b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="80a1b-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="80a1b-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="80a1b-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="80a1b-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="80a1b-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="80a1b-118">Read Paths</span></span>



| <span data-ttu-id="80a1b-119">JSON</span><span class="sxs-lookup"><span data-stu-id="80a1b-119">Order</span></span> | <span data-ttu-id="80a1b-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="80a1b-120">Path</span></span>                     | <span data-ttu-id="80a1b-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="80a1b-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="80a1b-122">1</span><span class="sxs-lookup"><span data-stu-id="80a1b-122">1</span></span>     | <span data-ttu-id="80a1b-123">/App1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="80a1b-123">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="80a1b-124">ascii</span><span class="sxs-lookup"><span data-stu-id="80a1b-124">ascii</span></span>       |
| <span data-ttu-id="80a1b-125">2</span><span class="sxs-lookup"><span data-stu-id="80a1b-125">2</span></span>     | <span data-ttu-id="80a1b-126">/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="80a1b-126">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="80a1b-127">unicode</span><span class="sxs-lookup"><span data-stu-id="80a1b-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="80a1b-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="80a1b-128">Write Paths</span></span>



| <span data-ttu-id="80a1b-129">JSON</span><span class="sxs-lookup"><span data-stu-id="80a1b-129">Order</span></span> | <span data-ttu-id="80a1b-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="80a1b-130">Path</span></span>                     | <span data-ttu-id="80a1b-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="80a1b-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="80a1b-132">1</span><span class="sxs-lookup"><span data-stu-id="80a1b-132">1</span></span>     | <span data-ttu-id="80a1b-133">/App1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="80a1b-133">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="80a1b-134">ascii</span><span class="sxs-lookup"><span data-stu-id="80a1b-134">ascii</span></span>       |
| <span data-ttu-id="80a1b-135">2</span><span class="sxs-lookup"><span data-stu-id="80a1b-135">2</span></span>     | <span data-ttu-id="80a1b-136">/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="80a1b-136">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="80a1b-137">unicode</span><span class="sxs-lookup"><span data-stu-id="80a1b-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="80a1b-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="80a1b-138">Remove Paths</span></span>



| <span data-ttu-id="80a1b-139">JSON</span><span class="sxs-lookup"><span data-stu-id="80a1b-139">Order</span></span> | <span data-ttu-id="80a1b-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="80a1b-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="80a1b-141">1</span><span class="sxs-lookup"><span data-stu-id="80a1b-141">1</span></span>     | <span data-ttu-id="80a1b-142">/App1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="80a1b-142">/app1/ifd/gps/{ushort=8}</span></span> |
| <span data-ttu-id="80a1b-143">2</span><span class="sxs-lookup"><span data-stu-id="80a1b-143">2</span></span>     | <span data-ttu-id="80a1b-144">/xmp/exif:gpssatellites</span><span class="sxs-lookup"><span data-stu-id="80a1b-144">/xmp/exif:gpssatellites</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="80a1b-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="80a1b-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="80a1b-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="80a1b-146">Read Paths</span></span>



| <span data-ttu-id="80a1b-147">JSON</span><span class="sxs-lookup"><span data-stu-id="80a1b-147">Order</span></span> | <span data-ttu-id="80a1b-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="80a1b-148">Path</span></span>                        | <span data-ttu-id="80a1b-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="80a1b-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="80a1b-150">1</span><span class="sxs-lookup"><span data-stu-id="80a1b-150">1</span></span>     | <span data-ttu-id="80a1b-151">/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="80a1b-151">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="80a1b-152">ascii</span><span class="sxs-lookup"><span data-stu-id="80a1b-152">ascii</span></span>       |
| <span data-ttu-id="80a1b-153">2</span><span class="sxs-lookup"><span data-stu-id="80a1b-153">2</span></span>     | <span data-ttu-id="80a1b-154">/ifd/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="80a1b-154">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="80a1b-155">unicode</span><span class="sxs-lookup"><span data-stu-id="80a1b-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="80a1b-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="80a1b-156">Write Paths</span></span>



| <span data-ttu-id="80a1b-157">JSON</span><span class="sxs-lookup"><span data-stu-id="80a1b-157">Order</span></span> | <span data-ttu-id="80a1b-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="80a1b-158">Path</span></span>                        | <span data-ttu-id="80a1b-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="80a1b-159">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="80a1b-160">1</span><span class="sxs-lookup"><span data-stu-id="80a1b-160">1</span></span>     | <span data-ttu-id="80a1b-161">/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="80a1b-161">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="80a1b-162">ascii</span><span class="sxs-lookup"><span data-stu-id="80a1b-162">ascii</span></span>       |
| <span data-ttu-id="80a1b-163">2</span><span class="sxs-lookup"><span data-stu-id="80a1b-163">2</span></span>     | <span data-ttu-id="80a1b-164">/ifd/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="80a1b-164">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="80a1b-165">unicode</span><span class="sxs-lookup"><span data-stu-id="80a1b-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="80a1b-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="80a1b-166">Remove Paths</span></span>



| <span data-ttu-id="80a1b-167">JSON</span><span class="sxs-lookup"><span data-stu-id="80a1b-167">Order</span></span> | <span data-ttu-id="80a1b-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="80a1b-168">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="80a1b-169">1</span><span class="sxs-lookup"><span data-stu-id="80a1b-169">1</span></span>     | <span data-ttu-id="80a1b-170">/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="80a1b-170">/ifd/gps/{ushort=8}</span></span>         |
| <span data-ttu-id="80a1b-171">2</span><span class="sxs-lookup"><span data-stu-id="80a1b-171">2</span></span>     | <span data-ttu-id="80a1b-172">/ifd/xmp/exif:gpssatellites</span><span class="sxs-lookup"><span data-stu-id="80a1b-172">/ifd/xmp/exif:gpssatellites</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="80a1b-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="80a1b-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="80a1b-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80a1b-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80a1b-175">System. GPS. Satellites</span><span class="sxs-lookup"><span data-stu-id="80a1b-175">System.GPS.Satellites</span></span>](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
