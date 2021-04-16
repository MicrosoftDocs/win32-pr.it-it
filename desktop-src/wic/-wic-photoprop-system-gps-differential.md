---
description: Criteri per i metadati delle foto per la proprietà System. GPS. differenziale.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: Criteri di metadati della foto System. GPS. differenziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348576"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a><span data-ttu-id="cfd09-103">Criteri di metadati della foto System. GPS. differenziale</span><span class="sxs-lookup"><span data-stu-id="cfd09-103">System.GPS.Differential Photo Metadata Policy</span></span>

<span data-ttu-id="cfd09-104">Criteri per i metadati delle foto per la proprietà [System. GPS. differenziale](../properties/props-system-gps-differential.md) .</span><span class="sxs-lookup"><span data-stu-id="cfd09-104">The photo metadata policy for the [System.GPS.Differential](../properties/props-system-gps-differential.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="cfd09-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="cfd09-105">PKEY</span></span>

<span data-ttu-id="cfd09-106">\_ \_ Differenziale GPS pkey</span><span class="sxs-lookup"><span data-stu-id="cfd09-106">PKEY\_GPS\_Differential</span></span>

### <a name="containers"></a><span data-ttu-id="cfd09-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="cfd09-107">Containers</span></span>

<span data-ttu-id="cfd09-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="cfd09-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="cfd09-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="cfd09-109">Read-Only</span></span>

<span data-ttu-id="cfd09-110">No</span><span class="sxs-lookup"><span data-stu-id="cfd09-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="cfd09-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="cfd09-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="cfd09-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="cfd09-112">VT\_UI2</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="cfd09-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="cfd09-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="cfd09-114">VT \_ Ui1, VT \_ UI2 e VT \_ UI4 sono tutti accettati.</span><span class="sxs-lookup"><span data-stu-id="cfd09-114">VT\_UI1, VT\_UI2, and VT\_UI4 are all accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="cfd09-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="cfd09-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="cfd09-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="cfd09-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="cfd09-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="cfd09-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="cfd09-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="cfd09-118">Read Paths</span></span>



| <span data-ttu-id="cfd09-119">JSON</span><span class="sxs-lookup"><span data-stu-id="cfd09-119">Order</span></span> | <span data-ttu-id="cfd09-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="cfd09-120">Path</span></span>                      | <span data-ttu-id="cfd09-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="cfd09-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="cfd09-122">1</span><span class="sxs-lookup"><span data-stu-id="cfd09-122">1</span></span>     | <span data-ttu-id="cfd09-123">/App1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="cfd09-123">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="cfd09-124">ushort</span><span class="sxs-lookup"><span data-stu-id="cfd09-124">ushort</span></span>      |
| <span data-ttu-id="cfd09-125">2</span><span class="sxs-lookup"><span data-stu-id="cfd09-125">2</span></span>     | <span data-ttu-id="cfd09-126">/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="cfd09-126">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="cfd09-127">unicode</span><span class="sxs-lookup"><span data-stu-id="cfd09-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="cfd09-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="cfd09-128">Write Paths</span></span>



| <span data-ttu-id="cfd09-129">JSON</span><span class="sxs-lookup"><span data-stu-id="cfd09-129">Order</span></span> | <span data-ttu-id="cfd09-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="cfd09-130">Path</span></span>                      | <span data-ttu-id="cfd09-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="cfd09-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="cfd09-132">1</span><span class="sxs-lookup"><span data-stu-id="cfd09-132">1</span></span>     | <span data-ttu-id="cfd09-133">/App1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="cfd09-133">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="cfd09-134">ushort</span><span class="sxs-lookup"><span data-stu-id="cfd09-134">ushort</span></span>      |
| <span data-ttu-id="cfd09-135">2</span><span class="sxs-lookup"><span data-stu-id="cfd09-135">2</span></span>     | <span data-ttu-id="cfd09-136">/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="cfd09-136">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="cfd09-137">unicode</span><span class="sxs-lookup"><span data-stu-id="cfd09-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="cfd09-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="cfd09-138">Remove Paths</span></span>



| <span data-ttu-id="cfd09-139">JSON</span><span class="sxs-lookup"><span data-stu-id="cfd09-139">Order</span></span> | <span data-ttu-id="cfd09-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="cfd09-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="cfd09-141">1</span><span class="sxs-lookup"><span data-stu-id="cfd09-141">1</span></span>     | <span data-ttu-id="cfd09-142">/App1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="cfd09-142">/app1/ifd/gps/{ushort=30}</span></span> |
| <span data-ttu-id="cfd09-143">2</span><span class="sxs-lookup"><span data-stu-id="cfd09-143">2</span></span>     | <span data-ttu-id="cfd09-144">/xmp/exif:gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="cfd09-144">/xmp/exif:gpsdifferential</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="cfd09-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="cfd09-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="cfd09-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="cfd09-146">Read Paths</span></span>



| <span data-ttu-id="cfd09-147">JSON</span><span class="sxs-lookup"><span data-stu-id="cfd09-147">Order</span></span> | <span data-ttu-id="cfd09-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="cfd09-148">Path</span></span>                          | <span data-ttu-id="cfd09-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="cfd09-149">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="cfd09-150">1</span><span class="sxs-lookup"><span data-stu-id="cfd09-150">1</span></span>     | <span data-ttu-id="cfd09-151">/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="cfd09-151">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="cfd09-152">ushort</span><span class="sxs-lookup"><span data-stu-id="cfd09-152">ushort</span></span>      |
| <span data-ttu-id="cfd09-153">2</span><span class="sxs-lookup"><span data-stu-id="cfd09-153">2</span></span>     | <span data-ttu-id="cfd09-154">/ifd/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="cfd09-154">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="cfd09-155">unicode</span><span class="sxs-lookup"><span data-stu-id="cfd09-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="cfd09-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="cfd09-156">Write Paths</span></span>



| <span data-ttu-id="cfd09-157">JSON</span><span class="sxs-lookup"><span data-stu-id="cfd09-157">Order</span></span> | <span data-ttu-id="cfd09-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="cfd09-158">Path</span></span>                          | <span data-ttu-id="cfd09-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="cfd09-159">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="cfd09-160">1</span><span class="sxs-lookup"><span data-stu-id="cfd09-160">1</span></span>     | <span data-ttu-id="cfd09-161">/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="cfd09-161">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="cfd09-162">ushort</span><span class="sxs-lookup"><span data-stu-id="cfd09-162">ushort</span></span>      |
| <span data-ttu-id="cfd09-163">2</span><span class="sxs-lookup"><span data-stu-id="cfd09-163">2</span></span>     | <span data-ttu-id="cfd09-164">/ifd/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="cfd09-164">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="cfd09-165">unicode</span><span class="sxs-lookup"><span data-stu-id="cfd09-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="cfd09-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="cfd09-166">Remove Paths</span></span>



| <span data-ttu-id="cfd09-167">JSON</span><span class="sxs-lookup"><span data-stu-id="cfd09-167">Order</span></span> | <span data-ttu-id="cfd09-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="cfd09-168">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="cfd09-169">1</span><span class="sxs-lookup"><span data-stu-id="cfd09-169">1</span></span>     | <span data-ttu-id="cfd09-170">/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="cfd09-170">/ifd/gps/{ushort=30}</span></span>          |
| <span data-ttu-id="cfd09-171">2</span><span class="sxs-lookup"><span data-stu-id="cfd09-171">2</span></span>     | <span data-ttu-id="cfd09-172">/ifd/xmp/exif:gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="cfd09-172">/ifd/xmp/exif:gpsdifferential</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cfd09-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfd09-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfd09-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cfd09-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfd09-175">System. GPS. differenziale</span><span class="sxs-lookup"><span data-stu-id="cfd09-175">System.GPS.Differential</span></span>](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
