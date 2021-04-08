---
description: Criteri per i metadati delle foto per la proprietà System. GPS. MeasureMode.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Criteri per i metadati delle foto di System. GPS. MeasureMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967635"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a><span data-ttu-id="ae65a-103">Criteri per i metadati delle foto di System. GPS. MeasureMode</span><span class="sxs-lookup"><span data-stu-id="ae65a-103">System.GPS.MeasureMode Photo Metadata Policy</span></span>

<span data-ttu-id="ae65a-104">Criteri per i metadati delle foto per la proprietà [System. GPS. MeasureMode](../properties/props-system-gps-measuremode.md) .</span><span class="sxs-lookup"><span data-stu-id="ae65a-104">The photo metadata policy for the [System.GPS.MeasureMode](../properties/props-system-gps-measuremode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ae65a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ae65a-105">PKEY</span></span>

<span data-ttu-id="ae65a-106">PKEY \_ GPS \_ MeasureMode</span><span class="sxs-lookup"><span data-stu-id="ae65a-106">PKEY\_GPS\_MeasureMode</span></span>

### <a name="containers"></a><span data-ttu-id="ae65a-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="ae65a-107">Containers</span></span>

<span data-ttu-id="ae65a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ae65a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ae65a-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="ae65a-109">Read-Only</span></span>

<span data-ttu-id="ae65a-110">No</span><span class="sxs-lookup"><span data-stu-id="ae65a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ae65a-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="ae65a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ae65a-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="ae65a-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="ae65a-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="ae65a-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="ae65a-114">VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="ae65a-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ae65a-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="ae65a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ae65a-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="ae65a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="ae65a-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="ae65a-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ae65a-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="ae65a-118">Read Paths</span></span>



| <span data-ttu-id="ae65a-119">JSON</span><span class="sxs-lookup"><span data-stu-id="ae65a-119">Order</span></span> | <span data-ttu-id="ae65a-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="ae65a-120">Path</span></span>                      | <span data-ttu-id="ae65a-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ae65a-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ae65a-122">1</span><span class="sxs-lookup"><span data-stu-id="ae65a-122">1</span></span>     | <span data-ttu-id="ae65a-123">/App1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ae65a-123">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="ae65a-124">ascii</span><span class="sxs-lookup"><span data-stu-id="ae65a-124">ascii</span></span>       |
| <span data-ttu-id="ae65a-125">2</span><span class="sxs-lookup"><span data-stu-id="ae65a-125">2</span></span>     | <span data-ttu-id="ae65a-126">/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="ae65a-126">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="ae65a-127">unicode</span><span class="sxs-lookup"><span data-stu-id="ae65a-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ae65a-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="ae65a-128">Write Paths</span></span>



| <span data-ttu-id="ae65a-129">JSON</span><span class="sxs-lookup"><span data-stu-id="ae65a-129">Order</span></span> | <span data-ttu-id="ae65a-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="ae65a-130">Path</span></span>                      | <span data-ttu-id="ae65a-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ae65a-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ae65a-132">1</span><span class="sxs-lookup"><span data-stu-id="ae65a-132">1</span></span>     | <span data-ttu-id="ae65a-133">/App1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ae65a-133">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="ae65a-134">ascii</span><span class="sxs-lookup"><span data-stu-id="ae65a-134">ascii</span></span>       |
| <span data-ttu-id="ae65a-135">2</span><span class="sxs-lookup"><span data-stu-id="ae65a-135">2</span></span>     | <span data-ttu-id="ae65a-136">/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="ae65a-136">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="ae65a-137">unicode</span><span class="sxs-lookup"><span data-stu-id="ae65a-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ae65a-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="ae65a-138">Remove Paths</span></span>



| <span data-ttu-id="ae65a-139">JSON</span><span class="sxs-lookup"><span data-stu-id="ae65a-139">Order</span></span> | <span data-ttu-id="ae65a-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="ae65a-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="ae65a-141">1</span><span class="sxs-lookup"><span data-stu-id="ae65a-141">1</span></span>     | <span data-ttu-id="ae65a-142">/App1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ae65a-142">/app1/ifd/gps/{ushort=10}</span></span> |
| <span data-ttu-id="ae65a-143">2</span><span class="sxs-lookup"><span data-stu-id="ae65a-143">2</span></span>     | <span data-ttu-id="ae65a-144">/xmp/exif:gpsmeasuremode</span><span class="sxs-lookup"><span data-stu-id="ae65a-144">/xmp/exif:gpsmeasuremode</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="ae65a-145">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="ae65a-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ae65a-146">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="ae65a-146">Read Paths</span></span>



| <span data-ttu-id="ae65a-147">JSON</span><span class="sxs-lookup"><span data-stu-id="ae65a-147">Order</span></span> | <span data-ttu-id="ae65a-148">Percorso</span><span class="sxs-lookup"><span data-stu-id="ae65a-148">Path</span></span>                         | <span data-ttu-id="ae65a-149">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ae65a-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="ae65a-150">1</span><span class="sxs-lookup"><span data-stu-id="ae65a-150">1</span></span>     | <span data-ttu-id="ae65a-151">/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ae65a-151">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="ae65a-152">ascii</span><span class="sxs-lookup"><span data-stu-id="ae65a-152">ascii</span></span>       |
| <span data-ttu-id="ae65a-153">2</span><span class="sxs-lookup"><span data-stu-id="ae65a-153">2</span></span>     | <span data-ttu-id="ae65a-154">/ifd/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="ae65a-154">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="ae65a-155">unicode</span><span class="sxs-lookup"><span data-stu-id="ae65a-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ae65a-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="ae65a-156">Write Paths</span></span>



| <span data-ttu-id="ae65a-157">JSON</span><span class="sxs-lookup"><span data-stu-id="ae65a-157">Order</span></span> | <span data-ttu-id="ae65a-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="ae65a-158">Path</span></span>                         | <span data-ttu-id="ae65a-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ae65a-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="ae65a-160">1</span><span class="sxs-lookup"><span data-stu-id="ae65a-160">1</span></span>     | <span data-ttu-id="ae65a-161">/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ae65a-161">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="ae65a-162">ascii</span><span class="sxs-lookup"><span data-stu-id="ae65a-162">ascii</span></span>       |
| <span data-ttu-id="ae65a-163">2</span><span class="sxs-lookup"><span data-stu-id="ae65a-163">2</span></span>     | <span data-ttu-id="ae65a-164">/ifd/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="ae65a-164">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="ae65a-165">unicode</span><span class="sxs-lookup"><span data-stu-id="ae65a-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ae65a-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="ae65a-166">Remove Paths</span></span>



| <span data-ttu-id="ae65a-167">JSON</span><span class="sxs-lookup"><span data-stu-id="ae65a-167">Order</span></span> | <span data-ttu-id="ae65a-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="ae65a-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="ae65a-169">1</span><span class="sxs-lookup"><span data-stu-id="ae65a-169">1</span></span>     | <span data-ttu-id="ae65a-170">/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="ae65a-170">/ifd/gps/{ushort=10}</span></span>         |
| <span data-ttu-id="ae65a-171">2</span><span class="sxs-lookup"><span data-stu-id="ae65a-171">2</span></span>     | <span data-ttu-id="ae65a-172">/ifd/xmp/exif:gpsmeasuremode</span><span class="sxs-lookup"><span data-stu-id="ae65a-172">/ifd/xmp/exif:gpsmeasuremode</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ae65a-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae65a-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae65a-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ae65a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae65a-175">System. GPS. MeasureMode</span><span class="sxs-lookup"><span data-stu-id="ae65a-175">System.GPS.MeasureMode</span></span>](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
