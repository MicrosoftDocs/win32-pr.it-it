---
description: Criteri per i metadati delle foto per la proprietà System. GPS. Speed.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: Criteri per i metadati di Photo System. GPS. Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315973"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a><span data-ttu-id="6242b-103">Criteri per i metadati di Photo System. GPS. Speed</span><span class="sxs-lookup"><span data-stu-id="6242b-103">System.GPS.Speed Photo Metadata Policy</span></span>

<span data-ttu-id="6242b-104">Criteri per i metadati delle foto per la proprietà [System. GPS. Speed](../properties/props-system-gps-speed.md) .</span><span class="sxs-lookup"><span data-stu-id="6242b-104">The photo metadata policy for the [System.GPS.Speed](../properties/props-system-gps-speed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6242b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="6242b-105">PKEY</span></span>

<span data-ttu-id="6242b-106">\_Velocità GPS \_ pkey</span><span class="sxs-lookup"><span data-stu-id="6242b-106">PKEY\_GPS\_Speed</span></span>

### <a name="containers"></a><span data-ttu-id="6242b-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="6242b-107">Containers</span></span>

<span data-ttu-id="6242b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6242b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6242b-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="6242b-109">Read-Only</span></span>

<span data-ttu-id="6242b-110">Sì</span><span class="sxs-lookup"><span data-stu-id="6242b-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6242b-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="6242b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6242b-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="6242b-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6242b-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="6242b-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="6242b-114">Questo valore viene generato da System. GPS. SpeedNumerator e System. GPS. SpeedDenominator.</span><span class="sxs-lookup"><span data-stu-id="6242b-114">This value is generated from System.GPS.SpeedNumerator and System.GPS.SpeedDenominator.</span></span> <span data-ttu-id="6242b-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="6242b-115">It cannot be written directly.</span></span> <span data-ttu-id="6242b-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="6242b-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6242b-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="6242b-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6242b-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="6242b-118">Read Paths</span></span>



| <span data-ttu-id="6242b-119">JSON</span><span class="sxs-lookup"><span data-stu-id="6242b-119">Order</span></span> | <span data-ttu-id="6242b-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="6242b-120">Path</span></span>                      | <span data-ttu-id="6242b-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6242b-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="6242b-122">1</span><span class="sxs-lookup"><span data-stu-id="6242b-122">1</span></span>     | <span data-ttu-id="6242b-123">/App1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="6242b-123">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="6242b-124">2</span><span class="sxs-lookup"><span data-stu-id="6242b-124">2</span></span>     | <span data-ttu-id="6242b-125">/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="6242b-125">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="6242b-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="6242b-126">Write Paths</span></span>



| <span data-ttu-id="6242b-127">JSON</span><span class="sxs-lookup"><span data-stu-id="6242b-127">Order</span></span> | <span data-ttu-id="6242b-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="6242b-128">Path</span></span>                      | <span data-ttu-id="6242b-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6242b-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="6242b-130">1</span><span class="sxs-lookup"><span data-stu-id="6242b-130">1</span></span>     | <span data-ttu-id="6242b-131">/App1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="6242b-131">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="6242b-132">2</span><span class="sxs-lookup"><span data-stu-id="6242b-132">2</span></span>     | <span data-ttu-id="6242b-133">/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="6242b-133">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6242b-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="6242b-134">Remove Paths</span></span>



| <span data-ttu-id="6242b-135">JSON</span><span class="sxs-lookup"><span data-stu-id="6242b-135">Order</span></span> | <span data-ttu-id="6242b-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="6242b-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="6242b-137">1</span><span class="sxs-lookup"><span data-stu-id="6242b-137">1</span></span>     | <span data-ttu-id="6242b-138">/App1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="6242b-138">/app1/ifd/gps/{ushort=13}</span></span> |
| <span data-ttu-id="6242b-139">2</span><span class="sxs-lookup"><span data-stu-id="6242b-139">2</span></span>     | <span data-ttu-id="6242b-140">/xmp/exif:gpsspeed</span><span class="sxs-lookup"><span data-stu-id="6242b-140">/xmp/exif:gpsspeed</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="6242b-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="6242b-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6242b-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="6242b-142">Read Paths</span></span>



| <span data-ttu-id="6242b-143">JSON</span><span class="sxs-lookup"><span data-stu-id="6242b-143">Order</span></span> | <span data-ttu-id="6242b-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="6242b-144">Path</span></span>                   | <span data-ttu-id="6242b-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6242b-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="6242b-146">1</span><span class="sxs-lookup"><span data-stu-id="6242b-146">1</span></span>     | <span data-ttu-id="6242b-147">/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="6242b-147">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="6242b-148">2</span><span class="sxs-lookup"><span data-stu-id="6242b-148">2</span></span>     | <span data-ttu-id="6242b-149">/ifd/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="6242b-149">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="6242b-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="6242b-150">Write Paths</span></span>



| <span data-ttu-id="6242b-151">JSON</span><span class="sxs-lookup"><span data-stu-id="6242b-151">Order</span></span> | <span data-ttu-id="6242b-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="6242b-152">Path</span></span>                   | <span data-ttu-id="6242b-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="6242b-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="6242b-154">1</span><span class="sxs-lookup"><span data-stu-id="6242b-154">1</span></span>     | <span data-ttu-id="6242b-155">/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="6242b-155">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="6242b-156">2</span><span class="sxs-lookup"><span data-stu-id="6242b-156">2</span></span>     | <span data-ttu-id="6242b-157">/ifd/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="6242b-157">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6242b-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="6242b-158">Remove Paths</span></span>



| <span data-ttu-id="6242b-159">JSON</span><span class="sxs-lookup"><span data-stu-id="6242b-159">Order</span></span> | <span data-ttu-id="6242b-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="6242b-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="6242b-161">1</span><span class="sxs-lookup"><span data-stu-id="6242b-161">1</span></span>     | <span data-ttu-id="6242b-162">/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="6242b-162">/ifd/gps/{ushort=13}</span></span>   |
| <span data-ttu-id="6242b-163">2</span><span class="sxs-lookup"><span data-stu-id="6242b-163">2</span></span>     | <span data-ttu-id="6242b-164">/ifd/xmp/exif:gpsspeed</span><span class="sxs-lookup"><span data-stu-id="6242b-164">/ifd/xmp/exif:gpsspeed</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6242b-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="6242b-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6242b-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6242b-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6242b-167">System. GPS. Speed</span><span class="sxs-lookup"><span data-stu-id="6242b-167">System.GPS.Speed</span></span>](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
