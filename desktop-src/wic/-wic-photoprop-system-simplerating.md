---
description: Criteri per i metadati delle foto per la proprietà System. SimpleRating.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: Criteri per i metadati delle foto System. SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058044"
---
# <a name="systemsimplerating-photo-metadata-policy"></a><span data-ttu-id="f5041-103">Criteri per i metadati delle foto System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="f5041-103">System.SimpleRating Photo Metadata Policy</span></span>

<span data-ttu-id="f5041-104">Criteri per i metadati delle foto per la proprietà [System. SimpleRating](../properties/props-system-simplerating.md) .</span><span class="sxs-lookup"><span data-stu-id="f5041-104">The photo metadata policy for the [System.SimpleRating](../properties/props-system-simplerating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f5041-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f5041-105">PKEY</span></span>

<span data-ttu-id="f5041-106">\_SIMPLERATING pkey</span><span class="sxs-lookup"><span data-stu-id="f5041-106">PKEY\_SimpleRating</span></span>

### <a name="containers"></a><span data-ttu-id="f5041-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="f5041-107">Containers</span></span>

<span data-ttu-id="f5041-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f5041-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f5041-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="f5041-109">Read-Only</span></span>

<span data-ttu-id="f5041-110">No</span><span class="sxs-lookup"><span data-stu-id="f5041-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f5041-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="f5041-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f5041-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="f5041-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="f5041-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="f5041-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="f5041-114">Può essere VT \_ Ui1, VT \_ UI2 o VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="f5041-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="f5041-115">Il valore integer può variare da 0 a 5.</span><span class="sxs-lookup"><span data-stu-id="f5041-115">The integer value may range from 0 to 5.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f5041-116">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="f5041-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="f5041-117">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="f5041-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f5041-118">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="f5041-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f5041-119">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="f5041-119">Read Paths</span></span>



| <span data-ttu-id="f5041-120">JSON</span><span class="sxs-lookup"><span data-stu-id="f5041-120">Order</span></span> | <span data-ttu-id="f5041-121">Percorso</span><span class="sxs-lookup"><span data-stu-id="f5041-121">Path</span></span>                     | <span data-ttu-id="f5041-122">Formato disco</span><span class="sxs-lookup"><span data-stu-id="f5041-122">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="f5041-123">1</span><span class="sxs-lookup"><span data-stu-id="f5041-123">1</span></span>     | <span data-ttu-id="f5041-124">/App1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="f5041-124">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="f5041-125">ushort</span><span class="sxs-lookup"><span data-stu-id="f5041-125">ushort</span></span>      |
| <span data-ttu-id="f5041-126">2</span><span class="sxs-lookup"><span data-stu-id="f5041-126">2</span></span>     | <span data-ttu-id="f5041-127">/XMP/XMP: valutazione</span><span class="sxs-lookup"><span data-stu-id="f5041-127">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="f5041-128">unicode</span><span class="sxs-lookup"><span data-stu-id="f5041-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f5041-129">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="f5041-129">Write Paths</span></span>



| <span data-ttu-id="f5041-130">JSON</span><span class="sxs-lookup"><span data-stu-id="f5041-130">Order</span></span> | <span data-ttu-id="f5041-131">Percorso</span><span class="sxs-lookup"><span data-stu-id="f5041-131">Path</span></span>                     | <span data-ttu-id="f5041-132">Formato disco</span><span class="sxs-lookup"><span data-stu-id="f5041-132">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="f5041-133">1</span><span class="sxs-lookup"><span data-stu-id="f5041-133">1</span></span>     | <span data-ttu-id="f5041-134">/App1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="f5041-134">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="f5041-135">ushort</span><span class="sxs-lookup"><span data-stu-id="f5041-135">ushort</span></span>      |
| <span data-ttu-id="f5041-136">2</span><span class="sxs-lookup"><span data-stu-id="f5041-136">2</span></span>     | <span data-ttu-id="f5041-137">/XMP/XMP: valutazione</span><span class="sxs-lookup"><span data-stu-id="f5041-137">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="f5041-138">unicode</span><span class="sxs-lookup"><span data-stu-id="f5041-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f5041-139">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="f5041-139">Remove Paths</span></span>



| <span data-ttu-id="f5041-140">JSON</span><span class="sxs-lookup"><span data-stu-id="f5041-140">Order</span></span> | <span data-ttu-id="f5041-141">Percorso</span><span class="sxs-lookup"><span data-stu-id="f5041-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="f5041-142">1</span><span class="sxs-lookup"><span data-stu-id="f5041-142">1</span></span>     | <span data-ttu-id="f5041-143">/App1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="f5041-143">/app1/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="f5041-144">2</span><span class="sxs-lookup"><span data-stu-id="f5041-144">2</span></span>     | <span data-ttu-id="f5041-145">/XMP/XMP: valutazione</span><span class="sxs-lookup"><span data-stu-id="f5041-145">/xmp/xmp:rating</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="f5041-146">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="f5041-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f5041-147">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="f5041-147">Read Paths</span></span>



| <span data-ttu-id="f5041-148">JSON</span><span class="sxs-lookup"><span data-stu-id="f5041-148">Order</span></span> | <span data-ttu-id="f5041-149">Percorso</span><span class="sxs-lookup"><span data-stu-id="f5041-149">Path</span></span>                | <span data-ttu-id="f5041-150">Formato disco</span><span class="sxs-lookup"><span data-stu-id="f5041-150">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="f5041-151">1</span><span class="sxs-lookup"><span data-stu-id="f5041-151">1</span></span>     | <span data-ttu-id="f5041-152">/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="f5041-152">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="f5041-153">ushort</span><span class="sxs-lookup"><span data-stu-id="f5041-153">ushort</span></span>      |
| <span data-ttu-id="f5041-154">2</span><span class="sxs-lookup"><span data-stu-id="f5041-154">2</span></span>     | <span data-ttu-id="f5041-155">/IFD/XMP/XMP: valutazione</span><span class="sxs-lookup"><span data-stu-id="f5041-155">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="f5041-156">unicode</span><span class="sxs-lookup"><span data-stu-id="f5041-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f5041-157">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="f5041-157">Write Paths</span></span>



| <span data-ttu-id="f5041-158">JSON</span><span class="sxs-lookup"><span data-stu-id="f5041-158">Order</span></span> | <span data-ttu-id="f5041-159">Percorso</span><span class="sxs-lookup"><span data-stu-id="f5041-159">Path</span></span>                | <span data-ttu-id="f5041-160">Formato disco</span><span class="sxs-lookup"><span data-stu-id="f5041-160">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="f5041-161">1</span><span class="sxs-lookup"><span data-stu-id="f5041-161">1</span></span>     | <span data-ttu-id="f5041-162">/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="f5041-162">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="f5041-163">ushort</span><span class="sxs-lookup"><span data-stu-id="f5041-163">ushort</span></span>      |
| <span data-ttu-id="f5041-164">2</span><span class="sxs-lookup"><span data-stu-id="f5041-164">2</span></span>     | <span data-ttu-id="f5041-165">/IFD/XMP/XMP: valutazione</span><span class="sxs-lookup"><span data-stu-id="f5041-165">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="f5041-166">unicode</span><span class="sxs-lookup"><span data-stu-id="f5041-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f5041-167">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="f5041-167">Remove Paths</span></span>



| <span data-ttu-id="f5041-168">JSON</span><span class="sxs-lookup"><span data-stu-id="f5041-168">Order</span></span> | <span data-ttu-id="f5041-169">Percorso</span><span class="sxs-lookup"><span data-stu-id="f5041-169">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="f5041-170">1</span><span class="sxs-lookup"><span data-stu-id="f5041-170">1</span></span>     | <span data-ttu-id="f5041-171">/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="f5041-171">/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="f5041-172">2</span><span class="sxs-lookup"><span data-stu-id="f5041-172">2</span></span>     | <span data-ttu-id="f5041-173">/IFD/XMP/XMP: valutazione</span><span class="sxs-lookup"><span data-stu-id="f5041-173">/ifd/xmp/xmp:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f5041-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5041-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5041-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5041-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5041-176">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="f5041-176">System.SimpleRating</span></span>](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
