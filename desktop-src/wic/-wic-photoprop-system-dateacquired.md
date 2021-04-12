---
description: Criteri per i metadati delle foto per la proprietà System. DateAcquired.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Criteri per i metadati delle foto System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233538"
---
# <a name="systemdateacquired-photo-metadata-policy"></a><span data-ttu-id="22e98-103">Criteri per i metadati delle foto System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="22e98-103">System.DateAcquired Photo Metadata Policy</span></span>

<span data-ttu-id="22e98-104">Criteri per i metadati delle foto per la proprietà [System. DateAcquired](../properties/props-system-dateacquired.md) .</span><span class="sxs-lookup"><span data-stu-id="22e98-104">The photo metadata policy for the [System.DateAcquired](../properties/props-system-dateacquired.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="22e98-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="22e98-105">PKEY</span></span>

<span data-ttu-id="22e98-106">\_DATEACQUIRED pkey</span><span class="sxs-lookup"><span data-stu-id="22e98-106">PKEY\_DateAcquired</span></span>

### <a name="containers"></a><span data-ttu-id="22e98-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="22e98-107">Containers</span></span>

<span data-ttu-id="22e98-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="22e98-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="22e98-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="22e98-109">Read-Only</span></span>

<span data-ttu-id="22e98-110">No</span><span class="sxs-lookup"><span data-stu-id="22e98-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="22e98-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="22e98-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="22e98-112">FILETIME VT \_</span><span class="sxs-lookup"><span data-stu-id="22e98-112">VT\_FILETIME</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="22e98-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="22e98-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="22e98-114">FILETIME VT \_</span><span class="sxs-lookup"><span data-stu-id="22e98-114">VT\_FILETIME</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="22e98-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="22e98-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="22e98-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="22e98-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="22e98-117">Precedenza dei percorsi (JPEG)</span><span class="sxs-lookup"><span data-stu-id="22e98-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="22e98-118">Se il file è in formato JPEG, il gestore cerca i dati nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="22e98-118">If the file is in JPEG format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="22e98-119">JSON</span><span class="sxs-lookup"><span data-stu-id="22e98-119">Order</span></span> | <span data-ttu-id="22e98-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="22e98-120">Path</span></span>                             | <span data-ttu-id="22e98-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="22e98-121">Disk Format</span></span>                        | <span data-ttu-id="22e98-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="22e98-122">Required</span></span> |
|-------|----------------------------------|------------------------------------|----------|
| <span data-ttu-id="22e98-123">1</span><span class="sxs-lookup"><span data-stu-id="22e98-123">1</span></span>     | <span data-ttu-id="22e98-124">/xmp/MicrosoftPhoto:DateAcquired</span><span class="sxs-lookup"><span data-stu-id="22e98-124">/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="22e98-125">Stringa Unicode nel formato di data XMP.</span><span class="sxs-lookup"><span data-stu-id="22e98-125">Unicode string in XMP date format.</span></span> | <span data-ttu-id="22e98-126">Sì</span><span class="sxs-lookup"><span data-stu-id="22e98-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="22e98-127">Precedenza dei percorsi (TIFF)</span><span class="sxs-lookup"><span data-stu-id="22e98-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="22e98-128">Se il file è in formato TIFF, il gestore cerca i dati nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="22e98-128">If the file is in TIFF format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="22e98-129">JSON</span><span class="sxs-lookup"><span data-stu-id="22e98-129">Order</span></span> | <span data-ttu-id="22e98-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="22e98-130">Path</span></span>                                 | <span data-ttu-id="22e98-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="22e98-131">Disk Format</span></span>                        | <span data-ttu-id="22e98-132">Necessario</span><span class="sxs-lookup"><span data-stu-id="22e98-132">Required</span></span> |
|-------|--------------------------------------|------------------------------------|----------|
| <span data-ttu-id="22e98-133">1</span><span class="sxs-lookup"><span data-stu-id="22e98-133">1</span></span>     | <span data-ttu-id="22e98-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span><span class="sxs-lookup"><span data-stu-id="22e98-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="22e98-135">Stringa Unicode nel formato di data XMP.</span><span class="sxs-lookup"><span data-stu-id="22e98-135">Unicode string in XMP date format.</span></span> | <span data-ttu-id="22e98-136">Sì</span><span class="sxs-lookup"><span data-stu-id="22e98-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="22e98-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="22e98-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="22e98-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22e98-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22e98-139">System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="22e98-139">System.DateAcquired</span></span>](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
