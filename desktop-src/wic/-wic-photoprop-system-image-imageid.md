---
description: Criteri per i metadati delle foto per la proprietà System. image. ImageID.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Criteri per i metadati delle foto di System. image. ImageID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529269"
---
# <a name="systemimageimageid-photo-metadata-policy"></a><span data-ttu-id="825de-103">Criteri per i metadati delle foto di System. image. ImageID</span><span class="sxs-lookup"><span data-stu-id="825de-103">System.Image.ImageID Photo Metadata Policy</span></span>

<span data-ttu-id="825de-104">Criteri per i metadati delle foto per la proprietà [System. image. ImageId](../properties/props-system-image-imageid.md) .</span><span class="sxs-lookup"><span data-stu-id="825de-104">The photo metadata policy for the [System.Image.ImageID](../properties/props-system-image-imageid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="825de-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="825de-105">PKEY</span></span>

<span data-ttu-id="825de-106">Immagine di PKEY \_ \_ ImageId</span><span class="sxs-lookup"><span data-stu-id="825de-106">PKEY\_Image\_ImageID</span></span>

### <a name="containers"></a><span data-ttu-id="825de-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="825de-107">Containers</span></span>

<span data-ttu-id="825de-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="825de-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="825de-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="825de-109">Read-Only</span></span>

<span data-ttu-id="825de-110">No</span><span class="sxs-lookup"><span data-stu-id="825de-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="825de-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="825de-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="825de-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="825de-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="825de-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="825de-113">Input Type</span></span>

<span data-ttu-id="825de-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="825de-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="825de-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="825de-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="825de-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="825de-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="825de-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="825de-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="825de-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="825de-118">Read Paths</span></span>



| <span data-ttu-id="825de-119">JSON</span><span class="sxs-lookup"><span data-stu-id="825de-119">Order</span></span> | <span data-ttu-id="825de-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="825de-120">Path</span></span>                          | <span data-ttu-id="825de-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="825de-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="825de-122">1</span><span class="sxs-lookup"><span data-stu-id="825de-122">1</span></span>     | <span data-ttu-id="825de-123">/App1/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="825de-123">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="825de-124">ascii</span><span class="sxs-lookup"><span data-stu-id="825de-124">ascii</span></span>       |
| <span data-ttu-id="825de-125">2</span><span class="sxs-lookup"><span data-stu-id="825de-125">2</span></span>     | <span data-ttu-id="825de-126">/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="825de-126">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="825de-127">unicode</span><span class="sxs-lookup"><span data-stu-id="825de-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="825de-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="825de-128">Write Paths</span></span>



| <span data-ttu-id="825de-129">JSON</span><span class="sxs-lookup"><span data-stu-id="825de-129">Order</span></span> | <span data-ttu-id="825de-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="825de-130">Path</span></span>                          | <span data-ttu-id="825de-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="825de-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="825de-132">1</span><span class="sxs-lookup"><span data-stu-id="825de-132">1</span></span>     | <span data-ttu-id="825de-133">/App1/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="825de-133">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="825de-134">ascii</span><span class="sxs-lookup"><span data-stu-id="825de-134">ascii</span></span>       |
| <span data-ttu-id="825de-135">2</span><span class="sxs-lookup"><span data-stu-id="825de-135">2</span></span>     | <span data-ttu-id="825de-136">/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="825de-136">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="825de-137">unicode</span><span class="sxs-lookup"><span data-stu-id="825de-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="825de-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="825de-138">Remove Paths</span></span>



| <span data-ttu-id="825de-139">JSON</span><span class="sxs-lookup"><span data-stu-id="825de-139">Order</span></span> | <span data-ttu-id="825de-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="825de-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="825de-141">1</span><span class="sxs-lookup"><span data-stu-id="825de-141">1</span></span>     | <span data-ttu-id="825de-142">/App1/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="825de-142">/app1/ifd/exif/{ushort=42016}</span></span> |
| <span data-ttu-id="825de-143">2</span><span class="sxs-lookup"><span data-stu-id="825de-143">2</span></span>     | <span data-ttu-id="825de-144">/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="825de-144">/xmp/exif:ImageUniqueID</span></span>       |



 

### <a name="tiff-policy"></a><span data-ttu-id="825de-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="825de-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="825de-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="825de-146">Read Paths</span></span>



| <span data-ttu-id="825de-147">JSON</span><span class="sxs-lookup"><span data-stu-id="825de-147">Order</span></span> | <span data-ttu-id="825de-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="825de-148">Path</span></span>                        | <span data-ttu-id="825de-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="825de-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="825de-150">/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="825de-150">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="825de-151">ascii</span><span class="sxs-lookup"><span data-stu-id="825de-151">ascii</span></span>       |
|       | <span data-ttu-id="825de-152">/IFD/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="825de-152">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="825de-153">unicode</span><span class="sxs-lookup"><span data-stu-id="825de-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="825de-154">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="825de-154">Write Paths</span></span>



| <span data-ttu-id="825de-155">JSON</span><span class="sxs-lookup"><span data-stu-id="825de-155">Order</span></span> | <span data-ttu-id="825de-156">Percorso</span><span class="sxs-lookup"><span data-stu-id="825de-156">Path</span></span>                        | <span data-ttu-id="825de-157">Formato disco</span><span class="sxs-lookup"><span data-stu-id="825de-157">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="825de-158">/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="825de-158">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="825de-159">ascii</span><span class="sxs-lookup"><span data-stu-id="825de-159">ascii</span></span>       |
|       | <span data-ttu-id="825de-160">/IFD/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="825de-160">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="825de-161">unicode</span><span class="sxs-lookup"><span data-stu-id="825de-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="825de-162">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="825de-162">Remove Paths</span></span>



| <span data-ttu-id="825de-163">JSON</span><span class="sxs-lookup"><span data-stu-id="825de-163">Order</span></span> | <span data-ttu-id="825de-164">Percorso</span><span class="sxs-lookup"><span data-stu-id="825de-164">Path</span></span>                        |
|-------|-----------------------------|
|       | <span data-ttu-id="825de-165">/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="825de-165">/ifd/exif/{ushort=42016}</span></span>    |
|       | <span data-ttu-id="825de-166">/IFD/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="825de-166">/ifd/xmp/exif:ImageUniqueID</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="825de-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="825de-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="825de-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="825de-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="825de-169">System. image. ImageID</span><span class="sxs-lookup"><span data-stu-id="825de-169">System.Image.ImageID</span></span>](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
