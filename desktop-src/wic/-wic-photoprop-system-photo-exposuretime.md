---
description: Criteri per i metadati delle foto per la proprietà System. Photo. ExposureTime.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: Criteri per i metadati delle foto di System. Photo. ExposureTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314455"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a><span data-ttu-id="06fc8-103">Criteri per i metadati delle foto di System. Photo. ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06fc8-103">System.Photo.ExposureTime Photo Metadata Policy</span></span>

<span data-ttu-id="06fc8-104">Criteri per i metadati delle foto per la proprietà [System. Photo. ExposureTime](../properties/props-system-photo-exposuretime.md) .</span><span class="sxs-lookup"><span data-stu-id="06fc8-104">The photo metadata policy for the [System.Photo.ExposureTime](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="06fc8-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="06fc8-105">PKEY</span></span>

<span data-ttu-id="06fc8-106">PKEY \_ Photo \_ ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06fc8-106">PKEY\_Photo\_ExposureTime</span></span>

### <a name="containers"></a><span data-ttu-id="06fc8-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="06fc8-107">Containers</span></span>

<span data-ttu-id="06fc8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="06fc8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="06fc8-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="06fc8-109">Read-Only</span></span>

<span data-ttu-id="06fc8-110">Sì</span><span class="sxs-lookup"><span data-stu-id="06fc8-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="06fc8-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="06fc8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="06fc8-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="06fc8-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="06fc8-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="06fc8-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="06fc8-114">Questo valore viene generato da System. Photo. ExposureTimeNumerator e System. Photo. ExposureTimeDenominator.</span><span class="sxs-lookup"><span data-stu-id="06fc8-114">This value is generated from System.Photo.ExposureTimeNumerator and System.Photo.ExposureTimeDenominator.</span></span> <span data-ttu-id="06fc8-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="06fc8-115">It cannot be written directly.</span></span> <span data-ttu-id="06fc8-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="06fc8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="06fc8-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="06fc8-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="06fc8-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="06fc8-118">Read Paths</span></span>



| <span data-ttu-id="06fc8-119">JSON</span><span class="sxs-lookup"><span data-stu-id="06fc8-119">Order</span></span> | <span data-ttu-id="06fc8-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="06fc8-120">Path</span></span>                          | <span data-ttu-id="06fc8-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="06fc8-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="06fc8-122">1</span><span class="sxs-lookup"><span data-stu-id="06fc8-122">1</span></span>     | <span data-ttu-id="06fc8-123">/App1/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06fc8-123">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="06fc8-124">2</span><span class="sxs-lookup"><span data-stu-id="06fc8-124">2</span></span>     | <span data-ttu-id="06fc8-125">/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06fc8-125">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="06fc8-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="06fc8-126">Write Paths</span></span>



| <span data-ttu-id="06fc8-127">JSON</span><span class="sxs-lookup"><span data-stu-id="06fc8-127">Order</span></span> | <span data-ttu-id="06fc8-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="06fc8-128">Path</span></span>                          | <span data-ttu-id="06fc8-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="06fc8-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="06fc8-130">1</span><span class="sxs-lookup"><span data-stu-id="06fc8-130">1</span></span>     | <span data-ttu-id="06fc8-131">/App1/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06fc8-131">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="06fc8-132">2</span><span class="sxs-lookup"><span data-stu-id="06fc8-132">2</span></span>     | <span data-ttu-id="06fc8-133">/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06fc8-133">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="06fc8-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="06fc8-134">Remove Paths</span></span>



| <span data-ttu-id="06fc8-135">JSON</span><span class="sxs-lookup"><span data-stu-id="06fc8-135">Order</span></span> | <span data-ttu-id="06fc8-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="06fc8-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="06fc8-137">1</span><span class="sxs-lookup"><span data-stu-id="06fc8-137">1</span></span>     | <span data-ttu-id="06fc8-138">/App1/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06fc8-138">/app1/ifd/exif/{ushort=33434}</span></span> |
| <span data-ttu-id="06fc8-139">2</span><span class="sxs-lookup"><span data-stu-id="06fc8-139">2</span></span>     | <span data-ttu-id="06fc8-140">/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06fc8-140">/xmp/exif:exposuretime</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="06fc8-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="06fc8-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="06fc8-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="06fc8-142">Read Paths</span></span>



| <span data-ttu-id="06fc8-143">JSON</span><span class="sxs-lookup"><span data-stu-id="06fc8-143">Order</span></span> | <span data-ttu-id="06fc8-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="06fc8-144">Path</span></span>                       | <span data-ttu-id="06fc8-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="06fc8-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="06fc8-146">1</span><span class="sxs-lookup"><span data-stu-id="06fc8-146">1</span></span>     | <span data-ttu-id="06fc8-147">/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06fc8-147">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="06fc8-148">2</span><span class="sxs-lookup"><span data-stu-id="06fc8-148">2</span></span>     | <span data-ttu-id="06fc8-149">/IFD/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06fc8-149">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="06fc8-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="06fc8-150">Write Paths</span></span>



| <span data-ttu-id="06fc8-151">JSON</span><span class="sxs-lookup"><span data-stu-id="06fc8-151">Order</span></span> | <span data-ttu-id="06fc8-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="06fc8-152">Path</span></span>                       | <span data-ttu-id="06fc8-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="06fc8-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="06fc8-154">1</span><span class="sxs-lookup"><span data-stu-id="06fc8-154">1</span></span>     | <span data-ttu-id="06fc8-155">/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06fc8-155">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="06fc8-156">2</span><span class="sxs-lookup"><span data-stu-id="06fc8-156">2</span></span>     | <span data-ttu-id="06fc8-157">/IFD/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06fc8-157">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="06fc8-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="06fc8-158">Remove Paths</span></span>



| <span data-ttu-id="06fc8-159">JSON</span><span class="sxs-lookup"><span data-stu-id="06fc8-159">Order</span></span> | <span data-ttu-id="06fc8-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="06fc8-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="06fc8-161">1</span><span class="sxs-lookup"><span data-stu-id="06fc8-161">1</span></span>     | <span data-ttu-id="06fc8-162">/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06fc8-162">/ifd/exif/{ushort=33434}</span></span>   |
| <span data-ttu-id="06fc8-163">2</span><span class="sxs-lookup"><span data-stu-id="06fc8-163">2</span></span>     | <span data-ttu-id="06fc8-164">/IFD/XMP/EXIF: ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06fc8-164">/ifd/xmp/exif:exposuretime</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="06fc8-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="06fc8-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="06fc8-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06fc8-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06fc8-167">System. Photo. ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06fc8-167">System.Photo.ExposureTime</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
