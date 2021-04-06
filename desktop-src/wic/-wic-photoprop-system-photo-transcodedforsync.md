---
description: Criteri per i metadati delle foto per la proprietà System. Photo. TranscodedForSync.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Criteri per i metadati delle foto di System. Photo. TranscodedForSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883970"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a><span data-ttu-id="1c47c-103">Criteri per i metadati delle foto di System. Photo. TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="1c47c-103">System.Photo.TranscodedForSync Photo Metadata Policy</span></span>

<span data-ttu-id="1c47c-104">Criteri per i metadati delle foto per la proprietà [System. Photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) .</span><span class="sxs-lookup"><span data-stu-id="1c47c-104">The photo metadata policy for the [System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1c47c-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="1c47c-105">PKEY</span></span>

<span data-ttu-id="1c47c-106">PKEY \_ Photo \_ TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="1c47c-106">PKEY\_Photo\_TranscodedForSync</span></span>

### <a name="containers"></a><span data-ttu-id="1c47c-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="1c47c-107">Containers</span></span>

<span data-ttu-id="1c47c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1c47c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1c47c-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="1c47c-109">Read-Only</span></span>

<span data-ttu-id="1c47c-110">No</span><span class="sxs-lookup"><span data-stu-id="1c47c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1c47c-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="1c47c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1c47c-112">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="1c47c-112">VT\_BOOL</span></span>

### <a name="input-type"></a><span data-ttu-id="1c47c-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="1c47c-113">Input Type</span></span>

<span data-ttu-id="1c47c-114">Proprietà di tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="1c47c-114">Boolean.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1c47c-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="1c47c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="1c47c-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="1c47c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1c47c-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="1c47c-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1c47c-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="1c47c-118">Read Paths</span></span>



| <span data-ttu-id="1c47c-119">JSON</span><span class="sxs-lookup"><span data-stu-id="1c47c-119">Order</span></span> | <span data-ttu-id="1c47c-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="1c47c-120">Path</span></span>                                  | <span data-ttu-id="1c47c-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1c47c-121">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="1c47c-122">1</span><span class="sxs-lookup"><span data-stu-id="1c47c-122">1</span></span>     | <span data-ttu-id="1c47c-123">/App1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="1c47c-123">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="1c47c-124">ushort di bool \_</span><span class="sxs-lookup"><span data-stu-id="1c47c-124">bool\_ushort</span></span> |
| <span data-ttu-id="1c47c-125">2</span><span class="sxs-lookup"><span data-stu-id="1c47c-125">2</span></span>     | <span data-ttu-id="1c47c-126">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="1c47c-126">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="1c47c-127">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="1c47c-127">Write Paths</span></span>



| <span data-ttu-id="1c47c-128">JSON</span><span class="sxs-lookup"><span data-stu-id="1c47c-128">Order</span></span> | <span data-ttu-id="1c47c-129">Percorso</span><span class="sxs-lookup"><span data-stu-id="1c47c-129">Path</span></span>                                  | <span data-ttu-id="1c47c-130">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1c47c-130">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="1c47c-131">1</span><span class="sxs-lookup"><span data-stu-id="1c47c-131">1</span></span>     | <span data-ttu-id="1c47c-132">/App1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="1c47c-132">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="1c47c-133">ushort di bool \_</span><span class="sxs-lookup"><span data-stu-id="1c47c-133">bool\_ushort</span></span> |
| <span data-ttu-id="1c47c-134">2</span><span class="sxs-lookup"><span data-stu-id="1c47c-134">2</span></span>     | <span data-ttu-id="1c47c-135">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="1c47c-135">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="1c47c-136">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="1c47c-136">Remove Paths</span></span>



| <span data-ttu-id="1c47c-137">JSON</span><span class="sxs-lookup"><span data-stu-id="1c47c-137">Order</span></span> | <span data-ttu-id="1c47c-138">Percorso</span><span class="sxs-lookup"><span data-stu-id="1c47c-138">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="1c47c-139">1</span><span class="sxs-lookup"><span data-stu-id="1c47c-139">1</span></span>     | <span data-ttu-id="1c47c-140">/App1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="1c47c-140">/app1/ifd/{ushort=18248}</span></span>              |
| <span data-ttu-id="1c47c-141">2</span><span class="sxs-lookup"><span data-stu-id="1c47c-141">2</span></span>     | <span data-ttu-id="1c47c-142">/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="1c47c-142">/xmp/microsoftphoto:transcodedforsync</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="1c47c-143">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="1c47c-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1c47c-144">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="1c47c-144">Read Paths</span></span>



| <span data-ttu-id="1c47c-145">JSON</span><span class="sxs-lookup"><span data-stu-id="1c47c-145">Order</span></span> | <span data-ttu-id="1c47c-146">Percorso</span><span class="sxs-lookup"><span data-stu-id="1c47c-146">Path</span></span>                                      | <span data-ttu-id="1c47c-147">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1c47c-147">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="1c47c-148">1</span><span class="sxs-lookup"><span data-stu-id="1c47c-148">1</span></span>     | <span data-ttu-id="1c47c-149">/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="1c47c-149">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="1c47c-150">ushort di bool \_</span><span class="sxs-lookup"><span data-stu-id="1c47c-150">bool\_ushort</span></span> |
| <span data-ttu-id="1c47c-151">2</span><span class="sxs-lookup"><span data-stu-id="1c47c-151">2</span></span>     | <span data-ttu-id="1c47c-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="1c47c-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="1c47c-153">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="1c47c-153">Write Paths</span></span>



| <span data-ttu-id="1c47c-154">JSON</span><span class="sxs-lookup"><span data-stu-id="1c47c-154">Order</span></span> | <span data-ttu-id="1c47c-155">Percorso</span><span class="sxs-lookup"><span data-stu-id="1c47c-155">Path</span></span>                                      | <span data-ttu-id="1c47c-156">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1c47c-156">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="1c47c-157">1</span><span class="sxs-lookup"><span data-stu-id="1c47c-157">1</span></span>     | <span data-ttu-id="1c47c-158">/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="1c47c-158">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="1c47c-159">ushort di bool \_</span><span class="sxs-lookup"><span data-stu-id="1c47c-159">bool\_ushort</span></span> |
| <span data-ttu-id="1c47c-160">2</span><span class="sxs-lookup"><span data-stu-id="1c47c-160">2</span></span>     | <span data-ttu-id="1c47c-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="1c47c-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="1c47c-162">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="1c47c-162">Remove Paths</span></span>



| <span data-ttu-id="1c47c-163">JSON</span><span class="sxs-lookup"><span data-stu-id="1c47c-163">Order</span></span> | <span data-ttu-id="1c47c-164">Percorso</span><span class="sxs-lookup"><span data-stu-id="1c47c-164">Path</span></span>                                      |
|-------|-------------------------------------------|
| <span data-ttu-id="1c47c-165">1</span><span class="sxs-lookup"><span data-stu-id="1c47c-165">1</span></span>     | <span data-ttu-id="1c47c-166">/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="1c47c-166">/ifd/{ushort=18248}</span></span>                       |
| <span data-ttu-id="1c47c-167">2</span><span class="sxs-lookup"><span data-stu-id="1c47c-167">2</span></span>     | <span data-ttu-id="1c47c-168">/ifd/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="1c47c-168">/ifd/xmp/microsoftphoto:transcodedforsync</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1c47c-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c47c-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c47c-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c47c-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c47c-171">System. Photo. TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="1c47c-171">System.Photo.TranscodedForSync</span></span>](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
