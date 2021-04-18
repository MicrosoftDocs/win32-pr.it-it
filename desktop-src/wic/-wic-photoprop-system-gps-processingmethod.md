---
description: Criteri per i metadati delle foto per la proprietà System. GPS. ProcessingMethod.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: Criteri per i metadati delle foto di System. GPS. ProcessingMethod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319109"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a><span data-ttu-id="947f6-103">Criteri per i metadati delle foto di System. GPS. ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="947f6-103">System.GPS.ProcessingMethod Photo Metadata Policy</span></span>

<span data-ttu-id="947f6-104">Criteri per i metadati delle foto per la proprietà [System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="947f6-104">The photo metadata policy for the [System.GPS.ProcessingMethod](../properties/props-system-gps-processingmethod.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="947f6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="947f6-105">PKEY</span></span>

<span data-ttu-id="947f6-106">PKEY \_ GPS \_ ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="947f6-106">PKEY\_GPS\_ProcessingMethod</span></span>

### <a name="containers"></a><span data-ttu-id="947f6-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="947f6-107">Containers</span></span>

<span data-ttu-id="947f6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="947f6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="947f6-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="947f6-109">Read-Only</span></span>

<span data-ttu-id="947f6-110">No</span><span class="sxs-lookup"><span data-stu-id="947f6-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="947f6-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="947f6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="947f6-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="947f6-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="947f6-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="947f6-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="947f6-114">VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="947f6-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="947f6-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="947f6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="947f6-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="947f6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="947f6-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="947f6-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="947f6-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="947f6-118">Read Paths</span></span>



| <span data-ttu-id="947f6-119">JSON</span><span class="sxs-lookup"><span data-stu-id="947f6-119">Order</span></span> | <span data-ttu-id="947f6-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="947f6-120">Path</span></span>                          | <span data-ttu-id="947f6-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="947f6-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="947f6-122">1</span><span class="sxs-lookup"><span data-stu-id="947f6-122">1</span></span>     | <span data-ttu-id="947f6-123">/App1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="947f6-123">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="947f6-124">2</span><span class="sxs-lookup"><span data-stu-id="947f6-124">2</span></span>     | <span data-ttu-id="947f6-125">/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="947f6-125">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="947f6-126">unicode</span><span class="sxs-lookup"><span data-stu-id="947f6-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="947f6-127">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="947f6-127">Write Paths</span></span>



| <span data-ttu-id="947f6-128">JSON</span><span class="sxs-lookup"><span data-stu-id="947f6-128">Order</span></span> | <span data-ttu-id="947f6-129">Percorso</span><span class="sxs-lookup"><span data-stu-id="947f6-129">Path</span></span>                          | <span data-ttu-id="947f6-130">Formato disco</span><span class="sxs-lookup"><span data-stu-id="947f6-130">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="947f6-131">1</span><span class="sxs-lookup"><span data-stu-id="947f6-131">1</span></span>     | <span data-ttu-id="947f6-132">/App1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="947f6-132">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="947f6-133">2</span><span class="sxs-lookup"><span data-stu-id="947f6-133">2</span></span>     | <span data-ttu-id="947f6-134">/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="947f6-134">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="947f6-135">unicode</span><span class="sxs-lookup"><span data-stu-id="947f6-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="947f6-136">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="947f6-136">Remove Paths</span></span>



| <span data-ttu-id="947f6-137">JSON</span><span class="sxs-lookup"><span data-stu-id="947f6-137">Order</span></span> | <span data-ttu-id="947f6-138">Percorso</span><span class="sxs-lookup"><span data-stu-id="947f6-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="947f6-139">1</span><span class="sxs-lookup"><span data-stu-id="947f6-139">1</span></span>     | <span data-ttu-id="947f6-140">/App1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="947f6-140">/app1/ifd/gps/{ushort=27}</span></span>     |
| <span data-ttu-id="947f6-141">2</span><span class="sxs-lookup"><span data-stu-id="947f6-141">2</span></span>     | <span data-ttu-id="947f6-142">/xmp/exif:gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="947f6-142">/xmp/exif:gpsprocessingmethod</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="947f6-143">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="947f6-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="947f6-144">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="947f6-144">Read Paths</span></span>



| <span data-ttu-id="947f6-145">JSON</span><span class="sxs-lookup"><span data-stu-id="947f6-145">Order</span></span> | <span data-ttu-id="947f6-146">Percorso</span><span class="sxs-lookup"><span data-stu-id="947f6-146">Path</span></span>                              | <span data-ttu-id="947f6-147">Formato disco</span><span class="sxs-lookup"><span data-stu-id="947f6-147">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="947f6-148">1</span><span class="sxs-lookup"><span data-stu-id="947f6-148">1</span></span>     | <span data-ttu-id="947f6-149">/ifd/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="947f6-149">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="947f6-150">unicode</span><span class="sxs-lookup"><span data-stu-id="947f6-150">unicode</span></span>     |
| <span data-ttu-id="947f6-151">2</span><span class="sxs-lookup"><span data-stu-id="947f6-151">2</span></span>     | <span data-ttu-id="947f6-152">/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="947f6-152">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="write-paths"></a><span data-ttu-id="947f6-153">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="947f6-153">Write Paths</span></span>



| <span data-ttu-id="947f6-154">JSON</span><span class="sxs-lookup"><span data-stu-id="947f6-154">Order</span></span> | <span data-ttu-id="947f6-155">Percorso</span><span class="sxs-lookup"><span data-stu-id="947f6-155">Path</span></span>                              | <span data-ttu-id="947f6-156">Formato disco</span><span class="sxs-lookup"><span data-stu-id="947f6-156">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="947f6-157">1</span><span class="sxs-lookup"><span data-stu-id="947f6-157">1</span></span>     | <span data-ttu-id="947f6-158">/ifd/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="947f6-158">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="947f6-159">unicode</span><span class="sxs-lookup"><span data-stu-id="947f6-159">unicode</span></span>     |
| <span data-ttu-id="947f6-160">2</span><span class="sxs-lookup"><span data-stu-id="947f6-160">2</span></span>     | <span data-ttu-id="947f6-161">/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="947f6-161">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="remove-paths"></a><span data-ttu-id="947f6-162">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="947f6-162">Remove Paths</span></span>



| <span data-ttu-id="947f6-163">JSON</span><span class="sxs-lookup"><span data-stu-id="947f6-163">Order</span></span> | <span data-ttu-id="947f6-164">Percorso</span><span class="sxs-lookup"><span data-stu-id="947f6-164">Path</span></span>                              |
|-------|-----------------------------------|
| <span data-ttu-id="947f6-165">1</span><span class="sxs-lookup"><span data-stu-id="947f6-165">1</span></span>     | <span data-ttu-id="947f6-166">/ifd/xmp/exif:gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="947f6-166">/ifd/xmp/exif:gpsprocessingmethod</span></span> |
| <span data-ttu-id="947f6-167">2</span><span class="sxs-lookup"><span data-stu-id="947f6-167">2</span></span>     | <span data-ttu-id="947f6-168">/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="947f6-168">/ifd/gps/{ushort=27}</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="947f6-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="947f6-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="947f6-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="947f6-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="947f6-171">System. GPS. ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="947f6-171">System.GPS.ProcessingMethod</span></span>](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
