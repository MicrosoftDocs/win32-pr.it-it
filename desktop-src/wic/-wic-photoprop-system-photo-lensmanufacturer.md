---
description: Criteri per i metadati delle foto per la proprietà System. Photo. LensManufacturer.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Criteri per i metadati delle foto di System. Photo. LensManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232886"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a><span data-ttu-id="8a19a-103">Criteri per i metadati delle foto di System. Photo. LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="8a19a-103">System.Photo.LensManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="8a19a-104">Criteri per i metadati delle foto per la proprietà [System. Photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="8a19a-104">The photo metadata policy for the [System.Photo.LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8a19a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="8a19a-105">PKEY</span></span>

<span data-ttu-id="8a19a-106">PKEY \_ Photo \_ LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="8a19a-106">PKEY\_Photo\_LensManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="8a19a-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="8a19a-107">Containers</span></span>

<span data-ttu-id="8a19a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8a19a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8a19a-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="8a19a-109">Read-Only</span></span>

<span data-ttu-id="8a19a-110">No</span><span class="sxs-lookup"><span data-stu-id="8a19a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8a19a-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="8a19a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8a19a-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="8a19a-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="8a19a-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="8a19a-113">Input Type</span></span>

<span data-ttu-id="8a19a-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="8a19a-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8a19a-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="8a19a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="8a19a-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="8a19a-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="8a19a-117">Precedenza dei percorsi (JPEG)</span><span class="sxs-lookup"><span data-stu-id="8a19a-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="8a19a-118">Se il file è in formato JPEG, il gestore utilizzerà il percorso seguente durante la lettura o la scrittura dei dati.</span><span class="sxs-lookup"><span data-stu-id="8a19a-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="8a19a-119">JSON</span><span class="sxs-lookup"><span data-stu-id="8a19a-119">Order</span></span> | <span data-ttu-id="8a19a-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="8a19a-120">Path</span></span>                                 | <span data-ttu-id="8a19a-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="8a19a-121">Disk Format</span></span> | <span data-ttu-id="8a19a-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="8a19a-122">Required</span></span> |
|-------|--------------------------------------|-------------|----------|
| <span data-ttu-id="8a19a-123">1</span><span class="sxs-lookup"><span data-stu-id="8a19a-123">1</span></span>     | <span data-ttu-id="8a19a-124">/xmp/MicrosoftPhoto:LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="8a19a-124">/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="8a19a-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="8a19a-125">Unicode</span></span>     | <span data-ttu-id="8a19a-126">Sì</span><span class="sxs-lookup"><span data-stu-id="8a19a-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="8a19a-127">Precedenza dei percorsi (TIFF)</span><span class="sxs-lookup"><span data-stu-id="8a19a-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="8a19a-128">Se il file è in formato TIFF, il gestore utilizzerà l'ordine di precedenza seguente durante la lettura o la scrittura dei dati.</span><span class="sxs-lookup"><span data-stu-id="8a19a-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="8a19a-129">JSON</span><span class="sxs-lookup"><span data-stu-id="8a19a-129">Order</span></span> | <span data-ttu-id="8a19a-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="8a19a-130">Path</span></span>                                     | <span data-ttu-id="8a19a-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="8a19a-131">Disk Format</span></span> | <span data-ttu-id="8a19a-132">Necessario</span><span class="sxs-lookup"><span data-stu-id="8a19a-132">Required</span></span> |
|-------|------------------------------------------|-------------|----------|
| <span data-ttu-id="8a19a-133">1</span><span class="sxs-lookup"><span data-stu-id="8a19a-133">1</span></span>     | <span data-ttu-id="8a19a-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="8a19a-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="8a19a-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="8a19a-135">Unicode</span></span>     | <span data-ttu-id="8a19a-136">Sì</span><span class="sxs-lookup"><span data-stu-id="8a19a-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="8a19a-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a19a-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a19a-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a19a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a19a-139">System. Photo. LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="8a19a-139">System.Photo.LensManufacturer</span></span>](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
