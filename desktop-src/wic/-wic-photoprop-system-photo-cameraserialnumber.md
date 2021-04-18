---
description: Criteri per i metadati delle foto per la proprietà System. Photo. CameraSerialNumber.
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: Criteri per i metadati delle foto di System. Photo. CameraSerialNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c329cd4c56b49e39de5da97ac9d9f8b14bffb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317247"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a><span data-ttu-id="a3564-103">Criteri per i metadati delle foto di System. Photo. CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="a3564-103">System.Photo.CameraSerialNumber Photo Metadata Policy</span></span>

<span data-ttu-id="a3564-104">Criteri per i metadati delle foto per la proprietà [System. Photo. CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="a3564-104">The photo metadata policy for the [System.Photo.CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a3564-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a3564-105">PKEY</span></span>

<span data-ttu-id="a3564-106">PKEY \_ Photo \_ CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="a3564-106">PKEY\_Photo\_CameraSerialNumber</span></span>

### <a name="containers"></a><span data-ttu-id="a3564-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="a3564-107">Containers</span></span>

<span data-ttu-id="a3564-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a3564-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a3564-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="a3564-109">Read-Only</span></span>

<span data-ttu-id="a3564-110">No</span><span class="sxs-lookup"><span data-stu-id="a3564-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a3564-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="a3564-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a3564-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="a3564-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="a3564-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="a3564-113">Input Type</span></span>

<span data-ttu-id="a3564-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="a3564-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a3564-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="a3564-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a3564-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="a3564-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="a3564-117">Precedenza dei percorsi (JPEG)</span><span class="sxs-lookup"><span data-stu-id="a3564-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="a3564-118">Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore dal percorso seguente:</span><span class="sxs-lookup"><span data-stu-id="a3564-118">If the file is in JPEG format, the handler will read, write, and remove the data from the following path:</span></span>



| <span data-ttu-id="a3564-119">JSON</span><span class="sxs-lookup"><span data-stu-id="a3564-119">Order</span></span> | <span data-ttu-id="a3564-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="a3564-120">Path</span></span>                                   | <span data-ttu-id="a3564-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="a3564-121">Disk Format</span></span> | <span data-ttu-id="a3564-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="a3564-122">Required</span></span> |
|-------|----------------------------------------|-------------|----------|
| <span data-ttu-id="a3564-123">1</span><span class="sxs-lookup"><span data-stu-id="a3564-123">1</span></span>     | <span data-ttu-id="a3564-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="a3564-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="a3564-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="a3564-125">Unicode</span></span>     | <span data-ttu-id="a3564-126">Sì</span><span class="sxs-lookup"><span data-stu-id="a3564-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="a3564-127">Precedenza dei percorsi (TIFF)</span><span class="sxs-lookup"><span data-stu-id="a3564-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="a3564-128">Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi dal gestore dal percorso seguente</span><span class="sxs-lookup"><span data-stu-id="a3564-128">If the file is in TIFF format, the handler will read, write, and remove the data from the following path</span></span>



| <span data-ttu-id="a3564-129">JSON</span><span class="sxs-lookup"><span data-stu-id="a3564-129">Order</span></span> | <span data-ttu-id="a3564-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="a3564-130">Path</span></span>                                       | <span data-ttu-id="a3564-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="a3564-131">Disk Format</span></span> | <span data-ttu-id="a3564-132">Necessario</span><span class="sxs-lookup"><span data-stu-id="a3564-132">Required</span></span> |
|-------|--------------------------------------------|-------------|----------|
| <span data-ttu-id="a3564-133">1</span><span class="sxs-lookup"><span data-stu-id="a3564-133">1</span></span>     | <span data-ttu-id="a3564-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="a3564-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="a3564-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="a3564-135">Unicode</span></span>     | <span data-ttu-id="a3564-136">Sì</span><span class="sxs-lookup"><span data-stu-id="a3564-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="a3564-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3564-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3564-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3564-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3564-139">System. Photo. CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="a3564-139">System.Photo.CameraSerialNumber</span></span>](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
