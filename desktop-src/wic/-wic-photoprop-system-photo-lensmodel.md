---
description: Criteri per i metadati delle foto per la proprietà System. Photo. LensModel.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Criteri per i metadati delle foto di System. Photo. LensModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058050"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a><span data-ttu-id="53984-103">Criteri per i metadati delle foto di System. Photo. LensModel</span><span class="sxs-lookup"><span data-stu-id="53984-103">System.Photo.LensModel Photo Metadata Policy</span></span>

<span data-ttu-id="53984-104">Criteri per i metadati delle foto per la proprietà [System. Photo. LensModel](../properties/props-system-photo-lensmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="53984-104">The photo metadata policy for the [System.Photo.LensModel](../properties/props-system-photo-lensmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="53984-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="53984-105">PKEY</span></span>

<span data-ttu-id="53984-106">PKEY \_ Photo \_ LensModel</span><span class="sxs-lookup"><span data-stu-id="53984-106">PKEY\_Photo\_LensModel</span></span>

### <a name="containers"></a><span data-ttu-id="53984-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="53984-107">Containers</span></span>

<span data-ttu-id="53984-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="53984-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="53984-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="53984-109">Read-Only</span></span>

<span data-ttu-id="53984-110">No</span><span class="sxs-lookup"><span data-stu-id="53984-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="53984-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="53984-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="53984-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="53984-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="53984-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="53984-113">Input Type</span></span>

<span data-ttu-id="53984-114">Stringa.</span><span class="sxs-lookup"><span data-stu-id="53984-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="53984-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="53984-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="53984-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="53984-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="53984-117">Precedenza dei percorsi (JPEG)</span><span class="sxs-lookup"><span data-stu-id="53984-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="53984-118">Se il file è in formato JPEG, il gestore utilizzerà il percorso seguente durante la lettura o la scrittura dei dati.</span><span class="sxs-lookup"><span data-stu-id="53984-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="53984-119">JSON</span><span class="sxs-lookup"><span data-stu-id="53984-119">Order</span></span> | <span data-ttu-id="53984-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="53984-120">Path</span></span>                          | <span data-ttu-id="53984-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="53984-121">Disk Format</span></span> | <span data-ttu-id="53984-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="53984-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="53984-123">1</span><span class="sxs-lookup"><span data-stu-id="53984-123">1</span></span>     | <span data-ttu-id="53984-124">/xmp/MicrosoftPhoto:LensModel</span><span class="sxs-lookup"><span data-stu-id="53984-124">/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="53984-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="53984-125">Unicode</span></span>     | <span data-ttu-id="53984-126">Sì</span><span class="sxs-lookup"><span data-stu-id="53984-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="53984-127">Precedenza dei percorsi (TIFF)</span><span class="sxs-lookup"><span data-stu-id="53984-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="53984-128">Se il file è in formato TIFF, il gestore utilizzerà l'ordine di precedenza seguente durante la lettura o la scrittura dei dati.</span><span class="sxs-lookup"><span data-stu-id="53984-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="53984-129">JSON</span><span class="sxs-lookup"><span data-stu-id="53984-129">Order</span></span> | <span data-ttu-id="53984-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="53984-130">Path</span></span>                              | <span data-ttu-id="53984-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="53984-131">Disk Format</span></span> | <span data-ttu-id="53984-132">Necessario</span><span class="sxs-lookup"><span data-stu-id="53984-132">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="53984-133">1</span><span class="sxs-lookup"><span data-stu-id="53984-133">1</span></span>     | <span data-ttu-id="53984-134">/ifd/xmp/MicrosoftPhoto:LensModel</span><span class="sxs-lookup"><span data-stu-id="53984-134">/ifd/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="53984-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="53984-135">Unicode</span></span>     | <span data-ttu-id="53984-136">Sì</span><span class="sxs-lookup"><span data-stu-id="53984-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="53984-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="53984-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="53984-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53984-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53984-139">System. Photo. LensModel</span><span class="sxs-lookup"><span data-stu-id="53984-139">System.Photo.LensModel</span></span>](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
