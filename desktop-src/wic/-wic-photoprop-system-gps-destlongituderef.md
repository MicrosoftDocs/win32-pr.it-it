---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestLongitudeRef.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Criteri per i metadati delle foto di System. GPS. DestLongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317252"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a><span data-ttu-id="e4834-103">Criteri per i metadati delle foto di System. GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="e4834-103">System.GPS.DestLongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="e4834-104">Criteri per i metadati delle foto per la proprietà [System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="e4834-104">The photo metadata policy for the [System.GPS.DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e4834-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e4834-105">PKEY</span></span>

<span data-ttu-id="e4834-106">PKEY \_ GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="e4834-106">PKEY\_GPS.DestLongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="e4834-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="e4834-107">Containers</span></span>

<span data-ttu-id="e4834-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e4834-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e4834-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="e4834-109">Read-Only</span></span>

<span data-ttu-id="e4834-110">No</span><span class="sxs-lookup"><span data-stu-id="e4834-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e4834-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="e4834-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e4834-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="e4834-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="e4834-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="e4834-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="e4834-114">VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="e4834-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e4834-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="e4834-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e4834-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="e4834-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="e4834-117">Precedenza dei percorsi (JPEG)</span><span class="sxs-lookup"><span data-stu-id="e4834-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="e4834-118">Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="e4834-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="e4834-119">JSON</span><span class="sxs-lookup"><span data-stu-id="e4834-119">Order</span></span> | <span data-ttu-id="e4834-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="e4834-120">Path</span></span>                          | <span data-ttu-id="e4834-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e4834-121">Disk Format</span></span> | <span data-ttu-id="e4834-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="e4834-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="e4834-123">1</span><span class="sxs-lookup"><span data-stu-id="e4834-123">1</span></span>     | <span data-ttu-id="e4834-124">/xmp/exif:GPSDestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="e4834-124">/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="e4834-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="e4834-125">Unicode</span></span>     | <span data-ttu-id="e4834-126">Sì</span><span class="sxs-lookup"><span data-stu-id="e4834-126">Yes</span></span>      |
| <span data-ttu-id="e4834-127">2</span><span class="sxs-lookup"><span data-stu-id="e4834-127">2</span></span>     | <span data-ttu-id="e4834-128">/App1/IFD/GPS/ \\ {ushort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="e4834-128">/app1/ifd/gps/\\{ushort=21\\}</span></span> | <span data-ttu-id="e4834-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="e4834-129">ASCII</span></span>       | <span data-ttu-id="e4834-130">No</span><span class="sxs-lookup"><span data-stu-id="e4834-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="e4834-131">Precedenza dei percorsi (TIFF)</span><span class="sxs-lookup"><span data-stu-id="e4834-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="e4834-132">Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="e4834-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="e4834-133">JSON</span><span class="sxs-lookup"><span data-stu-id="e4834-133">Order</span></span> | <span data-ttu-id="e4834-134">Percorso</span><span class="sxs-lookup"><span data-stu-id="e4834-134">Path</span></span>                              | <span data-ttu-id="e4834-135">Formato disco</span><span class="sxs-lookup"><span data-stu-id="e4834-135">Disk Format</span></span> | <span data-ttu-id="e4834-136">Necessario</span><span class="sxs-lookup"><span data-stu-id="e4834-136">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="e4834-137">1</span><span class="sxs-lookup"><span data-stu-id="e4834-137">1</span></span>     | <span data-ttu-id="e4834-138">/ifd/xmp/exif:GPSDestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="e4834-138">/ifd/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="e4834-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="e4834-139">Unicode</span></span>     | <span data-ttu-id="e4834-140">Sì</span><span class="sxs-lookup"><span data-stu-id="e4834-140">Yes</span></span>      |
| <span data-ttu-id="e4834-141">2</span><span class="sxs-lookup"><span data-stu-id="e4834-141">2</span></span>     | <span data-ttu-id="e4834-142">/IFD/GPS/ \\ {ushort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="e4834-142">/ifd/gps/\\{ushort=21\\}</span></span>          | <span data-ttu-id="e4834-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="e4834-143">ASCII</span></span>       | <span data-ttu-id="e4834-144">No</span><span class="sxs-lookup"><span data-stu-id="e4834-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="e4834-145">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e4834-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4834-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4834-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4834-147">System. GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="e4834-147">System.GPS.DestLongitudeRef</span></span>](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
