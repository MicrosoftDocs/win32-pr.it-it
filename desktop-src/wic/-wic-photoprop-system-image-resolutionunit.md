---
description: Criteri per i metadati delle foto per la proprietà System. image. ResolutionUnit.
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: Criteri per i metadati delle foto di System. image. ResolutionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312951"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a><span data-ttu-id="ee653-103">Criteri per i metadati delle foto di System. image. ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="ee653-103">System.Image.ResolutionUnit Photo Metadata Policy</span></span>

<span data-ttu-id="ee653-104">Criteri per i metadati delle foto per la proprietà [System. image. ResolutionUnit](../properties/props-system-image-resolutionunit.md) .</span><span class="sxs-lookup"><span data-stu-id="ee653-104">The photo metadata policy for the [System.Image.ResolutionUnit](../properties/props-system-image-resolutionunit.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ee653-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ee653-105">PKEY</span></span>

<span data-ttu-id="ee653-106">Immagine di PKEY \_ \_ ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="ee653-106">PKEY\_Image\_ResolutionUnit</span></span>

### <a name="containers"></a><span data-ttu-id="ee653-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="ee653-107">Containers</span></span>

<span data-ttu-id="ee653-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ee653-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ee653-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="ee653-109">Read-Only</span></span>

<span data-ttu-id="ee653-110">Sì.</span><span class="sxs-lookup"><span data-stu-id="ee653-110">Yes.</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ee653-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="ee653-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ee653-112">\_I2 VT</span><span class="sxs-lookup"><span data-stu-id="ee653-112">VT\_I2</span></span>

### <a name="input-type"></a><span data-ttu-id="ee653-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="ee653-113">Input Type</span></span>

<span data-ttu-id="ee653-114">UShort</span><span class="sxs-lookup"><span data-stu-id="ee653-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ee653-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="ee653-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ee653-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="ee653-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ee653-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="ee653-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ee653-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="ee653-118">Read Paths</span></span>



| <span data-ttu-id="ee653-119">JSON</span><span class="sxs-lookup"><span data-stu-id="ee653-119">Order</span></span> | <span data-ttu-id="ee653-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="ee653-120">Path</span></span>                     | <span data-ttu-id="ee653-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ee653-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="ee653-122">1</span><span class="sxs-lookup"><span data-stu-id="ee653-122">1</span></span>     | <span data-ttu-id="ee653-123">/App1/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="ee653-123">/app1/ifd/{ushort=296}</span></span>   | <span data-ttu-id="ee653-124">ushort</span><span class="sxs-lookup"><span data-stu-id="ee653-124">ushort</span></span>      |
| <span data-ttu-id="ee653-125">2</span><span class="sxs-lookup"><span data-stu-id="ee653-125">2</span></span>     | <span data-ttu-id="ee653-126">/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="ee653-126">/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="ee653-127">unicode</span><span class="sxs-lookup"><span data-stu-id="ee653-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ee653-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="ee653-128">Write Paths</span></span>



| <span data-ttu-id="ee653-129">JSON</span><span class="sxs-lookup"><span data-stu-id="ee653-129">Order</span></span> | <span data-ttu-id="ee653-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="ee653-130">Path</span></span>                     | <span data-ttu-id="ee653-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ee653-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="ee653-132">1</span><span class="sxs-lookup"><span data-stu-id="ee653-132">1</span></span>     | <span data-ttu-id="ee653-133">/App1/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="ee653-133">/app1/ifd/{ushort=296}</span></span>   | <span data-ttu-id="ee653-134">ushort</span><span class="sxs-lookup"><span data-stu-id="ee653-134">ushort</span></span>      |
| <span data-ttu-id="ee653-135">2</span><span class="sxs-lookup"><span data-stu-id="ee653-135">2</span></span>     | <span data-ttu-id="ee653-136">/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="ee653-136">/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="ee653-137">unicode</span><span class="sxs-lookup"><span data-stu-id="ee653-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ee653-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="ee653-138">Remove Paths</span></span>



| <span data-ttu-id="ee653-139">JSON</span><span class="sxs-lookup"><span data-stu-id="ee653-139">Order</span></span> | <span data-ttu-id="ee653-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="ee653-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="ee653-141">1</span><span class="sxs-lookup"><span data-stu-id="ee653-141">1</span></span>     | <span data-ttu-id="ee653-142">/App1/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="ee653-142">/app1/ifd/{ushort=296}</span></span>   |
| <span data-ttu-id="ee653-143">2</span><span class="sxs-lookup"><span data-stu-id="ee653-143">2</span></span>     | <span data-ttu-id="ee653-144">/xmp/tiff:resolutionunit</span><span class="sxs-lookup"><span data-stu-id="ee653-144">/xmp/tiff:resolutionunit</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="ee653-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="ee653-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ee653-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="ee653-146">Read Paths</span></span>



| <span data-ttu-id="ee653-147">JSON</span><span class="sxs-lookup"><span data-stu-id="ee653-147">Order</span></span> | <span data-ttu-id="ee653-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="ee653-148">Path</span></span>                         | <span data-ttu-id="ee653-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ee653-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="ee653-150">1</span><span class="sxs-lookup"><span data-stu-id="ee653-150">1</span></span>     | <span data-ttu-id="ee653-151">/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="ee653-151">/ifd/{ushort=296}</span></span>            | <span data-ttu-id="ee653-152">ushort</span><span class="sxs-lookup"><span data-stu-id="ee653-152">ushort</span></span>      |
| <span data-ttu-id="ee653-153">2</span><span class="sxs-lookup"><span data-stu-id="ee653-153">2</span></span>     | <span data-ttu-id="ee653-154">/ifd/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="ee653-154">/ifd/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="ee653-155">unicode</span><span class="sxs-lookup"><span data-stu-id="ee653-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ee653-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="ee653-156">Write Paths</span></span>



| <span data-ttu-id="ee653-157">JSON</span><span class="sxs-lookup"><span data-stu-id="ee653-157">Order</span></span> | <span data-ttu-id="ee653-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="ee653-158">Path</span></span>                         | <span data-ttu-id="ee653-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ee653-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="ee653-160">1</span><span class="sxs-lookup"><span data-stu-id="ee653-160">1</span></span>     | <span data-ttu-id="ee653-161">/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="ee653-161">/ifd/{ushort=296}</span></span>            | <span data-ttu-id="ee653-162">ushort</span><span class="sxs-lookup"><span data-stu-id="ee653-162">ushort</span></span>      |
| <span data-ttu-id="ee653-163">2</span><span class="sxs-lookup"><span data-stu-id="ee653-163">2</span></span>     | <span data-ttu-id="ee653-164">/ifd/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="ee653-164">/ifd/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="ee653-165">unicode</span><span class="sxs-lookup"><span data-stu-id="ee653-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ee653-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="ee653-166">Remove Paths</span></span>



| <span data-ttu-id="ee653-167">JSON</span><span class="sxs-lookup"><span data-stu-id="ee653-167">Order</span></span> | <span data-ttu-id="ee653-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="ee653-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="ee653-169">1</span><span class="sxs-lookup"><span data-stu-id="ee653-169">1</span></span>     | <span data-ttu-id="ee653-170">/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="ee653-170">/ifd/{ushort=296}</span></span>            |
| <span data-ttu-id="ee653-171">2</span><span class="sxs-lookup"><span data-stu-id="ee653-171">2</span></span>     | <span data-ttu-id="ee653-172">/ifd/xmp/tiff:resolutionunit</span><span class="sxs-lookup"><span data-stu-id="ee653-172">/ifd/xmp/tiff:resolutionunit</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ee653-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee653-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee653-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee653-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee653-175">System. image. ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="ee653-175">System.Image.ResolutionUnit</span></span>](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
