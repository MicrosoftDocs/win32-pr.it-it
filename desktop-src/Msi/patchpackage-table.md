---
description: La tabella PacchettoPatch descrive tutti i pacchetti di patch applicati al prodotto. Per ogni pacchetto di patch, l'identificatore univoco per la patch viene fornito insieme alle informazioni sull'immagine multimediale in cui si trova la patch.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Tabella PacchettoPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234026"
---
# <a name="patchpackage-table"></a><span data-ttu-id="5af67-104">Tabella PacchettoPatch</span><span class="sxs-lookup"><span data-stu-id="5af67-104">PatchPackage Table</span></span>

<span data-ttu-id="5af67-105">La tabella PacchettoPatch descrive tutti i pacchetti di patch applicati al prodotto.</span><span class="sxs-lookup"><span data-stu-id="5af67-105">The PatchPackage table describes all patch packages that have been applied to this product.</span></span> <span data-ttu-id="5af67-106">Per ogni pacchetto di patch, l'identificatore univoco per la patch viene fornito insieme alle informazioni sull'immagine multimediale in cui si trova la patch.</span><span class="sxs-lookup"><span data-stu-id="5af67-106">For each patch package, the unique identifier for the patch is provided along with information about the media image the on which the patch is located.</span></span>

<span data-ttu-id="5af67-107">La tabella PacchettoPatch include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="5af67-107">The PatchPackage table has the following columns.</span></span>



| <span data-ttu-id="5af67-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="5af67-108">Column</span></span>  | <span data-ttu-id="5af67-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5af67-109">Type</span></span>                   | <span data-ttu-id="5af67-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="5af67-110">Key</span></span> | <span data-ttu-id="5af67-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="5af67-111">Nullable</span></span> |
|---------|------------------------|-----|----------|
| <span data-ttu-id="5af67-112">PatchId</span><span class="sxs-lookup"><span data-stu-id="5af67-112">PatchId</span></span> | [<span data-ttu-id="5af67-113">GUID</span><span class="sxs-lookup"><span data-stu-id="5af67-113">GUID</span></span>](guid.md)       | <span data-ttu-id="5af67-114">S</span><span class="sxs-lookup"><span data-stu-id="5af67-114">Y</span></span>   | <span data-ttu-id="5af67-115">N</span><span class="sxs-lookup"><span data-stu-id="5af67-115">N</span></span>        |
| <span data-ttu-id="5af67-116">File multimediali\_</span><span class="sxs-lookup"><span data-stu-id="5af67-116">Media\_</span></span> | [<span data-ttu-id="5af67-117">Integer</span><span class="sxs-lookup"><span data-stu-id="5af67-117">Integer</span></span>](integer.md) | <span data-ttu-id="5af67-118">N</span><span class="sxs-lookup"><span data-stu-id="5af67-118">N</span></span>   | <span data-ttu-id="5af67-119">N</span><span class="sxs-lookup"><span data-stu-id="5af67-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5af67-120">Colonne</span><span class="sxs-lookup"><span data-stu-id="5af67-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5af67-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId</span><span class="sxs-lookup"><span data-stu-id="5af67-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId</span></span>
</dt> <dd>

<span data-ttu-id="5af67-122">Questa colonna contiene un identificatore univoco per questa patch particolare.</span><span class="sxs-lookup"><span data-stu-id="5af67-122">This column contains a unique identifier for this particular patch.</span></span>

</dd> <dt>

<span data-ttu-id="5af67-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_</span><span class="sxs-lookup"><span data-stu-id="5af67-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_</span></span>
</dt> <dd>

<span data-ttu-id="5af67-124">Questa colonna è una chiave esterna per la colonna DiskID della [tabella dei supporti](media-table.md) e indica il disco contenente il pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="5af67-124">This column is a foreign key to the DiskId column of the [Media Table](media-table.md) and indicates the disk containing the patch package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5af67-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="5af67-125">Remarks</span></span>

<span data-ttu-id="5af67-126">La tabella PacchettoPatch è obbligatoria in ogni pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="5af67-126">The PatchPackage table is required in every patch package.</span></span> <span data-ttu-id="5af67-127">Se la tabella non è presente, i tentativi di installazione della patch avranno esito negativo con l'errore 2768: la trasformazione nel pacchetto della patch non è valida.</span><span class="sxs-lookup"><span data-stu-id="5af67-127">If the table is missing, attempts to install the patch fail with "Error 2768: Transform in patch package is invalid."</span></span> <span data-ttu-id="5af67-128">Questa tabella viene in genere aggiunta al pacchetto di installazione da una trasformazione da un pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="5af67-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="5af67-129">Non viene in genere creato direttamente in un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="5af67-129">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="5af67-130">Convalida</span><span class="sxs-lookup"><span data-stu-id="5af67-130">Validation</span></span>

<dl>

[<span data-ttu-id="5af67-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="5af67-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5af67-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="5af67-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



