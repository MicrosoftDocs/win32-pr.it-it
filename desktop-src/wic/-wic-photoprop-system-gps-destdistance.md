---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestDistance.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: Criteri per i metadati delle foto di System. GPS. DestDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314465"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a><span data-ttu-id="ececc-103">Criteri per i metadati delle foto di System. GPS. DestDistance</span><span class="sxs-lookup"><span data-stu-id="ececc-103">System.GPS.DestDistance Photo Metadata Policy</span></span>

<span data-ttu-id="ececc-104">Criteri per i metadati delle foto per la proprietà [System. GPS. DestDistance](../properties/props-system-gps-destdistance.md) .</span><span class="sxs-lookup"><span data-stu-id="ececc-104">The photo metadata policy for the [System.GPS.DestDistance](../properties/props-system-gps-destdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ececc-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ececc-105">PKEY</span></span>

<span data-ttu-id="ececc-106">PKEY \_ GPS \_ DestDistance</span><span class="sxs-lookup"><span data-stu-id="ececc-106">PKEY\_GPS\_DestDistance</span></span>

### <a name="containers"></a><span data-ttu-id="ececc-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="ececc-107">Containers</span></span>

<span data-ttu-id="ececc-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ececc-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ececc-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="ececc-109">Read-Only</span></span>

<span data-ttu-id="ececc-110">Sì</span><span class="sxs-lookup"><span data-stu-id="ececc-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ececc-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="ececc-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ececc-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="ececc-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ececc-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="ececc-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="ececc-114">Questo valore viene generato da System. GPS. DestDistanceNumerator e System. GPS. DestDistanceDenominator.</span><span class="sxs-lookup"><span data-stu-id="ececc-114">This value is generated from System.GPS.DestDistanceNumerator and System.GPS.DestDistanceDenominator.</span></span> <span data-ttu-id="ececc-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="ececc-115">It cannot be written directly.</span></span> <span data-ttu-id="ececc-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="ececc-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ececc-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="ececc-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ececc-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="ececc-118">Read Paths</span></span>



| <span data-ttu-id="ececc-119">JSON</span><span class="sxs-lookup"><span data-stu-id="ececc-119">Order</span></span> | <span data-ttu-id="ececc-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="ececc-120">Path</span></span>                      | <span data-ttu-id="ececc-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ececc-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ececc-122">1</span><span class="sxs-lookup"><span data-stu-id="ececc-122">1</span></span>     | <span data-ttu-id="ececc-123">/App1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="ececc-123">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="ececc-124">2</span><span class="sxs-lookup"><span data-stu-id="ececc-124">2</span></span>     | <span data-ttu-id="ececc-125">/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="ececc-125">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ececc-126">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="ececc-126">Write Paths</span></span>



| <span data-ttu-id="ececc-127">JSON</span><span class="sxs-lookup"><span data-stu-id="ececc-127">Order</span></span> | <span data-ttu-id="ececc-128">Percorso</span><span class="sxs-lookup"><span data-stu-id="ececc-128">Path</span></span>                      | <span data-ttu-id="ececc-129">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ececc-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ececc-130">1</span><span class="sxs-lookup"><span data-stu-id="ececc-130">1</span></span>     | <span data-ttu-id="ececc-131">/App1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="ececc-131">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="ececc-132">2</span><span class="sxs-lookup"><span data-stu-id="ececc-132">2</span></span>     | <span data-ttu-id="ececc-133">/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="ececc-133">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ececc-134">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="ececc-134">Remove Paths</span></span>



| <span data-ttu-id="ececc-135">JSON</span><span class="sxs-lookup"><span data-stu-id="ececc-135">Order</span></span> | <span data-ttu-id="ececc-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="ececc-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="ececc-137">1</span><span class="sxs-lookup"><span data-stu-id="ececc-137">1</span></span>     | <span data-ttu-id="ececc-138">/App1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="ececc-138">/app1/ifd/gps/{ushort=26}</span></span> |
| <span data-ttu-id="ececc-139">2</span><span class="sxs-lookup"><span data-stu-id="ececc-139">2</span></span>     | <span data-ttu-id="ececc-140">/xmp/exif:gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="ececc-140">/xmp/exif:gpsdestdistance</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="ececc-141">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="ececc-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ececc-142">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="ececc-142">Read Paths</span></span>



| <span data-ttu-id="ececc-143">JSON</span><span class="sxs-lookup"><span data-stu-id="ececc-143">Order</span></span> | <span data-ttu-id="ececc-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="ececc-144">Path</span></span>                          | <span data-ttu-id="ececc-145">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ececc-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="ececc-146">1</span><span class="sxs-lookup"><span data-stu-id="ececc-146">1</span></span>     | <span data-ttu-id="ececc-147">/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="ececc-147">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="ececc-148">2</span><span class="sxs-lookup"><span data-stu-id="ececc-148">2</span></span>     | <span data-ttu-id="ececc-149">/ifd/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="ececc-149">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ececc-150">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="ececc-150">Write Paths</span></span>



| <span data-ttu-id="ececc-151">JSON</span><span class="sxs-lookup"><span data-stu-id="ececc-151">Order</span></span> | <span data-ttu-id="ececc-152">Percorso</span><span class="sxs-lookup"><span data-stu-id="ececc-152">Path</span></span>                          | <span data-ttu-id="ececc-153">Formato disco</span><span class="sxs-lookup"><span data-stu-id="ececc-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="ececc-154">1</span><span class="sxs-lookup"><span data-stu-id="ececc-154">1</span></span>     | <span data-ttu-id="ececc-155">/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="ececc-155">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="ececc-156">2</span><span class="sxs-lookup"><span data-stu-id="ececc-156">2</span></span>     | <span data-ttu-id="ececc-157">/ifd/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="ececc-157">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ececc-158">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="ececc-158">Remove Paths</span></span>



| <span data-ttu-id="ececc-159">JSON</span><span class="sxs-lookup"><span data-stu-id="ececc-159">Order</span></span> | <span data-ttu-id="ececc-160">Percorso</span><span class="sxs-lookup"><span data-stu-id="ececc-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="ececc-161">1</span><span class="sxs-lookup"><span data-stu-id="ececc-161">1</span></span>     | <span data-ttu-id="ececc-162">/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="ececc-162">/ifd/gps/{ushort=26}</span></span>          |
| <span data-ttu-id="ececc-163">2</span><span class="sxs-lookup"><span data-stu-id="ececc-163">2</span></span>     | <span data-ttu-id="ececc-164">/ifd/xmp/exif:gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="ececc-164">/ifd/xmp/exif:gpsdestdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ececc-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="ececc-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ececc-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ececc-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ececc-167">System. GPS. DestDistance</span><span class="sxs-lookup"><span data-stu-id="ececc-167">System.GPS.DestDistance</span></span>](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
