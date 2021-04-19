---
description: Criteri per i metadati delle foto per la proprietà System. GPS. ImgDirection.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: Criteri per i metadati delle foto di System. GPS. ImgDirection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013edd632f98f1359c4f3c04856b0409c70eaa56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317872"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a><span data-ttu-id="3580d-103">Criteri per i metadati delle foto di System. GPS. ImgDirection</span><span class="sxs-lookup"><span data-stu-id="3580d-103">System.GPS.ImgDirection Photo Metadata Policy</span></span>

<span data-ttu-id="3580d-104">Criteri per i metadati delle foto per la proprietà [System. GPS. ImgDirection](../properties/props-system-gps-imgdirection.md) .</span><span class="sxs-lookup"><span data-stu-id="3580d-104">The photo metadata policy for the [System.GPS.ImgDirection](../properties/props-system-gps-imgdirection.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3580d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3580d-105">PKEY</span></span>

<span data-ttu-id="3580d-106">PKEY \_ GPS \_ ImgDirection</span><span class="sxs-lookup"><span data-stu-id="3580d-106">PKEY\_GPS\_ImgDirection</span></span>

### <a name="containers"></a><span data-ttu-id="3580d-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="3580d-107">Containers</span></span>

<span data-ttu-id="3580d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3580d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3580d-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="3580d-109">Read-Only</span></span>

<span data-ttu-id="3580d-110">Sì</span><span class="sxs-lookup"><span data-stu-id="3580d-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3580d-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="3580d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3580d-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="3580d-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3580d-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="3580d-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="3580d-114">Questo valore può essere scritto scrivendo in System. GPS. ImgDirectionNumerator e System. GPS. ImgDirectionDenominator.</span><span class="sxs-lookup"><span data-stu-id="3580d-114">This value can be written by writing to System.GPS.ImgDirectionNumerator and System.GPS.ImgDirectionDenominator.</span></span> <span data-ttu-id="3580d-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="3580d-115">It cannot be written directly.</span></span> <span data-ttu-id="3580d-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="3580d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="3580d-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="3580d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3580d-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="3580d-118">Read Paths</span></span>



| <span data-ttu-id="3580d-119">JSON</span><span class="sxs-lookup"><span data-stu-id="3580d-119">Order</span></span> | <span data-ttu-id="3580d-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="3580d-120">Path</span></span>                      | <span data-ttu-id="3580d-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="3580d-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3580d-122">1</span><span class="sxs-lookup"><span data-stu-id="3580d-122">1</span></span>     | <span data-ttu-id="3580d-123">/App1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="3580d-123">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="3580d-124">2</span><span class="sxs-lookup"><span data-stu-id="3580d-124">2</span></span>     | <span data-ttu-id="3580d-125">/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="3580d-125">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="3580d-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="3580d-126">Write Paths</span></span>



| <span data-ttu-id="3580d-127">JSON</span><span class="sxs-lookup"><span data-stu-id="3580d-127">Order</span></span> | <span data-ttu-id="3580d-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="3580d-128">Path</span></span>                      | <span data-ttu-id="3580d-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="3580d-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3580d-130">1</span><span class="sxs-lookup"><span data-stu-id="3580d-130">1</span></span>     | <span data-ttu-id="3580d-131">/App1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="3580d-131">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="3580d-132">2</span><span class="sxs-lookup"><span data-stu-id="3580d-132">2</span></span>     | <span data-ttu-id="3580d-133">/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="3580d-133">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="3580d-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="3580d-134">Remove Paths</span></span>



| <span data-ttu-id="3580d-135">JSON</span><span class="sxs-lookup"><span data-stu-id="3580d-135">Order</span></span> | <span data-ttu-id="3580d-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="3580d-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="3580d-137">1</span><span class="sxs-lookup"><span data-stu-id="3580d-137">1</span></span>     | <span data-ttu-id="3580d-138">/App1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="3580d-138">/app1/ifd/gps/{ushort=17}</span></span> |
| <span data-ttu-id="3580d-139">2</span><span class="sxs-lookup"><span data-stu-id="3580d-139">2</span></span>     | <span data-ttu-id="3580d-140">/xmp/exif:gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="3580d-140">/xmp/exif:gpsimgdirection</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="3580d-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="3580d-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3580d-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="3580d-142">Read Paths</span></span>



| <span data-ttu-id="3580d-143">JSON</span><span class="sxs-lookup"><span data-stu-id="3580d-143">Order</span></span> | <span data-ttu-id="3580d-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="3580d-144">Path</span></span>                          | <span data-ttu-id="3580d-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="3580d-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="3580d-146">1</span><span class="sxs-lookup"><span data-stu-id="3580d-146">1</span></span>     | <span data-ttu-id="3580d-147">/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="3580d-147">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="3580d-148">2</span><span class="sxs-lookup"><span data-stu-id="3580d-148">2</span></span>     | <span data-ttu-id="3580d-149">/ifd/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="3580d-149">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="3580d-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="3580d-150">Write Paths</span></span>



| <span data-ttu-id="3580d-151">JSON</span><span class="sxs-lookup"><span data-stu-id="3580d-151">Order</span></span> | <span data-ttu-id="3580d-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="3580d-152">Path</span></span>                          | <span data-ttu-id="3580d-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="3580d-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="3580d-154">1</span><span class="sxs-lookup"><span data-stu-id="3580d-154">1</span></span>     | <span data-ttu-id="3580d-155">/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="3580d-155">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="3580d-156">2</span><span class="sxs-lookup"><span data-stu-id="3580d-156">2</span></span>     | <span data-ttu-id="3580d-157">/ifd/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="3580d-157">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="3580d-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="3580d-158">Remove Paths</span></span>



| <span data-ttu-id="3580d-159">JSON</span><span class="sxs-lookup"><span data-stu-id="3580d-159">Order</span></span> | <span data-ttu-id="3580d-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="3580d-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="3580d-161">1</span><span class="sxs-lookup"><span data-stu-id="3580d-161">1</span></span>     | <span data-ttu-id="3580d-162">/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="3580d-162">/ifd/gps/{ushort=17}</span></span>          |
| <span data-ttu-id="3580d-163">2</span><span class="sxs-lookup"><span data-stu-id="3580d-163">2</span></span>     | <span data-ttu-id="3580d-164">/ifd/xmp/exif:gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="3580d-164">/ifd/xmp/exif:gpsimgdirection</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3580d-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="3580d-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3580d-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3580d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3580d-167">System. GPS. ImgDirection</span><span class="sxs-lookup"><span data-stu-id="3580d-167">System.GPS.ImgDirection</span></span>](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
