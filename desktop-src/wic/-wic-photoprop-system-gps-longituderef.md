---
description: Criteri per i metadati delle foto per la proprietà System. GPS. LongitudeRef.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: Criteri per i metadati delle foto di System. GPS. LongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a93d37b59ca7c77bc05e049860cf4e2608eb60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317871"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a><span data-ttu-id="40355-103">Criteri per i metadati delle foto di System. GPS. LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="40355-103">System.GPS.LongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="40355-104">Criteri per i metadati delle foto per la proprietà [System. GPS. LongitudeRef](../properties/props-system-gps-longituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="40355-104">The photo metadata policy for the [System.GPS.LongitudeRef](../properties/props-system-gps-longituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="40355-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="40355-105">PKEY</span></span>

<span data-ttu-id="40355-106">PKEY \_ GPS \_ LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="40355-106">PKEY\_GPS\_LongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="40355-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="40355-107">Containers</span></span>

<span data-ttu-id="40355-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="40355-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="40355-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="40355-109">Read-Only</span></span>

<span data-ttu-id="40355-110">No</span><span class="sxs-lookup"><span data-stu-id="40355-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="40355-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="40355-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="40355-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="40355-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="40355-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="40355-113">Input Type</span></span>

<span data-ttu-id="40355-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="40355-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="40355-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="40355-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="40355-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="40355-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="40355-117">Precedenza dei percorsi (JPEG)</span><span class="sxs-lookup"><span data-stu-id="40355-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="40355-118">Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="40355-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="40355-119">JSON</span><span class="sxs-lookup"><span data-stu-id="40355-119">Order</span></span> | <span data-ttu-id="40355-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="40355-120">Path</span></span>                         | <span data-ttu-id="40355-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="40355-121">Disk Format</span></span> | <span data-ttu-id="40355-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="40355-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="40355-123">1</span><span class="sxs-lookup"><span data-stu-id="40355-123">1</span></span>     | <span data-ttu-id="40355-124">/xmp/exif:GPSLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="40355-124">/xmp/exif:GPSLongitudeRef</span></span>    | <span data-ttu-id="40355-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="40355-125">Unicode</span></span>     | <span data-ttu-id="40355-126">Sì</span><span class="sxs-lookup"><span data-stu-id="40355-126">Yes</span></span>      |
| <span data-ttu-id="40355-127">2</span><span class="sxs-lookup"><span data-stu-id="40355-127">2</span></span>     | <span data-ttu-id="40355-128">/App1/IFD/GPS/ \\ {ushort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="40355-128">/app1/ifd/gps/\\{ushort=3\\}</span></span> | <span data-ttu-id="40355-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="40355-129">ASCII</span></span>       | <span data-ttu-id="40355-130">No</span><span class="sxs-lookup"><span data-stu-id="40355-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="40355-131">Precedenza dei percorsi (TIFF)</span><span class="sxs-lookup"><span data-stu-id="40355-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="40355-132">Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="40355-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="40355-133">JSON</span><span class="sxs-lookup"><span data-stu-id="40355-133">Order</span></span> | <span data-ttu-id="40355-134">Percorso</span><span class="sxs-lookup"><span data-stu-id="40355-134">Path</span></span>                          | <span data-ttu-id="40355-135">Formato disco</span><span class="sxs-lookup"><span data-stu-id="40355-135">Disk Format</span></span> | <span data-ttu-id="40355-136">Necessario</span><span class="sxs-lookup"><span data-stu-id="40355-136">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="40355-137">1</span><span class="sxs-lookup"><span data-stu-id="40355-137">1</span></span>     | <span data-ttu-id="40355-138">/ifd/xmp/exif:GPSLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="40355-138">/ifd/xmp/exif:GPSLongitudeRef</span></span> | <span data-ttu-id="40355-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="40355-139">Unicode</span></span>     | <span data-ttu-id="40355-140">Sì</span><span class="sxs-lookup"><span data-stu-id="40355-140">Yes</span></span>      |
| <span data-ttu-id="40355-141">2</span><span class="sxs-lookup"><span data-stu-id="40355-141">2</span></span>     | <span data-ttu-id="40355-142">/IFD/GPS/ \\ {ushort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="40355-142">/ifd/gps/\\{ushort=3\\}</span></span>       | <span data-ttu-id="40355-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="40355-143">ASCII</span></span>       | <span data-ttu-id="40355-144">No</span><span class="sxs-lookup"><span data-stu-id="40355-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="40355-145">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="40355-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="40355-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40355-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40355-147">System. GPS. LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="40355-147">System.GPS.LongitudeRef</span></span>](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
