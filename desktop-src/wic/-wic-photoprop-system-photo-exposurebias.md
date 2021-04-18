---
description: Criteri per i metadati delle foto per la proprietà System. Photo. ExposureBias.
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: Criteri per i metadati delle foto di System. Photo. ExposureBias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314459"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a><span data-ttu-id="657d6-103">Criteri per i metadati delle foto di System. Photo. ExposureBias</span><span class="sxs-lookup"><span data-stu-id="657d6-103">System.Photo.ExposureBias Photo Metadata Policy</span></span>

<span data-ttu-id="657d6-104">Criteri per i metadati delle foto per la proprietà [System. Photo. ExposureBias](../properties/props-system-photo-exposurebias.md) .</span><span class="sxs-lookup"><span data-stu-id="657d6-104">The photo metadata policy for the [System.Photo.ExposureBias](../properties/props-system-photo-exposurebias.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="657d6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="657d6-105">PKEY</span></span>

<span data-ttu-id="657d6-106">PKEY \_ Photo \_ ExposureBias</span><span class="sxs-lookup"><span data-stu-id="657d6-106">PKEY\_Photo\_ExposureBias</span></span>

### <a name="containers"></a><span data-ttu-id="657d6-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="657d6-107">Containers</span></span>

<span data-ttu-id="657d6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="657d6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="657d6-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="657d6-109">Read-Only</span></span>

<span data-ttu-id="657d6-110">Sì</span><span class="sxs-lookup"><span data-stu-id="657d6-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="657d6-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="657d6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="657d6-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="657d6-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="657d6-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="657d6-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="657d6-114">Questo valore viene generato da System. Photo. ExposureBiasNumerator e System. Photo. ExposureBiasDenominator.</span><span class="sxs-lookup"><span data-stu-id="657d6-114">This value is generated from System.Photo.ExposureBiasNumerator and System.Photo.ExposureBiasDenominator.</span></span> <span data-ttu-id="657d6-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="657d6-115">It cannot be written directly.</span></span> <span data-ttu-id="657d6-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="657d6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="657d6-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="657d6-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="657d6-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="657d6-118">Read Paths</span></span>



| <span data-ttu-id="657d6-119">JSON</span><span class="sxs-lookup"><span data-stu-id="657d6-119">Order</span></span> | <span data-ttu-id="657d6-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="657d6-120">Path</span></span>                          | <span data-ttu-id="657d6-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="657d6-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="657d6-122">1</span><span class="sxs-lookup"><span data-stu-id="657d6-122">1</span></span>     | <span data-ttu-id="657d6-123">/App1/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="657d6-123">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="657d6-124">2</span><span class="sxs-lookup"><span data-stu-id="657d6-124">2</span></span>     | <span data-ttu-id="657d6-125">/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="657d6-125">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="657d6-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="657d6-126">Write Paths</span></span>



| <span data-ttu-id="657d6-127">JSON</span><span class="sxs-lookup"><span data-stu-id="657d6-127">Order</span></span> | <span data-ttu-id="657d6-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="657d6-128">Path</span></span>                          | <span data-ttu-id="657d6-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="657d6-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="657d6-130">1</span><span class="sxs-lookup"><span data-stu-id="657d6-130">1</span></span>     | <span data-ttu-id="657d6-131">/App1/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="657d6-131">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="657d6-132">2</span><span class="sxs-lookup"><span data-stu-id="657d6-132">2</span></span>     | <span data-ttu-id="657d6-133">/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="657d6-133">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="657d6-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="657d6-134">Remove Paths</span></span>



| <span data-ttu-id="657d6-135">JSON</span><span class="sxs-lookup"><span data-stu-id="657d6-135">Order</span></span> | <span data-ttu-id="657d6-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="657d6-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="657d6-137">1</span><span class="sxs-lookup"><span data-stu-id="657d6-137">1</span></span>     | <span data-ttu-id="657d6-138">/App1/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="657d6-138">/app1/ifd/exif/{ushort=37380}</span></span> |
| <span data-ttu-id="657d6-139">2</span><span class="sxs-lookup"><span data-stu-id="657d6-139">2</span></span>     | <span data-ttu-id="657d6-140">/xmp/exif:exposurebiasvalue</span><span class="sxs-lookup"><span data-stu-id="657d6-140">/xmp/exif:exposurebiasvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="657d6-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="657d6-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="657d6-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="657d6-142">Read Paths</span></span>



| <span data-ttu-id="657d6-143">JSON</span><span class="sxs-lookup"><span data-stu-id="657d6-143">Order</span></span> | <span data-ttu-id="657d6-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="657d6-144">Path</span></span>                            | <span data-ttu-id="657d6-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="657d6-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="657d6-146">1</span><span class="sxs-lookup"><span data-stu-id="657d6-146">1</span></span>     | <span data-ttu-id="657d6-147">/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="657d6-147">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="657d6-148">2</span><span class="sxs-lookup"><span data-stu-id="657d6-148">2</span></span>     | <span data-ttu-id="657d6-149">/ifd/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="657d6-149">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="657d6-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="657d6-150">Write Paths</span></span>



| <span data-ttu-id="657d6-151">JSON</span><span class="sxs-lookup"><span data-stu-id="657d6-151">Order</span></span> | <span data-ttu-id="657d6-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="657d6-152">Path</span></span>                            | <span data-ttu-id="657d6-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="657d6-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="657d6-154">1</span><span class="sxs-lookup"><span data-stu-id="657d6-154">1</span></span>     | <span data-ttu-id="657d6-155">/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="657d6-155">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="657d6-156">2</span><span class="sxs-lookup"><span data-stu-id="657d6-156">2</span></span>     | <span data-ttu-id="657d6-157">/ifd/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="657d6-157">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="657d6-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="657d6-158">Remove Paths</span></span>



| <span data-ttu-id="657d6-159">JSON</span><span class="sxs-lookup"><span data-stu-id="657d6-159">Order</span></span> | <span data-ttu-id="657d6-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="657d6-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="657d6-161">1</span><span class="sxs-lookup"><span data-stu-id="657d6-161">1</span></span>     | <span data-ttu-id="657d6-162">/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="657d6-162">/ifd/exif/{ushort=37380}</span></span>        |
| <span data-ttu-id="657d6-163">2</span><span class="sxs-lookup"><span data-stu-id="657d6-163">2</span></span>     | <span data-ttu-id="657d6-164">/ifd/xmp/exif:exposurebiasvalue</span><span class="sxs-lookup"><span data-stu-id="657d6-164">/ifd/xmp/exif:exposurebiasvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="657d6-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="657d6-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="657d6-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="657d6-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="657d6-167">System. Photo. ExposureBias</span><span class="sxs-lookup"><span data-stu-id="657d6-167">System.Photo.ExposureBias</span></span>](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
