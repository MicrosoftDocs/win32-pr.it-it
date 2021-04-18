---
description: Criteri per i metadati delle foto per la proprietà System. GPS. VersionId.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Criteri per i metadati delle foto System. GPS. VersionId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312959"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a><span data-ttu-id="3f0c7-103">Criteri per i metadati delle foto System. GPS. VersionId</span><span class="sxs-lookup"><span data-stu-id="3f0c7-103">System.GPS.VersionID Photo Metadata Policy</span></span>

<span data-ttu-id="3f0c7-104">Criteri per i metadati delle foto per la proprietà [System. GPS. VersionId](../properties/props-system-gps-versionid.md) .</span><span class="sxs-lookup"><span data-stu-id="3f0c7-104">The photo metadata policy for the [System.GPS.VersionID](../properties/props-system-gps-versionid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3f0c7-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3f0c7-105">PKEY</span></span>

<span data-ttu-id="3f0c7-106">PKEY \_ GPS \_ VersionId</span><span class="sxs-lookup"><span data-stu-id="3f0c7-106">PKEY\_GPS\_VersionID</span></span>

### <a name="containers"></a><span data-ttu-id="3f0c7-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="3f0c7-107">Containers</span></span>

<span data-ttu-id="3f0c7-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3f0c7-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3f0c7-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="3f0c7-109">Read-Only</span></span>

<span data-ttu-id="3f0c7-110">No</span><span class="sxs-lookup"><span data-stu-id="3f0c7-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3f0c7-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="3f0c7-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3f0c7-112">\_ \| interfaccia utente VT vettore VT \_</span><span class="sxs-lookup"><span data-stu-id="3f0c7-112">VT\_VECTOR \| VT\_UI</span></span>

### <a name="input-type"></a><span data-ttu-id="3f0c7-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="3f0c7-113">Input Type</span></span>

<span data-ttu-id="3f0c7-114">Buffer</span><span class="sxs-lookup"><span data-stu-id="3f0c7-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3f0c7-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="3f0c7-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3f0c7-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="3f0c7-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="3f0c7-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="3f0c7-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3f0c7-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="3f0c7-118">Read Paths</span></span>



| <span data-ttu-id="3f0c7-119">JSON</span><span class="sxs-lookup"><span data-stu-id="3f0c7-119">Order</span></span> | <span data-ttu-id="3f0c7-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="3f0c7-120">Path</span></span>                     | <span data-ttu-id="3f0c7-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="3f0c7-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="3f0c7-122">1</span><span class="sxs-lookup"><span data-stu-id="3f0c7-122">1</span></span>     | <span data-ttu-id="3f0c7-123">/App1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3f0c7-123">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="3f0c7-124">2</span><span class="sxs-lookup"><span data-stu-id="3f0c7-124">2</span></span>     | <span data-ttu-id="3f0c7-125">/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="3f0c7-125">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="3f0c7-126">unicode</span><span class="sxs-lookup"><span data-stu-id="3f0c7-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3f0c7-127">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="3f0c7-127">Write Paths</span></span>



| <span data-ttu-id="3f0c7-128">JSON</span><span class="sxs-lookup"><span data-stu-id="3f0c7-128">Order</span></span> | <span data-ttu-id="3f0c7-129">Percorso</span><span class="sxs-lookup"><span data-stu-id="3f0c7-129">Path</span></span>                     | <span data-ttu-id="3f0c7-130">Formato disco</span><span class="sxs-lookup"><span data-stu-id="3f0c7-130">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="3f0c7-131">1</span><span class="sxs-lookup"><span data-stu-id="3f0c7-131">1</span></span>     | <span data-ttu-id="3f0c7-132">/App1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3f0c7-132">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="3f0c7-133">2</span><span class="sxs-lookup"><span data-stu-id="3f0c7-133">2</span></span>     | <span data-ttu-id="3f0c7-134">/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="3f0c7-134">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="3f0c7-135">unicode</span><span class="sxs-lookup"><span data-stu-id="3f0c7-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3f0c7-136">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="3f0c7-136">Remove Paths</span></span>



| <span data-ttu-id="3f0c7-137">JSON</span><span class="sxs-lookup"><span data-stu-id="3f0c7-137">Order</span></span> | <span data-ttu-id="3f0c7-138">Percorso</span><span class="sxs-lookup"><span data-stu-id="3f0c7-138">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="3f0c7-139">1</span><span class="sxs-lookup"><span data-stu-id="3f0c7-139">1</span></span>     | <span data-ttu-id="3f0c7-140">/App1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3f0c7-140">/app1/ifd/gps/{ushort=0}</span></span> |
| <span data-ttu-id="3f0c7-141">2</span><span class="sxs-lookup"><span data-stu-id="3f0c7-141">2</span></span>     | <span data-ttu-id="3f0c7-142">/xmp/exif:gpsversionid</span><span class="sxs-lookup"><span data-stu-id="3f0c7-142">/xmp/exif:gpsversionid</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="3f0c7-143">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="3f0c7-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3f0c7-144">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="3f0c7-144">Read Paths</span></span>



| <span data-ttu-id="3f0c7-145">JSON</span><span class="sxs-lookup"><span data-stu-id="3f0c7-145">Order</span></span> | <span data-ttu-id="3f0c7-146">Percorso</span><span class="sxs-lookup"><span data-stu-id="3f0c7-146">Path</span></span>                       | <span data-ttu-id="3f0c7-147">Formato disco</span><span class="sxs-lookup"><span data-stu-id="3f0c7-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="3f0c7-148">1</span><span class="sxs-lookup"><span data-stu-id="3f0c7-148">1</span></span>     | <span data-ttu-id="3f0c7-149">/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3f0c7-149">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="3f0c7-150">2</span><span class="sxs-lookup"><span data-stu-id="3f0c7-150">2</span></span>     | <span data-ttu-id="3f0c7-151">/ifd/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="3f0c7-151">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="3f0c7-152">unicode</span><span class="sxs-lookup"><span data-stu-id="3f0c7-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3f0c7-153">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="3f0c7-153">Write Paths</span></span>



| <span data-ttu-id="3f0c7-154">JSON</span><span class="sxs-lookup"><span data-stu-id="3f0c7-154">Order</span></span> | <span data-ttu-id="3f0c7-155">Percorso</span><span class="sxs-lookup"><span data-stu-id="3f0c7-155">Path</span></span>                       | <span data-ttu-id="3f0c7-156">Formato disco</span><span class="sxs-lookup"><span data-stu-id="3f0c7-156">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="3f0c7-157">1</span><span class="sxs-lookup"><span data-stu-id="3f0c7-157">1</span></span>     | <span data-ttu-id="3f0c7-158">/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3f0c7-158">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="3f0c7-159">2</span><span class="sxs-lookup"><span data-stu-id="3f0c7-159">2</span></span>     | <span data-ttu-id="3f0c7-160">/ifd/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="3f0c7-160">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="3f0c7-161">unicode</span><span class="sxs-lookup"><span data-stu-id="3f0c7-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3f0c7-162">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="3f0c7-162">Remove Paths</span></span>



| <span data-ttu-id="3f0c7-163">JSON</span><span class="sxs-lookup"><span data-stu-id="3f0c7-163">Order</span></span> | <span data-ttu-id="3f0c7-164">Percorso</span><span class="sxs-lookup"><span data-stu-id="3f0c7-164">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="3f0c7-165">1</span><span class="sxs-lookup"><span data-stu-id="3f0c7-165">1</span></span>     | <span data-ttu-id="3f0c7-166">/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3f0c7-166">/ifd/gps/{ushort=0}</span></span>        |
| <span data-ttu-id="3f0c7-167">2</span><span class="sxs-lookup"><span data-stu-id="3f0c7-167">2</span></span>     | <span data-ttu-id="3f0c7-168">/ifd/xmp/exif:gpsversionid</span><span class="sxs-lookup"><span data-stu-id="3f0c7-168">/ifd/xmp/exif:gpsversionid</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3f0c7-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f0c7-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f0c7-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f0c7-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f0c7-171">System. GPS. VersionId</span><span class="sxs-lookup"><span data-stu-id="3f0c7-171">System.GPS.VersionID</span></span>](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
