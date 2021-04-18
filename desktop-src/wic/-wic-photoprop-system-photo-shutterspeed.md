---
description: Criteri per i metadati delle foto per la proprietà System. Photo. ShutterSpeed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Criteri per i metadati delle foto di System. Photo. ShutterSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315959"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a><span data-ttu-id="6fa5c-103">Criteri per i metadati delle foto di System. Photo. ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="6fa5c-103">System.Photo.ShutterSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="6fa5c-104">Criteri per i metadati delle foto per la proprietà [System. Photo. ShutterSpeed](../properties/props-system-photo-shutterspeed.md) .</span><span class="sxs-lookup"><span data-stu-id="6fa5c-104">The photo metadata policy for the [System.Photo.ShutterSpeed](../properties/props-system-photo-shutterspeed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6fa5c-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="6fa5c-105">PKEY</span></span>

<span data-ttu-id="6fa5c-106">PKEY \_ Photo \_ ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="6fa5c-106">PKEY\_Photo\_ShutterSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="6fa5c-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="6fa5c-107">Containers</span></span>

<span data-ttu-id="6fa5c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6fa5c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6fa5c-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="6fa5c-109">Read-Only</span></span>

<span data-ttu-id="6fa5c-110">Sì</span><span class="sxs-lookup"><span data-stu-id="6fa5c-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6fa5c-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="6fa5c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6fa5c-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="6fa5c-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6fa5c-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="6fa5c-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="6fa5c-114">Questo valore viene generato da System. Photo. ShutterSpeedNumerator e System. Photo. ShutterSpeedDenominator.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-114">This value is generated from System.Photo.ShutterSpeedNumerator and System.Photo.ShutterSpeedDenominator.</span></span> <span data-ttu-id="6fa5c-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-115">It cannot be written directly.</span></span> <span data-ttu-id="6fa5c-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6fa5c-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="6fa5c-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6fa5c-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="6fa5c-118">Read Paths</span></span>



| <span data-ttu-id="6fa5c-119">JSON</span><span class="sxs-lookup"><span data-stu-id="6fa5c-119">Order</span></span> | <span data-ttu-id="6fa5c-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="6fa5c-120">Path</span></span>                          | <span data-ttu-id="6fa5c-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6fa5c-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="6fa5c-122">1</span><span class="sxs-lookup"><span data-stu-id="6fa5c-122">1</span></span>     | <span data-ttu-id="6fa5c-123">/App1/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="6fa5c-123">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="6fa5c-124">2</span><span class="sxs-lookup"><span data-stu-id="6fa5c-124">2</span></span>     | <span data-ttu-id="6fa5c-125">/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="6fa5c-125">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="6fa5c-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="6fa5c-126">Write Paths</span></span>



| <span data-ttu-id="6fa5c-127">JSON</span><span class="sxs-lookup"><span data-stu-id="6fa5c-127">Order</span></span> | <span data-ttu-id="6fa5c-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="6fa5c-128">Path</span></span>                          | <span data-ttu-id="6fa5c-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6fa5c-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="6fa5c-130">1</span><span class="sxs-lookup"><span data-stu-id="6fa5c-130">1</span></span>     | <span data-ttu-id="6fa5c-131">/App1/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="6fa5c-131">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="6fa5c-132">2</span><span class="sxs-lookup"><span data-stu-id="6fa5c-132">2</span></span>     | <span data-ttu-id="6fa5c-133">/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="6fa5c-133">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6fa5c-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="6fa5c-134">Remove Paths</span></span>



| <span data-ttu-id="6fa5c-135">JSON</span><span class="sxs-lookup"><span data-stu-id="6fa5c-135">Order</span></span> | <span data-ttu-id="6fa5c-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="6fa5c-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="6fa5c-137">1</span><span class="sxs-lookup"><span data-stu-id="6fa5c-137">1</span></span>     | <span data-ttu-id="6fa5c-138">/App1/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="6fa5c-138">/app1/ifd/exif/{ushort=37377}</span></span> |
| <span data-ttu-id="6fa5c-139">2</span><span class="sxs-lookup"><span data-stu-id="6fa5c-139">2</span></span>     | <span data-ttu-id="6fa5c-140">/xmp/exif:shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="6fa5c-140">/xmp/exif:shutterspeedvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="6fa5c-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="6fa5c-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6fa5c-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="6fa5c-142">Read Paths</span></span>



| <span data-ttu-id="6fa5c-143">JSON</span><span class="sxs-lookup"><span data-stu-id="6fa5c-143">Order</span></span> | <span data-ttu-id="6fa5c-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="6fa5c-144">Path</span></span>                            | <span data-ttu-id="6fa5c-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6fa5c-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="6fa5c-146">1</span><span class="sxs-lookup"><span data-stu-id="6fa5c-146">1</span></span>     | <span data-ttu-id="6fa5c-147">/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="6fa5c-147">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="6fa5c-148">2</span><span class="sxs-lookup"><span data-stu-id="6fa5c-148">2</span></span>     | <span data-ttu-id="6fa5c-149">/ifd/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="6fa5c-149">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="6fa5c-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="6fa5c-150">Write Paths</span></span>



| <span data-ttu-id="6fa5c-151">JSON</span><span class="sxs-lookup"><span data-stu-id="6fa5c-151">Order</span></span> | <span data-ttu-id="6fa5c-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="6fa5c-152">Path</span></span>                            | <span data-ttu-id="6fa5c-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6fa5c-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="6fa5c-154">1</span><span class="sxs-lookup"><span data-stu-id="6fa5c-154">1</span></span>     | <span data-ttu-id="6fa5c-155">/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="6fa5c-155">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="6fa5c-156">2</span><span class="sxs-lookup"><span data-stu-id="6fa5c-156">2</span></span>     | <span data-ttu-id="6fa5c-157">/ifd/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="6fa5c-157">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6fa5c-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="6fa5c-158">Remove Paths</span></span>



| <span data-ttu-id="6fa5c-159">JSON</span><span class="sxs-lookup"><span data-stu-id="6fa5c-159">Order</span></span> | <span data-ttu-id="6fa5c-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="6fa5c-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="6fa5c-161">1</span><span class="sxs-lookup"><span data-stu-id="6fa5c-161">1</span></span>     | <span data-ttu-id="6fa5c-162">/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="6fa5c-162">/ifd/exif/{ushort=37377}</span></span>        |
| <span data-ttu-id="6fa5c-163">2</span><span class="sxs-lookup"><span data-stu-id="6fa5c-163">2</span></span>     | <span data-ttu-id="6fa5c-164">/ifd/xmp/exif:shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="6fa5c-164">/ifd/xmp/exif:shutterspeedvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6fa5c-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fa5c-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fa5c-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6fa5c-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fa5c-167">System. Photo. ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="6fa5c-167">System.Photo.ShutterSpeed</span></span>](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
