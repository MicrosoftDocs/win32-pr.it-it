---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestLatitudeRef.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: Criteri per i metadati delle foto di System. GPS. DestLatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314461"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a><span data-ttu-id="7e2c6-103">Criteri per i metadati delle foto di System. GPS. DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="7e2c6-103">System.GPS.DestLatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="7e2c6-104">Criteri per i metadati delle foto per la proprietà [System. GPS. DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="7e2c6-104">The photo metadata policy for the [System.GPS.DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7e2c6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="7e2c6-105">PKEY</span></span>

<span data-ttu-id="7e2c6-106">PKEY \_ GPS \_ DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="7e2c6-106">PKEY\_GPS\_DestLatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="7e2c6-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="7e2c6-107">Containers</span></span>

<span data-ttu-id="7e2c6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7e2c6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7e2c6-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="7e2c6-109">Read-Only</span></span>

<span data-ttu-id="7e2c6-110">No</span><span class="sxs-lookup"><span data-stu-id="7e2c6-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7e2c6-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="7e2c6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7e2c6-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="7e2c6-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="7e2c6-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="7e2c6-113">Input Type</span></span>

<span data-ttu-id="7e2c6-114">\_È preferibile LPWSTR VT, ma \_ viene accettato il LPSTR VT.</span><span class="sxs-lookup"><span data-stu-id="7e2c6-114">VT\_LPWSTR is preferred, but VT\_LPSTR is accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7e2c6-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="7e2c6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="7e2c6-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="7e2c6-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="7e2c6-117">Precedenza dei percorsi (JPEG)</span><span class="sxs-lookup"><span data-stu-id="7e2c6-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="7e2c6-118">Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="7e2c6-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="7e2c6-119">JSON</span><span class="sxs-lookup"><span data-stu-id="7e2c6-119">Order</span></span> | <span data-ttu-id="7e2c6-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="7e2c6-120">Path</span></span>                          | <span data-ttu-id="7e2c6-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="7e2c6-121">Disk Format</span></span> | <span data-ttu-id="7e2c6-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="7e2c6-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="7e2c6-123">1</span><span class="sxs-lookup"><span data-stu-id="7e2c6-123">1</span></span>     | <span data-ttu-id="7e2c6-124">/xmp/exif:GPSDestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="7e2c6-124">/xmp/exif:GPSDestLatitudeRef</span></span>  | <span data-ttu-id="7e2c6-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="7e2c6-125">Unicode</span></span>     | <span data-ttu-id="7e2c6-126">Sì</span><span class="sxs-lookup"><span data-stu-id="7e2c6-126">Yes</span></span>      |
| <span data-ttu-id="7e2c6-127">2</span><span class="sxs-lookup"><span data-stu-id="7e2c6-127">2</span></span>     | <span data-ttu-id="7e2c6-128">/App1/IFD/GPS/ \\ {ushort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="7e2c6-128">/app1/ifd/gps/\\{ushort=19\\}</span></span> | <span data-ttu-id="7e2c6-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="7e2c6-129">ASCII</span></span>       | <span data-ttu-id="7e2c6-130">No</span><span class="sxs-lookup"><span data-stu-id="7e2c6-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="7e2c6-131">Precedenza dei percorsi (TIFF)</span><span class="sxs-lookup"><span data-stu-id="7e2c6-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="7e2c6-132">Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="7e2c6-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="7e2c6-133">JSON</span><span class="sxs-lookup"><span data-stu-id="7e2c6-133">Order</span></span> | <span data-ttu-id="7e2c6-134">Percorso</span><span class="sxs-lookup"><span data-stu-id="7e2c6-134">Path</span></span>                             | <span data-ttu-id="7e2c6-135">Formato disco</span><span class="sxs-lookup"><span data-stu-id="7e2c6-135">Disk Format</span></span> | <span data-ttu-id="7e2c6-136">Necessario</span><span class="sxs-lookup"><span data-stu-id="7e2c6-136">Required</span></span> |
|-------|----------------------------------|-------------|----------|
| <span data-ttu-id="7e2c6-137">1</span><span class="sxs-lookup"><span data-stu-id="7e2c6-137">1</span></span>     | <span data-ttu-id="7e2c6-138">/ifd/xmp/exif:GPSDestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="7e2c6-138">/ifd/xmp/exif:GPSDestLatitudeRef</span></span> | <span data-ttu-id="7e2c6-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="7e2c6-139">Unicode</span></span>     | <span data-ttu-id="7e2c6-140">Sì</span><span class="sxs-lookup"><span data-stu-id="7e2c6-140">Yes</span></span>      |
| <span data-ttu-id="7e2c6-141">2</span><span class="sxs-lookup"><span data-stu-id="7e2c6-141">2</span></span>     | <span data-ttu-id="7e2c6-142">/IFD/GPS/ \\ {ushort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="7e2c6-142">/ifd/gps/\\{ushort=19\\}</span></span>         | <span data-ttu-id="7e2c6-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="7e2c6-143">ASCII</span></span>       | <span data-ttu-id="7e2c6-144">No</span><span class="sxs-lookup"><span data-stu-id="7e2c6-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="7e2c6-145">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7e2c6-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e2c6-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e2c6-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e2c6-147">System. GPS. DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="7e2c6-147">System.GPS.DestLatitudeRef</span></span>](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
