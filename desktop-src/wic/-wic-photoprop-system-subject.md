---
description: Criteri per i metadati delle foto per la proprietà System. Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Criteri per i metadati della foto System. Subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315957"
---
# <a name="systemsubject-photo-metadata-policy"></a><span data-ttu-id="600d1-103">Criteri per i metadati della foto System. Subject</span><span class="sxs-lookup"><span data-stu-id="600d1-103">System.Subject Photo Metadata Policy</span></span>

<span data-ttu-id="600d1-104">Criteri per i metadati delle foto per la proprietà [System. Subject](../properties/props-system-subject.md) .</span><span class="sxs-lookup"><span data-stu-id="600d1-104">The photo metadata policy for the [System.Subject](../properties/props-system-subject.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="600d1-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="600d1-105">PKEY</span></span>

<span data-ttu-id="600d1-106">\_Oggetto pkey</span><span class="sxs-lookup"><span data-stu-id="600d1-106">PKEY\_Subject</span></span>

### <a name="containers"></a><span data-ttu-id="600d1-107">Contenitori</span><span class="sxs-lookup"><span data-stu-id="600d1-107">Containers</span></span>

<span data-ttu-id="600d1-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="600d1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="600d1-109">Read-Only</span><span class="sxs-lookup"><span data-stu-id="600d1-109">Read-Only</span></span>

<span data-ttu-id="600d1-110">No</span><span class="sxs-lookup"><span data-stu-id="600d1-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="600d1-111">Tipo di PROPVARIANT di output</span><span class="sxs-lookup"><span data-stu-id="600d1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="600d1-112">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="600d1-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="600d1-113">Tipo di PROPVARIANT di input</span><span class="sxs-lookup"><span data-stu-id="600d1-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="600d1-114">VT \_ LPWSTR o VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="600d1-114">Either VT\_LPWSTR or VT\_LPWSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="600d1-115">Criteri di risoluzione dei conflitti</span><span class="sxs-lookup"><span data-stu-id="600d1-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="600d1-116">I valori di schemi diversi vengono risolti.</span><span class="sxs-lookup"><span data-stu-id="600d1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="600d1-117">Criteri JPEG</span><span class="sxs-lookup"><span data-stu-id="600d1-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="600d1-118">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="600d1-118">Read Paths</span></span>



| <span data-ttu-id="600d1-119">JSON</span><span class="sxs-lookup"><span data-stu-id="600d1-119">Order</span></span> | <span data-ttu-id="600d1-120">Percorso</span><span class="sxs-lookup"><span data-stu-id="600d1-120">Path</span></span>                     | <span data-ttu-id="600d1-121">Formato disco</span><span class="sxs-lookup"><span data-stu-id="600d1-121">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="600d1-122">1</span><span class="sxs-lookup"><span data-stu-id="600d1-122">1</span></span>     | <span data-ttu-id="600d1-123">/App1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="600d1-123">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="600d1-124">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="600d1-124">unicode\_bytes</span></span> |
| <span data-ttu-id="600d1-125">2</span><span class="sxs-lookup"><span data-stu-id="600d1-125">2</span></span>     | <span data-ttu-id="600d1-126">/App1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="600d1-126">/app1/ifd/{ushort=270}</span></span>   | <span data-ttu-id="600d1-127">ascii</span><span class="sxs-lookup"><span data-stu-id="600d1-127">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="600d1-128">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="600d1-128">Write Paths</span></span>



| <span data-ttu-id="600d1-129">JSON</span><span class="sxs-lookup"><span data-stu-id="600d1-129">Order</span></span> | <span data-ttu-id="600d1-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="600d1-130">Path</span></span>                     | <span data-ttu-id="600d1-131">Formato disco</span><span class="sxs-lookup"><span data-stu-id="600d1-131">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="600d1-132">1</span><span class="sxs-lookup"><span data-stu-id="600d1-132">1</span></span>     | <span data-ttu-id="600d1-133">/App1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="600d1-133">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="600d1-134">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="600d1-134">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="600d1-135">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="600d1-135">Remove Paths</span></span>



| <span data-ttu-id="600d1-136">JSON</span><span class="sxs-lookup"><span data-stu-id="600d1-136">Order</span></span> | <span data-ttu-id="600d1-137">Percorso</span><span class="sxs-lookup"><span data-stu-id="600d1-137">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="600d1-138">1</span><span class="sxs-lookup"><span data-stu-id="600d1-138">1</span></span>     | <span data-ttu-id="600d1-139">/App1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="600d1-139">/app1/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="600d1-140">2</span><span class="sxs-lookup"><span data-stu-id="600d1-140">2</span></span>     | <span data-ttu-id="600d1-141">/App1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="600d1-141">/app1/ifd/{ushort=270}</span></span>   |



 

### <a name="tiff-policy"></a><span data-ttu-id="600d1-142">Criteri TIFF</span><span class="sxs-lookup"><span data-stu-id="600d1-142">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="600d1-143">Leggi percorsi</span><span class="sxs-lookup"><span data-stu-id="600d1-143">Read Paths</span></span>



| <span data-ttu-id="600d1-144">JSON</span><span class="sxs-lookup"><span data-stu-id="600d1-144">Order</span></span> | <span data-ttu-id="600d1-145">Percorso</span><span class="sxs-lookup"><span data-stu-id="600d1-145">Path</span></span>                | <span data-ttu-id="600d1-146">Formato disco</span><span class="sxs-lookup"><span data-stu-id="600d1-146">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="600d1-147">1</span><span class="sxs-lookup"><span data-stu-id="600d1-147">1</span></span>     | <span data-ttu-id="600d1-148">/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="600d1-148">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="600d1-149">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="600d1-149">unicode\_bytes</span></span> |
| <span data-ttu-id="600d1-150">2</span><span class="sxs-lookup"><span data-stu-id="600d1-150">2</span></span>     | <span data-ttu-id="600d1-151">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="600d1-151">/ifd/{ushort=270}</span></span>   | <span data-ttu-id="600d1-152">ascii</span><span class="sxs-lookup"><span data-stu-id="600d1-152">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="600d1-153">Percorsi di scrittura</span><span class="sxs-lookup"><span data-stu-id="600d1-153">Write Paths</span></span>



| <span data-ttu-id="600d1-154">JSON</span><span class="sxs-lookup"><span data-stu-id="600d1-154">Order</span></span> | <span data-ttu-id="600d1-155">Percorso</span><span class="sxs-lookup"><span data-stu-id="600d1-155">Path</span></span>                | <span data-ttu-id="600d1-156">Formato disco</span><span class="sxs-lookup"><span data-stu-id="600d1-156">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="600d1-157">1</span><span class="sxs-lookup"><span data-stu-id="600d1-157">1</span></span>     | <span data-ttu-id="600d1-158">/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="600d1-158">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="600d1-159">\_byte Unicode</span><span class="sxs-lookup"><span data-stu-id="600d1-159">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="600d1-160">Rimuovi percorsi</span><span class="sxs-lookup"><span data-stu-id="600d1-160">Remove Paths</span></span>



| <span data-ttu-id="600d1-161">JSON</span><span class="sxs-lookup"><span data-stu-id="600d1-161">Order</span></span> | <span data-ttu-id="600d1-162">Percorso</span><span class="sxs-lookup"><span data-stu-id="600d1-162">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="600d1-163">1</span><span class="sxs-lookup"><span data-stu-id="600d1-163">1</span></span>     | <span data-ttu-id="600d1-164">/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="600d1-164">/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="600d1-165">2</span><span class="sxs-lookup"><span data-stu-id="600d1-165">2</span></span>     | <span data-ttu-id="600d1-166">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="600d1-166">/ifd/{ushort=270}</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="600d1-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="600d1-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="600d1-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="600d1-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="600d1-169">System. Subject</span><span class="sxs-lookup"><span data-stu-id="600d1-169">System.Subject</span></span>](../properties/props-system-subject.md)
</dt> </dl>

 

 
