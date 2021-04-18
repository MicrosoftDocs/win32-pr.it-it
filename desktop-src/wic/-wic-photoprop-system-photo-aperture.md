---
description: Criteri per i metadati delle foto per la proprietà System. Photo. aperture.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: Criteri per i metadati di Photo System. Photo. aperture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317251"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a><span data-ttu-id="05959-103">Criteri per i metadati di Photo System. Photo. aperture</span><span class="sxs-lookup"><span data-stu-id="05959-103">System.Photo.Aperture Photo Metadata Policy</span></span>

<span data-ttu-id="05959-104">Criteri per i metadati delle foto per la proprietà [System. Photo. aperture](../properties/props-system-photo-aperture.md) .</span><span class="sxs-lookup"><span data-stu-id="05959-104">The photo metadata policy for the [System.Photo.Aperture](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="05959-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="05959-105">PKEY</span></span>

<span data-ttu-id="05959-106">\_Apertura foto \_ pkey</span><span class="sxs-lookup"><span data-stu-id="05959-106">PKEY\_Photo\_Aperture</span></span>

### <a name="containers"></a><span data-ttu-id="05959-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="05959-107">Containers</span></span>

<span data-ttu-id="05959-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="05959-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="05959-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="05959-109">Read-Only</span></span>

<span data-ttu-id="05959-110">Sì</span><span class="sxs-lookup"><span data-stu-id="05959-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="05959-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="05959-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="05959-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="05959-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="05959-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="05959-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="05959-114">Questo valore viene generato da System. Photo. ApertureNumerator e System. Photo. ApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="05959-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="05959-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="05959-115">It cannot be written directly.</span></span> <span data-ttu-id="05959-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="05959-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="05959-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="05959-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="05959-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="05959-118">Read Paths</span></span>



| <span data-ttu-id="05959-119">JSON</span><span class="sxs-lookup"><span data-stu-id="05959-119">Order</span></span> | <span data-ttu-id="05959-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="05959-120">Path</span></span>                          | <span data-ttu-id="05959-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="05959-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="05959-122">1</span><span class="sxs-lookup"><span data-stu-id="05959-122">1</span></span>     | <span data-ttu-id="05959-123">/App1/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="05959-123">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="05959-124">2</span><span class="sxs-lookup"><span data-stu-id="05959-124">2</span></span>     | <span data-ttu-id="05959-125">/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="05959-125">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="write-paths"></a><span data-ttu-id="05959-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="05959-126">Write Paths</span></span>



| <span data-ttu-id="05959-127">JSON</span><span class="sxs-lookup"><span data-stu-id="05959-127">Order</span></span> | <span data-ttu-id="05959-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="05959-128">Path</span></span>                          | <span data-ttu-id="05959-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="05959-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="05959-130">1</span><span class="sxs-lookup"><span data-stu-id="05959-130">1</span></span>     | <span data-ttu-id="05959-131">/App1/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="05959-131">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="05959-132">2</span><span class="sxs-lookup"><span data-stu-id="05959-132">2</span></span>     | <span data-ttu-id="05959-133">/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="05959-133">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="remove-paths"></a><span data-ttu-id="05959-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="05959-134">Remove Paths</span></span>



| <span data-ttu-id="05959-135">JSON</span><span class="sxs-lookup"><span data-stu-id="05959-135">Order</span></span> | <span data-ttu-id="05959-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="05959-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="05959-137">1</span><span class="sxs-lookup"><span data-stu-id="05959-137">1</span></span>     | <span data-ttu-id="05959-138">/App1/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="05959-138">/app1/ifd/exif/{ushort=37378}</span></span> |
| <span data-ttu-id="05959-139">2</span><span class="sxs-lookup"><span data-stu-id="05959-139">2</span></span>     | <span data-ttu-id="05959-140">/xmp/exif:aperturevalue</span><span class="sxs-lookup"><span data-stu-id="05959-140">/xmp/exif:aperturevalue</span></span>       |



 

### <a name="tiff-policies"></a><span data-ttu-id="05959-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="05959-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="05959-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="05959-142">Read Paths</span></span>



| <span data-ttu-id="05959-143">JSON</span><span class="sxs-lookup"><span data-stu-id="05959-143">Order</span></span> | <span data-ttu-id="05959-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="05959-144">Path</span></span>                        | <span data-ttu-id="05959-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="05959-145">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="05959-146">1</span><span class="sxs-lookup"><span data-stu-id="05959-146">1</span></span>     | <span data-ttu-id="05959-147">/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="05959-147">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="05959-148">2</span><span class="sxs-lookup"><span data-stu-id="05959-148">2</span></span>     | <span data-ttu-id="05959-149">/ifd/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="05959-149">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="05959-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="05959-150">Write Paths</span></span>



| <span data-ttu-id="05959-151">JSON</span><span class="sxs-lookup"><span data-stu-id="05959-151">Order</span></span> | <span data-ttu-id="05959-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="05959-152">Path</span></span>                        | <span data-ttu-id="05959-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="05959-153">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="05959-154">1</span><span class="sxs-lookup"><span data-stu-id="05959-154">1</span></span>     | <span data-ttu-id="05959-155">/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="05959-155">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="05959-156">2</span><span class="sxs-lookup"><span data-stu-id="05959-156">2</span></span>     | <span data-ttu-id="05959-157">/ifd/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="05959-157">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="05959-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="05959-158">Remove Paths</span></span>



| <span data-ttu-id="05959-159">JSON</span><span class="sxs-lookup"><span data-stu-id="05959-159">Order</span></span> | <span data-ttu-id="05959-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="05959-160">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="05959-161">1</span><span class="sxs-lookup"><span data-stu-id="05959-161">1</span></span>     | <span data-ttu-id="05959-162">/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="05959-162">/ifd/exif/{ushort=37378}</span></span>    |
| <span data-ttu-id="05959-163">2</span><span class="sxs-lookup"><span data-stu-id="05959-163">2</span></span>     | <span data-ttu-id="05959-164">/ifd/xmp/exif:aperturevalue</span><span class="sxs-lookup"><span data-stu-id="05959-164">/ifd/xmp/exif:aperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="05959-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="05959-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="05959-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="05959-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05959-167">System. Photo. aperture</span><span class="sxs-lookup"><span data-stu-id="05959-167">System.Photo.Aperture</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
