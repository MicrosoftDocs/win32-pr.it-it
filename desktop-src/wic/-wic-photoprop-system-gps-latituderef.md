---
description: Criteri per i metadati delle foto per la proprietà System. GPS. LatitudeRef.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: Criteri per i metadati delle foto di System. GPS. LatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782fbcecbed90c9c75c1ae5fe9d5409496f842a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233022"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a><span data-ttu-id="c0014-103">Criteri per i metadati delle foto di System. GPS. LatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0014-103">System.GPS.LatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="c0014-104">Criteri per i metadati delle foto per la proprietà [System. GPS. LatitudeRef](../properties/props-system-gps-latitude.md) .</span><span class="sxs-lookup"><span data-stu-id="c0014-104">The photo metadata policy for the [System.GPS.LatitudeRef](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c0014-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c0014-105">PKEY</span></span>

<span data-ttu-id="c0014-106">PKEY \_ GPS \_ LatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0014-106">PKEY\_GPS\_LatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="c0014-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="c0014-107">Containers</span></span>

<span data-ttu-id="c0014-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c0014-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c0014-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="c0014-109">Read-Only</span></span>

<span data-ttu-id="c0014-110">No</span><span class="sxs-lookup"><span data-stu-id="c0014-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c0014-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="c0014-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c0014-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="c0014-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="c0014-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="c0014-113">Input Type</span></span>

<span data-ttu-id="c0014-114">VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="c0014-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c0014-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="c0014-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c0014-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="c0014-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="c0014-117">Precedenza dei percorsi (JPEG)</span><span class="sxs-lookup"><span data-stu-id="c0014-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="c0014-118">Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="c0014-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="c0014-119">JSON</span><span class="sxs-lookup"><span data-stu-id="c0014-119">Order</span></span> | <span data-ttu-id="c0014-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="c0014-120">Path</span></span>                         | <span data-ttu-id="c0014-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="c0014-121">Disk Format</span></span> | <span data-ttu-id="c0014-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="c0014-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="c0014-123">1</span><span class="sxs-lookup"><span data-stu-id="c0014-123">1</span></span>     | <span data-ttu-id="c0014-124">/xmp/exif:GPSLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0014-124">/xmp/exif:GPSLatitudeRef</span></span>     | <span data-ttu-id="c0014-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="c0014-125">Unicode</span></span>     | <span data-ttu-id="c0014-126">Sì</span><span class="sxs-lookup"><span data-stu-id="c0014-126">Yes</span></span>      |
| <span data-ttu-id="c0014-127">2</span><span class="sxs-lookup"><span data-stu-id="c0014-127">2</span></span>     | <span data-ttu-id="c0014-128">/App1/IFD/GPS/ \\ {ushort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="c0014-128">/app1/ifd/gps/\\{ushort=1\\}</span></span> | <span data-ttu-id="c0014-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="c0014-129">ASCII</span></span>       | <span data-ttu-id="c0014-130">No</span><span class="sxs-lookup"><span data-stu-id="c0014-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="c0014-131">Precedenza dei percorsi (TIFF)</span><span class="sxs-lookup"><span data-stu-id="c0014-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="c0014-132">Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="c0014-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="c0014-133">JSON</span><span class="sxs-lookup"><span data-stu-id="c0014-133">Order</span></span> | <span data-ttu-id="c0014-134">Percorso</span><span class="sxs-lookup"><span data-stu-id="c0014-134">Path</span></span>                         | <span data-ttu-id="c0014-135">Formato disco</span><span class="sxs-lookup"><span data-stu-id="c0014-135">Disk Format</span></span> | <span data-ttu-id="c0014-136">Necessario</span><span class="sxs-lookup"><span data-stu-id="c0014-136">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="c0014-137">1</span><span class="sxs-lookup"><span data-stu-id="c0014-137">1</span></span>     | <span data-ttu-id="c0014-138">/ifd/xmp/exif:GPSLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0014-138">/ifd/xmp/exif:GPSLatitudeRef</span></span> | <span data-ttu-id="c0014-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="c0014-139">Unicode</span></span>     | <span data-ttu-id="c0014-140">Sì</span><span class="sxs-lookup"><span data-stu-id="c0014-140">Yes</span></span>      |
| <span data-ttu-id="c0014-141">2</span><span class="sxs-lookup"><span data-stu-id="c0014-141">2</span></span>     | <span data-ttu-id="c0014-142">/IFD/GPS/ \\ {ushort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="c0014-142">/ifd/gps/\\{ushort=1\\}</span></span>      | <span data-ttu-id="c0014-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="c0014-143">ASCII</span></span>       | <span data-ttu-id="c0014-144">No</span><span class="sxs-lookup"><span data-stu-id="c0014-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="c0014-145">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c0014-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0014-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0014-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0014-147">System. GPS. LatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0014-147">System.GPS.LatitudeRef</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
