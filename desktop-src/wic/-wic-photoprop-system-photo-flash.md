---
description: Criteri per i metadati delle foto per la proprietà System. Photo. Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Criteri per i metadati delle foto di System. Photo. Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314454"
---
# <a name="systemphotoflash-photo-metadata-policy"></a><span data-ttu-id="ed677-103">Criteri per i metadati delle foto di System. Photo. Flash</span><span class="sxs-lookup"><span data-stu-id="ed677-103">System.Photo.Flash Photo Metadata Policy</span></span>

<span data-ttu-id="ed677-104">Criteri per i metadati delle foto per la proprietà [System. Photo. Flash](../properties/props-system-photo-exposuretime.md) .</span><span class="sxs-lookup"><span data-stu-id="ed677-104">The photo metadata policy for the [System.Photo.Flash](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ed677-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ed677-105">PKEY</span></span>

<span data-ttu-id="ed677-106">PKEY \_ Photo \_ Flash</span><span class="sxs-lookup"><span data-stu-id="ed677-106">PKEY\_Photo\_Flash</span></span>

### <a name="containers"></a><span data-ttu-id="ed677-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="ed677-107">Containers</span></span>

<span data-ttu-id="ed677-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ed677-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ed677-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="ed677-109">Read-Only</span></span>

<span data-ttu-id="ed677-110">No</span><span class="sxs-lookup"><span data-stu-id="ed677-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ed677-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="ed677-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ed677-112">VT \_ Ui1 (se lo schema di origine è XMP) o VT \_ UI2 (se lo schema di origine è EXIF)</span><span class="sxs-lookup"><span data-stu-id="ed677-112">VT\_UI1 (if the source schema was XMP), or VT\_UI2 (if the source schema was EXIF)</span></span>

<span data-ttu-id="ed677-113">\\lang1036</span><span class="sxs-lookup"><span data-stu-id="ed677-113">\\lang1036</span></span>

### <a name="input-type"></a><span data-ttu-id="ed677-114">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="ed677-114">Input Type</span></span>

<span data-ttu-id="ed677-115">VT \_ Ui1, VTUI2, VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ed677-115">VT\_UI1, VTUI2, VT\_UI4</span></span>

<span data-ttu-id="ed677-116">\\lang1033</span><span class="sxs-lookup"><span data-stu-id="ed677-116">\\lang1033</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ed677-117">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="ed677-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="ed677-118">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="ed677-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ed677-119">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="ed677-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed677-120">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="ed677-120">Read Paths</span></span>



| <span data-ttu-id="ed677-121">JSON</span><span class="sxs-lookup"><span data-stu-id="ed677-121">Order</span></span> | <span data-ttu-id="ed677-122">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed677-122">Path</span></span>                             | <span data-ttu-id="ed677-123">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ed677-123">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="ed677-124">1</span><span class="sxs-lookup"><span data-stu-id="ed677-124">1</span></span>     | <span data-ttu-id="ed677-125">/App1/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="ed677-125">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="ed677-126">ushort</span><span class="sxs-lookup"><span data-stu-id="ed677-126">ushort</span></span>      |
| <span data-ttu-id="ed677-127">2</span><span class="sxs-lookup"><span data-stu-id="ed677-127">2</span></span>     | <span data-ttu-id="ed677-128">/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="ed677-128">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ed677-129">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="ed677-129">Write Paths</span></span>



| <span data-ttu-id="ed677-130">JSON</span><span class="sxs-lookup"><span data-stu-id="ed677-130">Order</span></span> | <span data-ttu-id="ed677-131">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed677-131">Path</span></span>                             | <span data-ttu-id="ed677-132">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ed677-132">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="ed677-133">1</span><span class="sxs-lookup"><span data-stu-id="ed677-133">1</span></span>     | <span data-ttu-id="ed677-134">/App1/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="ed677-134">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="ed677-135">ushort</span><span class="sxs-lookup"><span data-stu-id="ed677-135">ushort</span></span>      |
| <span data-ttu-id="ed677-136">2</span><span class="sxs-lookup"><span data-stu-id="ed677-136">2</span></span>     | <span data-ttu-id="ed677-137">/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="ed677-137">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ed677-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="ed677-138">Remove Paths</span></span>



| <span data-ttu-id="ed677-139">JSON</span><span class="sxs-lookup"><span data-stu-id="ed677-139">Order</span></span> | <span data-ttu-id="ed677-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed677-140">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="ed677-141">1</span><span class="sxs-lookup"><span data-stu-id="ed677-141">1</span></span>     | <span data-ttu-id="ed677-142">/App1/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="ed677-142">/app1/ifd/exif/{ushort=37385}</span></span>    |
| <span data-ttu-id="ed677-143">2</span><span class="sxs-lookup"><span data-stu-id="ed677-143">2</span></span>     | <span data-ttu-id="ed677-144">/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="ed677-144">/xmp/<xmpstruct>exif:flash</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="ed677-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="ed677-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed677-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="ed677-146">Read Paths</span></span>



| <span data-ttu-id="ed677-147">JSON</span><span class="sxs-lookup"><span data-stu-id="ed677-147">Order</span></span> | <span data-ttu-id="ed677-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed677-148">Path</span></span>                                 | <span data-ttu-id="ed677-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ed677-149">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="ed677-150">1</span><span class="sxs-lookup"><span data-stu-id="ed677-150">1</span></span>     | <span data-ttu-id="ed677-151">/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="ed677-151">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="ed677-152">ushort</span><span class="sxs-lookup"><span data-stu-id="ed677-152">ushort</span></span>      |
| <span data-ttu-id="ed677-153">2</span><span class="sxs-lookup"><span data-stu-id="ed677-153">2</span></span>     | <span data-ttu-id="ed677-154">/IFD/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="ed677-154">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ed677-155">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="ed677-155">Write Paths</span></span>



| <span data-ttu-id="ed677-156">JSON</span><span class="sxs-lookup"><span data-stu-id="ed677-156">Order</span></span> | <span data-ttu-id="ed677-157">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed677-157">Path</span></span>                                 | <span data-ttu-id="ed677-158">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ed677-158">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="ed677-159">1</span><span class="sxs-lookup"><span data-stu-id="ed677-159">1</span></span>     | <span data-ttu-id="ed677-160">/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="ed677-160">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="ed677-161">ushort</span><span class="sxs-lookup"><span data-stu-id="ed677-161">ushort</span></span>      |
| <span data-ttu-id="ed677-162">2</span><span class="sxs-lookup"><span data-stu-id="ed677-162">2</span></span>     | <span data-ttu-id="ed677-163">/IFD/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="ed677-163">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ed677-164">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="ed677-164">Remove Paths</span></span>



| <span data-ttu-id="ed677-165">JSON</span><span class="sxs-lookup"><span data-stu-id="ed677-165">Order</span></span> | <span data-ttu-id="ed677-166">Percorso</span><span class="sxs-lookup"><span data-stu-id="ed677-166">Path</span></span>                                 |
|-------|--------------------------------------|
| <span data-ttu-id="ed677-167">1</span><span class="sxs-lookup"><span data-stu-id="ed677-167">1</span></span>     | <span data-ttu-id="ed677-168">/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="ed677-168">/ifd/exif/{ushort=37385}</span></span>             |
| <span data-ttu-id="ed677-169">2</span><span class="sxs-lookup"><span data-stu-id="ed677-169">2</span></span>     | <span data-ttu-id="ed677-170">/IFD/XMP/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="ed677-170">/ifd/xmp/<xmpstruct>exif:flash</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ed677-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed677-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed677-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed677-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed677-173">System. Photo. Flash</span><span class="sxs-lookup"><span data-stu-id="ed677-173">System.Photo.Flash</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
