---
description: Criteri per i metadati delle foto per la proprietà System. Photo. SubjectDistance.
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: Criteri per i metadati delle foto di System. Photo. SubjectDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3335b17f45cce7dc60881dc7ea8d9ffecc711016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883973"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a><span data-ttu-id="dc913-103">Criteri per i metadati delle foto di System. Photo. SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="dc913-103">System.Photo.SubjectDistance Photo Metadata Policy</span></span>

<span data-ttu-id="dc913-104">Criteri per i metadati delle foto per la proprietà [System. Photo. SubjectDistance](../properties/props-system-photo-subjectdistance.md) .</span><span class="sxs-lookup"><span data-stu-id="dc913-104">The photo metadata policy for the [System.Photo.SubjectDistance](../properties/props-system-photo-subjectdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="dc913-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="dc913-105">PKEY</span></span>

<span data-ttu-id="dc913-106">PKEY \_ Photo \_ SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="dc913-106">PKEY\_Photo\_SubjectDistance</span></span>

### <a name="containers"></a><span data-ttu-id="dc913-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="dc913-107">Containers</span></span>

<span data-ttu-id="dc913-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="dc913-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="dc913-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="dc913-109">Read-Only</span></span>

<span data-ttu-id="dc913-110">Sì</span><span class="sxs-lookup"><span data-stu-id="dc913-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="dc913-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="dc913-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="dc913-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="dc913-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="dc913-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="dc913-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="dc913-114">Questo valore viene generato da System. Photo. SubjectDistanceNumerator e System. Photo. SubjectDistanceDenominator.</span><span class="sxs-lookup"><span data-stu-id="dc913-114">This value is generated from System.Photo.SubjectDistanceNumerator and System.Photo.SubjectDistanceDenominator.</span></span> <span data-ttu-id="dc913-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="dc913-115">It cannot be written directly.</span></span> <span data-ttu-id="dc913-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="dc913-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="dc913-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="dc913-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="dc913-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="dc913-118">Read Paths</span></span>



| <span data-ttu-id="dc913-119">JSON</span><span class="sxs-lookup"><span data-stu-id="dc913-119">Order</span></span> | <span data-ttu-id="dc913-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="dc913-120">Path</span></span>                          | <span data-ttu-id="dc913-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="dc913-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="dc913-122">1</span><span class="sxs-lookup"><span data-stu-id="dc913-122">1</span></span>     | <span data-ttu-id="dc913-123">/App1/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="dc913-123">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="dc913-124">2</span><span class="sxs-lookup"><span data-stu-id="dc913-124">2</span></span>     | <span data-ttu-id="dc913-125">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="dc913-125">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="dc913-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="dc913-126">Write Paths</span></span>



| <span data-ttu-id="dc913-127">JSON</span><span class="sxs-lookup"><span data-stu-id="dc913-127">Order</span></span> | <span data-ttu-id="dc913-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="dc913-128">Path</span></span>                          | <span data-ttu-id="dc913-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="dc913-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="dc913-130">1</span><span class="sxs-lookup"><span data-stu-id="dc913-130">1</span></span>     | <span data-ttu-id="dc913-131">/App1/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="dc913-131">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="dc913-132">2</span><span class="sxs-lookup"><span data-stu-id="dc913-132">2</span></span>     | <span data-ttu-id="dc913-133">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="dc913-133">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="dc913-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="dc913-134">Remove Paths</span></span>



| <span data-ttu-id="dc913-135">JSON</span><span class="sxs-lookup"><span data-stu-id="dc913-135">Order</span></span> | <span data-ttu-id="dc913-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="dc913-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="dc913-137">1</span><span class="sxs-lookup"><span data-stu-id="dc913-137">1</span></span>     | <span data-ttu-id="dc913-138">/App1/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="dc913-138">/app1/ifd/exif/{ushort=37382}</span></span> |
| <span data-ttu-id="dc913-139">2</span><span class="sxs-lookup"><span data-stu-id="dc913-139">2</span></span>     | <span data-ttu-id="dc913-140">/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="dc913-140">/xmp/exif:subjectdistance</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="dc913-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="dc913-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="dc913-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="dc913-142">Read Paths</span></span>



| <span data-ttu-id="dc913-143">JSON</span><span class="sxs-lookup"><span data-stu-id="dc913-143">Order</span></span> | <span data-ttu-id="dc913-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="dc913-144">Path</span></span>                          | <span data-ttu-id="dc913-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="dc913-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="dc913-146">1</span><span class="sxs-lookup"><span data-stu-id="dc913-146">1</span></span>     | <span data-ttu-id="dc913-147">/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="dc913-147">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="dc913-148">2</span><span class="sxs-lookup"><span data-stu-id="dc913-148">2</span></span>     | <span data-ttu-id="dc913-149">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="dc913-149">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="dc913-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="dc913-150">Write Paths</span></span>



| <span data-ttu-id="dc913-151">JSON</span><span class="sxs-lookup"><span data-stu-id="dc913-151">Order</span></span> | <span data-ttu-id="dc913-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="dc913-152">Path</span></span>                          | <span data-ttu-id="dc913-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="dc913-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="dc913-154">1</span><span class="sxs-lookup"><span data-stu-id="dc913-154">1</span></span>     | <span data-ttu-id="dc913-155">/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="dc913-155">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="dc913-156">2</span><span class="sxs-lookup"><span data-stu-id="dc913-156">2</span></span>     | <span data-ttu-id="dc913-157">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="dc913-157">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="dc913-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="dc913-158">Remove Paths</span></span>



| <span data-ttu-id="dc913-159">JSON</span><span class="sxs-lookup"><span data-stu-id="dc913-159">Order</span></span> | <span data-ttu-id="dc913-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="dc913-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="dc913-161">1</span><span class="sxs-lookup"><span data-stu-id="dc913-161">1</span></span>     | <span data-ttu-id="dc913-162">/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="dc913-162">/ifd/exif/{ushort=37382}</span></span>      |
| <span data-ttu-id="dc913-163">2</span><span class="sxs-lookup"><span data-stu-id="dc913-163">2</span></span>     | <span data-ttu-id="dc913-164">/ifd/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="dc913-164">/ifd/xmp/exif:subjectdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="dc913-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc913-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc913-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc913-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc913-167">System. Photo. SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="dc913-167">System.Photo.SubjectDistance</span></span>](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
