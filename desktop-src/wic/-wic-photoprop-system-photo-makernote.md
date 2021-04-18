---
description: Criteri per i metadati delle foto per la proprietà System. Photo. MakerNote.
ms.assetid: e1018bc6-3fd2-4212-afee-6811bfe99f14
title: Criteri per i metadati delle foto di System. Photo. MakerNote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df1a16205d6a9d1229d3627e6b9cc8c746d8a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312943"
---
# <a name="systemphotomakernote-photo-metadata-policy"></a><span data-ttu-id="f2b26-103">Criteri per i metadati delle foto di System. Photo. MakerNote</span><span class="sxs-lookup"><span data-stu-id="f2b26-103">System.Photo.MakerNote Photo Metadata Policy</span></span>

<span data-ttu-id="f2b26-104">Criteri per i metadati delle foto per la proprietà [System. Photo. Makernote](../properties/props-system-photo-makernote.md) .</span><span class="sxs-lookup"><span data-stu-id="f2b26-104">The photo metadata policy for the [System.Photo.MakerNote](../properties/props-system-photo-makernote.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f2b26-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f2b26-105">PKEY</span></span>

<span data-ttu-id="f2b26-106">PKEY \_ Photo \_ Makernote</span><span class="sxs-lookup"><span data-stu-id="f2b26-106">PKEY\_Photo\_MakerNote</span></span>

### <a name="containers"></a><span data-ttu-id="f2b26-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="f2b26-107">Containers</span></span>

<span data-ttu-id="f2b26-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f2b26-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f2b26-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="f2b26-109">Read-Only</span></span>

<span data-ttu-id="f2b26-110">No</span><span class="sxs-lookup"><span data-stu-id="f2b26-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f2b26-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="f2b26-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f2b26-112">\_VTUI1 vettore \| VT</span><span class="sxs-lookup"><span data-stu-id="f2b26-112">VT\_VECTOR \| VTUI1</span></span>

### <a name="input-type"></a><span data-ttu-id="f2b26-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="f2b26-113">Input Type</span></span>

<span data-ttu-id="f2b26-114">Buffer</span><span class="sxs-lookup"><span data-stu-id="f2b26-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f2b26-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="f2b26-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f2b26-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="f2b26-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f2b26-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="f2b26-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f2b26-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="f2b26-118">Read Paths</span></span>



| <span data-ttu-id="f2b26-119">JSON</span><span class="sxs-lookup"><span data-stu-id="f2b26-119">Order</span></span> | <span data-ttu-id="f2b26-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="f2b26-120">Path</span></span>                          | <span data-ttu-id="f2b26-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="f2b26-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f2b26-122">1</span><span class="sxs-lookup"><span data-stu-id="f2b26-122">1</span></span>     | <span data-ttu-id="f2b26-123">/App1/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="f2b26-123">/app1/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="f2b26-124">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="f2b26-124">Write Paths</span></span>



| <span data-ttu-id="f2b26-125">JSON</span><span class="sxs-lookup"><span data-stu-id="f2b26-125">Order</span></span> | <span data-ttu-id="f2b26-126">Percorso</span><span class="sxs-lookup"><span data-stu-id="f2b26-126">Path</span></span>                          | <span data-ttu-id="f2b26-127">Formato disco</span><span class="sxs-lookup"><span data-stu-id="f2b26-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f2b26-128">1</span><span class="sxs-lookup"><span data-stu-id="f2b26-128">1</span></span>     | <span data-ttu-id="f2b26-129">/App1/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="f2b26-129">/app1/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="f2b26-130">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="f2b26-130">Remove Paths</span></span>



| <span data-ttu-id="f2b26-131">JSON</span><span class="sxs-lookup"><span data-stu-id="f2b26-131">Order</span></span> | <span data-ttu-id="f2b26-132">Percorso</span><span class="sxs-lookup"><span data-stu-id="f2b26-132">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="f2b26-133">1</span><span class="sxs-lookup"><span data-stu-id="f2b26-133">1</span></span>     | <span data-ttu-id="f2b26-134">/App1/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="f2b26-134">/app1/ifd/exif/{ushort=37500}</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="f2b26-135">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="f2b26-135">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f2b26-136">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="f2b26-136">Read Paths</span></span>



| <span data-ttu-id="f2b26-137">JSON</span><span class="sxs-lookup"><span data-stu-id="f2b26-137">Order</span></span> | <span data-ttu-id="f2b26-138">Percorso</span><span class="sxs-lookup"><span data-stu-id="f2b26-138">Path</span></span>                     | <span data-ttu-id="f2b26-139">Formato disco</span><span class="sxs-lookup"><span data-stu-id="f2b26-139">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="f2b26-140">1</span><span class="sxs-lookup"><span data-stu-id="f2b26-140">1</span></span>     | <span data-ttu-id="f2b26-141">/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="f2b26-141">/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="f2b26-142">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="f2b26-142">Write Paths</span></span>



| <span data-ttu-id="f2b26-143">JSON</span><span class="sxs-lookup"><span data-stu-id="f2b26-143">Order</span></span> | <span data-ttu-id="f2b26-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="f2b26-144">Path</span></span>                     | <span data-ttu-id="f2b26-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="f2b26-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="f2b26-146">1</span><span class="sxs-lookup"><span data-stu-id="f2b26-146">1</span></span>     | <span data-ttu-id="f2b26-147">/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="f2b26-147">/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="f2b26-148">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="f2b26-148">Remove Paths</span></span>



| <span data-ttu-id="f2b26-149">JSON</span><span class="sxs-lookup"><span data-stu-id="f2b26-149">Order</span></span> | <span data-ttu-id="f2b26-150">Percorso</span><span class="sxs-lookup"><span data-stu-id="f2b26-150">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="f2b26-151">1</span><span class="sxs-lookup"><span data-stu-id="f2b26-151">1</span></span>     | <span data-ttu-id="f2b26-152">/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="f2b26-152">/ifd/exif/{ushort=37500}</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f2b26-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2b26-153">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2b26-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2b26-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2b26-155">System. Photo. MakerNote</span><span class="sxs-lookup"><span data-stu-id="f2b26-155">System.Photo.MakerNote</span></span>](../properties/props-system-photo-makernote.md)
</dt> </dl>

 

 
