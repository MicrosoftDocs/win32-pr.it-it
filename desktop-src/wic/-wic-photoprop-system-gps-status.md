---
description: Criteri per i metadati delle foto per la proprietà System. GPS. status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Criteri dei metadati della foto System. GPS. status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac08139a267052f8d6dd3dc463e2a2768309a41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312966"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a><span data-ttu-id="30a7d-103">Criteri dei metadati della foto System. GPS. status</span><span class="sxs-lookup"><span data-stu-id="30a7d-103">System.GPS.Status Photo Metadata Policy</span></span>

<span data-ttu-id="30a7d-104">Criteri per i metadati delle foto per la proprietà [System. GPS. status](../properties/props-system-gps-status.md) .</span><span class="sxs-lookup"><span data-stu-id="30a7d-104">The photo metadata policy for the [System.GPS.Status](../properties/props-system-gps-status.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="30a7d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="30a7d-105">PKEY</span></span>

<span data-ttu-id="30a7d-106">\_Stato pkey GPS \_</span><span class="sxs-lookup"><span data-stu-id="30a7d-106">PKEY\_GPS\_Status</span></span>

### <a name="containers"></a><span data-ttu-id="30a7d-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="30a7d-107">Containers</span></span>

<span data-ttu-id="30a7d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="30a7d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="30a7d-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="30a7d-109">Read-Only</span></span>

<span data-ttu-id="30a7d-110">No</span><span class="sxs-lookup"><span data-stu-id="30a7d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="30a7d-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="30a7d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="30a7d-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="30a7d-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="30a7d-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="30a7d-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="30a7d-114">VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="30a7d-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="30a7d-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="30a7d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="30a7d-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="30a7d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="30a7d-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="30a7d-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="30a7d-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="30a7d-118">Read Paths</span></span>



| <span data-ttu-id="30a7d-119">JSON</span><span class="sxs-lookup"><span data-stu-id="30a7d-119">Order</span></span> | <span data-ttu-id="30a7d-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="30a7d-120">Path</span></span>                     | <span data-ttu-id="30a7d-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="30a7d-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="30a7d-122">1</span><span class="sxs-lookup"><span data-stu-id="30a7d-122">1</span></span>     | <span data-ttu-id="30a7d-123">/App1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="30a7d-123">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="30a7d-124">ascii</span><span class="sxs-lookup"><span data-stu-id="30a7d-124">ascii</span></span>       |
| <span data-ttu-id="30a7d-125">2</span><span class="sxs-lookup"><span data-stu-id="30a7d-125">2</span></span>     | <span data-ttu-id="30a7d-126">/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="30a7d-126">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="30a7d-127">unicode</span><span class="sxs-lookup"><span data-stu-id="30a7d-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="30a7d-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="30a7d-128">Write Paths</span></span>



| <span data-ttu-id="30a7d-129">JSON</span><span class="sxs-lookup"><span data-stu-id="30a7d-129">Order</span></span> | <span data-ttu-id="30a7d-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="30a7d-130">Path</span></span>                     | <span data-ttu-id="30a7d-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="30a7d-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="30a7d-132">1</span><span class="sxs-lookup"><span data-stu-id="30a7d-132">1</span></span>     | <span data-ttu-id="30a7d-133">/App1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="30a7d-133">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="30a7d-134">ascii</span><span class="sxs-lookup"><span data-stu-id="30a7d-134">ascii</span></span>       |
| <span data-ttu-id="30a7d-135">2</span><span class="sxs-lookup"><span data-stu-id="30a7d-135">2</span></span>     | <span data-ttu-id="30a7d-136">/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="30a7d-136">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="30a7d-137">unicode</span><span class="sxs-lookup"><span data-stu-id="30a7d-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="30a7d-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="30a7d-138">Remove Paths</span></span>



| <span data-ttu-id="30a7d-139">JSON</span><span class="sxs-lookup"><span data-stu-id="30a7d-139">Order</span></span> | <span data-ttu-id="30a7d-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="30a7d-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="30a7d-141">1</span><span class="sxs-lookup"><span data-stu-id="30a7d-141">1</span></span>     | <span data-ttu-id="30a7d-142">/App1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="30a7d-142">/app1/ifd/gps/{ushort=9}</span></span> |
| <span data-ttu-id="30a7d-143">2</span><span class="sxs-lookup"><span data-stu-id="30a7d-143">2</span></span>     | <span data-ttu-id="30a7d-144">/xmp/exif:gpsstatus</span><span class="sxs-lookup"><span data-stu-id="30a7d-144">/xmp/exif:gpsstatus</span></span>      |



 

### <a name="tiff-policies"></a><span data-ttu-id="30a7d-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="30a7d-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="30a7d-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="30a7d-146">Read Paths</span></span>



| <span data-ttu-id="30a7d-147">JSON</span><span class="sxs-lookup"><span data-stu-id="30a7d-147">Order</span></span> | <span data-ttu-id="30a7d-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="30a7d-148">Path</span></span>                    | <span data-ttu-id="30a7d-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="30a7d-149">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="30a7d-150">1</span><span class="sxs-lookup"><span data-stu-id="30a7d-150">1</span></span>     | <span data-ttu-id="30a7d-151">/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="30a7d-151">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="30a7d-152">ascii</span><span class="sxs-lookup"><span data-stu-id="30a7d-152">ascii</span></span>       |
| <span data-ttu-id="30a7d-153">2</span><span class="sxs-lookup"><span data-stu-id="30a7d-153">2</span></span>     | <span data-ttu-id="30a7d-154">/ifd/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="30a7d-154">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="30a7d-155">unicode</span><span class="sxs-lookup"><span data-stu-id="30a7d-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="30a7d-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="30a7d-156">Write Paths</span></span>



| <span data-ttu-id="30a7d-157">JSON</span><span class="sxs-lookup"><span data-stu-id="30a7d-157">Order</span></span> | <span data-ttu-id="30a7d-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="30a7d-158">Path</span></span>                    | <span data-ttu-id="30a7d-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="30a7d-159">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="30a7d-160">1</span><span class="sxs-lookup"><span data-stu-id="30a7d-160">1</span></span>     | <span data-ttu-id="30a7d-161">/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="30a7d-161">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="30a7d-162">ascii</span><span class="sxs-lookup"><span data-stu-id="30a7d-162">ascii</span></span>       |
| <span data-ttu-id="30a7d-163">2</span><span class="sxs-lookup"><span data-stu-id="30a7d-163">2</span></span>     | <span data-ttu-id="30a7d-164">/ifd/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="30a7d-164">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="30a7d-165">unicode</span><span class="sxs-lookup"><span data-stu-id="30a7d-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="30a7d-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="30a7d-166">Remove Paths</span></span>



| <span data-ttu-id="30a7d-167">JSON</span><span class="sxs-lookup"><span data-stu-id="30a7d-167">Order</span></span> | <span data-ttu-id="30a7d-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="30a7d-168">Path</span></span>                    |
|-------|-------------------------|
| <span data-ttu-id="30a7d-169">1</span><span class="sxs-lookup"><span data-stu-id="30a7d-169">1</span></span>     | <span data-ttu-id="30a7d-170">/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="30a7d-170">/ifd/gps/{ushort=9}</span></span>     |
| <span data-ttu-id="30a7d-171">2</span><span class="sxs-lookup"><span data-stu-id="30a7d-171">2</span></span>     | <span data-ttu-id="30a7d-172">/ifd/xmp/exif:gpsstatus</span><span class="sxs-lookup"><span data-stu-id="30a7d-172">/ifd/xmp/exif:gpsstatus</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="30a7d-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="30a7d-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="30a7d-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30a7d-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30a7d-175">System. GPS. status</span><span class="sxs-lookup"><span data-stu-id="30a7d-175">System.GPS.Status</span></span>](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
