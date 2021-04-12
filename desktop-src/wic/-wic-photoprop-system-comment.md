---
description: Criteri per i metadati delle foto per la proprietà System. Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Criteri di metadati della foto di System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348596"
---
# <a name="systemcomment-photo-metadata-policy"></a><span data-ttu-id="0485e-103">Criteri di metadati della foto di System. Comment</span><span class="sxs-lookup"><span data-stu-id="0485e-103">System.Comment Photo Metadata Policy</span></span>

<span data-ttu-id="0485e-104">Criteri per i metadati delle foto per la proprietà [System. Comment](../properties/props-system-comment.md) .</span><span class="sxs-lookup"><span data-stu-id="0485e-104">The photo metadata policy for the [System.Comment](../properties/props-system-comment.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0485e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="0485e-105">PKEY</span></span>

<span data-ttu-id="0485e-106">\_Commento pkey</span><span class="sxs-lookup"><span data-stu-id="0485e-106">PKEY\_Comment</span></span>

### <a name="containers"></a><span data-ttu-id="0485e-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="0485e-107">Containers</span></span>

<span data-ttu-id="0485e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0485e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0485e-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="0485e-109">Read-Only</span></span>

<span data-ttu-id="0485e-110">No</span><span class="sxs-lookup"><span data-stu-id="0485e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0485e-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="0485e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0485e-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="0485e-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="0485e-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="0485e-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="0485e-114">VT \_ LPWSTR o VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="0485e-114">VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0485e-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="0485e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="0485e-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="0485e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="0485e-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="0485e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="0485e-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="0485e-118">Read Paths</span></span>



| <span data-ttu-id="0485e-119">JSON</span><span class="sxs-lookup"><span data-stu-id="0485e-119">Order</span></span> | <span data-ttu-id="0485e-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="0485e-120">Path</span></span>                                | <span data-ttu-id="0485e-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="0485e-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="0485e-122">1</span><span class="sxs-lookup"><span data-stu-id="0485e-122">1</span></span>     | <span data-ttu-id="0485e-123">/App1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="0485e-123">/app1/ifd/{ushort=40092}</span></span>            | <span data-ttu-id="0485e-124">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="0485e-124">unicode\_bytes</span></span> |
| <span data-ttu-id="0485e-125">2</span><span class="sxs-lookup"><span data-stu-id="0485e-125">2</span></span>     | <span data-ttu-id="0485e-126">/App1/IFD/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="0485e-126">/app1/ifd/{ushort=37510}</span></span>            | <span data-ttu-id="0485e-127">unicode</span><span class="sxs-lookup"><span data-stu-id="0485e-127">unicode</span></span>        |
| <span data-ttu-id="0485e-128">3</span><span class="sxs-lookup"><span data-stu-id="0485e-128">3</span></span>     | <span data-ttu-id="0485e-129">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="0485e-129">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="0485e-130">unicode</span><span class="sxs-lookup"><span data-stu-id="0485e-130">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="0485e-131">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="0485e-131">Write Paths</span></span>



| <span data-ttu-id="0485e-132">JSON</span><span class="sxs-lookup"><span data-stu-id="0485e-132">Order</span></span> | <span data-ttu-id="0485e-133">Percorso</span><span class="sxs-lookup"><span data-stu-id="0485e-133">Path</span></span>                     | <span data-ttu-id="0485e-134">Formato disco</span><span class="sxs-lookup"><span data-stu-id="0485e-134">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="0485e-135">1</span><span class="sxs-lookup"><span data-stu-id="0485e-135">1</span></span>     | <span data-ttu-id="0485e-136">/App1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="0485e-136">/app1/ifd/{ushort=40092}</span></span> | <span data-ttu-id="0485e-137">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="0485e-137">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="0485e-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="0485e-138">Remove Paths</span></span>



| <span data-ttu-id="0485e-139">JSON</span><span class="sxs-lookup"><span data-stu-id="0485e-139">Order</span></span> | <span data-ttu-id="0485e-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="0485e-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="0485e-141">1</span><span class="sxs-lookup"><span data-stu-id="0485e-141">1</span></span>     | <span data-ttu-id="0485e-142">/App1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="0485e-142">/app1/ifd/{ushort=40092}</span></span>      |
| <span data-ttu-id="0485e-143">2</span><span class="sxs-lookup"><span data-stu-id="0485e-143">2</span></span>     | <span data-ttu-id="0485e-144">/App1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="0485e-144">/app1/ifd/exif/{ushort=37510}</span></span> |
| <span data-ttu-id="0485e-145">3</span><span class="sxs-lookup"><span data-stu-id="0485e-145">3</span></span>     | <span data-ttu-id="0485e-146">/XMP/EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="0485e-146">/xmp/exif:UserComment</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="0485e-147">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="0485e-147">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="0485e-148">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="0485e-148">Read Paths</span></span>



| <span data-ttu-id="0485e-149">JSON</span><span class="sxs-lookup"><span data-stu-id="0485e-149">Order</span></span> | <span data-ttu-id="0485e-150">Percorso</span><span class="sxs-lookup"><span data-stu-id="0485e-150">Path</span></span>                                    | <span data-ttu-id="0485e-151">Formato disco</span><span class="sxs-lookup"><span data-stu-id="0485e-151">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="0485e-152">1</span><span class="sxs-lookup"><span data-stu-id="0485e-152">1</span></span>     | <span data-ttu-id="0485e-153">/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="0485e-153">/ifd/{ushort=40092}</span></span>                     | <span data-ttu-id="0485e-154">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="0485e-154">unicode\_bytes</span></span> |
| <span data-ttu-id="0485e-155">2</span><span class="sxs-lookup"><span data-stu-id="0485e-155">2</span></span>     | <span data-ttu-id="0485e-156">/IFD/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="0485e-156">/ifd/{ushort=37510}</span></span>                     | <span data-ttu-id="0485e-157">unicode</span><span class="sxs-lookup"><span data-stu-id="0485e-157">unicode</span></span>        |
| <span data-ttu-id="0485e-158">3</span><span class="sxs-lookup"><span data-stu-id="0485e-158">3</span></span>     | <span data-ttu-id="0485e-159">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="0485e-159">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="0485e-160">unicode</span><span class="sxs-lookup"><span data-stu-id="0485e-160">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="0485e-161">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="0485e-161">Write Paths</span></span>



| <span data-ttu-id="0485e-162">JSON</span><span class="sxs-lookup"><span data-stu-id="0485e-162">Order</span></span> | <span data-ttu-id="0485e-163">Percorso</span><span class="sxs-lookup"><span data-stu-id="0485e-163">Path</span></span>                | <span data-ttu-id="0485e-164">Formato disco</span><span class="sxs-lookup"><span data-stu-id="0485e-164">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="0485e-165">1</span><span class="sxs-lookup"><span data-stu-id="0485e-165">1</span></span>     | <span data-ttu-id="0485e-166">/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="0485e-166">/ifd/{ushort=40092}</span></span> | <span data-ttu-id="0485e-167">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="0485e-167">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="0485e-168">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="0485e-168">Remove Paths</span></span>



| <span data-ttu-id="0485e-169">JSON</span><span class="sxs-lookup"><span data-stu-id="0485e-169">Order</span></span> | <span data-ttu-id="0485e-170">Percorso</span><span class="sxs-lookup"><span data-stu-id="0485e-170">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="0485e-171">1</span><span class="sxs-lookup"><span data-stu-id="0485e-171">1</span></span>     | <span data-ttu-id="0485e-172">/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="0485e-172">/ifd/{ushort=40092}</span></span>       |
| <span data-ttu-id="0485e-173">2</span><span class="sxs-lookup"><span data-stu-id="0485e-173">2</span></span>     | <span data-ttu-id="0485e-174">/IFD/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="0485e-174">/ifd/{ushort=37510}</span></span>       |
| <span data-ttu-id="0485e-175">3</span><span class="sxs-lookup"><span data-stu-id="0485e-175">3</span></span>     | <span data-ttu-id="0485e-176">/IFD/XMP/EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="0485e-176">/ifd/xmp/exif:UserComment</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0485e-177">Commenti</span><span class="sxs-lookup"><span data-stu-id="0485e-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0485e-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0485e-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0485e-179">System. Comment</span><span class="sxs-lookup"><span data-stu-id="0485e-179">System.Comment</span></span>](../properties/props-system-comment.md)
</dt> </dl>

 

 
