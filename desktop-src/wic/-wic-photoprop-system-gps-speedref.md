---
description: Criteri per i metadati delle foto per la proprietà System. GPS. SpeedRef.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Criteri per i metadati delle foto di System. GPS. SpeedRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315972"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a><span data-ttu-id="8c316-103">Criteri per i metadati delle foto di System. GPS. SpeedRef</span><span class="sxs-lookup"><span data-stu-id="8c316-103">System.GPS.SpeedRef Photo Metadata Policy</span></span>

<span data-ttu-id="8c316-104">Criteri per i metadati delle foto per la proprietà [System. GPS. SpeedRef](../properties/props-system-gps-speedref.md) .</span><span class="sxs-lookup"><span data-stu-id="8c316-104">The photo metadata policy for the [System.GPS.SpeedRef](../properties/props-system-gps-speedref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8c316-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="8c316-105">PKEY</span></span>

<span data-ttu-id="8c316-106">PKEY \_ GPS \_ SpeedRef</span><span class="sxs-lookup"><span data-stu-id="8c316-106">PKEY\_GPS\_SpeedRef</span></span>

### <a name="containers"></a><span data-ttu-id="8c316-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="8c316-107">Containers</span></span>

<span data-ttu-id="8c316-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8c316-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8c316-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="8c316-109">Read-Only</span></span>

<span data-ttu-id="8c316-110">No</span><span class="sxs-lookup"><span data-stu-id="8c316-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8c316-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="8c316-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8c316-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="8c316-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="8c316-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="8c316-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="8c316-114">VT \_ LPWSTR è preferibile, ma \_ anche VT LPSTR è accettato.</span><span class="sxs-lookup"><span data-stu-id="8c316-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted..</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8c316-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="8c316-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="8c316-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="8c316-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="8c316-117">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="8c316-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8c316-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="8c316-118">Read Paths</span></span>



| <span data-ttu-id="8c316-119">JSON</span><span class="sxs-lookup"><span data-stu-id="8c316-119">Order</span></span> | <span data-ttu-id="8c316-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="8c316-120">Path</span></span>                      | <span data-ttu-id="8c316-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="8c316-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8c316-122">1</span><span class="sxs-lookup"><span data-stu-id="8c316-122">1</span></span>     | <span data-ttu-id="8c316-123">/App1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8c316-123">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="8c316-124">ascii</span><span class="sxs-lookup"><span data-stu-id="8c316-124">ascii</span></span>       |
| <span data-ttu-id="8c316-125">2</span><span class="sxs-lookup"><span data-stu-id="8c316-125">2</span></span>     | <span data-ttu-id="8c316-126">/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="8c316-126">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="8c316-127">unicode</span><span class="sxs-lookup"><span data-stu-id="8c316-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="8c316-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="8c316-128">Write Paths</span></span>



| <span data-ttu-id="8c316-129">JSON</span><span class="sxs-lookup"><span data-stu-id="8c316-129">Order</span></span> | <span data-ttu-id="8c316-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="8c316-130">Path</span></span>                      | <span data-ttu-id="8c316-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="8c316-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8c316-132">1</span><span class="sxs-lookup"><span data-stu-id="8c316-132">1</span></span>     | <span data-ttu-id="8c316-133">/App1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8c316-133">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="8c316-134">ascii</span><span class="sxs-lookup"><span data-stu-id="8c316-134">ascii</span></span>       |
| <span data-ttu-id="8c316-135">2</span><span class="sxs-lookup"><span data-stu-id="8c316-135">2</span></span>     | <span data-ttu-id="8c316-136">/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="8c316-136">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="8c316-137">unicode</span><span class="sxs-lookup"><span data-stu-id="8c316-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="8c316-138">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="8c316-138">Remove Paths</span></span>



| <span data-ttu-id="8c316-139">JSON</span><span class="sxs-lookup"><span data-stu-id="8c316-139">Order</span></span> | <span data-ttu-id="8c316-140">Percorso</span><span class="sxs-lookup"><span data-stu-id="8c316-140">Path</span></span>                      | <span data-ttu-id="8c316-141">Formato del disco</span><span class="sxs-lookup"><span data-stu-id="8c316-141">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8c316-142">1</span><span class="sxs-lookup"><span data-stu-id="8c316-142">1</span></span>     | <span data-ttu-id="8c316-143">/App1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8c316-143">/app1/ifd/gps/{ushort=12}</span></span> |             |
| <span data-ttu-id="8c316-144">2</span><span class="sxs-lookup"><span data-stu-id="8c316-144">2</span></span>     | <span data-ttu-id="8c316-145">/xmp/exif:gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="8c316-145">/xmp/exif:gpsspeedref</span></span>     |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="8c316-146">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="8c316-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8c316-147">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="8c316-147">Read Paths</span></span>



| <span data-ttu-id="8c316-148">JSON</span><span class="sxs-lookup"><span data-stu-id="8c316-148">Order</span></span> | <span data-ttu-id="8c316-149">Percorso</span><span class="sxs-lookup"><span data-stu-id="8c316-149">Path</span></span>                      |         |
|-------|---------------------------|---------|
| <span data-ttu-id="8c316-150">1</span><span class="sxs-lookup"><span data-stu-id="8c316-150">1</span></span>     | <span data-ttu-id="8c316-151">/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8c316-151">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="8c316-152">ascii</span><span class="sxs-lookup"><span data-stu-id="8c316-152">ascii</span></span>   |
| <span data-ttu-id="8c316-153">2</span><span class="sxs-lookup"><span data-stu-id="8c316-153">2</span></span>     | <span data-ttu-id="8c316-154">/ifd/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="8c316-154">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="8c316-155">unicode</span><span class="sxs-lookup"><span data-stu-id="8c316-155">unicode</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="8c316-156">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="8c316-156">Write Paths</span></span>



| <span data-ttu-id="8c316-157">JSON</span><span class="sxs-lookup"><span data-stu-id="8c316-157">Order</span></span> | <span data-ttu-id="8c316-158">Percorso</span><span class="sxs-lookup"><span data-stu-id="8c316-158">Path</span></span>                      | <span data-ttu-id="8c316-159">Formato disco</span><span class="sxs-lookup"><span data-stu-id="8c316-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8c316-160">1</span><span class="sxs-lookup"><span data-stu-id="8c316-160">1</span></span>     | <span data-ttu-id="8c316-161">/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8c316-161">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="8c316-162">ascii</span><span class="sxs-lookup"><span data-stu-id="8c316-162">ascii</span></span>       |
| <span data-ttu-id="8c316-163">2</span><span class="sxs-lookup"><span data-stu-id="8c316-163">2</span></span>     | <span data-ttu-id="8c316-164">/ifd/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="8c316-164">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="8c316-165">unicode</span><span class="sxs-lookup"><span data-stu-id="8c316-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="8c316-166">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="8c316-166">Remove Paths</span></span>



| <span data-ttu-id="8c316-167">JSON</span><span class="sxs-lookup"><span data-stu-id="8c316-167">Order</span></span> | <span data-ttu-id="8c316-168">Percorso</span><span class="sxs-lookup"><span data-stu-id="8c316-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="8c316-169">1</span><span class="sxs-lookup"><span data-stu-id="8c316-169">1</span></span>     | <span data-ttu-id="8c316-170">/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8c316-170">/ifd/gps/{ushort=12}</span></span>      |
| <span data-ttu-id="8c316-171">2</span><span class="sxs-lookup"><span data-stu-id="8c316-171">2</span></span>     | <span data-ttu-id="8c316-172">/ifd/xmp/exif:gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="8c316-172">/ifd/xmp/exif:gpsspeedref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8c316-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c316-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c316-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c316-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c316-175">System. GPS. SpeedRef</span><span class="sxs-lookup"><span data-stu-id="8c316-175">System.GPS.SpeedRef</span></span>](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
