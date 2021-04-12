---
description: Criteri per i metadati delle foto per la proprietà System. GPS. date.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: Criteri dei metadati della foto System. GPS. date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233537"
---
# <a name="systemgpsdate-photo-metadata-policy"></a><span data-ttu-id="c4b38-103">Criteri dei metadati della foto System. GPS. date</span><span class="sxs-lookup"><span data-stu-id="c4b38-103">System.GPS.Date Photo Metadata Policy</span></span>

<span data-ttu-id="c4b38-104">Criteri per i metadati delle foto per la proprietà [System. GPS. date](../properties/props-system-gps-date.md) .</span><span class="sxs-lookup"><span data-stu-id="c4b38-104">The photo metadata policy for the [System.GPS.Date](../properties/props-system-gps-date.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c4b38-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c4b38-105">PKEY</span></span>

<span data-ttu-id="c4b38-106">\_Data GPS \_ pkey</span><span class="sxs-lookup"><span data-stu-id="c4b38-106">PKEY\_GPS\_Date</span></span>

### <a name="containers"></a><span data-ttu-id="c4b38-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="c4b38-107">Containers</span></span>

<span data-ttu-id="c4b38-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c4b38-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c4b38-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="c4b38-109">Read-Only</span></span>

<span data-ttu-id="c4b38-110">No</span><span class="sxs-lookup"><span data-stu-id="c4b38-110">No</span></span>

### <a name="input-type"></a><span data-ttu-id="c4b38-111">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="c4b38-111">Input Type</span></span>

<span data-ttu-id="c4b38-112">Stringa.</span><span class="sxs-lookup"><span data-stu-id="c4b38-112">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c4b38-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="c4b38-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="c4b38-114">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="c4b38-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="c4b38-115">Criteri di JPEG</span><span class="sxs-lookup"><span data-stu-id="c4b38-115">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c4b38-116">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="c4b38-116">Read Paths</span></span>



| <span data-ttu-id="c4b38-117">JSON</span><span class="sxs-lookup"><span data-stu-id="c4b38-117">Order</span></span> | <span data-ttu-id="c4b38-118">Percorso</span><span class="sxs-lookup"><span data-stu-id="c4b38-118">Path</span></span>                      | <span data-ttu-id="c4b38-119">Formato disco</span><span class="sxs-lookup"><span data-stu-id="c4b38-119">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c4b38-120">1</span><span class="sxs-lookup"><span data-stu-id="c4b38-120">1</span></span>     | <span data-ttu-id="c4b38-121">/App1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="c4b38-121">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="c4b38-122">ascii</span><span class="sxs-lookup"><span data-stu-id="c4b38-122">ascii</span></span>       |
| <span data-ttu-id="c4b38-123">2</span><span class="sxs-lookup"><span data-stu-id="c4b38-123">2</span></span>     | <span data-ttu-id="c4b38-124">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="c4b38-124">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="c4b38-125">unicode</span><span class="sxs-lookup"><span data-stu-id="c4b38-125">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c4b38-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="c4b38-126">Write Paths</span></span>



| <span data-ttu-id="c4b38-127">JSON</span><span class="sxs-lookup"><span data-stu-id="c4b38-127">Order</span></span> | <span data-ttu-id="c4b38-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="c4b38-128">Path</span></span>                      | <span data-ttu-id="c4b38-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="c4b38-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c4b38-130">1</span><span class="sxs-lookup"><span data-stu-id="c4b38-130">1</span></span>     | <span data-ttu-id="c4b38-131">/App1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="c4b38-131">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="c4b38-132">ascii</span><span class="sxs-lookup"><span data-stu-id="c4b38-132">ascii</span></span>       |
| <span data-ttu-id="c4b38-133">2</span><span class="sxs-lookup"><span data-stu-id="c4b38-133">2</span></span>     | <span data-ttu-id="c4b38-134">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="c4b38-134">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="c4b38-135">unicode</span><span class="sxs-lookup"><span data-stu-id="c4b38-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c4b38-136">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="c4b38-136">Remove Paths</span></span>



| <span data-ttu-id="c4b38-137">JSON</span><span class="sxs-lookup"><span data-stu-id="c4b38-137">Order</span></span> | <span data-ttu-id="c4b38-138">Percorso</span><span class="sxs-lookup"><span data-stu-id="c4b38-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="c4b38-139">1</span><span class="sxs-lookup"><span data-stu-id="c4b38-139">1</span></span>     | <span data-ttu-id="c4b38-140">/App1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="c4b38-140">/app1/ifd/gps/{ushort=29}</span></span> |
| <span data-ttu-id="c4b38-141">2</span><span class="sxs-lookup"><span data-stu-id="c4b38-141">2</span></span>     | <span data-ttu-id="c4b38-142">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="c4b38-142">/xmp/exif:GPSTimeStamp</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="c4b38-143">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="c4b38-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c4b38-144">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="c4b38-144">Read Paths</span></span>



| <span data-ttu-id="c4b38-145">JSON</span><span class="sxs-lookup"><span data-stu-id="c4b38-145">Order</span></span> | <span data-ttu-id="c4b38-146">Percorso</span><span class="sxs-lookup"><span data-stu-id="c4b38-146">Path</span></span>                       | <span data-ttu-id="c4b38-147">Formato disco</span><span class="sxs-lookup"><span data-stu-id="c4b38-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="c4b38-148">1</span><span class="sxs-lookup"><span data-stu-id="c4b38-148">1</span></span>     | <span data-ttu-id="c4b38-149">/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="c4b38-149">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="c4b38-150">ascii</span><span class="sxs-lookup"><span data-stu-id="c4b38-150">ascii</span></span>       |
| <span data-ttu-id="c4b38-151">2</span><span class="sxs-lookup"><span data-stu-id="c4b38-151">2</span></span>     | <span data-ttu-id="c4b38-152">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="c4b38-152">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="c4b38-153">unicode</span><span class="sxs-lookup"><span data-stu-id="c4b38-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c4b38-154">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="c4b38-154">Write Paths</span></span>



| <span data-ttu-id="c4b38-155">JSON</span><span class="sxs-lookup"><span data-stu-id="c4b38-155">Order</span></span> | <span data-ttu-id="c4b38-156">Percorso</span><span class="sxs-lookup"><span data-stu-id="c4b38-156">Path</span></span>                       | <span data-ttu-id="c4b38-157">Formato disco</span><span class="sxs-lookup"><span data-stu-id="c4b38-157">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="c4b38-158">1</span><span class="sxs-lookup"><span data-stu-id="c4b38-158">1</span></span>     | <span data-ttu-id="c4b38-159">/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="c4b38-159">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="c4b38-160">ascii</span><span class="sxs-lookup"><span data-stu-id="c4b38-160">ascii</span></span>       |
| <span data-ttu-id="c4b38-161">2</span><span class="sxs-lookup"><span data-stu-id="c4b38-161">2</span></span>     | <span data-ttu-id="c4b38-162">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="c4b38-162">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="c4b38-163">unicode</span><span class="sxs-lookup"><span data-stu-id="c4b38-163">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c4b38-164">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="c4b38-164">Remove Paths</span></span>



| <span data-ttu-id="c4b38-165">JSON</span><span class="sxs-lookup"><span data-stu-id="c4b38-165">Order</span></span> | <span data-ttu-id="c4b38-166">Percorso</span><span class="sxs-lookup"><span data-stu-id="c4b38-166">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="c4b38-167">1</span><span class="sxs-lookup"><span data-stu-id="c4b38-167">1</span></span>     | <span data-ttu-id="c4b38-168">/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="c4b38-168">/ifd/gps/{ushort=29}</span></span>       |
| <span data-ttu-id="c4b38-169">2</span><span class="sxs-lookup"><span data-stu-id="c4b38-169">2</span></span>     | <span data-ttu-id="c4b38-170">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="c4b38-170">/ifd/xmp/exif:GPSTimeStamp</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c4b38-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4b38-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4b38-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4b38-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4b38-173">System. GPS. date</span><span class="sxs-lookup"><span data-stu-id="c4b38-173">System.GPS.Date</span></span>](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
