---
description: Criteri per i metadati delle foto per la proprietà System. GPS. ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Criteri per i metadati delle foto di System. GPS. ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233535"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a><span data-ttu-id="02134-103">Criteri per i metadati delle foto di System. GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="02134-103">System.GPS.ImgDirectionRef Photo Metadata Policy</span></span>

<span data-ttu-id="02134-104">Criteri per i metadati delle foto per la proprietà [System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) .</span><span class="sxs-lookup"><span data-stu-id="02134-104">The photo metadata policy for the [System.GPS.ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="02134-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="02134-105">PKEY</span></span>

<span data-ttu-id="02134-106">PKEY \_ GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="02134-106">PKEY\_GPS.ImgDirectionRef</span></span>

### <a name="containers"></a><span data-ttu-id="02134-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="02134-107">Containers</span></span>

<span data-ttu-id="02134-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="02134-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="02134-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="02134-109">Read-Only</span></span>

<span data-ttu-id="02134-110">No</span><span class="sxs-lookup"><span data-stu-id="02134-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="02134-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="02134-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="02134-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="02134-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="02134-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="02134-113">Input Type</span></span>

<span data-ttu-id="02134-114">VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="02134-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="02134-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="02134-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="02134-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="02134-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="02134-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="02134-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="02134-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="02134-118">Read Paths</span></span>



| <span data-ttu-id="02134-119">JSON</span><span class="sxs-lookup"><span data-stu-id="02134-119">Order</span></span> | <span data-ttu-id="02134-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="02134-120">Path</span></span>                         | <span data-ttu-id="02134-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="02134-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="02134-122">1</span><span class="sxs-lookup"><span data-stu-id="02134-122">1</span></span>     | <span data-ttu-id="02134-123">/App1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="02134-123">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="02134-124">ascii</span><span class="sxs-lookup"><span data-stu-id="02134-124">ascii</span></span>       |
| <span data-ttu-id="02134-125">2</span><span class="sxs-lookup"><span data-stu-id="02134-125">2</span></span>     | <span data-ttu-id="02134-126">/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="02134-126">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="02134-127">unicode</span><span class="sxs-lookup"><span data-stu-id="02134-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="02134-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="02134-128">Write Paths</span></span>



| <span data-ttu-id="02134-129">JSON</span><span class="sxs-lookup"><span data-stu-id="02134-129">Order</span></span> | <span data-ttu-id="02134-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="02134-130">Path</span></span>                         | <span data-ttu-id="02134-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="02134-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="02134-132">1</span><span class="sxs-lookup"><span data-stu-id="02134-132">1</span></span>     | <span data-ttu-id="02134-133">/App1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="02134-133">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="02134-134">ascii</span><span class="sxs-lookup"><span data-stu-id="02134-134">ascii</span></span>       |
| <span data-ttu-id="02134-135">2</span><span class="sxs-lookup"><span data-stu-id="02134-135">2</span></span>     | <span data-ttu-id="02134-136">/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="02134-136">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="02134-137">unicode</span><span class="sxs-lookup"><span data-stu-id="02134-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="02134-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="02134-138">Remove Paths</span></span>



| <span data-ttu-id="02134-139">JSON</span><span class="sxs-lookup"><span data-stu-id="02134-139">Order</span></span> | <span data-ttu-id="02134-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="02134-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="02134-141">1</span><span class="sxs-lookup"><span data-stu-id="02134-141">1</span></span>     | <span data-ttu-id="02134-142">/App1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="02134-142">/app1/ifd/gps/{ushort=16}</span></span>    |
| <span data-ttu-id="02134-143">2</span><span class="sxs-lookup"><span data-stu-id="02134-143">2</span></span>     | <span data-ttu-id="02134-144">/xmp/exif:gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="02134-144">/xmp/exif:gpsimgdirectionref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="02134-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="02134-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="02134-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="02134-146">Read Paths</span></span>



| <span data-ttu-id="02134-147">JSON</span><span class="sxs-lookup"><span data-stu-id="02134-147">Order</span></span> | <span data-ttu-id="02134-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="02134-148">Path</span></span>                             | <span data-ttu-id="02134-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="02134-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="02134-150">1</span><span class="sxs-lookup"><span data-stu-id="02134-150">1</span></span>     | <span data-ttu-id="02134-151">/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="02134-151">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="02134-152">ascii</span><span class="sxs-lookup"><span data-stu-id="02134-152">ascii</span></span>       |
| <span data-ttu-id="02134-153">2</span><span class="sxs-lookup"><span data-stu-id="02134-153">2</span></span>     | <span data-ttu-id="02134-154">/ifd/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="02134-154">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="02134-155">unicode</span><span class="sxs-lookup"><span data-stu-id="02134-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="02134-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="02134-156">Write Paths</span></span>



| <span data-ttu-id="02134-157">JSON</span><span class="sxs-lookup"><span data-stu-id="02134-157">Order</span></span> | <span data-ttu-id="02134-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="02134-158">Path</span></span>                             | <span data-ttu-id="02134-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="02134-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="02134-160">1</span><span class="sxs-lookup"><span data-stu-id="02134-160">1</span></span>     | <span data-ttu-id="02134-161">/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="02134-161">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="02134-162">ascii</span><span class="sxs-lookup"><span data-stu-id="02134-162">ascii</span></span>       |
| <span data-ttu-id="02134-163">2</span><span class="sxs-lookup"><span data-stu-id="02134-163">2</span></span>     | <span data-ttu-id="02134-164">/ifd/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="02134-164">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="02134-165">unicode</span><span class="sxs-lookup"><span data-stu-id="02134-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="02134-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="02134-166">Remove Paths</span></span>



| <span data-ttu-id="02134-167">JSON</span><span class="sxs-lookup"><span data-stu-id="02134-167">Order</span></span> | <span data-ttu-id="02134-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="02134-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="02134-169">1</span><span class="sxs-lookup"><span data-stu-id="02134-169">1</span></span>     | <span data-ttu-id="02134-170">/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="02134-170">/ifd/gps/{ushort=16}</span></span>             |
| <span data-ttu-id="02134-171">2</span><span class="sxs-lookup"><span data-stu-id="02134-171">2</span></span>     | <span data-ttu-id="02134-172">/ifd/xmp/exif:gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="02134-172">/ifd/xmp/exif:gpsimgdirectionref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="02134-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="02134-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="02134-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02134-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02134-175">System. GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="02134-175">System.GPS.ImgDirectionRef</span></span>](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
