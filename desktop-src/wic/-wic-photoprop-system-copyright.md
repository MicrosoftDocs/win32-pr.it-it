---
description: Criteri per i metadati delle foto per la proprietà System. copyright.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Criteri per i metadati della foto System. Copyright
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc65024458d88088e3c0cbeccc3bc9ea0211910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317888"
---
# <a name="systemcopyright-photo-metadata-policy"></a><span data-ttu-id="939fe-103">Criteri per i metadati della foto System. Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-103">System.Copyright Photo Metadata Policy</span></span>

<span data-ttu-id="939fe-104">Criteri per i metadati delle foto per la proprietà [System. Copyright](../properties/props-system-copyright.md) .</span><span class="sxs-lookup"><span data-stu-id="939fe-104">The photo metadata policy for the [System.Copyright](../properties/props-system-copyright.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="939fe-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="939fe-105">PKEY</span></span>

<span data-ttu-id="939fe-106">\_Copyright pkey</span><span class="sxs-lookup"><span data-stu-id="939fe-106">PKEY\_Copyright</span></span>

### <a name="containers"></a><span data-ttu-id="939fe-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="939fe-107">Containers</span></span>

<span data-ttu-id="939fe-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="939fe-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="939fe-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="939fe-109">Read-Only</span></span>

<span data-ttu-id="939fe-110">No</span><span class="sxs-lookup"><span data-stu-id="939fe-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="939fe-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="939fe-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="939fe-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="939fe-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="939fe-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="939fe-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="939fe-114">string</span><span class="sxs-lookup"><span data-stu-id="939fe-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="939fe-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="939fe-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="939fe-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="939fe-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="939fe-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="939fe-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="939fe-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="939fe-118">Read Paths</span></span>



| <span data-ttu-id="939fe-119">JSON</span><span class="sxs-lookup"><span data-stu-id="939fe-119">Order</span></span> | <span data-ttu-id="939fe-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="939fe-120">Path</span></span>                                      | <span data-ttu-id="939fe-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="939fe-121">Disk Format</span></span> |
|-------|-------------------------------------------|-------------|
|       | <span data-ttu-id="939fe-122">/App1/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="939fe-122">/app1/ifd/{ushort=33432}</span></span>                  | <span data-ttu-id="939fe-123">ascii</span><span class="sxs-lookup"><span data-stu-id="939fe-123">ascii</span></span>       |
|       | <span data-ttu-id="939fe-124">avviso/App13/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-124">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="939fe-125">/XMP/ <xmpalt> DC: diritti</span><span class="sxs-lookup"><span data-stu-id="939fe-125">/xmp/<xmpalt>dc:rights</span></span>              | <span data-ttu-id="939fe-126">unicode</span><span class="sxs-lookup"><span data-stu-id="939fe-126">unicode</span></span>     |
|       | <span data-ttu-id="939fe-127">/XMP/DC: diritti</span><span class="sxs-lookup"><span data-stu-id="939fe-127">/xmp/dc:rights</span></span>                            | <span data-ttu-id="939fe-128">unicode</span><span class="sxs-lookup"><span data-stu-id="939fe-128">unicode</span></span>     |
|       | <span data-ttu-id="939fe-129">avviso/App13/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-129">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="939fe-130">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="939fe-130">Write Paths</span></span>



| <span data-ttu-id="939fe-131">JSON</span><span class="sxs-lookup"><span data-stu-id="939fe-131">Order</span></span> | <span data-ttu-id="939fe-132">Percorso</span><span class="sxs-lookup"><span data-stu-id="939fe-132">Path</span></span>                                      | <span data-ttu-id="939fe-133">Formato disco</span><span class="sxs-lookup"><span data-stu-id="939fe-133">Disk Format</span></span> |
|-------|-------------------------------------------|-------------|
|       | <span data-ttu-id="939fe-134">/XMP/DC: diritti</span><span class="sxs-lookup"><span data-stu-id="939fe-134">/xmp/dc:rights</span></span>                            | <span data-ttu-id="939fe-135">unicode</span><span class="sxs-lookup"><span data-stu-id="939fe-135">unicode</span></span>     |
|       | <span data-ttu-id="939fe-136">/XMP/ <xmpalt> DC: diritti</span><span class="sxs-lookup"><span data-stu-id="939fe-136">/xmp/<xmpalt>dc:rights</span></span>              | <span data-ttu-id="939fe-137">unicode</span><span class="sxs-lookup"><span data-stu-id="939fe-137">unicode</span></span>     |
|       | <span data-ttu-id="939fe-138">avviso/App13/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-138">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="939fe-139">/App1/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="939fe-139">/app1/ifd/{ushort=33432}</span></span>                  | <span data-ttu-id="939fe-140">ascii</span><span class="sxs-lookup"><span data-stu-id="939fe-140">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="939fe-141">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="939fe-141">Remove Paths</span></span>



| <span data-ttu-id="939fe-142">JSON</span><span class="sxs-lookup"><span data-stu-id="939fe-142">Order</span></span> | <span data-ttu-id="939fe-143">Percorso</span><span class="sxs-lookup"><span data-stu-id="939fe-143">Path</span></span>                                      |
|-------|-------------------------------------------|
|       | <span data-ttu-id="939fe-144">/XMP/DC: diritti</span><span class="sxs-lookup"><span data-stu-id="939fe-144">/xmp/dc:rights</span></span>                            |
|       | <span data-ttu-id="939fe-145">avviso/App13/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-145">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |
|       | <span data-ttu-id="939fe-146">/App1/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="939fe-146">/app1/ifd/{ushort=33432}</span></span>                  |



 

### <a name="tiff-policy"></a><span data-ttu-id="939fe-147">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="939fe-147">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="939fe-148">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="939fe-148">Read Paths</span></span>



| <span data-ttu-id="939fe-149">JSON</span><span class="sxs-lookup"><span data-stu-id="939fe-149">Order</span></span> | <span data-ttu-id="939fe-150">Percorso</span><span class="sxs-lookup"><span data-stu-id="939fe-150">Path</span></span>                                    | <span data-ttu-id="939fe-151">Formato disco</span><span class="sxs-lookup"><span data-stu-id="939fe-151">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
|       | <span data-ttu-id="939fe-152">/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="939fe-152">/ifd/{ushort=33432}</span></span>                     | <span data-ttu-id="939fe-153">ascii</span><span class="sxs-lookup"><span data-stu-id="939fe-153">ascii</span></span>       |
|       | <span data-ttu-id="939fe-154">avviso/IFD/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-154">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="939fe-155">/IFD/XMP/ <xmpalt> DC: diritti</span><span class="sxs-lookup"><span data-stu-id="939fe-155">/ifd/xmp/<xmpalt>dc:rights</span></span>        | <span data-ttu-id="939fe-156">unicode</span><span class="sxs-lookup"><span data-stu-id="939fe-156">unicode</span></span>     |
|       | <span data-ttu-id="939fe-157">/IFD/XMP/DC: diritti</span><span class="sxs-lookup"><span data-stu-id="939fe-157">/ifd/xmp/dc:rights</span></span>                      | <span data-ttu-id="939fe-158">unicode</span><span class="sxs-lookup"><span data-stu-id="939fe-158">unicode</span></span>     |
|       | <span data-ttu-id="939fe-159">avviso/IFD/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-159">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="939fe-160">avviso/IFD/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-160">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="939fe-161">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="939fe-161">Write Paths</span></span>



| <span data-ttu-id="939fe-162">JSON</span><span class="sxs-lookup"><span data-stu-id="939fe-162">Order</span></span> | <span data-ttu-id="939fe-163">Percorso</span><span class="sxs-lookup"><span data-stu-id="939fe-163">Path</span></span>                                    | <span data-ttu-id="939fe-164">Formato disco</span><span class="sxs-lookup"><span data-stu-id="939fe-164">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
|       | <span data-ttu-id="939fe-165">/IFD/XMP/DC: diritti</span><span class="sxs-lookup"><span data-stu-id="939fe-165">/ifd/xmp/dc:rights</span></span>                      | <span data-ttu-id="939fe-166">unicode</span><span class="sxs-lookup"><span data-stu-id="939fe-166">unicode</span></span>     |
|       | <span data-ttu-id="939fe-167">/IFD/XMP/ <xmpalt> DC: diritti</span><span class="sxs-lookup"><span data-stu-id="939fe-167">/ifd/xmp/<xmpalt>dc:rights</span></span>        | <span data-ttu-id="939fe-168">unicode</span><span class="sxs-lookup"><span data-stu-id="939fe-168">unicode</span></span>     |
|       | <span data-ttu-id="939fe-169">avviso/IFD/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-169">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="939fe-170">avviso/IFD/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-170">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="939fe-171">/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="939fe-171">/ifd/{ushort=33432}</span></span>                     | <span data-ttu-id="939fe-172">ascii</span><span class="sxs-lookup"><span data-stu-id="939fe-172">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="939fe-173">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="939fe-173">Remove Paths</span></span>



| <span data-ttu-id="939fe-174">JSON</span><span class="sxs-lookup"><span data-stu-id="939fe-174">Order</span></span> | <span data-ttu-id="939fe-175">Percorso</span><span class="sxs-lookup"><span data-stu-id="939fe-175">Path</span></span>                                    |
|-------|-----------------------------------------|
|       | <span data-ttu-id="939fe-176">/IFD/XMP/DC: diritti</span><span class="sxs-lookup"><span data-stu-id="939fe-176">/ifd/xmp/dc:rights</span></span>                      |
|       | <span data-ttu-id="939fe-177">avviso/IFD/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-177">/ifd/iptc/copyright notice</span></span>              |
|       | <span data-ttu-id="939fe-178">avviso/IFD/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-178">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |
|       | <span data-ttu-id="939fe-179">/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="939fe-179">/ifd/{ushort=33432}</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="939fe-180">Commenti</span><span class="sxs-lookup"><span data-stu-id="939fe-180">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="939fe-181">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="939fe-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="939fe-182">System. Copyright</span><span class="sxs-lookup"><span data-stu-id="939fe-182">System.Copyright</span></span>](../properties/props-system-copyright.md)
</dt> </dl>

 

 
