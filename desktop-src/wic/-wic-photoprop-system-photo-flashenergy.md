---
description: Criteri per i metadati delle foto per la proprietà System. Photo. FlashEnergy.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: Criteri per i metadati delle foto di System. Photo. FlashEnergy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058190"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a><span data-ttu-id="b90a2-103">Criteri per i metadati delle foto di System. Photo. FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="b90a2-103">System.Photo.FlashEnergy Photo Metadata Policy</span></span>

<span data-ttu-id="b90a2-104">Criteri per i metadati delle foto per la proprietà [System. Photo. FlashEnergy](../properties/props-system-photo-flashenergy.md) .</span><span class="sxs-lookup"><span data-stu-id="b90a2-104">The photo metadata policy for the [System.Photo.FlashEnergy](../properties/props-system-photo-flashenergy.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b90a2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b90a2-105">PKEY</span></span>

<span data-ttu-id="b90a2-106">PKEY \_ Photo \_ FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="b90a2-106">PKEY\_Photo\_FlashEnergy</span></span>

### <a name="containers"></a><span data-ttu-id="b90a2-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="b90a2-107">Containers</span></span>

<span data-ttu-id="b90a2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b90a2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b90a2-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="b90a2-109">Read-Only</span></span>

<span data-ttu-id="b90a2-110">Sì</span><span class="sxs-lookup"><span data-stu-id="b90a2-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="b90a2-111">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="b90a2-111">Input Type</span></span>

<span data-ttu-id="b90a2-112">Double</span><span class="sxs-lookup"><span data-stu-id="b90a2-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b90a2-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="b90a2-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="b90a2-114">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="b90a2-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b90a2-115">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="b90a2-115">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b90a2-116">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="b90a2-116">Read Paths</span></span>



| <span data-ttu-id="b90a2-117">JSON</span><span class="sxs-lookup"><span data-stu-id="b90a2-117">Order</span></span> | <span data-ttu-id="b90a2-118">Percorso</span><span class="sxs-lookup"><span data-stu-id="b90a2-118">Path</span></span>                          | <span data-ttu-id="b90a2-119">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b90a2-119">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b90a2-120">1</span><span class="sxs-lookup"><span data-stu-id="b90a2-120">1</span></span>     | <span data-ttu-id="b90a2-121">/App1/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="b90a2-121">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="b90a2-122">2</span><span class="sxs-lookup"><span data-stu-id="b90a2-122">2</span></span>     | <span data-ttu-id="b90a2-123">/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="b90a2-123">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="b90a2-124">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="b90a2-124">Write Paths</span></span>



| <span data-ttu-id="b90a2-125">JSON</span><span class="sxs-lookup"><span data-stu-id="b90a2-125">Order</span></span> | <span data-ttu-id="b90a2-126">Percorso</span><span class="sxs-lookup"><span data-stu-id="b90a2-126">Path</span></span>                          | <span data-ttu-id="b90a2-127">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b90a2-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b90a2-128">1</span><span class="sxs-lookup"><span data-stu-id="b90a2-128">1</span></span>     | <span data-ttu-id="b90a2-129">/App1/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="b90a2-129">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="b90a2-130">2</span><span class="sxs-lookup"><span data-stu-id="b90a2-130">2</span></span>     | <span data-ttu-id="b90a2-131">/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="b90a2-131">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b90a2-132">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="b90a2-132">Remove Paths</span></span>



| <span data-ttu-id="b90a2-133">JSON</span><span class="sxs-lookup"><span data-stu-id="b90a2-133">Order</span></span> | <span data-ttu-id="b90a2-134">Percorso</span><span class="sxs-lookup"><span data-stu-id="b90a2-134">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="b90a2-135">1</span><span class="sxs-lookup"><span data-stu-id="b90a2-135">1</span></span>     | <span data-ttu-id="b90a2-136">/App1/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="b90a2-136">/app1/ifd/exif/{ushort=41483}</span></span> |
| <span data-ttu-id="b90a2-137">2</span><span class="sxs-lookup"><span data-stu-id="b90a2-137">2</span></span>     | <span data-ttu-id="b90a2-138">/xmp/exif:flashenergy</span><span class="sxs-lookup"><span data-stu-id="b90a2-138">/xmp/exif:flashenergy</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="b90a2-139">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="b90a2-139">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b90a2-140">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="b90a2-140">Read Paths</span></span>



| <span data-ttu-id="b90a2-141">JSON</span><span class="sxs-lookup"><span data-stu-id="b90a2-141">Order</span></span> | <span data-ttu-id="b90a2-142">Percorso</span><span class="sxs-lookup"><span data-stu-id="b90a2-142">Path</span></span>                      | <span data-ttu-id="b90a2-143">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b90a2-143">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b90a2-144">1</span><span class="sxs-lookup"><span data-stu-id="b90a2-144">1</span></span>     | <span data-ttu-id="b90a2-145">/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="b90a2-145">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="b90a2-146">2</span><span class="sxs-lookup"><span data-stu-id="b90a2-146">2</span></span>     | <span data-ttu-id="b90a2-147">/ifd/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="b90a2-147">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b90a2-148">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="b90a2-148">Write Paths</span></span>



| <span data-ttu-id="b90a2-149">JSON</span><span class="sxs-lookup"><span data-stu-id="b90a2-149">Order</span></span> | <span data-ttu-id="b90a2-150">Percorso</span><span class="sxs-lookup"><span data-stu-id="b90a2-150">Path</span></span>                      | <span data-ttu-id="b90a2-151">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b90a2-151">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b90a2-152">1</span><span class="sxs-lookup"><span data-stu-id="b90a2-152">1</span></span>     | <span data-ttu-id="b90a2-153">/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="b90a2-153">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="b90a2-154">2</span><span class="sxs-lookup"><span data-stu-id="b90a2-154">2</span></span>     | <span data-ttu-id="b90a2-155">/ifd/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="b90a2-155">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b90a2-156">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="b90a2-156">Remove Paths</span></span>



| <span data-ttu-id="b90a2-157">JSON</span><span class="sxs-lookup"><span data-stu-id="b90a2-157">Order</span></span> | <span data-ttu-id="b90a2-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="b90a2-158">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="b90a2-159">1</span><span class="sxs-lookup"><span data-stu-id="b90a2-159">1</span></span>     | <span data-ttu-id="b90a2-160">/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="b90a2-160">/ifd/exif/{ushort=41483}</span></span>  |
| <span data-ttu-id="b90a2-161">2</span><span class="sxs-lookup"><span data-stu-id="b90a2-161">2</span></span>     | <span data-ttu-id="b90a2-162">/ifd/xmp/exif:flashenergy</span><span class="sxs-lookup"><span data-stu-id="b90a2-162">/ifd/xmp/exif:flashenergy</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b90a2-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="b90a2-163">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b90a2-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b90a2-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b90a2-165">System. Photo. FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="b90a2-165">System.Photo.FlashEnergy</span></span>](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
