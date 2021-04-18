---
description: Criteri per i metadati delle foto per la proprietà System. Photo. PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Criteri per i metadati delle foto di System. Photo. PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3de9f5adda67fcd0e555194500f109df078bdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315966"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a><span data-ttu-id="a236c-103">Criteri per i metadati delle foto di System. Photo. PeopleNames</span><span class="sxs-lookup"><span data-stu-id="a236c-103">System.Photo.PeopleNames Photo Metadata Policy</span></span>

<span data-ttu-id="a236c-104">Criteri per i metadati delle foto per la proprietà [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .</span><span class="sxs-lookup"><span data-stu-id="a236c-104">The photo metadata policy for the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a236c-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a236c-105">PKEY</span></span>

<span data-ttu-id="a236c-106">PKEY \_ Photo \_ PeopleNames</span><span class="sxs-lookup"><span data-stu-id="a236c-106">PKEY\_Photo\_PeopleNames</span></span>

### <a name="containers"></a><span data-ttu-id="a236c-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="a236c-107">Containers</span></span>

<span data-ttu-id="a236c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a236c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a236c-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="a236c-109">Read-Only</span></span>

<span data-ttu-id="a236c-110">No</span><span class="sxs-lookup"><span data-stu-id="a236c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a236c-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="a236c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a236c-112">VT \_ vettore \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a236c-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="a236c-113">Tipo di input</span><span class="sxs-lookup"><span data-stu-id="a236c-113">Input Type</span></span>

<span data-ttu-id="a236c-114">StringMulti</span><span class="sxs-lookup"><span data-stu-id="a236c-114">StringMulti</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a236c-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="a236c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a236c-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="a236c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a236c-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="a236c-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a236c-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="a236c-118">Read Paths</span></span>



| <span data-ttu-id="a236c-119">JSON</span><span class="sxs-lookup"><span data-stu-id="a236c-119">Order</span></span> | <span data-ttu-id="a236c-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="a236c-120">Path</span></span>                                                           | <span data-ttu-id="a236c-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="a236c-121">Disk Format</span></span> |
|-------|----------------------------------------------------------------|-------------|
| <span data-ttu-id="a236c-122">1</span><span class="sxs-lookup"><span data-stu-id="a236c-122">1</span></span>     | <span data-ttu-id="a236c-123">/XMP/ <xmpstruct> MP: RegionInfo/ <xmpbag> MPRI: aree</span><span class="sxs-lookup"><span data-stu-id="a236c-123">/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="a236c-124">ushort</span><span class="sxs-lookup"><span data-stu-id="a236c-124">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="a236c-125">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="a236c-125">Write Paths</span></span>

<span data-ttu-id="a236c-126">Questa proprietà non può essere scritta usando i criteri dei metadati.</span><span class="sxs-lookup"><span data-stu-id="a236c-126">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="a236c-127">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="a236c-127">Remove Paths</span></span>



| <span data-ttu-id="a236c-128">JSON</span><span class="sxs-lookup"><span data-stu-id="a236c-128">Order</span></span> | <span data-ttu-id="a236c-129">Percorso</span><span class="sxs-lookup"><span data-stu-id="a236c-129">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="a236c-130">1</span><span class="sxs-lookup"><span data-stu-id="a236c-130">1</span></span>     | <span data-ttu-id="a236c-131"><xmpstruct>MP/XMP/: RegionInfo</span><span class="sxs-lookup"><span data-stu-id="a236c-131">/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="a236c-132">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="a236c-132">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a236c-133">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="a236c-133">Read Paths</span></span>



| <span data-ttu-id="a236c-134">JSON</span><span class="sxs-lookup"><span data-stu-id="a236c-134">Order</span></span> | <span data-ttu-id="a236c-135">Percorso</span><span class="sxs-lookup"><span data-stu-id="a236c-135">Path</span></span>                                                               | <span data-ttu-id="a236c-136">Formato disco</span><span class="sxs-lookup"><span data-stu-id="a236c-136">Disk Format</span></span> |
|-------|--------------------------------------------------------------------|-------------|
| <span data-ttu-id="a236c-137">1</span><span class="sxs-lookup"><span data-stu-id="a236c-137">1</span></span>     | <span data-ttu-id="a236c-138">/IFD/XMP/ <xmpstruct> MP: RegionInfo/ <xmpbag> MPRI: aree</span><span class="sxs-lookup"><span data-stu-id="a236c-138">/ifd/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="a236c-139">ushort</span><span class="sxs-lookup"><span data-stu-id="a236c-139">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="a236c-140">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="a236c-140">Write Paths</span></span>

<span data-ttu-id="a236c-141">Questa proprietà non può essere scritta usando i criteri dei metadati.</span><span class="sxs-lookup"><span data-stu-id="a236c-141">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="a236c-142">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="a236c-142">Remove Paths</span></span>



| <span data-ttu-id="a236c-143">JSON</span><span class="sxs-lookup"><span data-stu-id="a236c-143">Order</span></span> | <span data-ttu-id="a236c-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="a236c-144">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="a236c-145">1</span><span class="sxs-lookup"><span data-stu-id="a236c-145">1</span></span>     | <span data-ttu-id="a236c-146"><xmpstruct>MP/IFD/XMP/: RegionInfo</span><span class="sxs-lookup"><span data-stu-id="a236c-146">/ifd/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a236c-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="a236c-147">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a236c-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a236c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a236c-149">System. Photo. ProgramMode</span><span class="sxs-lookup"><span data-stu-id="a236c-149">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
