---
description: Criteri per i metadati delle foto per la proprietà System. rating.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Criteri per i metadati delle foto System. rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347176"
---
# <a name="systemrating-photo-metadata-policy"></a><span data-ttu-id="1651e-103">Criteri per i metadati delle foto System. rating</span><span class="sxs-lookup"><span data-stu-id="1651e-103">System.Rating Photo Metadata Policy</span></span>

<span data-ttu-id="1651e-104">Criteri per i metadati delle foto per la proprietà [System. rating](../properties/props-system-rating.md) .</span><span class="sxs-lookup"><span data-stu-id="1651e-104">The photo metadata policy for the [System.Rating](../properties/props-system-rating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1651e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="1651e-105">PKEY</span></span>

<span data-ttu-id="1651e-106">\_Classificazione pkey</span><span class="sxs-lookup"><span data-stu-id="1651e-106">PKEY\_Rating</span></span>

### <a name="containers"></a><span data-ttu-id="1651e-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="1651e-107">Containers</span></span>

<span data-ttu-id="1651e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1651e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1651e-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="1651e-109">Read-Only</span></span>

<span data-ttu-id="1651e-110">No</span><span class="sxs-lookup"><span data-stu-id="1651e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1651e-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="1651e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1651e-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="1651e-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="1651e-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="1651e-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="1651e-114">Può essere VT \_ Ui1, VT \_ UI2 o VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="1651e-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="1651e-115">Il valore può essere compreso tra 0 e 99.</span><span class="sxs-lookup"><span data-stu-id="1651e-115">The value may range from 0 to 99.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1651e-116">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="1651e-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="1651e-117">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="1651e-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1651e-118">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="1651e-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1651e-119">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="1651e-119">Read Paths</span></span>



| <span data-ttu-id="1651e-120">JSON</span><span class="sxs-lookup"><span data-stu-id="1651e-120">Order</span></span> | <span data-ttu-id="1651e-121">Percorso</span><span class="sxs-lookup"><span data-stu-id="1651e-121">Path</span></span>                       | <span data-ttu-id="1651e-122">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1651e-122">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="1651e-123">1</span><span class="sxs-lookup"><span data-stu-id="1651e-123">1</span></span>     | <span data-ttu-id="1651e-124">/App1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="1651e-124">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="1651e-125">ushort</span><span class="sxs-lookup"><span data-stu-id="1651e-125">ushort</span></span>      |
| <span data-ttu-id="1651e-126">2</span><span class="sxs-lookup"><span data-stu-id="1651e-126">2</span></span>     | <span data-ttu-id="1651e-127">/xmp/MicrosoftPhoto: valutazione</span><span class="sxs-lookup"><span data-stu-id="1651e-127">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="1651e-128">unicode</span><span class="sxs-lookup"><span data-stu-id="1651e-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1651e-129">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="1651e-129">Write Paths</span></span>



| <span data-ttu-id="1651e-130">JSON</span><span class="sxs-lookup"><span data-stu-id="1651e-130">Order</span></span> | <span data-ttu-id="1651e-131">Percorso</span><span class="sxs-lookup"><span data-stu-id="1651e-131">Path</span></span>                       | <span data-ttu-id="1651e-132">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1651e-132">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="1651e-133">1</span><span class="sxs-lookup"><span data-stu-id="1651e-133">1</span></span>     | <span data-ttu-id="1651e-134">/App1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="1651e-134">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="1651e-135">ushort</span><span class="sxs-lookup"><span data-stu-id="1651e-135">ushort</span></span>      |
| <span data-ttu-id="1651e-136">2</span><span class="sxs-lookup"><span data-stu-id="1651e-136">2</span></span>     | <span data-ttu-id="1651e-137">/xmp/MicrosoftPhoto: valutazione</span><span class="sxs-lookup"><span data-stu-id="1651e-137">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="1651e-138">unicode</span><span class="sxs-lookup"><span data-stu-id="1651e-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1651e-139">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="1651e-139">Remove Paths</span></span>



| <span data-ttu-id="1651e-140">JSON</span><span class="sxs-lookup"><span data-stu-id="1651e-140">Order</span></span> | <span data-ttu-id="1651e-141">Percorso</span><span class="sxs-lookup"><span data-stu-id="1651e-141">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="1651e-142">1</span><span class="sxs-lookup"><span data-stu-id="1651e-142">1</span></span>     | <span data-ttu-id="1651e-143">/App1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="1651e-143">/app1/ifd/{ushort=18249}</span></span>   |
| <span data-ttu-id="1651e-144">2</span><span class="sxs-lookup"><span data-stu-id="1651e-144">2</span></span>     | <span data-ttu-id="1651e-145">/XMP/microsoftphoto: valutazione</span><span class="sxs-lookup"><span data-stu-id="1651e-145">/xmp/microsoftphoto:rating</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="1651e-146">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="1651e-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1651e-147">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="1651e-147">Read Paths</span></span>



| <span data-ttu-id="1651e-148">JSON</span><span class="sxs-lookup"><span data-stu-id="1651e-148">Order</span></span> | <span data-ttu-id="1651e-149">Percorso</span><span class="sxs-lookup"><span data-stu-id="1651e-149">Path</span></span>                           | <span data-ttu-id="1651e-150">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1651e-150">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="1651e-151">1</span><span class="sxs-lookup"><span data-stu-id="1651e-151">1</span></span>     | <span data-ttu-id="1651e-152">/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="1651e-152">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="1651e-153">ushort</span><span class="sxs-lookup"><span data-stu-id="1651e-153">ushort</span></span>      |
| <span data-ttu-id="1651e-154">2</span><span class="sxs-lookup"><span data-stu-id="1651e-154">2</span></span>     | <span data-ttu-id="1651e-155">/ifd/xmp/MicrosoftPhoto: valutazione</span><span class="sxs-lookup"><span data-stu-id="1651e-155">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="1651e-156">unicode</span><span class="sxs-lookup"><span data-stu-id="1651e-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1651e-157">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="1651e-157">Write Paths</span></span>



| <span data-ttu-id="1651e-158">JSON</span><span class="sxs-lookup"><span data-stu-id="1651e-158">Order</span></span> | <span data-ttu-id="1651e-159">Percorso</span><span class="sxs-lookup"><span data-stu-id="1651e-159">Path</span></span>                           | <span data-ttu-id="1651e-160">Formato disco</span><span class="sxs-lookup"><span data-stu-id="1651e-160">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="1651e-161">1</span><span class="sxs-lookup"><span data-stu-id="1651e-161">1</span></span>     | <span data-ttu-id="1651e-162">/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="1651e-162">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="1651e-163">ushort</span><span class="sxs-lookup"><span data-stu-id="1651e-163">ushort</span></span>      |
| <span data-ttu-id="1651e-164">2</span><span class="sxs-lookup"><span data-stu-id="1651e-164">2</span></span>     | <span data-ttu-id="1651e-165">/ifd/xmp/MicrosoftPhoto: valutazione</span><span class="sxs-lookup"><span data-stu-id="1651e-165">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="1651e-166">unicode</span><span class="sxs-lookup"><span data-stu-id="1651e-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1651e-167">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="1651e-167">Remove Paths</span></span>



| <span data-ttu-id="1651e-168">JSON</span><span class="sxs-lookup"><span data-stu-id="1651e-168">Order</span></span> | <span data-ttu-id="1651e-169">Percorso</span><span class="sxs-lookup"><span data-stu-id="1651e-169">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="1651e-170">1</span><span class="sxs-lookup"><span data-stu-id="1651e-170">1</span></span>     | <span data-ttu-id="1651e-171">/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="1651e-171">/ifd/{ushort=18249}</span></span>            |
| <span data-ttu-id="1651e-172">2</span><span class="sxs-lookup"><span data-stu-id="1651e-172">2</span></span>     | <span data-ttu-id="1651e-173">/IFD/XMP/microsoftphoto: valutazione</span><span class="sxs-lookup"><span data-stu-id="1651e-173">/ifd/xmp/microsoftphoto:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1651e-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="1651e-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1651e-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1651e-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1651e-176">System. rating</span><span class="sxs-lookup"><span data-stu-id="1651e-176">System.Rating</span></span>](../properties/props-system-rating.md)
</dt> </dl>

 

 
