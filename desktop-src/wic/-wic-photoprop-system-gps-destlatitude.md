---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestLatitude.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: Criteri per i metadati delle foto di System. GPS. DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192db0f8efc868e9457e86d283d9967e4692c95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317879"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a><span data-ttu-id="532be-103">Criteri per i metadati delle foto di System. GPS. DestLatitude</span><span class="sxs-lookup"><span data-stu-id="532be-103">System.GPS.DestLatitude Photo Metadata Policy</span></span>

<span data-ttu-id="532be-104">Criteri per i metadati delle foto per la proprietà [System. GPS. DestLatitude](../properties/props-system-gps-destlatitude.md) .</span><span class="sxs-lookup"><span data-stu-id="532be-104">The photo metadata policy for the [System.GPS.DestLatitude](../properties/props-system-gps-destlatitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="532be-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="532be-105">PKEY</span></span>

<span data-ttu-id="532be-106">PKEY \_ GPS \_ DestLatitude</span><span class="sxs-lookup"><span data-stu-id="532be-106">PKEY\_GPS\_DestLatitude</span></span>

### <a name="containers"></a><span data-ttu-id="532be-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="532be-107">Containers</span></span>

<span data-ttu-id="532be-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="532be-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="532be-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="532be-109">Read-Only</span></span>

<span data-ttu-id="532be-110">Sì</span><span class="sxs-lookup"><span data-stu-id="532be-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="532be-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="532be-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="532be-112">VT \_ vettore \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="532be-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="532be-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="532be-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="532be-114">VT \_ vettore \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="532be-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="532be-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="532be-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="532be-116">Questo valore viene generato da System. GPS. DestLatitudeNumerator e System. GPS. DestLatitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="532be-116">This value is generated from System.GPS.DestLatitudeNumerator and System.GPS.DestLatitudeDenominator.</span></span> <span data-ttu-id="532be-117">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="532be-117">It cannot be written directly.</span></span> <span data-ttu-id="532be-118">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="532be-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="532be-119">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="532be-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="532be-120">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="532be-120">Read Paths</span></span>



| <span data-ttu-id="532be-121">JSON</span><span class="sxs-lookup"><span data-stu-id="532be-121">Order</span></span> | <span data-ttu-id="532be-122">Percorso</span><span class="sxs-lookup"><span data-stu-id="532be-122">Path</span></span>                      | <span data-ttu-id="532be-123">Formato disco</span><span class="sxs-lookup"><span data-stu-id="532be-123">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="532be-124">1</span><span class="sxs-lookup"><span data-stu-id="532be-124">1</span></span>     | <span data-ttu-id="532be-125">/App1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="532be-125">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="532be-126">2</span><span class="sxs-lookup"><span data-stu-id="532be-126">2</span></span>     | <span data-ttu-id="532be-127">/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="532be-127">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="532be-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="532be-128">Write Paths</span></span>



| <span data-ttu-id="532be-129">JSON</span><span class="sxs-lookup"><span data-stu-id="532be-129">Order</span></span> | <span data-ttu-id="532be-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="532be-130">Path</span></span>                      | <span data-ttu-id="532be-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="532be-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="532be-132">1</span><span class="sxs-lookup"><span data-stu-id="532be-132">1</span></span>     | <span data-ttu-id="532be-133">/App1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="532be-133">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="532be-134">2</span><span class="sxs-lookup"><span data-stu-id="532be-134">2</span></span>     | <span data-ttu-id="532be-135">/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="532be-135">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="532be-136">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="532be-136">Remove Paths</span></span>



| <span data-ttu-id="532be-137">JSON</span><span class="sxs-lookup"><span data-stu-id="532be-137">Order</span></span> | <span data-ttu-id="532be-138">Percorso</span><span class="sxs-lookup"><span data-stu-id="532be-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="532be-139">1</span><span class="sxs-lookup"><span data-stu-id="532be-139">1</span></span>     | <span data-ttu-id="532be-140">/App1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="532be-140">/app1/ifd/gps/{ushort=20}</span></span> |
| <span data-ttu-id="532be-141">2</span><span class="sxs-lookup"><span data-stu-id="532be-141">2</span></span>     | <span data-ttu-id="532be-142">/xmp/exif:gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="532be-142">/xmp/exif:gpsdestlatitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="532be-143">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="532be-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="532be-144">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="532be-144">Read Paths</span></span>



| <span data-ttu-id="532be-145">JSON</span><span class="sxs-lookup"><span data-stu-id="532be-145">Order</span></span> | <span data-ttu-id="532be-146">Percorso</span><span class="sxs-lookup"><span data-stu-id="532be-146">Path</span></span>                          | <span data-ttu-id="532be-147">Formato disco</span><span class="sxs-lookup"><span data-stu-id="532be-147">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="532be-148">1</span><span class="sxs-lookup"><span data-stu-id="532be-148">1</span></span>     | <span data-ttu-id="532be-149">/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="532be-149">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="532be-150">2</span><span class="sxs-lookup"><span data-stu-id="532be-150">2</span></span>     | <span data-ttu-id="532be-151">/ifd/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="532be-151">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="532be-152">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="532be-152">Write Paths</span></span>



| <span data-ttu-id="532be-153">JSON</span><span class="sxs-lookup"><span data-stu-id="532be-153">Order</span></span> | <span data-ttu-id="532be-154">Percorso</span><span class="sxs-lookup"><span data-stu-id="532be-154">Path</span></span>                          | <span data-ttu-id="532be-155">Formato disco</span><span class="sxs-lookup"><span data-stu-id="532be-155">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="532be-156">1</span><span class="sxs-lookup"><span data-stu-id="532be-156">1</span></span>     | <span data-ttu-id="532be-157">/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="532be-157">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="532be-158">2</span><span class="sxs-lookup"><span data-stu-id="532be-158">2</span></span>     | <span data-ttu-id="532be-159">/ifd/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="532be-159">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="532be-160">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="532be-160">Remove Paths</span></span>



| <span data-ttu-id="532be-161">JSON</span><span class="sxs-lookup"><span data-stu-id="532be-161">Order</span></span> | <span data-ttu-id="532be-162">Percorso</span><span class="sxs-lookup"><span data-stu-id="532be-162">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="532be-163">1</span><span class="sxs-lookup"><span data-stu-id="532be-163">1</span></span>     | <span data-ttu-id="532be-164">/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="532be-164">/ifd/gps/{ushort=20}</span></span>          |
| <span data-ttu-id="532be-165">2</span><span class="sxs-lookup"><span data-stu-id="532be-165">2</span></span>     | <span data-ttu-id="532be-166">/ifd/xmp/exif:gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="532be-166">/ifd/xmp/exif:gpsdestlatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="532be-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="532be-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="532be-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="532be-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="532be-169">System. GPS. DestLatitude</span><span class="sxs-lookup"><span data-stu-id="532be-169">System.GPS.DestLatitude</span></span>](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
