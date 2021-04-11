---
description: Criteri per i metadati delle foto per la proprietà System. GPS. AreaInformation.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Criteri per i metadati delle foto di System. GPS. AreaInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e14837da9ffa8b688caf1a544e222043988cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346416"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a><span data-ttu-id="c9f51-103">Criteri per i metadati delle foto di System. GPS. AreaInformation</span><span class="sxs-lookup"><span data-stu-id="c9f51-103">System.GPS.AreaInformation Photo Metadata Policy</span></span>

<span data-ttu-id="c9f51-104">Criteri per i metadati delle foto per la proprietà [System. GPS. AreaInformation](../properties/props-system-gps-areainformation.md) .</span><span class="sxs-lookup"><span data-stu-id="c9f51-104">The photo metadata policy for the [System.GPS.AreaInformation](../properties/props-system-gps-areainformation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c9f51-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c9f51-105">PKEY</span></span>

<span data-ttu-id="c9f51-106">PKEY \_ GPS \_ AreaInformation</span><span class="sxs-lookup"><span data-stu-id="c9f51-106">PKEY\_GPS\_AreaInformation</span></span>

### <a name="containers"></a><span data-ttu-id="c9f51-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="c9f51-107">Containers</span></span>

<span data-ttu-id="c9f51-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c9f51-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c9f51-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="c9f51-109">Read-Only</span></span>

<span data-ttu-id="c9f51-110">No</span><span class="sxs-lookup"><span data-stu-id="c9f51-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c9f51-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="c9f51-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c9f51-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="c9f51-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="c9f51-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="c9f51-113">Input Type</span></span>

<span data-ttu-id="c9f51-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="c9f51-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c9f51-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="c9f51-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c9f51-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="c9f51-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="c9f51-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="c9f51-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c9f51-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="c9f51-118">Read Paths</span></span>



| <span data-ttu-id="c9f51-119">JSON</span><span class="sxs-lookup"><span data-stu-id="c9f51-119">Order</span></span> | <span data-ttu-id="c9f51-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="c9f51-120">Path</span></span>                         | <span data-ttu-id="c9f51-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="c9f51-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="c9f51-122">1</span><span class="sxs-lookup"><span data-stu-id="c9f51-122">1</span></span>     | <span data-ttu-id="c9f51-123">/App1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="c9f51-123">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="c9f51-124">2</span><span class="sxs-lookup"><span data-stu-id="c9f51-124">2</span></span>     | <span data-ttu-id="c9f51-125">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="c9f51-125">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="c9f51-126">unicode</span><span class="sxs-lookup"><span data-stu-id="c9f51-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c9f51-127">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="c9f51-127">Write Paths</span></span>



| <span data-ttu-id="c9f51-128">JSON</span><span class="sxs-lookup"><span data-stu-id="c9f51-128">Order</span></span> | <span data-ttu-id="c9f51-129">Percorso</span><span class="sxs-lookup"><span data-stu-id="c9f51-129">Path</span></span>                         | <span data-ttu-id="c9f51-130">Formato disco</span><span class="sxs-lookup"><span data-stu-id="c9f51-130">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="c9f51-131">1</span><span class="sxs-lookup"><span data-stu-id="c9f51-131">1</span></span>     | <span data-ttu-id="c9f51-132">/App1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="c9f51-132">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="c9f51-133">2</span><span class="sxs-lookup"><span data-stu-id="c9f51-133">2</span></span>     | <span data-ttu-id="c9f51-134">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="c9f51-134">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="c9f51-135">unicode</span><span class="sxs-lookup"><span data-stu-id="c9f51-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c9f51-136">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="c9f51-136">Remove Paths</span></span>



| <span data-ttu-id="c9f51-137">JSON</span><span class="sxs-lookup"><span data-stu-id="c9f51-137">Order</span></span> | <span data-ttu-id="c9f51-138">Percorso</span><span class="sxs-lookup"><span data-stu-id="c9f51-138">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="c9f51-139">1</span><span class="sxs-lookup"><span data-stu-id="c9f51-139">1</span></span>     | <span data-ttu-id="c9f51-140">/App1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="c9f51-140">/app1/ifd/gps/{ushort=28}</span></span>    |
| <span data-ttu-id="c9f51-141">2</span><span class="sxs-lookup"><span data-stu-id="c9f51-141">2</span></span>     | <span data-ttu-id="c9f51-142">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="c9f51-142">/xmp/exif:GPSAreaInformation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="c9f51-143">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="c9f51-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c9f51-144">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="c9f51-144">Read Paths</span></span>



| <span data-ttu-id="c9f51-145">JSON</span><span class="sxs-lookup"><span data-stu-id="c9f51-145">Order</span></span> | <span data-ttu-id="c9f51-146">Percorso</span><span class="sxs-lookup"><span data-stu-id="c9f51-146">Path</span></span>                             | <span data-ttu-id="c9f51-147">Formato disco</span><span class="sxs-lookup"><span data-stu-id="c9f51-147">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="c9f51-148">1</span><span class="sxs-lookup"><span data-stu-id="c9f51-148">1</span></span>     | <span data-ttu-id="c9f51-149">/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="c9f51-149">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="c9f51-150">2</span><span class="sxs-lookup"><span data-stu-id="c9f51-150">2</span></span>     | <span data-ttu-id="c9f51-151">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="c9f51-151">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="c9f51-152">unicode</span><span class="sxs-lookup"><span data-stu-id="c9f51-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c9f51-153">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="c9f51-153">Write Paths</span></span>



| <span data-ttu-id="c9f51-154">JSON</span><span class="sxs-lookup"><span data-stu-id="c9f51-154">Order</span></span> | <span data-ttu-id="c9f51-155">Percorso</span><span class="sxs-lookup"><span data-stu-id="c9f51-155">Path</span></span>                             | <span data-ttu-id="c9f51-156">Formato disco</span><span class="sxs-lookup"><span data-stu-id="c9f51-156">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="c9f51-157">1</span><span class="sxs-lookup"><span data-stu-id="c9f51-157">1</span></span>     | <span data-ttu-id="c9f51-158">/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="c9f51-158">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="c9f51-159">2</span><span class="sxs-lookup"><span data-stu-id="c9f51-159">2</span></span>     | <span data-ttu-id="c9f51-160">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="c9f51-160">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="c9f51-161">unicode</span><span class="sxs-lookup"><span data-stu-id="c9f51-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c9f51-162">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="c9f51-162">Remove Paths</span></span>



| <span data-ttu-id="c9f51-163">JSON</span><span class="sxs-lookup"><span data-stu-id="c9f51-163">Order</span></span> | <span data-ttu-id="c9f51-164">Percorso</span><span class="sxs-lookup"><span data-stu-id="c9f51-164">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="c9f51-165">1</span><span class="sxs-lookup"><span data-stu-id="c9f51-165">1</span></span>     | <span data-ttu-id="c9f51-166">/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="c9f51-166">/ifd/gps/{ushort=28}</span></span>             |
| <span data-ttu-id="c9f51-167">2</span><span class="sxs-lookup"><span data-stu-id="c9f51-167">2</span></span>     | <span data-ttu-id="c9f51-168">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="c9f51-168">/ifd/xmp/exif:GPSAreaInformation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c9f51-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9f51-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9f51-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9f51-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9f51-171">System. GPS. AreaInformation</span><span class="sxs-lookup"><span data-stu-id="c9f51-171">System.GPS.AreaInformation</span></span>](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
