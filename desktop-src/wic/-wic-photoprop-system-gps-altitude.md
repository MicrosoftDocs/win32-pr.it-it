---
description: Criteri per i metadati delle foto per la proprietà System. GPS. Altitude.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Criteri dei metadati della foto System. GPS. Altitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317886"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a><span data-ttu-id="b171d-103">Criteri dei metadati della foto System. GPS. Altitude</span><span class="sxs-lookup"><span data-stu-id="b171d-103">System.GPS.Altitude Photo Metadata Policy</span></span>

<span data-ttu-id="b171d-104">Criteri per i metadati delle foto per la proprietà [System. GPS. Altitude](../properties/props-system-gps-altitude.md) .</span><span class="sxs-lookup"><span data-stu-id="b171d-104">The photo metadata policy for the [System.GPS.Altitude](../properties/props-system-gps-altitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b171d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b171d-105">PKEY</span></span>

<span data-ttu-id="b171d-106">\_Altitudine GPS \_ pkey</span><span class="sxs-lookup"><span data-stu-id="b171d-106">PKEY\_GPS\_Altitude</span></span>

### <a name="description"></a><span data-ttu-id="b171d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b171d-107">Description</span></span>

<span data-ttu-id="b171d-108">L'altitudine è indicata come un valore assoluto a cui si fa riferimento in metri.</span><span class="sxs-lookup"><span data-stu-id="b171d-108">The altitude is indicated as an absolute value referenced in meters.</span></span>

### <a name="containers"></a><span data-ttu-id="b171d-109">Contenitori</span><span class="sxs-lookup"><span data-stu-id="b171d-109">Containers</span></span>

<span data-ttu-id="b171d-110">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b171d-110">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b171d-111">Read-Only</span><span class="sxs-lookup"><span data-stu-id="b171d-111">Read-Only</span></span>

<span data-ttu-id="b171d-112">Sì</span><span class="sxs-lookup"><span data-stu-id="b171d-112">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b171d-113">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="b171d-113">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b171d-114">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="b171d-114">VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="b171d-115">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="b171d-115">Input PROPVARIANT Type</span></span>

<span data-ttu-id="b171d-116">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="b171d-116">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b171d-117">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="b171d-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="b171d-118">Questo valore può essere scritto scrivendo in System. GPS. Altitude. numerator e System. GPS. Altitude. denominator.</span><span class="sxs-lookup"><span data-stu-id="b171d-118">This value can be written by writing to System.GPS.Altitude.Numerator and System.GPS.Altitude.Denominator.</span></span> <span data-ttu-id="b171d-119">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="b171d-119">It cannot be written directly.</span></span> <span data-ttu-id="b171d-120">I percorsi di scrittura nelle tabelle seguenti indicano la posizione in cui il valore può essere salvato quando viene generato e non quando viene scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="b171d-120">The write paths in the following tables indicate where the value may be saved when it is generated, not when it is written directly.</span></span> <span data-ttu-id="b171d-121">Quando viene letto il valore, i valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="b171d-121">When the value is read, values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b171d-122">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="b171d-122">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b171d-123">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="b171d-123">Read Paths</span></span>



| <span data-ttu-id="b171d-124">JSON</span><span class="sxs-lookup"><span data-stu-id="b171d-124">Order</span></span> | <span data-ttu-id="b171d-125">Percorso</span><span class="sxs-lookup"><span data-stu-id="b171d-125">Path</span></span>                     | <span data-ttu-id="b171d-126">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b171d-126">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b171d-127">1</span><span class="sxs-lookup"><span data-stu-id="b171d-127">1</span></span>     | <span data-ttu-id="b171d-128">/App1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="b171d-128">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="b171d-129">2</span><span class="sxs-lookup"><span data-stu-id="b171d-129">2</span></span>     | <span data-ttu-id="b171d-130">/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="b171d-130">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="b171d-131">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="b171d-131">Write Paths</span></span>



| <span data-ttu-id="b171d-132">JSON</span><span class="sxs-lookup"><span data-stu-id="b171d-132">Order</span></span> | <span data-ttu-id="b171d-133">Percorso</span><span class="sxs-lookup"><span data-stu-id="b171d-133">Path</span></span>                     | <span data-ttu-id="b171d-134">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b171d-134">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b171d-135">1</span><span class="sxs-lookup"><span data-stu-id="b171d-135">1</span></span>     | <span data-ttu-id="b171d-136">/App1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="b171d-136">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="b171d-137">2</span><span class="sxs-lookup"><span data-stu-id="b171d-137">2</span></span>     | <span data-ttu-id="b171d-138">/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="b171d-138">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b171d-139">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="b171d-139">Remove Paths</span></span>



| <span data-ttu-id="b171d-140">JSON</span><span class="sxs-lookup"><span data-stu-id="b171d-140">Order</span></span> | <span data-ttu-id="b171d-141">Percorso</span><span class="sxs-lookup"><span data-stu-id="b171d-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="b171d-142">1</span><span class="sxs-lookup"><span data-stu-id="b171d-142">1</span></span>     | <span data-ttu-id="b171d-143">/App1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="b171d-143">/app1/ifd/gps/{ushort=6}</span></span> |
| <span data-ttu-id="b171d-144">2</span><span class="sxs-lookup"><span data-stu-id="b171d-144">2</span></span>     | <span data-ttu-id="b171d-145">/xmp/exif:gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="b171d-145">/xmp/exif:gpsaltitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="b171d-146">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="b171d-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b171d-147">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="b171d-147">Read Paths</span></span>



| <span data-ttu-id="b171d-148">JSON</span><span class="sxs-lookup"><span data-stu-id="b171d-148">Order</span></span> | <span data-ttu-id="b171d-149">Percorso</span><span class="sxs-lookup"><span data-stu-id="b171d-149">Path</span></span>                      | <span data-ttu-id="b171d-150">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b171d-150">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b171d-151">1</span><span class="sxs-lookup"><span data-stu-id="b171d-151">1</span></span>     | <span data-ttu-id="b171d-152">/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="b171d-152">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="b171d-153">2</span><span class="sxs-lookup"><span data-stu-id="b171d-153">2</span></span>     | <span data-ttu-id="b171d-154">/ifd/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="b171d-154">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b171d-155">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="b171d-155">Write Paths</span></span>



| <span data-ttu-id="b171d-156">JSON</span><span class="sxs-lookup"><span data-stu-id="b171d-156">Order</span></span> | <span data-ttu-id="b171d-157">Percorso</span><span class="sxs-lookup"><span data-stu-id="b171d-157">Path</span></span>                      | <span data-ttu-id="b171d-158">Formato disco</span><span class="sxs-lookup"><span data-stu-id="b171d-158">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b171d-159">1</span><span class="sxs-lookup"><span data-stu-id="b171d-159">1</span></span>     | <span data-ttu-id="b171d-160">/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="b171d-160">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="b171d-161">2</span><span class="sxs-lookup"><span data-stu-id="b171d-161">2</span></span>     | <span data-ttu-id="b171d-162">/ifd/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="b171d-162">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b171d-163">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="b171d-163">Remove Paths</span></span>



| <span data-ttu-id="b171d-164">JSON</span><span class="sxs-lookup"><span data-stu-id="b171d-164">Order</span></span> | <span data-ttu-id="b171d-165">Percorso</span><span class="sxs-lookup"><span data-stu-id="b171d-165">Path</span></span>                      |     |
|-------|---------------------------|-----|
| <span data-ttu-id="b171d-166">1</span><span class="sxs-lookup"><span data-stu-id="b171d-166">1</span></span>     | <span data-ttu-id="b171d-167">/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="b171d-167">/ifd/gps/{ushort=6}</span></span>       |     |
| <span data-ttu-id="b171d-168">2</span><span class="sxs-lookup"><span data-stu-id="b171d-168">2</span></span>     | <span data-ttu-id="b171d-169">/ifd/xmp/exif:gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="b171d-169">/ifd/xmp/exif:gpsaltitude</span></span> |     |



 

## <a name="remarks"></a><span data-ttu-id="b171d-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="b171d-170">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b171d-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b171d-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b171d-172">System. GPS. Altitude</span><span class="sxs-lookup"><span data-stu-id="b171d-172">System.GPS.Altitude</span></span>](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
