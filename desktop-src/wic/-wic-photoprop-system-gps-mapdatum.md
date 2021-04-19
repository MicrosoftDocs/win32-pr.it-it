---
description: Criteri per i metadati delle foto per la proprietà System. GPS. MapDatum.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Criteri per i metadati delle foto di System. GPS. MapDatum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317870"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a><span data-ttu-id="48799-103">Criteri per i metadati delle foto di System. GPS. MapDatum</span><span class="sxs-lookup"><span data-stu-id="48799-103">System.GPS.MapDatum Photo Metadata Policy</span></span>

<span data-ttu-id="48799-104">Criteri per i metadati delle foto per la proprietà [System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md) .</span><span class="sxs-lookup"><span data-stu-id="48799-104">The photo metadata policy for the [System.GPS.MapDatum](../properties/props-system-gps-mapdatum.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="48799-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="48799-105">PKEY</span></span>

<span data-ttu-id="48799-106">PKEY \_ GPS \_ MapDatum</span><span class="sxs-lookup"><span data-stu-id="48799-106">PKEY\_GPS\_MapDatum</span></span>

### <a name="containers"></a><span data-ttu-id="48799-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="48799-107">Containers</span></span>

<span data-ttu-id="48799-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="48799-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="48799-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="48799-109">Read-Only</span></span>

<span data-ttu-id="48799-110">No</span><span class="sxs-lookup"><span data-stu-id="48799-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="48799-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="48799-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="48799-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="48799-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="48799-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="48799-113">Input Type</span></span>

<span data-ttu-id="48799-114">VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR</span><span class="sxs-lookup"><span data-stu-id="48799-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="48799-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="48799-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="48799-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="48799-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="48799-117">Precedenza dei percorsi (JPEG)</span><span class="sxs-lookup"><span data-stu-id="48799-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="48799-118">Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="48799-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="48799-119">JSON</span><span class="sxs-lookup"><span data-stu-id="48799-119">Order</span></span> | <span data-ttu-id="48799-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="48799-120">Path</span></span>                          | <span data-ttu-id="48799-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="48799-121">Disk Format</span></span> | <span data-ttu-id="48799-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="48799-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="48799-123">1</span><span class="sxs-lookup"><span data-stu-id="48799-123">1</span></span>     | <span data-ttu-id="48799-124">/xmp/exif:GPSMapDatum</span><span class="sxs-lookup"><span data-stu-id="48799-124">/xmp/exif:GPSMapDatum</span></span>         | <span data-ttu-id="48799-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="48799-125">Unicode</span></span>     | <span data-ttu-id="48799-126">Sì</span><span class="sxs-lookup"><span data-stu-id="48799-126">Yes</span></span>      |
| <span data-ttu-id="48799-127">2</span><span class="sxs-lookup"><span data-stu-id="48799-127">2</span></span>     | <span data-ttu-id="48799-128">/App1/IFD/GPS/ \\ {ushort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="48799-128">/app1/ifd/gps/\\{ushort=18\\}</span></span> | <span data-ttu-id="48799-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="48799-129">ASCII</span></span>       | <span data-ttu-id="48799-130">No</span><span class="sxs-lookup"><span data-stu-id="48799-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="48799-131">Precedenza dei percorsi (TIFF)</span><span class="sxs-lookup"><span data-stu-id="48799-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="48799-132">Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="48799-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="48799-133">JSON</span><span class="sxs-lookup"><span data-stu-id="48799-133">Order</span></span> | <span data-ttu-id="48799-134">Percorso</span><span class="sxs-lookup"><span data-stu-id="48799-134">Path</span></span>                      | <span data-ttu-id="48799-135">Formato disco</span><span class="sxs-lookup"><span data-stu-id="48799-135">Disk Format</span></span> | <span data-ttu-id="48799-136">Necessario</span><span class="sxs-lookup"><span data-stu-id="48799-136">Required</span></span> |
|-------|---------------------------|-------------|----------|
| <span data-ttu-id="48799-137">1</span><span class="sxs-lookup"><span data-stu-id="48799-137">1</span></span>     | <span data-ttu-id="48799-138">/ifd/xmp/exif:GPSMapDatum</span><span class="sxs-lookup"><span data-stu-id="48799-138">/ifd/xmp/exif:GPSMapDatum</span></span> | <span data-ttu-id="48799-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="48799-139">Unicode</span></span>     | <span data-ttu-id="48799-140">Sì</span><span class="sxs-lookup"><span data-stu-id="48799-140">Yes</span></span>      |
| <span data-ttu-id="48799-141">2</span><span class="sxs-lookup"><span data-stu-id="48799-141">2</span></span>     | <span data-ttu-id="48799-142">/IFD/GPS/ \\ {ushort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="48799-142">/ifd/gps/\\{ushort=18\\}</span></span>  | <span data-ttu-id="48799-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="48799-143">ASCII</span></span>       | <span data-ttu-id="48799-144">No</span><span class="sxs-lookup"><span data-stu-id="48799-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="48799-145">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="48799-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="48799-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48799-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48799-147">System. GPS. MapDatum</span><span class="sxs-lookup"><span data-stu-id="48799-147">System.GPS.MapDatum</span></span>](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
