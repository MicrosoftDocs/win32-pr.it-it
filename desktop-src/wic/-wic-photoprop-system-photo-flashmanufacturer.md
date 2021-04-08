---
description: Criteri per i metadati delle foto per la proprietà System. Photo. FlashManufacturer.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Criteri per i metadati delle foto di System. Photo. FlashManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058189"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a><span data-ttu-id="f845a-103">Criteri per i metadati delle foto di System. Photo. FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="f845a-103">System.Photo.FlashManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="f845a-104">Criteri per i metadati delle foto per la proprietà [System. Photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="f845a-104">The photo metadata policy for the [System.Photo.FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f845a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f845a-105">PKEY</span></span>

<span data-ttu-id="f845a-106">PKEY \_ Photo \_ FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="f845a-106">PKEY\_Photo\_FlashManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="f845a-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="f845a-107">Containers</span></span>

<span data-ttu-id="f845a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f845a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f845a-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="f845a-109">Read-Only</span></span>

<span data-ttu-id="f845a-110">No</span><span class="sxs-lookup"><span data-stu-id="f845a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f845a-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="f845a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f845a-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="f845a-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="f845a-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="f845a-113">Input Type</span></span>

<span data-ttu-id="f845a-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="f845a-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f845a-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="f845a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f845a-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="f845a-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="f845a-117">Precedenza dei percorsi (JPEG)</span><span class="sxs-lookup"><span data-stu-id="f845a-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="f845a-118">Se il file è in formato JPEG, il gestore utilizzerà il percorso seguente durante la lettura o la scrittura dei dati.</span><span class="sxs-lookup"><span data-stu-id="f845a-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="f845a-119">JSON</span><span class="sxs-lookup"><span data-stu-id="f845a-119">Order</span></span> | <span data-ttu-id="f845a-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="f845a-120">Path</span></span>                                  | <span data-ttu-id="f845a-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="f845a-121">Disk Format</span></span> | <span data-ttu-id="f845a-122">Formato dati</span><span class="sxs-lookup"><span data-stu-id="f845a-122">Data Format</span></span> | <span data-ttu-id="f845a-123">Necessario</span><span class="sxs-lookup"><span data-stu-id="f845a-123">Required</span></span> |
|-------|---------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="f845a-124">1</span><span class="sxs-lookup"><span data-stu-id="f845a-124">1</span></span>     | <span data-ttu-id="f845a-125">/xmp/MicrosoftPhoto:FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="f845a-125">/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="f845a-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="f845a-126">Unicode</span></span>     |             | <span data-ttu-id="f845a-127">Sì</span><span class="sxs-lookup"><span data-stu-id="f845a-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="f845a-128">Precedenza dei percorsi (TIFF)</span><span class="sxs-lookup"><span data-stu-id="f845a-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="f845a-129">Se il file è in formato TIFF, il gestore utilizzerà l'ordine di precedenza seguente durante la lettura o la scrittura dei dati.</span><span class="sxs-lookup"><span data-stu-id="f845a-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="f845a-130">JSON</span><span class="sxs-lookup"><span data-stu-id="f845a-130">Order</span></span> | <span data-ttu-id="f845a-131">Percorso</span><span class="sxs-lookup"><span data-stu-id="f845a-131">Path</span></span>                                      | <span data-ttu-id="f845a-132">Formato disco</span><span class="sxs-lookup"><span data-stu-id="f845a-132">Disk Format</span></span> | <span data-ttu-id="f845a-133">Formato dati</span><span class="sxs-lookup"><span data-stu-id="f845a-133">Data Format</span></span> | <span data-ttu-id="f845a-134">Necessario</span><span class="sxs-lookup"><span data-stu-id="f845a-134">Required</span></span> |
|-------|-------------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="f845a-135">1</span><span class="sxs-lookup"><span data-stu-id="f845a-135">1</span></span>     | <span data-ttu-id="f845a-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="f845a-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="f845a-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="f845a-137">Unicode</span></span>     |             | <span data-ttu-id="f845a-138">Sì</span><span class="sxs-lookup"><span data-stu-id="f845a-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="f845a-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="f845a-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f845a-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f845a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f845a-141">System. Photo. FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="f845a-141">System.Photo.FlashManufacturer</span></span>](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
