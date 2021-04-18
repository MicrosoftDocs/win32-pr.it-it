---
description: Criteri per i metadati delle foto per la proprietà System. Photo. PhotometricInterpretation.
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: Criteri per i metadati delle foto di System. Photo. PhotometricInterpretation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b371ce9257d526f941f3fdb33949e8788a7112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315965"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a><span data-ttu-id="d4e4e-103">Criteri per i metadati delle foto di System. Photo. PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="d4e4e-103">System.Photo.PhotometricInterpretation Photo Metadata Policy</span></span>

<span data-ttu-id="d4e4e-104">Criteri per i metadati delle foto per la proprietà [System. Photo. PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e4e-104">The photo metadata policy for the [System.Photo.PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d4e4e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d4e4e-105">PKEY</span></span>

<span data-ttu-id="d4e4e-106">PKEY \_ Photo \_ PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="d4e4e-106">PKEY\_Photo\_PhotometricInterpretation</span></span>

### <a name="containers"></a><span data-ttu-id="d4e4e-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="d4e4e-107">Containers</span></span>

<span data-ttu-id="d4e4e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d4e4e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d4e4e-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="d4e4e-109">Read-Only</span></span>

<span data-ttu-id="d4e4e-110">Sì</span><span class="sxs-lookup"><span data-stu-id="d4e4e-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d4e4e-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="d4e4e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d4e4e-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="d4e4e-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="d4e4e-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="d4e4e-113">Input Type</span></span>

<span data-ttu-id="d4e4e-114">UShort</span><span class="sxs-lookup"><span data-stu-id="d4e4e-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d4e4e-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="d4e4e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d4e4e-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="d4e4e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d4e4e-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="d4e4e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d4e4e-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="d4e4e-118">Read Paths</span></span>



| <span data-ttu-id="d4e4e-119">JSON</span><span class="sxs-lookup"><span data-stu-id="d4e4e-119">Order</span></span> | <span data-ttu-id="d4e4e-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="d4e4e-120">Path</span></span>                                | <span data-ttu-id="d4e4e-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d4e4e-121">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="d4e4e-122">1</span><span class="sxs-lookup"><span data-stu-id="d4e4e-122">1</span></span>     | <span data-ttu-id="d4e4e-123">/App1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="d4e4e-123">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="d4e4e-124">ushort</span><span class="sxs-lookup"><span data-stu-id="d4e4e-124">ushort</span></span>      |
| <span data-ttu-id="d4e4e-125">2</span><span class="sxs-lookup"><span data-stu-id="d4e4e-125">2</span></span>     | <span data-ttu-id="d4e4e-126">/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="d4e4e-126">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="d4e4e-127">unicode</span><span class="sxs-lookup"><span data-stu-id="d4e4e-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d4e4e-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="d4e4e-128">Write Paths</span></span>



| <span data-ttu-id="d4e4e-129">JSON</span><span class="sxs-lookup"><span data-stu-id="d4e4e-129">Order</span></span> | <span data-ttu-id="d4e4e-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="d4e4e-130">Path</span></span>                                | <span data-ttu-id="d4e4e-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d4e4e-131">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="d4e4e-132">1</span><span class="sxs-lookup"><span data-stu-id="d4e4e-132">1</span></span>     | <span data-ttu-id="d4e4e-133">/App1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="d4e4e-133">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="d4e4e-134">ushort</span><span class="sxs-lookup"><span data-stu-id="d4e4e-134">ushort</span></span>      |
| <span data-ttu-id="d4e4e-135">2</span><span class="sxs-lookup"><span data-stu-id="d4e4e-135">2</span></span>     | <span data-ttu-id="d4e4e-136">/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="d4e4e-136">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="d4e4e-137">unicode</span><span class="sxs-lookup"><span data-stu-id="d4e4e-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d4e4e-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="d4e4e-138">Remove Paths</span></span>



| <span data-ttu-id="d4e4e-139">JSON</span><span class="sxs-lookup"><span data-stu-id="d4e4e-139">Order</span></span> | <span data-ttu-id="d4e4e-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="d4e4e-140">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="d4e4e-141">1</span><span class="sxs-lookup"><span data-stu-id="d4e4e-141">1</span></span>     | <span data-ttu-id="d4e4e-142">/App1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="d4e4e-142">/app1/ifd/{ushort=262}</span></span>              |
| <span data-ttu-id="d4e4e-143">2</span><span class="sxs-lookup"><span data-stu-id="d4e4e-143">2</span></span>     | <span data-ttu-id="d4e4e-144">/xmp/tiff:photometricinterpretation</span><span class="sxs-lookup"><span data-stu-id="d4e4e-144">/xmp/tiff:photometricinterpretation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="d4e4e-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="d4e4e-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d4e4e-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="d4e4e-146">Read Paths</span></span>



| <span data-ttu-id="d4e4e-147">JSON</span><span class="sxs-lookup"><span data-stu-id="d4e4e-147">Order</span></span> | <span data-ttu-id="d4e4e-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="d4e4e-148">Path</span></span>                                    | <span data-ttu-id="d4e4e-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d4e4e-149">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="d4e4e-150">1</span><span class="sxs-lookup"><span data-stu-id="d4e4e-150">1</span></span>     | <span data-ttu-id="d4e4e-151">/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="d4e4e-151">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="d4e4e-152">ushort</span><span class="sxs-lookup"><span data-stu-id="d4e4e-152">ushort</span></span>      |
| <span data-ttu-id="d4e4e-153">2</span><span class="sxs-lookup"><span data-stu-id="d4e4e-153">2</span></span>     | <span data-ttu-id="d4e4e-154">/ifd/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="d4e4e-154">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="d4e4e-155">unicode</span><span class="sxs-lookup"><span data-stu-id="d4e4e-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d4e4e-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="d4e4e-156">Write Paths</span></span>



| <span data-ttu-id="d4e4e-157">JSON</span><span class="sxs-lookup"><span data-stu-id="d4e4e-157">Order</span></span> | <span data-ttu-id="d4e4e-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="d4e4e-158">Path</span></span>                                    | <span data-ttu-id="d4e4e-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="d4e4e-159">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="d4e4e-160">1</span><span class="sxs-lookup"><span data-stu-id="d4e4e-160">1</span></span>     | <span data-ttu-id="d4e4e-161">/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="d4e4e-161">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="d4e4e-162">ushort</span><span class="sxs-lookup"><span data-stu-id="d4e4e-162">ushort</span></span>      |
| <span data-ttu-id="d4e4e-163">2</span><span class="sxs-lookup"><span data-stu-id="d4e4e-163">2</span></span>     | <span data-ttu-id="d4e4e-164">/ifd/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="d4e4e-164">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="d4e4e-165">unicode</span><span class="sxs-lookup"><span data-stu-id="d4e4e-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d4e4e-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="d4e4e-166">Remove Paths</span></span>



| <span data-ttu-id="d4e4e-167">JSON</span><span class="sxs-lookup"><span data-stu-id="d4e4e-167">Order</span></span> | <span data-ttu-id="d4e4e-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="d4e4e-168">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="d4e4e-169">1</span><span class="sxs-lookup"><span data-stu-id="d4e4e-169">1</span></span>     | <span data-ttu-id="d4e4e-170">/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="d4e4e-170">/ifd/{ushort=262}</span></span>                       |
| <span data-ttu-id="d4e4e-171">2</span><span class="sxs-lookup"><span data-stu-id="d4e4e-171">2</span></span>     | <span data-ttu-id="d4e4e-172">/ifd/xmp/tiff:photometricinterpretation</span><span class="sxs-lookup"><span data-stu-id="d4e4e-172">/ifd/xmp/tiff:photometricinterpretation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d4e4e-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4e4e-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4e4e-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d4e4e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4e4e-175">System. Photo. PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="d4e4e-175">System.Photo.PhotometricInterpretation</span></span>](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
