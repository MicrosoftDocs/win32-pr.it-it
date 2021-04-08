---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Criteri dei metadati delle foto di System. GPS. DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968412"
---
# <a name="systemgpsdop-photo-metadata-policy"></a><span data-ttu-id="bc0eb-103">Criteri dei metadati delle foto di System. GPS. DOP</span><span class="sxs-lookup"><span data-stu-id="bc0eb-103">System.GPS.DOP Photo Metadata Policy</span></span>

<span data-ttu-id="bc0eb-104">Criteri per i metadati delle foto per la proprietà [System. GPS. DOP](../properties/props-system-gps-dop.md) .</span><span class="sxs-lookup"><span data-stu-id="bc0eb-104">The photo metadata policy for the [System.GPS.DOP](../properties/props-system-gps-dop.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bc0eb-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="bc0eb-105">PKEY</span></span>

<span data-ttu-id="bc0eb-106">PKEY \_ GPS \_ DOP</span><span class="sxs-lookup"><span data-stu-id="bc0eb-106">PKEY\_GPS\_DOP</span></span>

### <a name="containers"></a><span data-ttu-id="bc0eb-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="bc0eb-107">Containers</span></span>

<span data-ttu-id="bc0eb-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="bc0eb-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bc0eb-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="bc0eb-109">Read-Only</span></span>

<span data-ttu-id="bc0eb-110">Sì</span><span class="sxs-lookup"><span data-stu-id="bc0eb-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="bc0eb-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="bc0eb-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="bc0eb-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="bc0eb-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bc0eb-113">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="bc0eb-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="bc0eb-114">Questo valore può essere scritto scrivendo in System. GPS. DOPNumerator e System. GPS. DOPDenominator.</span><span class="sxs-lookup"><span data-stu-id="bc0eb-114">This value can be written by writing to System.GPS.DOPNumerator and System.GPS.DOPDenominator.</span></span> <span data-ttu-id="bc0eb-115">Non può essere scritto direttamente.</span><span class="sxs-lookup"><span data-stu-id="bc0eb-115">It cannot be written directly.</span></span> <span data-ttu-id="bc0eb-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="bc0eb-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="bc0eb-117">Precedenza dei percorsi (JPEG)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="bc0eb-118">Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="bc0eb-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="bc0eb-119">JSON</span><span class="sxs-lookup"><span data-stu-id="bc0eb-119">Order</span></span> | <span data-ttu-id="bc0eb-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="bc0eb-120">Path</span></span>                          | <span data-ttu-id="bc0eb-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="bc0eb-121">Disk Format</span></span>   | <span data-ttu-id="bc0eb-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="bc0eb-122">Required</span></span> |
|-------|-------------------------------|---------------|----------|
| <span data-ttu-id="bc0eb-123">1</span><span class="sxs-lookup"><span data-stu-id="bc0eb-123">1</span></span>     | <span data-ttu-id="bc0eb-124">/xmp/exif:GPSDOP</span><span class="sxs-lookup"><span data-stu-id="bc0eb-124">/xmp/exif:GPSDOP</span></span>              | <span data-ttu-id="bc0eb-125">Razionale XMP</span><span class="sxs-lookup"><span data-stu-id="bc0eb-125">XMP rational</span></span>  | <span data-ttu-id="bc0eb-126">Sì</span><span class="sxs-lookup"><span data-stu-id="bc0eb-126">Yes</span></span>      |
| <span data-ttu-id="bc0eb-127">2</span><span class="sxs-lookup"><span data-stu-id="bc0eb-127">2</span></span>     | <span data-ttu-id="bc0eb-128">/App1/IFD/GPS/ \\ {ushort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="bc0eb-128">/app1/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="bc0eb-129">Razionale EXIF</span><span class="sxs-lookup"><span data-stu-id="bc0eb-129">EXIF rational</span></span> | <span data-ttu-id="bc0eb-130">No</span><span class="sxs-lookup"><span data-stu-id="bc0eb-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="bc0eb-131">Precedenza dei percorsi (TIFF)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="bc0eb-132">Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="bc0eb-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="bc0eb-133">JSON</span><span class="sxs-lookup"><span data-stu-id="bc0eb-133">Order</span></span> | <span data-ttu-id="bc0eb-134">Percorso</span><span class="sxs-lookup"><span data-stu-id="bc0eb-134">Path</span></span>                     | <span data-ttu-id="bc0eb-135">Formato disco</span><span class="sxs-lookup"><span data-stu-id="bc0eb-135">Disk Format</span></span>   | <span data-ttu-id="bc0eb-136">Necessario</span><span class="sxs-lookup"><span data-stu-id="bc0eb-136">Required</span></span> |
|-------|--------------------------|---------------|----------|
| <span data-ttu-id="bc0eb-137">1</span><span class="sxs-lookup"><span data-stu-id="bc0eb-137">1</span></span>     | <span data-ttu-id="bc0eb-138">/ifd/xmp/exif:GPSDop</span><span class="sxs-lookup"><span data-stu-id="bc0eb-138">/ifd/xmp/exif:GPSDop</span></span>     | <span data-ttu-id="bc0eb-139">Razionale XMP</span><span class="sxs-lookup"><span data-stu-id="bc0eb-139">XMP rational</span></span>  | <span data-ttu-id="bc0eb-140">Sì</span><span class="sxs-lookup"><span data-stu-id="bc0eb-140">Yes</span></span>      |
| <span data-ttu-id="bc0eb-141">2</span><span class="sxs-lookup"><span data-stu-id="bc0eb-141">2</span></span>     | <span data-ttu-id="bc0eb-142">/IFD/GPS/ \\ {ushort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="bc0eb-142">/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="bc0eb-143">Razionale EXIF</span><span class="sxs-lookup"><span data-stu-id="bc0eb-143">EXIF rational</span></span> | <span data-ttu-id="bc0eb-144">No</span><span class="sxs-lookup"><span data-stu-id="bc0eb-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="bc0eb-145">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="bc0eb-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc0eb-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc0eb-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc0eb-147">System. GPS. DOP</span><span class="sxs-lookup"><span data-stu-id="bc0eb-147">System.GPS.DOP</span></span>](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
